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

### Customer-Facing (7 mockups)
| # | Mockup | Status |
|---|--------|--------|
| 01 | Storefront Homepage | ✅ Complete |
| 02 | Storefront Shop | ✅ Complete |
| 03 | Storefront Cart | ✅ Complete |
| 12 | Subscription Sign-up | ✅ Complete |
| 17 | First Purchase Popup | ✅ Complete |
| **24** | **Order Tracking (Customer)** | ✅ Complete |
| **22** | **My Subscription (Customer)** | ✅ **NEW** |

### Staff Scanner (3 mockups)
| # | Mockup | Status |
|---|--------|--------|
| 04 | Scanner QR Scan | ✅ Complete |
| 05 | Scanner Stock Overview | ✅ Complete |
| 06 | Scanner Print Labels | ✅ Complete |

### Admin Portal (10 mockups)
| # | Mockup | Status |
|---|--------|--------|
| 14 | Admin Login | ✅ Complete |
| 15 | Admin Dashboard | ✅ Complete |
| 16 | Admin Orders | ✅ Complete |
| **25** | **Order Fulfillment** | ✅ Complete |
| 20 | Admin Inventory | ✅ Complete |
| 19 | Admin Labels | ✅ Complete |
| 11 | Admin Discounts | ✅ Complete |
| 18 | Admin Staff | ✅ Complete |
| **21** | **Customer Management** | ✅ **NEW** |
| **23** | **Subscription Management (Admin)** | ✅ **NEW** |

### Yield IQ (3 mockups)
| # | Mockup | Status |
|---|--------|--------|
| 07 | Carcass Intake | ✅ Complete |
| 08 | Visual Cut Selector | ⏸️ Awaiting interactive SVG from user |
| 09 | Accuracy Dashboard | ✅ Complete |

### Email Templates (2 mockups)
| # | Mockup | Status |
|---|--------|--------|
| 13 | Email Subscription | ✅ Complete |
| **26** | **Order Status Emails (5 Templates)** | ✅ **NEW** |

### Pitch Documents (2 documents)
| # | Document | Status |
|---|----------|--------|
| **27** | **Pitch Deck (12 Slides)** | ✅ **NEW** |
| **28** | **ROI & Value Analysis** | ✅ **NEW** |

### Supporting Documents (TODO)
- [x] ~~Updated Pitch Deck~~ → Now `27_Pitch_Deck.html`
- [x] ~~ROI & Value Analysis~~ → Now `28_ROI_Analysis.html`
- [ ] Mockup Walkthrough Guide
- [ ] System Architecture Diagram
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

## Pitch Package Documents (TODO)

### Completed
- [x] 22+ UI Mockups (Customer, Admin, Scanner, Yield IQ, Email)
- [x] Order Tracking System mockups (customer + admin)
- [x] Email templates for all 5 order stages

### To Create
- [ ] Updated Pitch Deck
- [ ] Mockup Walkthrough Guide
- [ ] System Architecture Diagram
- [ ] ROI & Value Analysis

### Separate Document (After Pitch Package)
- [ ] **Pricing & Terms Proposal** - Flexible pricing models, payment terms, and personal introduction

---

## Notes for Pricing Document

**Personal Story & Values Alignment:**
- Genuine customer who loves Juniper Hill products
- Shared values: animal welfare, health, nutrition, environmental respect
- Coming out of retirement for this project - feels called to make a difference
- Want to see them succeed as a long-term customer
- Willingness to accommodate on payment terms and timelines
- Goal: Help communicate their unique value proposition to more Kiwis

**Pricing Approach:**
- Flexible payment terms available
- Timeline negotiable
- Investment in long-term partnership, not just a transaction

---

*Last Updated: December 2024*
