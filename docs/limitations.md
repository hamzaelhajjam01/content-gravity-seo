# Known Limitations

This document outlines known limitations of Content Gravity SEO Toolkit and suggested workarounds.

## Elementor Compatibility

### Limitation: Automatic Link Insertion

**Issue**: The plugin cannot automatically insert links into Elementor-built pages.

**Reason**: Elementor stores content in JSON format rather than standard HTML. Modifying this JSON programmatically risks breaking page layouts and widget configurations.

**Workaround**:
1. When the Link Plan shows an Elementor source page, it displays a "Manual" badge
2. Note the suggested anchor text and target URL
3. Open the source page in Elementor editor
4. Find the text widget containing the anchor text
5. Select the text and add the link manually
6. Save and update the page

**What Still Works with Elementor**:
- ✅ Link indexing (scans Elementor JSON for existing links)
- ✅ Link Juice calculation
- ✅ TOC generation from Elementor headings
- ✅ Content analysis

---

## Table of Contents

### Limitation: Minimum Heading Requirement

**Issue**: TOC only displays when content has 3+ headings.

**Reason**: A TOC with only 1-2 items provides little navigation value and clutters short content.

**Workaround**: If you need a TOC on short content, structure it with at least 3 heading elements (H2, H3, or H4).

### Limitation: Dynamic Content

**Issue**: TOC is generated at page load and doesn't update for dynamically loaded content.

**Reason**: The TOC is built from the initial HTML. JavaScript-loaded content (like AJAX tabs) isn't captured.

**Workaround**: Ensure critical navigational headings are in the initial page HTML, not dynamically loaded.

---

## Link Juice Calculation

### Limitation: Calculation Time on Large Sites

**Issue**: Initial Link Juice calculation can be slow on sites with 1000+ posts.

**Reason**: The algorithm runs multiple iterations to simulate PageRank-style authority flow.

**Workaround**:
1. Initial calculation runs via WP-Cron in batches
2. Progress is shown on the dashboard
3. Subsequent recalculations are faster (incremental updates)

### Limitation: External Links Not Tracked

**Issue**: Link Juice doesn't track authority from external backlinks.

**Reason**: This plugin focuses on internal linking. External backlink data requires search engine APIs or third-party tools.

**Workaround**: Use this plugin in combination with a backlink analysis tool for complete link profile data.

---

## Content Analyzer

### Limitation: Readability for Non-English Content

**Issue**: Flesch Reading Ease is optimized for English. Scores may be less accurate for other languages.

**Reason**: Syllable counting and sentence structure assumptions are based on English.

**Workaround**: Use readability scores as a general guide rather than absolute metrics for non-English content.

### Limitation: Page Builders and Shortcodes

**Issue**: Content analysis may not fully capture text inside complex shortcodes or page builder widgets.

**Reason**: Some shortcodes render at display time, not when the plugin analyzes saved content.

**Workaround**: View the "rendered" analysis by previewing the post, then running analysis.

---

## HTTP Status Checker

### Limitation: Timeout on Slow External Sites

**Issue**: Some links show status "0" (connection failed) even if the site is accessible.

**Reason**: The checker uses a 5-second timeout to avoid blocking. Slow servers may not respond in time.

**Workaround**: Links showing status "0" can be manually verified by clicking them.

### Limitation: Rate Limiting

**Issue**: Bulk checking many links may trigger rate limiting on target sites.

**Reason**: Making many requests to the same domain quickly can be detected as suspicious activity.

**Workaround**: The checker processes links in batches with delays. For very large sites, spread checks across multiple sessions.

---

## Browser Compatibility

### Limitation: Oldest Browser Support

**Issue**: Admin interface requires modern browsers.

**Supported Browsers**:
- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

**Not Supported**:
- Internet Explorer (any version)
- Older mobile browsers

---

## Multisite

### Limitation: Network-Level Settings

**Issue**: Settings are configured per-site, not at the network level.

**Reason**: Each site may have different SEO requirements and content structures.

**Workaround**: Configure settings individually for each site in the network.

---

## Performance

### Recommended Limits

| Metric | Recommended Maximum |
|--------|---------------------|
| Posts/Pages | 10,000 |
| Links per post | 100 |
| Concurrent users | 50 |

Sites exceeding these limits may experience slower dashboard loading times.

---

## Feature Requests

If you encounter a limitation that significantly impacts your workflow, please submit a feature request through our support portal. We prioritize features based on user demand and technical feasibility.
