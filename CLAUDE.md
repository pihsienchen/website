# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a multilingual Hugo-based website for pianist Pi-hsien Chen, featuring a sophisticated audio player system and comprehensive content management across 5 languages (English, German, French, Simplified Chinese, Traditional Chinese). The site showcases a distinguished pianist's career with an extensive recording archive and persistent audio playback functionality.

## Hugo Configuration & Build Commands

### Development
```bash
# Start development server with live reload
hugo server -D --bind 0.0.0.0

# Build for production
hugo --minify

# Clean build cache and resources
hugo mod clean
```

### Deployment
- **Hosting**: Netlify with automatic deployment on git push
- **Hugo Version**: 0.148.2 (specified in netlify.toml:6)
- **Build Command**: `hugo --minify` (netlify.toml:2)
- **Publish Directory**: `public` (netlify.toml:3)

## Development Notes

- **Audio Player**: Persistent across page navigation (technical specs in OLD-REQUIREMENTS.md:87-112)
- **Analytics**: Google Analytics 4 integration configured but not active (hugo.toml:160)
- **SEO**: Multilingual sitemaps and proper language declarations
- **Security**: HTTPS-only, no sensitive data storage
- Don't ask to run hugo server, it is usually running already

## Working Guidelines

- Let us first and foremost only work on the English version of the website, expect if I specifically ask you to copy all changes from the English version to those of other languages.

## Server Management Notes

- Do not reload the Hugo server, it is already running in the background and updates automatically when changes are made to the repository.