# wabss

Squarespace Developer Mode boilerplate theme with working examples of advanced features.

## Features

### Custom Collection (Portfolio)

- **Location**: `collections/portfolio.*`
- **Config**: `portfolio.conf` — user-orderable, accepts text and image posts
- **List**: `portfolio.list` — grid of portfolio items
- **Item**: `portfolio.item` — single item view with image and body

Add a Portfolio page in Squarespace (Pages → Add Page → Portfolio) to use it.

### Multiple Layouts

- **Regions**: `header.region`, `footer.region`, `full-width.region`, `sidebar.region`
- **Layouts** (in `template.conf`):
  - **Default (Sidebar)**: Header + main content + sidebar + footer
  - **Homepage (Full Width)**: Header + full-width content + footer

Set layout per page in Page Settings → Layout. Homepage defaults to Full Width.

### Static Pages

- **Location**: `pages/`
- **Examples**: `about.page`, `contact.page` with matching `.page.conf` files
- Static pages render in the main content area; they cannot be edited in the CMS.
- Add them in Pages panel; they appear in the navigation.

### Folder-Based Navigation (Dropdowns)

- **Config**: `collections/folders.conf` — enables folders
- **Navigation**: `blocks/navigation.block` — supports `.folder?` with dropdown submenus

Create a folder in Pages, add pages/collections inside it, then add the folder to the main nav. The dropdown shows on hover.

### Style Editor & Template Annotations

**Style Editor tweaks** (in `styles/global.less`):

- Page Width (value slider)
- Spacing (value slider)
- Text Color, Link Color, Link Hover Color, Border Color (color pickers)
- Show Sidebar (checkbox)

**Template annotations** (for in-context editing):

- `data-content-field="site-title"` — edit site title
- `data-content-field="main-content"` — edit main content
- `data-content-field="navigation-mainNav"` — edit navigation
- `data-content-field="title"` — edit item/collection title
- `data-item-id` / `data-collection-id` — identify editable items

## Deployment

1. Enable Developer Mode: Settings → Developer Tools → Developer Mode
2. Connect to GitHub and push this repo
3. Squarespace syncs template changes from the connected repository
