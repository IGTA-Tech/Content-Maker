# Content Maker Visual Flows for Napkin Pro

---

## FLOW 1: APPS SCRIPT INTERNAL TOOL (Current System)

### Overview
Autonomous content generation system using Google Apps Script for internal brands: Innovative Automations, Sherrod Sports Visas, and IGTA Aventus.

### The 5 Input Sources

1. **Target Website Content**
   - Website scraper at innovativeglobaltalent.com/webscrape
   - Scrapes target website pages
   - Extracts names, visa types, case studies, testimonials
   - Outputs to Google Sheet tab
   - Runs on scheduled trigger every X days
   - Only scrapes new content on subsequent runs

2. **Competitor Content**
   - Same website scraper tool
   - Scrapes competitor websites
   - Analyzes their topics, keywords, strategy
   - Identifies content gaps and opportunities
   - Outputs to Competitors tab in Google Sheet
   - Scheduled trigger for monitoring updates

3. **Influencer Content**
   - Perplexity API integration
   - Searches for industry thought leaders
   - Finds trending influencer topics
   - Identifies hot discussions
   - Runs on scheduled trigger
   - Outputs to Inspiration Sources tab

4. **Current Events and News**
   - Perplexity API real-time search
   - Today news at 20 percent weight
   - This week news at 50 percent weight
   - This month news at 30 percent weight
   - Monitors former client news
   - Feeds into content generation

5. **User Input On-Demand Requests**
   - Currently manual trigger via Google Sheets menu
   - Future state is web portal for requests
   - Allows specific topic requests
   - Specifies keywords and angle
   - Queues content for generation

### Knowledge Base System

- Google Drive folder structure
- Main folder is Innovative Automations Knowledge Base
- Contains Success Stories subfolder with Client Wins and Case Examples
- Contains News Updates subfolder with Industry Trends and Company News
- Contains Case Studies subfolder with Technical Deep Dives and Implementation Guides
- Contains Inspiration Sources subfolder with Competitor Blogs and Industry Leaders and Writing Guides
- Supports Google Docs, PDFs, Word files, Markdown, Text files
- Self Learning Database tracks generation metrics over time
- Activates learning mode after 5 generations

### Content Generation Pipeline

Step 1: Trigger fires at 4 AM EST daily or manual trigger from menu

Step 2: Load configuration from Script Properties and Config sheet

Step 3: Validate API keys for Claude and OpenAI

Step 4: Determine content strategy by analyzing category usage

Step 5: Gather all inputs including scraped data and current events and knowledge base

Step 6: Send to Claude Sonnet 4 with comprehensive prompt

Step 7: Claude generates 2 complete articles in JSON format

Step 8: Verification Layer 1 checks confidence score must be 90 percent or higher

Step 9: Verification Layer 2 checks all names against approved list

Step 10: Verification Layer 3 checks title length and meta description and word count and HTML structure

Step 11: If verification fails then retry up to 3 times

Step 12: Generate thumbnails using DALL-E 3 for each article

Step 13: 15 second delay between image generations for rate limiting

Step 14: Publish to WordPress via REST API for Innovative Automations brand

Step 15: Or send via email with attachments for SSV and IGTA brands

Step 16: Archive content to Content Archive sheet

Step 17: Update Self Learning Database with generation metrics

Step 18: Send notification email with success or failure status

### Cross-Brand Backlink System

Purpose is to build SEO authority across all internal brands

Brands in Network
- Innovative Automations at innovativeautomations.dev
- Sherrod Sports Visas at sherrodsportsvisas.com
- IGTA Aventus at aventus.com

How It Works
1. After article is generated analyze content for linking opportunities
2. Find contextually relevant articles from other internal brands
3. Inject 1 to 2 natural backlinks where they make sense
4. Use varied anchor text to avoid over-optimization
5. Prioritize links that add value for the reader
6. Track backlinks in Backlink Log sheet

Link Relationships
- IGTA links to SSV when immigration topics mentioned
- IGTA links to IA when automation topics mentioned
- SSV links to IGTA when international talent topics arise
- SSV links to IA when process automation discussed
- IA links to SSV when sports or visa examples used
- IA links to IGTA when global talent mentioned

Benefits
- Builds domain authority across all brands
- Creates natural link network
- Improves SEO for all sites
- Distributes link equity fairly
- Readers discover related services

### Output Per Run
- 2 SEO-optimized blog articles
- 2 AI-generated thumbnail images
- Cross-brand backlinks injected where relevant
- Updated analytics and learning data
- Email notification with results

---

## FLOW 2: SAAS PLATFORM (Next.js Future System)

### Overview
Multi-brand SaaS platform allowing any business to automate content generation with modern web interface and enterprise-grade infrastructure.

### User Journey

Step 1: User signs up with email via Supabase Auth

Step 2: User creates organization for their company

Step 3: User invites team members with roles of Owner or Admin or Member

Step 4: User creates a brand for their website or blog

Step 5: User completes 11 step onboarding wizard

Step 6: System runs automated daily content generation

Step 7: User monitors analytics dashboard

### 11 Step Onboarding Wizard

Step 1 Website Scraping
- Enter target website URL
- Choose full crawl up to 100 pages or specific pages
- System crawls and extracts titles headings content CTAs links
- Creates vector embeddings for semantic search
- Stores in PostgreSQL with pgvector

Step 2 News Sources
- AI suggests 8 to 10 industry-specific sources
- User selects relevant RSS feeds and websites
- System monitors for current events
- Scheduled fetching keeps data fresh

Step 3 YouTube Channels
- AI suggests 6 to 8 thought leaders
- User adds industry influencers
- Can mark own channel for priority
- Extracts transcripts for knowledge base

Step 4 RAG Documents Upload
- Upload PDFs, DOCX, TXT, MD files
- System chunks documents
- Creates embeddings with OpenAI
- Stores in vector database for retrieval

Step 5 Success Stories
- Add client case studies
- Include client name and industry
- Document challenge and solution and results
- Add testimonial quotes and metrics

Step 6 Thumbnail Settings
- Set brand colors primary secondary accent
- Choose image style like modern minimalist or dynamic action
- Configure DALL-E prompt preferences

Step 7 Competitors
- AI detects competitor websites
- User confirms and adds more
- System monitors their content
- Identifies topic gaps and opportunities

Step 8 Content Calendar
- AI suggests weekly themes
- Monday Motivation Tuesday Tutorial Wednesday Tips etc
- Customizable per day of week

Step 9 Generation Settings
- Select AI model Claude Sonnet 4
- Set posts per day 1 or 2 or 3
- Set run time in UTC
- Configure confidence threshold 90 percent
- Set word count range 1500 to 2500

Step 10 Publishing Platform
- Choose WordPress or Netlify or Vercel or Ghost or Squarespace
- Enter API credentials
- Test connection
- Select publish mode auto or approval or queue

Step 11 Brand Voice and Rules
- Define brand voice and tone
- Set required elements like CTA and links
- Set forbidden elements like competitor names
- Add custom rules

### Content Generation Pipeline

Step 1 Topic Selection
- Claude analyzes brand context
- Checks recent posts to avoid duplicates
- Suggests 5 topic options
- Or uses user-requested topic

Step 2 Research Context
- Perplexity API searches for current info
- Returns summary and key points and sources
- Provides relevance score

Step 3 RAG Retrieval
- Query embedded with OpenAI
- Semantic search in pgvector
- Returns top 5 matching chunks above 0.7 similarity
- Sources from scraped pages and documents and success stories

Step 4 Content Generation
- Claude Sonnet 4 generates article
- Includes brand voice guidelines
- Applies required and forbidden elements
- Produces title slug meta keywords content
- Outputs confidence score

Step 5 Confidence Check
- If below threshold then retry with enhanced instructions
- Adds exceptional quality requirement
- Adds actionable insights requirement

Step 6 Thumbnail Generation
- DALL-E 3 creates image
- Uses article title and category
- Applies brand colors
- 1792x1024 HD landscape
- No text or faces or logos

Step 7 Backlink Injection
- AI analyzes article content
- Finds related articles from other brands
- Injects 1 to 2 natural anchor text links
- Distributes link equity across brands

Step 8 Git Push
- Commits MDX file to GitHub repo
- Includes frontmatter with title date slug keywords thumbnail
- Triggers via Octokit API

Step 9 Deployment Trigger
- Calls Vercel or Netlify webhook
- Triggers site rebuild
- New content goes live

Step 10 Google Indexing
- Submits URL to Search Console API
- Requests instant indexing
- Logs response status

### Database Schema
- Organizations table for companies
- Users table with roles
- Brands table with settings
- Scraped Pages table with embeddings
- Knowledge Base table with chunks
- Generated Content table with articles
- Analytics table with performance data
- Publishing Platforms table with credentials
- Content Calendar table with themes
- Generation Settings table with AI config
- Brand Rules table with voice guidelines

### Publishing Platforms Supported
1. WordPress via REST API with Basic Auth
2. Netlify via Git push and deploy webhook
3. Vercel via Git push and deploy webhook
4. Ghost via Admin API
5. Squarespace via email delivery

### Analytics Dashboard
- Scraped pages count
- Generated articles count
- Published articles count
- Pending review count
- Recent content list with status
- Page views and unique visitors
- Bounce rate and engagement metrics
- Performance charts over time

---

## FLOW 3: THE 5 INPUT SOURCES (Detailed)

### Source 1 Target Website Content
- Purpose is to understand what content already exists
- Tool is website scraper at innovativeglobaltalent.com/webscrape
- Process is enter URL then scrape all pages then extract data then store in sheet
- Data extracted includes page titles and headings and main content and CTAs and internal links and external links
- Trigger runs every X days for new content only
- Output goes to Website URLs tab in Google Sheet

### Source 2 Competitor Content
- Purpose is to identify content gaps and opportunities
- Tool is same website scraper
- Process is enter competitor URLs then scrape their blogs then analyze topics and keywords
- Data extracted includes their article topics and keywords used and content structure and publishing frequency
- Trigger runs on schedule to monitor updates
- Output goes to Competitors tab in Google Sheet

### Source 3 Influencer Content
- Purpose is to find trending topics and thought leadership
- Tool is Perplexity API
- Process is search for industry influencers then find their hot topics then identify trends
- Data includes influencer names and their recent topics and engagement signals
- Trigger runs on schedule
- Output goes to Inspiration Sources tab

### Source 4 Current Events and News
- Purpose is to make content timely and relevant
- Tool is Perplexity API real-time search
- Process is search today news at 20 percent then this week at 50 percent then this month at 30 percent
- Also monitors former client news for updates
- Data includes headlines and dates and relevance scores and source links
- Feeds directly into content generation prompt

### Source 5 User Input Requests
- Purpose is to allow on-demand specific content
- Current tool is Google Sheets menu trigger
- Future tool is web portal
- Process is user enters topic and keywords and angle then queues for generation
- Data includes requested topic and target keywords and content angle and priority level
- Triggers immediate or scheduled generation

---

## FLOW 4: SELF LEARNING SYSTEM

### How It Works
1. System generates content daily
2. Archives each generation with metrics
3. Tracks confidence scores and word counts and success rates
4. After 5 generations has enough data
5. Activates self-learning mode
6. Analyzes patterns from past generations
7. Applies learned optimizations to new content
8. Avoids duplicating previous topics
9. Improves style based on success metrics

### Data Tracked
- Generation date
- Generation number
- Articles published count
- Success rate percentage
- Style confidence score
- Average word count
- Average confidence score
- Notes and observations

### Learning Applied
- Checks Content Archive before generating
- Instruction to Claude says create content different from existing
- Uses past confidence patterns to improve prompts
- Adapts word count targets based on success
- Refines tone based on brand voice feedback

---

## FLOW 5: VERIFICATION SYSTEM

### Triple Layer Verification for SSV

Layer 1 Confidence Score
- Check if confidence is 90 percent or higher
- If below then reject and retry

Layer 2 Name Verification
- Get list of approved names from Verified Names sheet
- Check every name used in article
- If any unapproved name found then reject

Layer 3 Critical Elements
- Check attorney name spelled correctly as Sherrod Seward
- Check word count between 1500 and 3000
- Check title under 60 characters
- Check meta description exactly 155 characters
- Check H1 and H2 headings present

### Six Layer Verification for Innovative Automations

Layer 1 Confidence Score at 92 percent threshold

Layer 2 Word Count between 1200 and 2500

Layer 3 Required Fields present including title slug meta content keywords image prompt

Layer 4 HTML Structure with proper p tags and h2 tags and h3 tags

Layer 5 SEO Elements including keywords and internal links

Layer 6 Excerpt Length under 150 characters

### Retry Logic
- If any layer fails then log error
- Wait 5 seconds
- Retry generation with same context
- Maximum 3 retry attempts
- If all fail then send error alert email

---

## FLOW 6: PUBLISHING DESTINATIONS

### WordPress Auto Publish Flow
1. Generate article content
2. Generate thumbnail image
3. Upload thumbnail to WordPress Media Library
4. Get or create category in WordPress
5. Get or create tags from keywords
6. Create post via REST API
7. Set featured image
8. Set Yoast SEO meta data
9. Publish immediately
10. Return published URL
11. Archive with URL

### Email Delivery Flow
1. Generate article content
2. Generate thumbnail image
3. Build HTML email with preview
4. Create markdown file attachment
5. Attach thumbnail image
6. Include SEO metadata in email
7. Include publishing instructions
8. Send to configured recipients
9. Recipients manually upload to Squarespace
10. Archive as sent

### Git Based Publishing Flow for SaaS
1. Generate article content
2. Generate thumbnail image
3. Create MDX file with frontmatter
4. Commit to GitHub repository via API
5. Include metadata in commit message
6. Trigger Vercel or Netlify webhook
7. Wait for deployment
8. Submit URL to Google Search Console
9. Log indexing response
10. Archive with published URL

---

## FLOW 7: THUMBNAIL GENERATION

### Input Requirements
- Article title
- Article category
- Primary keyword
- Brand color palette
- Image style preference

### DALL-E 3 Prompt Construction
- Start with professional blog thumbnail description
- Add article title context
- Add category theme
- Specify brand colors like blue palette
- Request 16:9 landscape at 1792x1024
- Request HD quality
- Request clean minimal aesthetic
- Specify NO text in image
- Specify NO logos in image
- Specify NO faces in image
- Request modern professional style

### Process
1. Build enhanced prompt from article data
2. Call OpenAI DALL-E 3 API
3. Request single image
4. Set size to 1792x1024
5. Set quality to HD
6. Set style to natural
7. Receive image URL
8. Download image as blob
9. Wait 15 seconds for rate limiting
10. Repeat for second article

### Output
- High resolution thumbnail image
- Professional corporate aesthetic
- Matches article theme
- Ready for WordPress or email attachment

---

## FLOW 8: CROSS-BRAND BACKLINK SYSTEM

### Purpose
Build SEO authority across all internal brands by creating natural contextual links between sites

### The Brand Network

Brand 1 Innovative Automations
- Website is innovativeautomations.dev
- Topics include business automation and AI integration and workflow optimization
- Links out when mentioning sports immigration or global talent

Brand 2 Sherrod Sports Visas
- Website is sherrodsportsvisas.com
- Topics include P1 visas and O1 visas and EB1A and athlete immigration
- Links out when mentioning automation solutions or global talent acquisition

Brand 3 IGTA Aventus
- Website is aventus.com
- Topics include international talent and global hiring and immigration services
- Links out when mentioning specific visa types or automation tools

### Backlink Injection Process

Step 1 Article Generation Complete
- Full article content is ready
- All verification passed
- Ready for backlink analysis

Step 2 Content Analysis
- AI scans article content
- Identifies topics and themes
- Finds potential link opportunities
- Checks for relevant keywords

Step 3 Match with Other Brands
- Compare topics against other brand content
- Find contextually relevant pages
- Prioritize high-value link targets
- Select 1 to 2 best matches

Step 4 Natural Link Insertion
- Find appropriate sentence or paragraph
- Create natural anchor text
- Insert link without disrupting flow
- Ensure link adds reader value

Step 5 Link Tracking
- Log source brand and article
- Log target brand and URL
- Log anchor text used
- Log date created
- Store in Backlink Log sheet

### Link Rules
- Maximum 2 backlinks per article
- Links must be contextually relevant
- Anchor text must be varied
- No keyword stuffing
- Links should help the reader
- Fair distribution across all brands

### Example Link Scenarios

Scenario 1 IA Article About Hiring International Developers
- Mention global talent acquisition
- Link to IGTA page about international hiring
- Anchor text like partnering with global talent experts

Scenario 2 SSV Article About Athlete Visa Success
- Mention streamlining visa process
- Link to IA page about automation
- Anchor text like automated document processing

Scenario 3 IGTA Article About Immigration Compliance
- Mention specific visa categories
- Link to SSV page about P1 or O1 visas
- Anchor text like specialized sports visa attorneys

### SEO Benefits
- Increases domain authority for all sites
- Creates topical relevance signals
- Improves internal link structure
- Helps search engines understand relationships
- Drives referral traffic between sites
- Builds trust through association

---

## COMPARISON: APPS SCRIPT vs SAAS

### User Interface
- Apps Script uses Google Sheets menus
- SaaS uses modern web dashboard

### Database
- Apps Script uses Google Sheets tabs
- SaaS uses PostgreSQL with pgvector

### Knowledge Base
- Apps Script uses Google Drive folders
- SaaS uses RAG with vector embeddings

### Scraping
- Apps Script uses external tool at innovativeglobaltalent.com
- SaaS has built-in scraper with semantic embedding

### Publishing
- Apps Script does WordPress or Email
- SaaS does WordPress and Git and Ghost and Squarespace

### Multi Brand
- Apps Script needs separate scripts per brand
- SaaS has native multi-tenant support

### Scalability
- Apps Script limited by Google Sheets
- SaaS is enterprise grade unlimited

### User Input Portal
- Apps Script needs manual menu trigger
- SaaS has web portal for requests

### SEO Features
- Apps Script has basic meta and keywords
- SaaS adds Google Search Console and instant indexing and cross-brand backlinks

### Self Learning
- Apps Script tracks in spreadsheet
- SaaS has full analytics with performance feedback loop
