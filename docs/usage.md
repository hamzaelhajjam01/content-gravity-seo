# Usage Guide

Quick reference guide for using Content Gravity SEO Toolkit.

## Table of Contents
1. [Dashboard Overview](#dashboard-overview)
2. [Building the Link Index](#building-the-link-index)
3. [Content Analyzer](#content-analyzer)
4. [Internal Linking](#internal-linking)
5. [Link Juice](#link-juice)
6. [Table of Contents](#table-of-contents)
7. [Content Clusters](#content-clusters)
8. [HTTP Status Checker](#http-status-checker)

---

## Dashboard Overview

Access the plugin at **Content Gravity** in your WordPress admin menu.

The dashboard displays:
- **Total Internal Links**: Count of all internal links indexed
- **Average Links Per Post**: Site-wide linking health
- **Orphan Pages**: Posts with zero inbound links
- **Weak Pages**: Posts with low link juice scores

---

## Building the Link Index

Before using link features, build your site's link map:

1. Go to **Content Gravity → Dashboard**
2. Click **Build Link Index**
3. Wait for completion (progress bar shown)

**When to Rebuild**:
- After bulk content imports
- If link counts seem incorrect
- After major content restructuring

The index auto-updates when you publish or edit posts.

---

## Content Analyzer

### Analyzing a Post

1. Edit any post or page
2. Find the **Content Gravity SEO** meta box
3. View real-time metrics:
   - Word count
   - Readability score
   - Heading structure
   - Link counts

### Setting Focus Keywords

1. Enter your target keyword in the **Focus Keyword** field
2. Save the post
3. The analyzer checks keyword presence in:
   - Title
   - Headings
   - First paragraph
   - Overall content

### Interpreting Scores

| Score | Grade | Meaning |
|-------|-------|---------|
| 80-100 | A | Excellent |
| 60-79 | B | Good |
| 40-59 | C | Needs improvement |
| 20-39 | D | Poor |
| 0-19 | F | Critical issues |

---

## Internal Linking

### Finding Link Opportunities

1. Go to **Content Gravity → Link Plan**
2. Select a **Target Page** (the page needing more links)
3. Click **Find Donors**
4. Review suggestions showing:
   - Source page with matching anchor text
   - Link Juice score of source
   - Text snippet showing context

### Inserting Links

**Automatic** (for standard WordPress posts):
1. Click **Insert Link** next to a suggestion
2. The link is automatically added
3. Action is logged for rollback

**Manual** (for Elementor posts):
1. Open source post in Elementor
2. Find the suggested anchor text
3. Add link manually
4. Save the page

### Rolling Back Links

1. Go to **Link Plan → Activity Log**
2. Find the action to undo
3. Click **Rollback**
4. Content reverts to pre-link state

Rollback is available for 24 hours after insertion.

---

## Link Juice

### Understanding Scores

Link Juice represents authority flow through your site:

| Score | Meaning | Action |
|-------|---------|--------|
| 80-100 | High authority | Use as link donor |
| 50-79 | Good | Maintain links |
| 25-49 | Moderate | Add inbound links |
| 0-24 | Weak/Orphan | Priority for linking |

### Viewing Link Juice

1. Go to **Content Gravity → Link Juice**
2. Sort by score (ascending for weak pages)
3. Click any page to see link flow

### Recalculating

Link Juice recalculates:
- Daily via WP-Cron (automatic)
- When posts are published/updated
- Manually via **Dashboard → Recalculate**

---

## Table of Contents

### Automatic TOC

1. Go to **Content Gravity → Settings → TOC**
2. Enable **Auto-Insert TOC**
3. Select headings: H2, H3, H4
4. Choose post types
5. Select position: Before Content or After First Paragraph
6. Save Settings

TOC appears automatically on qualifying posts (3+ headings).

### Manual Placement

Use the shortcode anywhere in your content:

```
[cg_toc]
```

In Gutenberg, use a **Shortcode** block.

### Styling Options

| Style | Description |
|-------|-------------|
| Boxed | Bordered container with background |
| Minimal | Simple list, no container |

Additional options:
- **Collapsible**: Expand/collapse toggle
- **Dark Mode**: Dark theme variant
- **Custom Class**: Add your own CSS class

---

## Content Clusters

### What Are Clusters?

Clusters are groups of related pages detected by their linking patterns:
- **Hub**: Highest authority page in the cluster
- **Spokes**: Related pages linked from the hub

### Building Clusters

1. Ensure Link Index is current
2. Go to **Content Gravity → Clusters**
3. Click **Build Clusters**
4. View cluster groupings

### Strengthening Clusters

1. Click any cluster to expand
2. View **Suggested Links**
3. Add missing links from hub to weak spokes

---

## HTTP Status Checker

### Scanning for Broken Links

1. Go to **Content Gravity → HTTP Status**
2. Click **Scan Content** to extract all links
3. Click **Check Status** to verify links
4. Filter by status code

### Status Code Reference

| Code | Meaning | Action |
|------|---------|--------|
| 200 | OK | ✅ None |
| 301 | Permanent redirect | Consider updating URL |
| 404 | Not found | ⚠️ Fix or remove |
| 500 | Server error | Check target site |
| 0 | Connection failed | Verify manually |

---

## Quick Tips

1. **Build index first** - Always build the link index before using link features
2. **Check orphans regularly** - Orphan pages hurt SEO; link to them
3. **Use clusters** - Strengthen topical authority by linking cluster members
4. **Monitor weak pages** - Low juice pages need more inbound links
5. **Review before rollback** - Rollback is only available for 24 hours

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+S` | Save settings (on settings pages) |
| `Esc` | Close modals |

---

## Getting Help

- **Documentation**: [documentation.md](documentation.md)
- **Limitations**: [limitations.md](limitations.md)
- **Changelog**: [CHANGELOG.md](CHANGELOG.md)
- **Support**: support.example.com
