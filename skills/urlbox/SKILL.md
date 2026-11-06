---
name: urlbox
description: Use when the user wants a full-page screenshot, PDF, Markdown or clean text of a web page (including bot-protected sites), wants to set up website captures or monitoring, or wants to check Urlbox usage or projects.
---

# Urlbox

Use the `urlbox` MCP tools. Every call needs an `intent` argument saying what the user wants.

- Screenshot: `screenshot`. Use `full_page` for the whole page; Urlbox loads lazy images and can hide cookie banners and popups. Call `describe_options` first for anything unusual (bot-protected sites, waits, viewports, delivery to S3).
- PDF: `pdf`. Markdown or text: `markdown`, `extract_text`. Rendered HTML: `scrape_html`. Video: `record_video`.
- Anything else: `render` with the right options.
- Pipelines: `create_project`, `set_project_defaults` and `create_webhook` set up the same captures the user will run through the Urlbox API.
- Account: `usage`, `list_projects`, `list_renders`, `get_render` (one id or up to 50), `report_render` if a render looks wrong.
- Renders count against the user's Urlbox plan. Do not loop renders without asking.
