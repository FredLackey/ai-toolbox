# UI Guidelines Document

This document captures the core UI/UX guidelines discussed across multiple conversations to ensure consistency and clarity throughout all application interfaces being designed or reviewed.

---

## Layout & Structure

- **Max Width:** 900px for all desktop views. This constraint improves readability and visual coherence.
- **Grid System:** Utilize a predictable grid layout. Avoid overly rigid or boxy appearances—introduce some spacing and margin softness.
- **Component Spacing:** Ensure consistent spacing between cards, tables, and UI components to avoid a squashed or claustrophobic feel.

## Colors & Themes

- **Backgrounds:** Always use **white** as the default background for main areas and cards.
- **Avoid Pale Green:** Previously used pale green hues for backgrounds or highlights were found to feel too clinical and overwhelming.
- **Status & Alerts:** Use varied color indicators for alerts, activity, and statuses to provide better visual feedback. Avoid monochrome interfaces.
- **Primary Theme Color:** Use a **dark green** for key visual elements such as buttons, highlights, and accents. This conveys a sense of confidence and stability.

## Typography & Links

- **Font Sizing:** Use sensible, readable font sizes. Headings should stand out but not overwhelm.
- **Links:** No underlines for navigation links or buttons unless it's an actual hyperlink in a block of text.

## Buttons & Controls

- **Button Design:** Buttons should have visible borders and adequate spacing. Rounded corners preferred for a modern feel.
- **Hover Effect:** Buttons should respond to hover states by changing their background color to a lighter shade of the button’s primary color.
- **Controls:** Ensure all UI controls (inputs, dropdowns, toggles) are distinguishable with clear boundaries.

## Tables

- **Layout:** Tables must have padding and spacing. Avoid crushed, edge-to-edge layouts.
- **Highlighting:** Use subtle row highlighting only when necessary—do not default to aggressive background tones.
- **Pagination:** All data tables must use pagination for consistency. The pagination component should appear in the table footer and include:
  - A **dropdown** to select the number of rows per page.
  - Navigation controls:
    - **First Page** button
    - **Back** button
    - **Text box** for entering a specific page number
    - **Next** button
    - **Last Page** button
- **Actions Column:**
  - If any row items support actions (e.g., edit, delete, view details), include an **actions column** on the far right side.
  - If there is only one action, show a single action icon.
  - If there are multiple actions, use a **hamburger menu icon** that reveals a **pop-up menu** listing the available actions.
  - This column should **not** have a header.

## Navigation

All applications must follow a horizontal navigation pattern.

### Primary Navigation

- Pinned to the top of every screen and always visible, regardless of login state.
- **Far Left:** Contains a **text-based logo**:
  - Should be larger and bolder than standard text.
  - Must link back to the root of the application.
- **Next to the Logo:** Text-based links to public pages (FAQ, Help, Features, About) that do not change based on login state.
- **Far Right:** Changes based on login state:
  - If not logged in: show “Sign In” or “Register”.
  - If logged in: show user-related links like “Profile” or “Settings”.

### Secondary Navigation

- Appears directly beneath the primary navigation (only when logged in).
- Structured in three zones:

  **1. Far Left:**  
  - Contains a **selector dropdown** that governs the top-level context (e.g., AWS account).
  - Immediately to the right of the dropdown is an **icon button** for adding a new item.

  **2. Far Right:**  
  - Anchored by a **call-to-action (CTA) button**, such as “Trigger Scan”.
  - **Text-based links** to major pages appear **immediately to the left of the CTA**.
  - If no CTA button exists, these links remain **right-justified** within the navigation bar.

- This should not be confused with tabs.

### Tabs (Page-Level)

- Used within the **body of the page** to separate areas of concern.
- Example: On the Organization Details screen:
  - Tabs: **Accounts**, **General Info**, **Members**
  - The “Leave Organization” button appears in the **General Info** tab.
- Visibility and permissions depend on user role.
- Tabs are **not** part of secondary navigation.

## Footer

- The footer is **always visible** on both public and private pages.
- Content is **public-facing only**, such as:
  - Helpful links
  - Copyright
  - Legal disclaimers
- Uses the same color scheme as the rest of the page.
- Separated visually from the page body using a **horizontal rule** or similar boundary.

## Device Considerations

- Mobile-friendly design principles:
  - Adjust max-width appropriately
  - Maintain spacing and clarity
  - Use a minimalist layout

## UI Libraries

- **React Applications:** Use **shadcn**.
- **React Native Applications:** Use **nativecn**.
- **Express Applications:** Use **Tailwind CSS**.

---

This document will be updated as new conversations refine our UI expectations. Let all project teams and designers reference this to ensure coherence across applications.