# Changelog

All notable changes to Content Gravity SEO Toolkit will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.9] - 2024-12-30

### Added
- Toast notifications for settings save confirmation
- Capability checks on all AJAX handlers
- Local bundling of Tailwind CSS (no CDN)

### Changed
- Replaced Google Fonts with system font stack
- Updated security hardening for CodeCanyon compliance

### Security
- Added `current_user_can()` checks to `ajax_get_status()` and `ajax_get_data()`
- Sanitized raw database queries with `esc_sql()`

## [1.1.8] - 2024-12-15

### Added
- Content Cluster visualization
- Hub page detection algorithm
- Cluster strength metrics

### Improved
- Link Juice calculation algorithm
- Dashboard performance optimization

## [1.1.7] - 2024-12-01

### Added
- HTTP Status Checker feature
- Bulk link scanning
- Elementor link extraction support

### Fixed
- Orphan page filter by post type
- Pagination on Link Juice page

## [1.1.0] - 2024-11-15

### Added
- Internal Link Assistant
- Link Plan with auto-insert capability
- Rollback functionality for bulk operations
- Orphan page detection
- Weak page identification

### Changed
- Redesigned dashboard with link metrics
- Improved TOC styling options

## [1.0.0] - 2024-10-01

### Added
- Initial release
- Content Analyzer with readability scoring
- Table of Contents (TOC) generator
- Auto-insert TOC functionality
- Shortcode `[cg_toc]` support
- Basic link metrics
- Focus keyword tracking
