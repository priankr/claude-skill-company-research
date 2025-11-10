# Substack Notes: Features and Functionality

**Document Version:** 1.0  
**Last Updated:** November 10, 2025

## Executive Summary

Substack Notes is a short-form microblogging feature integrated into the Substack subscription publishing platform. Launched in April 2023, Notes enables writers and readers to share quick thoughts, links, images, and videos in a Twitter-like social feed designed to drive discovery and engagement across the Substack network.

Unlike traditional social media platforms that rely on advertising and algorithmic manipulation, Notes operates within Substack's subscription economy model. The feature allows creators to maintain more frequent touchpoints with their audience between longer newsletter posts while fostering organic discovery of new writers and publications. Notes can include original posts, restacked content (similar to retweets), images, videos (up to 5 minutes), and links, all accessible through the Substack web platform and mobile apps.

As of 2025, Notes has evolved from a basic text-sharing feature to a multimedia platform supporting video, external embeds, and algorithmic distribution beyond immediate subscriber networks. The feature serves as a middle ground between Substack's long-form newsletter format and the immediacy of social media, positioning itself as a healthier alternative to attention-driven platforms.

**Key Differentiators:**

- **Subscription-based incentives** – Notes operates within a paid subscription model rather than an ad-driven attention economy, creating different content incentives
- **Creator ownership** – Writers maintain ownership of their audience relationships and content, with the ability to export data anytime
- **Content longevity** – Unlike typical social feeds where content disappears within hours, Notes posts can surface for days or weeks
- **Direct monetization** – Notes can drive subscription conversions directly, with no intermediary ad model
- **Network discovery** – Integrated recommendations and restacking features help new creators gain visibility organically
- **Multimedia integration** – Seamlessly combines with newsletters, podcasts, Chat, and other Substack features in a unified creator platform

---

## Target Audience

Substack Notes is designed for:

**Primary Users:**
- Independent writers and journalists building subscriber-based businesses
- Newsletter creators seeking to increase engagement between posts
- Readers interested in discovering new writing and participating in discussion
- Podcasters and multimedia creators expanding audience touchpoints
- Former social media users seeking healthier engagement patterns

**Secondary Audiences:**
- Casual readers exploring Substack's content network
- Writers testing content ideas before committing to full posts
- Community builders fostering discussion around specific topics or niches

---

## 1. Core Architecture / Product Overview

**Platform Components:**

Substack Notes is accessible through three primary interfaces:

1. **Web Application** – Full-featured desktop interface accessed via substack.com, available from user profile dropdown menu
2. **iOS Mobile App** – Native application with Home tab dedicated to Notes feed and integrated posting capabilities
3. **Android Mobile App** – Native application mirroring iOS functionality with platform-specific optimizations

**Technical Infrastructure:**

Notes operates as an integrated module within Substack's broader publishing infrastructure, sharing authentication, user profiles, and subscription management systems with the core newsletter platform. The feed uses a hybrid recommendation algorithm combining:
- Chronological display of followed users' activity
- Algorithmic surfacing of content from extended network
- Engagement-based amplification (restacks, likes, replies from followed users)

**Data Model:**

Notes exist as discrete content objects separate from newsletter posts but linked to user profiles and publications. Each note includes:
- Text content (with formatting options)
- Optional media attachments (images, videos up to 5 minutes)
- Metadata (timestamp, engagement metrics, visibility settings)
- Relationship data (replies, restacks, likes)

**Deployment:**

Notes is a cloud-hosted service with no self-hosted options, fully managed by Substack's infrastructure team.

---

## 2. Content Creation & Publishing

### 2.1. Creating Notes

**Creation Process:**

Users can create notes through multiple entry points:

**On Web:**
1. Navigate to Notes via profile picture dropdown
2. Click the "What's on your mind?" input field
3. Compose text, add media, mention users, or include links
4. Click "Post" to publish

**On Mobile App:**
1. Tap the "+" icon in the app navigation
2. Select "Note" from content type options
3. Compose and publish

**Content Options:**

- **Text Posts** – Plain text with basic formatting (bold, italic, paragraph breaks)
- **Link Sharing** – URLs automatically generate preview cards with titles and images
- **Image Upload** – Single or multiple images from device or gallery
- **Video Upload** – Videos up to 5 minutes long, recorded in-app or uploaded from device
- **Quotes** – Formatted text excerpts with attribution
- **Restacks** – Sharing others' notes with optional commentary

### 2.2. Restacking

**Functionality:**

Restacking is Substack's term for resharing content, analogous to Twitter's retweet feature. Users can:

- **Simple Restack** – Share a note as-is to your followers
- **Restack with Commentary** – Add your own thoughts above the shared content
- **Restack Newsletters** – Share full newsletter posts to the Notes feed, promoting long-form content

**Purpose:**

Restacking serves multiple functions:
- Amplifies quality content across the network
- Helps followers discover new writers
- Provides social proof and endorsement
- Drives newsletter subscriptions through content sampling

### 2.3. Text Formatting

**Available Formatting:**

Notes supports basic text formatting including:
- **Bold** and *italic* emphasis
- Paragraph breaks
- @ mentions (tagging other Substack users)
- Link embedding with automatic preview generation

**Limitations:**

Unlike full newsletter posts, Notes does not support:
- Headers or subheaders
- Bullet lists or numbered lists
- Block quotes
- Embedded media players beyond images/videos
- Custom HTML or CSS

---

## 3. Discovery & Feed Algorithm

### 3.1. Feed Types

**Home Feed:**

The primary Notes feed showing content from multiple sources:
- Notes from subscribed publications
- Notes from followed users
- Restacks by people you follow
- Comments on posts from your network
- Algorithmically recommended content from extended network
- "From the archives" – older Notes resurfaced by algorithm

**Subscribed Feed:**

A filtered view showing only content from publications the user has subscribed to, providing a more curated experience.

### 3.2. Distribution Mechanics

**Primary Distribution:**

When a user posts a note, it is immediately visible to:
- Their subscribers (free and paid)
- Their followers (users who follow without subscribing)
- Anyone with a direct link to the note

**Secondary Distribution:**

Notes can reach broader audiences through:
- **Engagement amplification** – When followed users like, reply, or restack a note, it may surface in their followers' feeds
- **Algorithmic recommendations** – Substack's algorithm may show notes to users who don't follow the creator but might be interested based on behavior
- **Network effects** – Notes from writers recommended by subscribed publications may appear
- **Trending/Featured** – High-engagement notes may receive additional algorithmic boost

### 3.3. Discoverability Features

**Follow vs. Subscribe:**

Substack distinguishes between two types of connections:
- **Follow** – See a user's Notes activity without receiving their newsletter emails
- **Subscribe** – Receive newsletters plus see Notes activity

This distinction allows readers to engage with creators at different commitment levels.

**User Discovery:**

Notes includes features to help users find new voices:
- Recommended writers based on interests
- "Who to follow" suggestions
- Trending notes and active discussions
- Search functionality for topics and users

---

## 4. Engagement Features

### 4.1. Likes

Users can "like" notes, similar to favoriting content on other platforms. Likes serve as:
- Lightweight engagement signal
- Bookmarking mechanism
- Algorithmic signal for distribution
- Social proof indicator

### 4.2. Replies

**Threading:**

Notes supports nested replies creating conversation threads. Users can:
- Reply directly to notes
- Reply to other replies (nested conversations)
- View entire conversation threads
- Be notified of replies to their notes or comments

**Visibility:**

Replies are visible to:
- The note author
- Other participants in the thread
- Followers of participants (via feed activity)
- Anyone viewing the original note

### 4.3. Restacks

As described earlier, restacking allows content to flow through the network, with engagement metrics tracking:
- Total restack count
- Who restacked (visible to note author)
- Restack activity appearing in followers' feeds

### 4.4. Sharing

**External Sharing:**

Notes can be shared outside Substack through:
- Direct links (notes are publicly accessible URLs)
- Social media sharing to X (Twitter), Facebook
- Image export for Instagram sharing
- Embedding on external websites (added April 2024)

---

## 5. Notifications & Engagement Tracking

### 5.1. Notification Types

**Push Notifications (Mobile):**

Users can receive mobile push notifications for:
- Likes on their notes
- Replies to their notes
- Restacks of their notes or posts
- Mentions in notes

**Email Notifications:**

Configurable email notifications for:
- Same engagement actions as push notifications
- Notes digest (periodic roundup of missed activity)
- Notes from specific followed users

**In-App Notifications:**

Real-time notification feed within the app showing all engagement activity.

### 5.2. Analytics

**View Stats:**

Each note includes a "View stats" option showing:
- Total views
- Likes, replies, and restacks
- Subscriber conversions generated (if applicable)
- Engagement over time

**Publication-Level Analytics:**

Dashboard analytics include:
- Notes performance metrics
- Engagement trends
- Traffic driven to newsletter posts
- Subscriber growth attributed to Notes activity

---

## 6. Video Capabilities

### 6.1. Video Notes

**Introduced:** April 2024

**Specifications:**
- Maximum length: 5 minutes
- Upload sources: Device camera roll, desktop files, or in-app recording
- Formats supported: Standard video formats (MP4, MOV, etc.)

**Features:**
- Caption/description text accompanying video
- Paywall option (restrict video to paid subscribers only)
- Notification options (email or push notification to followers)
- Inline player on mobile for watch-while-scrolling experience

**Use Cases:**
- Behind-the-scenes content
- Quick video commentary
- Interviews or conversations
- Visual updates or announcements
- Supplemental content for newsletters

### 6.2. Video in Chat Integration

Video support extends to Substack Chat (the private community feature), allowing:
- 5-minute video messages in threaded discussions
- Video replies from subscribers (planned feature)
- Community-exclusive video content

---

## 7. Integration with Broader Substack Ecosystem

### 7.1. Newsletter Integration

**Cross-Promotion:**

Notes and newsletters work together through:
- **Teaser content** – Short notes can preview or excerpt upcoming newsletter posts
- **Post promotion** – Full newsletter posts can be restacked into Notes feed
- **Link inclusion** – Notes can include links driving traffic to newsletters
- **Behind-the-scenes** – Notes provide casual updates between formal newsletter publications

### 7.2. Chat Integration

Substack Chat (private group messaging feature) connects with Notes through:
- Notes can reference Chat conversations
- Chat discussions can spawn public Notes
- Cross-promotion between private community and public feed

### 7.3. Recommendations

The Recommendations feature (allowing writers to recommend other publications) integrates with Notes by:
- Recommended writers' notes appearing in followers' feeds
- Notes activity influencing recommendation algorithms
- Restack behavior signaling publication quality

### 7.4. Substack Reader App

The Reader app (Substack's mobile reading application) treats Notes as a first-class feature:
- Dedicated Home tab for Notes feed
- Unified inbox combining newsletters and Notes
- Single interface for all Substack content consumption

---

## 8. Privacy & Moderation

### 8.1. Privacy Settings

**Note Visibility:**

All notes are publicly accessible by default. Currently, Substack does not offer:
- Private notes visible only to subscribers
- Draft notes saved for later
- Scheduled note posting

**Account Settings:**

Users control:
- Who can mention them in notes
- Notification preferences
- Blocking and muting other users

### 8.2. Content Moderation

**Platform Approach:**

Substack employs a light-touch moderation philosophy:
- Community self-moderation emphasized
- Publishers set their own engagement rules
- Platform intervenes only for harassment, threats, spam, pornography, or calls for violence
- Controversial: Substack has received criticism for allowing extremist and hateful content under free speech principles

**User Tools:**

Individual moderation controls include:
- Blocking users (prevents them from seeing or engaging with your content)
- Muting users (hides their content from your feed without blocking)
- Reporting inappropriate content
- Comment moderation on own notes

---

## 9. Monetization & Business Model

### 9.1. Direct Monetization

Notes does not have direct monetization (e.g., users cannot charge for notes), but it supports indirect monetization through:

**Subscriber Conversion:**

Notes serve as a funnel to paid newsletter subscriptions:
- Teaser content driving curiosity
- Personality and voice establishment
- Regular touchpoints maintaining top-of-mind awareness
- Direct links to subscription pages

**Metrics:**

Analytics track subscriber conversions attributed to Notes activity, helping creators understand ROI.

### 9.2. Creator Business Model

Notes fits into Substack's broader creator economy:
- Free to use regardless of subscriber count
- No per-note fees or engagement-based charges
- Supports overall subscription revenue through discovery
- Part of the 10% platform fee model (Notes don't change fee structure)

---

## 10. User Workflows

| Use Case | Workflow Steps |
|----------|----------------|
| **Writer sharing quick thought** | 1. Open Notes<br>2. Type thought in "What's on your mind?"<br>3. Click "Post"<br>4. Note appears in followers' feeds |
| **Promoting new newsletter** | 1. Publish newsletter post<br>2. Go to Notes<br>3. Click "Restack" on published post<br>4. Add commentary about post<br>5. Post to Notes feed |
| **Discovering new writers** | 1. Browse Home feed<br>2. See note from unfamiliar writer (appeared via algorithm or restack)<br>3. Click on writer's profile<br>4. Follow or subscribe |
| **Engaging with community** | 1. See interesting note in feed<br>2. Like, reply, or restack<br>3. Receive notifications when others respond<br>4. Continue threaded conversation |
| **Sharing video update** | 1. Open Notes<br>2. Click "+" icon<br>3. Select "Video"<br>4. Record or upload video (max 5 min)<br>5. Add caption<br>6. Choose whether to paywall<br>7. Post with optional email/push notification |

---

## 11. Competitive Positioning

### vs. Twitter/X

| Substack Notes | Twitter/X |
|----------------|-----------|
| • Subscription-based incentives<br>• No ads<br>• Content longevity (resurfaces over time)<br>• Writer ownership<br>• Lower toxicity (smaller community) | • Algorithm rewards engagement/controversy<br>• Ad-supported model<br>• Rapid content decay<br>• Platform owns audience relationship<br>• Larger network effects |

### vs. LinkedIn Posts

| Substack Notes | LinkedIn |
|----------------|----------|
| • Creator-focused (writers, journalists)<br>• Subscription monetization<br>• Integrated with newsletter platform<br>• More casual/personal tone | • Professional networking context<br>• Business/career focused<br>• Separate from direct monetization<br>• Corporate/professional tone |

### vs. Medium

| Substack Notes | Medium |
|----------------|--------|
| • Short-form focused<br>• Part of subscription network<br>• Direct audience ownership<br>• Feed-based discovery | • Long-form primary<br>• Revenue sharing based on reads<br>• Algorithm controls distribution<br>• Article-focused discovery |

---

## 12. User Feedback & Sentiment

**Common Praise:**

- "Notes creates a sense of community that email alone cannot achieve"
- Effective for gaining 10-30+ subscribers daily when used strategically
- Content longevity provides ongoing value (notes continue surfacing weeks later)
- Less toxic environment compared to Twitter
- Genuine writer-to-writer support culture

**Common Criticism:**

- Algorithm increasingly pushing content from outside immediate network (diluting subscribed feed)
- Platform becoming more social media-like, diverging from original newsletter focus
- "Trending topics" feature showing algorithm-driven content feels manipulative
- Some writers concerned about time investment required for Notes success
- Email delivery issues when Notes become primary focus

**Creator Strategies:**

Successful writers report:
- Consistency matters more than virality
- Building genuine connections with other writers
- Using Notes Boosts (coordinated sharing events in Chat)
- Studying high-performing notes for patterns
- Treating Notes as community participation, not just promotion

---

## 13. Platform Roadmap & Future Direction

**Recent Changes (2024-2025):**

- Video support added (April 2024)
- External embedding capability (April 2024)
- Algorithm expanded to surface content beyond immediate network
- Chat video integration
- Spotify podcast sync (benefiting multimedia creators using Notes)

**Inferred Future Development:**

Based on platform trajectory and announced initiatives:
- Enhanced video features (longer clips, better editing)
- More sophisticated recommendation algorithms
- Potential live streaming integration
- Expanded analytics for Notes performance
- More granular privacy/audience controls
- Possible integration with emerging AI writing/creation tools

**Strategic Direction:**

Substack's July 2025 $100 million funding round suggests expansion of Notes as part of broader "creator universe" strategy, potentially including:
- Advertising integration (controversial given anti-ad founding principles)
- More social features competing with mainstream platforms
- Balance tension between newsletter focus and social network aspiration

---

## 14. Technical Limitations & Constraints

**Current Limitations:**

- No private or draft notes
- No scheduled posting
- 5-minute video length cap
- Limited text formatting options
- No native GIF support
- Cannot edit notes after posting (must delete and repost)
- No content warnings or sensitivity filters
- Limited moderation tools for creators

**Performance Considerations:**

- Mobile app occasionally experiences feed refresh issues
- Video upload speeds vary by connection quality
- Large image files may require compression
- Web interface is responsive but may lag on older browsers

---

## 15. Conclusion

Substack Notes represents a thoughtful attempt to create a healthier alternative to traditional social media while maintaining the benefits of quick, informal communication. By embedding short-form content within a subscription economy rather than an attention economy, Notes aligns incentives around quality and subscriber satisfaction rather than viral engagement.

**Key Capabilities:**

- Seamless integration with newsletter publishing platform
- Effective discovery mechanism for new writers
- Community-building tool between newsletter issues
- Multimedia support (text, images, video)
- Direct subscriber conversion tracking

**Primary Differentiators:**

- Subscription model creates different content incentives than ad-driven platforms
- Writer ownership and portability of audience
- Content longevity beyond typical social media lifecycle
- Integration with robust newsletter and monetization tools
- Lower toxicity due to subscription alignment and smaller scale

**Best Suited For:**

- Writers building subscription-based businesses
- Journalists seeking independence from traditional media
- Creators wanting healthier social media alternatives
- Publishers needing engagement tools between long-form content
- Readers seeking curated, quality discussions

**Key Takeaways:**

1. Notes succeeds as a discovery tool but requires active participation to see results
2. The subscription model creates healthier incentives than advertising
3. Integration with newsletters provides unique value proposition
4. Platform is evolving toward more social features, with mixed creator reception
5. Success requires treating Notes as community participation, not just promotion

---

## 16. Sources

1. [Substack Support | Getting started on Substack Notes](https://support.substack.com/hc/en-us/articles/14564821756308-Getting-started-on-Substack-Notes)
2. [On Substack | Introducing Substack Notes](https://on.substack.com/p/introducing-notes)
3. [TechCrunch | Substack's new short-form 'Notes' feed looks a lot like Twitter](https://techcrunch.com/2023/04/05/substacks-new-short-form-notes-feed-looks-a-lot-like-twitter/)
4. [Substack Tools | Substack Notes: What They Are & How to Use Them](https://www.substacktools.com/blog/substack-notes-what-they-are-and-how-to-use-them)
5. [Pubstack Success | How to Use Substack Notes to Get More Subscribers](https://pubstacksuccess.substack.com/p/substack-notes-a-tutorial)
6. [Bad Redhead Media | 10 Little-Known Substack Features](https://badredheadmediallc.substack.com/p/10-little-known-substack-features)
7. [Substack Home | How to Write Viral Substack Notes](https://substack.com/home/post/p-154980691)
8. [TechCrunch | Substack's Notes feature getting more Twitter-like capabilities](https://techcrunch.com/2024/04/16/substacks-notes-feature-is-getting-more-twitter-like-capabilities/)
9. [MakeUseOf | What Is Substack Notes](https://www.makeuseof.com/what-is-substack-notes/)
10. [Really Good Business Ideas | Substack Notes Explained: Features, Strategies, and Best Practices](https://www.reallygoodbusinessideas.com/p/what-is-substack-notes)
11. [Substack | A new economic engine for culture](https://substack.com/about-i)
12. [Wikipedia | Substack](https://en.wikipedia.org/wiki/Substack)
13. [Veronica Llorca-Smith | The End of The Substack Bubble: Now What?](https://veronicallorcasmith.substack.com/p/the-end-of-the-substack-bubble-now)
14. [TechCrunch | Substack brings video to Chat feature](https://techcrunch.com/2024/06/05/substack-brings-video-to-chat-feature/)
15. [On Substack | Sitemap 2024](https://on.substack.com/sitemap/2024)
