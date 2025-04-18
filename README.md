# Cedar: Using Notion as a CMS for Your Next.js Portfolio

Hey! This is a simple way to use Notion as a content management system for your portfolio website. Instead of hardcoding your projects and content, you can just update your Notion pages and the changes will show up on your site.

## Setting Up Your Notion Database

First, you'll need to create a Notion database with these columns:

- **Name** (Title property)
- **Description** (Rich text property)
- **Type** (Select property with options: project, article, social, etc.)
- **Link** (URL property)
- **Timeline** (Date property)
- **Files** (Files property)
- **Publish** (Checkbox property)

## Creating a Notion Integration

1. Go to [Notion's integration page](https://www.notion.so/my-integrations)
2. Click "New integration"
3. Give it a name (like "Portfolio CMS")
4. Copy the "Internal Integration Token" (you'll need this later)
5. Go to your database, click the three dots menu, and select "Add connections"
6. Find your new integration and connect it to your database
7. Copy your database ID from the URL (it's the part after the workspace name and before the question mark)

## Project Structure

Here's where to put the files in your Next.js project:

your-project/

├── lib/

│ └── notion.ts # Notion integration code

├── components/

│ ├── parser.tsx # Content parser component

│ └── portfolio.tsx # Portfolio display component

└── .env.local # Your environment variables

## The Code

### 1. Notion Integration (`lib/notion.ts`)
This is the main file that talks to Notion. Copy this into your `lib` folder:

```typescript
// Your notion.ts code here
```

### 2. Content Parser (`components/parser.tsx`)
This component makes your Notion content look nice. Put it in your components folder:

```typescript
// Your parser.tsx code here
```

### 3. Portfolio Component (`components/portfolio.tsx`)
This is where you display everything. Add it to your components folder:

```typescript
// Your portfolio.tsx code here
```

## Setting Up Environment Variables

Create a `.env.local` file in your project root:

```
NEXT_PUBLIC_NOTION_PORTFOLIO_CMS_KEY=your_integration_token_here
NEXT_PUBLIC_NOTION_DB_ID=your_database_id_here
```


## Using the Components

In any page where you want to show your portfolio content:

```typescript
import { Portfolio } from '@/components/portfolio';

export default function Home() {
  return (
    <main>
      <Portfolio />
    </main>
  );
}
```

## How It Works

1. The `notion.ts` file fetches your content from Notion
2. The `parser.tsx` component makes the content look nice
3. The `portfolio.tsx` component displays everything in a clean layout

## Updating Your Content

To update your portfolio:
1. Just edit your Notion database
2. Make sure to check the "Publish" checkbox for items you want to show
3. Your changes will appear on your site

## Troubleshooting

If something's not working:
- Double-check your Notion integration is connected to your database
- Make sure your environment variables are correct
- Check that your database has all the required columns
- Look at the browser console for any errors

## Need Help?

Feel free to open an issue if you run into problems. I'm happy to help!
