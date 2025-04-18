# Notion CMS Helper for Next.js Websites
A simple tool that helps you use Notion as a content management system (CMS) for your Next.js website. It's like having a free, easy-to-use admin panel for your website content!

## What It Does
- Connects your website to your Notion pages
- Automatically organizes your content (like projects, articles, etc.)
- Makes it easy to update your website by just editing your Notion pages
- Keeps everything organized and type-safe

## How to Use It
```typescript
// Create a new portfolio helper
const portfolio = new Portfolio();

// Get all your content
const allContent = await portfolio.getPortfolio();

// Or get just your projects
const justProjects = await portfolio.getPortfolio('project');
```

## What You Can Add to Your Website
- About Me section
- Projects
- Social media links
- Articles
- School/Work experience
- Skills
- Certifications
- And more!

## What You Need
- A Notion account
- A Notion API key (free!)
- A Next.js website
- This code! ��

## Why It's Cool
- Free CMS (no need to pay for WordPress or similar)
- Super easy to update (just edit your Notion pages)
- Works great with Next.js
- Keeps your code organized
