# Juniper Hill Farm - Product Requirements Document

## Project Overview
**Client:** Juniper Hill Farm (Premium Beef Supplier, NZ)
**Project:** Inventory-to-Sale Automation System
**Status:** Mockup Phase - Building Complete Pitch Package

## Core Problems Addressed
1. Manual sales process causing revenue loss
2. Customer friction calculating weight minimums on current site
3. **NEW:** No order tracking visibility (customers don't know order status/ETA)

## Solution Architecture
Three interconnected applications:

### 1. Ecommerce Storefront (Customer-Facing)
- Live inventory display (packet-based, pre-weighed, pre-priced)
- Stripe payments integration
- Subscription model for regular customers
- Dynamic bulk discounts
- **NEW: Order Tracking Dashboard** - Real-time status updates, NZ Post integration, delivery ETA
- **NEW: Email notifications** at each stage (Confirmed → Processing → Packed → Shipped → Delivered)
- **NEW: PWA (Progressive Web App)** - "Add to Home Screen" for push notifications
- Marketing emphasis on unique value proposition:
  - NZ's first BioGro Certified on-farm micro-abattoir
  - Stress-free on-farm slaughter (no transport = superior meat quality)
  - 100% organic, grass-fed
  - 21-day dry ageing

### 2. Inventory Scanner (Mobile Web App - Staff-Facing)
- QR code scanning for real-time stock tracking
- Record Sale popup workflow
- Demand Forecasting view
- Label printing

### 3. Yield IQ (Desktop - Butcher Tool)
- Self-learning AI yield prediction
- Visual cut selector with interactive cow diagram
- Carcass intake and tracking
- Historical actuals dashboard

### 4. Admin Portal (Desktop - Staff)
- Dashboard with sales overview
- Order Management + **Fulfillment workflow**
- Inventory Management
- Label Printing
- Discounts & Promotions
- Staff Management (roles/permissions)
- Customer Management
- Subscription Management

## Tech Stack (Planned)
- **Frontend:** React
- **Backend:** Supabase/PostgreSQL
- **Payments:** Stripe
- **Shipping:** NZ Post API integration
- **PWA:** Service workers for offline capability + push notifications

---

## Mockup Status

### Customer-Facing (6 mockups)
| # | Mockup | Status |
|---|--------|--------|
| 01 | Storefront Homepage | ✅ Complete |
| 02 | Storefront Shop | ✅ Complete |
| 03 | Storefront Cart | ✅ Complete |
| 12 | Subscription Sign-up | ✅ Complete |
| 17 | First Purchase Popup | ✅ Complete |
| **24** | **Order Tracking (Customer)** | ✅ **NEW** |

### Staff Scanner (3 mockups)
| # | Mockup | Status |
|---|--------|--------|
| 04 | Scanner QR Scan | ✅ Complete |
| 05 | Scanner Stock Overview | ✅ Complete |
| 06 | Scanner Print Labels | ✅ Complete |

### Admin Portal (8 mockups)
| # | Mockup | Status |
|---|--------|--------|
| 14 | Admin Login | ✅ Complete |
| 15 | Admin Dashboard | ✅ Complete |
| 16 | Admin Orders | ✅ Complete |
| **25** | **Order Fulfillment** | ✅ **NEW** |
| 20 | Admin Inventory | ✅ Complete |
| 19 | Admin Labels | ✅ Complete |
| 11 | Admin Discounts | ✅ Complete |
| 18 | Admin Staff | ✅ Complete |

### Yield IQ (3 mockups)
| # | Mockup | Status |
|---|--------|--------|
| 07 | Carcass Intake | ✅ Complete |
| 08 | Visual Cut Selector | ⏸️ Awaiting interactive SVG from user |
| 09 | Accuracy Dashboard | ✅ Complete |

### Email Templates (1 mockup)
| # | Mockup | Status |
|---|--------|--------|
| 13 | Email Subscription | ✅ Complete |

### Supporting Documents (TODO)
- [ ] Updated Pitch Deck (10_Updated_Pitch_Deck.html)
- [ ] Mockup Walkthrough Guide
- [ ] System Architecture Diagram
- [ ] ROI & Value Analysis
- [ ] Implementation Proposal

---

## Order Tracking Feature (NEW)

### Customer-Facing Features
| Feature | Status |
|---------|--------|
| Order status timeline (Confirmed → Processing → Packed → Shipped → Delivered) | ✅ Included |
| Email notifications at each stage | ✅ Included |
| "Track on NZ Post" button (links to NZ Post tracking page) | ✅ Included |
| Delivery ETA (from NZ Post) | ✅ Included |
| "My Orders" dashboard | ✅ Included |
| Push notifications via PWA | ✅ Planned |

### Admin-Facing Features
| Feature | Status |
|---------|--------|
| Order status workflow (click to advance) | ✅ Included |
| NZ Post tracking number input | ✅ Included |
| Automatic email preview before sending | ✅ Included |
| Print packing slip | ✅ Included |
| Fulfillment stats (pending, packed, shipped) | ✅ Included |

---

## Key URLs
- **Mockup Index:** https://tag-replacement-app.preview.emergentagent.com/mockups/00_INDEX.html
- **Order Tracking (Customer):** https://tag-replacement-app.preview.emergentagent.com/mockups/24_Order_Tracking_Customer.html
- **Order Fulfillment (Admin):** https://tag-replacement-app.preview.emergentagent.com/mockups/25_Order_Fulfillment_Admin.html

---

## Interactive SVG Instructions (For User)

To make cow sections change color on hover/selection:

1. **Separate sections in Illustrator:**
   - Ungroup all → Use Shape Builder (Shift+M) or Pathfinder → Divide
   - Each primal cut becomes its own closed shape

2. **Name layers:** head, chuck, rib, loin, sirloin, rump, brisket, plate, flank, fore-shank, hind-shank

3. **Export SVG:**
   - Styling: Presentation Attributes
   - Object IDs: Layer Names
   - Uncheck "Preserve Illustrator Editing Capabilities"

4. **CSS for states:**
```css
.cut-section { fill: #2C2C2C; transition: fill 0.2s; }
.cut-section:hover { fill: #C41E3A; }
.cut-section.complete { fill: #1B4D3E; }
```

---

## Phase 2+ Development (Post-Approval)
1. Ecommerce Storefront (React + Stripe)
2. Inventory Scanner Mobile Web App
3. Admin Portal with Order Fulfillment
4. Yield IQ Desktop Tool with ML
5. NZ Post API Integration

---

*Last Updated: December 2024*
