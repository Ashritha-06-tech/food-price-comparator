# Design Guidelines: Food Price Comparator

## Design Approach
**Reference-Based**: Drawing inspiration from modern food delivery platforms (Swiggy, Zomato, Uber Eats) with a focus on clarity and quick decision-making. This is a utility-first comparison tool that needs instant visual hierarchy to communicate "best deal" at a glance.

## Typography System

**Font Families:**
- Primary: Inter or DM Sans (clean, modern sans-serif)
- Use single font family with weight variations

**Hierarchy:**
- Hero Title: text-5xl font-bold (48-60px desktop)
- Section Headers: text-2xl font-bold
- Price Display: text-4xl font-bold (primary focus)
- App Names: text-2xl font-bold
- Labels: text-sm font-medium
- Body/Helper Text: text-base
- Disclaimer: text-sm

## Layout System

**Spacing Primitives:**
Use Tailwind units: 2, 4, 6, 8, 12, 16, 20, 24
- Consistent padding: p-6 for cards, p-4 for mobile
- Vertical rhythm: mb-8 between major sections, mb-4 between elements
- Gap spacing: gap-4 for form grids, gap-6 for price cards

**Container Strategy:**
- Max width: max-w-6xl for main content
- Responsive padding: p-4 md:p-8
- Grid system: grid-cols-1 md:grid-cols-3 for comparison cards

## Component Library

### Input Section Card
- Unified card containing all search inputs
- 3-column grid on desktop, stacked on mobile
- Labels above inputs (text-sm font-medium)
- Full-width CTA button below inputs
- Shadow: shadow-lg for depth

### Price Comparison Cards
- 3-column grid on desktop, stacked on mobile
- Each card shows: app logo circle, app name, price (₹), CTA button
- Best price card: Prominent visual distinction with ring treatment and "Best Price" badge
- Logo circles: 16x16 (w-16 h-16) with centered emoji/icon
- Equal height cards with hover elevation
- Scale transformation on best price card (scale-105)

### Best Price Indicator
- Floating badge positioned absolutely at top center (-top-3)
- Clear "Best Price" text
- Visually distinct from other cards

### CTA Buttons
- Primary action: Full-width "Compare Prices" in search section
- Secondary actions: Full-width "Order Now" buttons in each price card
- Button text: Medium weight, clear action verbs

## Page Structure

### Header Section
- Centered text alignment
- Clear hierarchy: Large title, supporting subtitle
- Minimal, focused messaging
- Spacing: mb-8 from content below

### Search Interface
- Single unified card for all inputs
- Logical field grouping (restaurant, item, location)
- Immediate visual feedback on interaction
- Clear call-to-action placement

### Results Display
- Context text showing search criteria (restaurant, item, location)
- Equal-width price cards in responsive grid
- Consistent spacing between cards (gap-6)
- Visual hierarchy: Best price stands out immediately

### Footer Disclaimer
- Centered text
- Subtle styling (text-gray-600 text-sm)
- Clear communication about simulated data
- Spacing: mt-8 from cards above

## Visual Treatment

**Cards:**
- Rounded corners (default card radius)
- Layered shadows for depth (shadow-lg, shadow-xl on hover/best)
- White background for clarity
- Padding: p-6 for breathing room

**Interactive States:**
- Subtle hover elevation on all cards (hover:shadow-xl)
- Smooth transitions (transition-all duration-300)
- Button hover states with opacity or color shifts

**Icons/Logos:**
- Circular containers for app logos
- Centered placement
- Consistent sizing (w-16 h-16)
- Emoji placeholders (to be replaced with brand assets later)

## Accessibility

- Proper label-input associations
- Clear focus states on all interactive elements
- Sufficient contrast ratios for text
- Semantic HTML structure
- Descriptive button text ("Compare Prices", "Order Now")

## Responsive Behavior

**Mobile (< 768px):**
- Single column layout for all grids
- Stacked form inputs
- Full-width cards
- Reduced padding (p-4)

**Desktop (≥ 768px):**
- 3-column grids for inputs and price cards
- Increased padding (p-8)
- Side-by-side comparison view

## Images
No hero image needed. This is a utility-focused tool where functionality comes first. App logos are represented by emoji placeholders within circular containers, suitable for quick prototype visualization.