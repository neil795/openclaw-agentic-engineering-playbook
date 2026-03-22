# Navigation Specification (Issue #3)

## Desktop
- Sticky top navigation:
  - Work
  - AI Risk
  - Experience
  - Web Foundry
  - Contact
- Right-edge section indicator (dot/rail) with active state.
- Top progress bar (thin) for narrative completion awareness.

## Mobile
- Condensed sticky header with menu drawer.
- Section list maps to anchor IDs.
- No right-edge dot navigation.

## Anchor strategy
- Each primary section has stable hash anchor:
  - `#hero`
  - `#problem-landscape`
  - `#operating-philosophy`
  - `#case-studies`
  - `#ai-governance`
  - `#experience`
  - `#web-foundry`
  - `#trust`
  - `#contact`
- Active section updates URL hash via IntersectionObserver (no scroll-jacking math).

## Accessibility
- Keyboard focusable nav controls.
- Skip-to-content link on first tab.
- Visible focus states with high contrast.
