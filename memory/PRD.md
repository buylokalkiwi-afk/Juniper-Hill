# Juniper Hill Farm - Product Requirements Document

## Project Overview
**Client:** Juniper Hill Farm (Premium Beef Supplier, NZ)
**Project:** Inventory-to-Sale Automation System
**Status:** Mockup Phase - Ready for Client Pitch

## Core Problem
Manual sales process causing revenue loss; customer friction calculating weight minimums on current site.

## Solution Architecture
Three interconnected applications:

### 1. Ecommerce Storefront (Customer-Facing)
- Live inventory display
- Stripe payments integration
- Subscription model for regular customers
- Dynamic bulk discounts
- 21-day dry ageing marketing emphasis

### 2. Inventory Scanner (PWA - Staff-Facing)
- QR code scanning for real-time stock tracking
- Record Sale popup workflow
- Demand Forecasting view
- Label printing (moved to desktop admin)

### 3. Yield IQ (Desktop - Butcher Tool)
- Self-learning AI yield prediction
- Visual cut selector with interactive cow diagram
- Carcass intake and tracking
- Historical actuals dashboard

## Tech Stack (Planned)
- **Frontend:** React
- **Backend:** Supabase/PostgreSQL
- **Payments:** Stripe
- **PWA:** Service workers for offline capability

---

## Mockup Status

### Completed & Approved
| Mockup | Description | Status |
|--------|-------------|--------|
| 01 | Storefront Homepage | ✅ Approved |
| 02 | Storefront Shop | ✅ Approved |
| 03 | Storefront Cart | ✅ Approved |
| 04 | Scanner QR Scan | ✅ Approved |
| 05 | Scanner Stock Overview | ✅ Approved |
| 07 | Predictor Intake | ✅ Approved |
| 08 | Yield IQ Visual Cut Selector | ✅ Ready for Pitch |
| 09 | Predictor Dashboard | ✅ Approved |
| 11 | Admin Discounts | ✅ Approved |
| 12 | Storefront Subscribe | ✅ Approved |
| 13 | Email Subscription | ✅ Approved |

### Pending Tasks
- [ ] Make cow SVG sections individually colorable (user will complete in Illustrator)
- [ ] Add "21-day dry ageing" marketing copy to storefront mockups
- [ ] Update 00_INDEX.html with links to all mockups
- [ ] Create Desktop Label Printing mockup
- [ ] Review mockups 07 & 09 for "Yield IQ" branding consistency

---

## Key URLs
- **Mockup Index:** https://tag-replacement-app.preview.emergentagent.com/mockups/00_INDEX.html
- **Yield IQ Cut Selector:** https://tag-replacement-app.preview.emergentagent.com/mockups/08_Predictor_Optimiser.html

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
2. Inventory Scanner PWA
3. Yield IQ Desktop Tool with ML

---

*Last Updated: March 2025*
