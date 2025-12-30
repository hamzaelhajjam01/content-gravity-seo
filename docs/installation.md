# Installation Guide

## Requirements

Before installing Content Gravity SEO Toolkit, ensure your server meets these requirements:

| Requirement | Minimum | Recommended |
|-------------|---------|-------------|
| WordPress | 6.0 | Latest |
| PHP | 7.4 | 8.0+ |
| MySQL | 5.6 | 8.0 |
| Memory Limit | 64MB | 256MB |

## Installation Methods

### Method 1: WordPress Admin Upload

1. Download the plugin ZIP file
2. Log in to your WordPress admin panel
3. Go to **Plugins → Add New → Upload Plugin**
4. Click **Choose File** and select the ZIP
5. Click **Install Now**
6. After installation, click **Activate Plugin**

### Method 2: FTP Upload

1. Extract the plugin ZIP file on your computer
2. Connect to your server via FTP
3. Navigate to `/wp-content/plugins/`
4. Upload the `content-gravity-seo` folder
5. Log in to WordPress admin
6. Go to **Plugins** and click **Activate** under Content Gravity SEO

### Method 3: WP-CLI

```bash
wp plugin install /path/to/content-gravity-seo.zip --activate
```

## Post-Installation Setup

### Step 1: Build the Link Index

After activation, build your site's link map:

1. Go to **Content Gravity → Dashboard**
2. Click **Build Link Index**
3. Wait for the indexing to complete

This process scans all published posts and pages for internal links.

### Step 2: Configure TOC Settings

1. Go to **Content Gravity → Settings → TOC Settings**
2. Enable **Auto-Insert TOC** if desired
3. Select which headings to include (H2, H3, H4)
4. Choose your preferred style
5. Save Settings

### Step 3: Set Up Focus Keywords (Optional)

For each post you want to optimize:

1. Edit the post
2. Find the **Content Gravity SEO** meta box
3. Enter your focus keyword
4. Save the post

## Database Tables

The plugin creates these tables on activation:

- `wp_cg_seo_link_index` - Internal link relationships
- `wp_cg_seo_link_metrics` - Cached link juice scores
- `wp_cg_seo_link_actions` - Audit log for bulk operations
- `wp_cg_seo_link_status` - HTTP status check results

These tables are automatically created and managed by the plugin.

## Verification

To verify successful installation:

1. Check that **Content Gravity** appears in the admin menu
2. Go to **Content Gravity → Dashboard**
3. Confirm you see the dashboard interface
4. Run **Build Link Index** to test functionality

## Troubleshooting

### Plugin doesn't appear after activation

- Clear any caching plugins
- Check file permissions (folders: 755, files: 644)
- Verify PHP version meets requirements

### Database tables not created

- Deactivate and reactivate the plugin
- Check that your database user has CREATE TABLE permissions
- Look for errors in `wp-content/debug.log`

### White screen after activation

- Enable debug mode in `wp-config.php`:
  ```php
  define('WP_DEBUG', true);
  define('WP_DEBUG_LOG', true);
  ```
- Check `/wp-content/debug.log` for error messages

## Uninstallation

1. Go to **Plugins** in WordPress admin
2. Deactivate **Content Gravity SEO Toolkit**
3. Click **Delete**

**Note**: Database tables are preserved after deletion. To remove all data, use the **Maintenance** page before uninstalling.
