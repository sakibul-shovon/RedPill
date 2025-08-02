# RedPill - Movie Social Media Platform


### Project Title
**RedPill** - A Comprehensive Movie Social Media Platform

### Project Objective
To create a vibrant social media ecosystem that seamlessly combines movie discovery, social networking, and community building for cinema enthusiasts. RedPill aims to become the definitive destination where users can discover films, share experiences, connect with like-minded viewers, and build meaningful communities around their shared passion for cinema.

### Target Audience
- **Primary Audience**: Movie enthusiasts aged 12+ who actively seek new films and enjoy sharing their viewing experiences
- **Secondary Audience**: Casual moviegoers looking for personalized recommendations and social validation for their movie choices
- **Tertiary Audience**: Film critics, industry professionals, and content creators seeking a platform to engage with movie communities

### Details of Core Features

#### Movie Discovery & Intelligence
- **Advanced Search & Filtering**: Multi-criteria filtering by genre, year, director, actor, rating, language, and country
- **Real-time Trending**: Regional popularity tracking and editor's curated collections
- **Release Calendar**: Comprehensive upcoming movie releases with notification system and cinema showtimes integration

#### AI-Powered Recommendation Engine (Primary AI Feature)
- **Intelligent Recommendations**: User preference analysis based on website usage patterns and movie interactions
- **"Movies like this" Suggestions**: AI-driven recommendations based on genre, cast, and director similarities
- **Contextual Recommendations**: Mood-based and contextual suggestions considering weather, time of day, and season
- **Personalized Discovery**: Algorithms that adapt and evolve based on individual user interactions and ratings

#### Enhanced Review & Rating System
- **Multi-Dimensional Ratings**: Comprehensive ratings for plot, acting, cinematography, and soundtrack
- **Diverse Review Formats**: Quick ratings, detailed written reviews, video reviews, and photo reviews
- **AI-Powered Review Analysis**: Sentiment analysis and automated review categorization
- **Community Review Features**: Voting system, professional vs. user review distinction, and trending selections

#### Social Networking & Community
- **Smart Social Matching**: AI-powered movie taste compatibility algorithm for friend suggestions
- **Community Groups**: Genre-specific communities, franchise-focused groups, and location-based cinema groups
- **Interactive Features**: Movie meetup organization, group movie night planning, and virtual watch parties
- **Group Chat Features**: Real-time group discussions within communities and friend circles
- **Movie-Based Chat Rooms**: Dedicated chat spaces for specific movies, genres, and trending topics
- **Live Chat**: Real-time functionality during movie premieres and events

#### Gamification & Engagement
- **Achievement System**: Milestone badges for reviews, genre expertise, and community engagement
- **Points & Rewards Program**: Leaderboards, competitions, and unlockable premium features
- **Interactive Challenges**: Movie trivia contests, "guess the movie" games, and viewing challenges

#### Advanced Personalization Features
- **Watchlist Management**: Smart organization with priority levels, status tracking, and completion time estimates
- **Personal Movie Journal**: Detailed viewing history with notes, diary entries, and progress tracking
- **Custom Lists**: User-generated top 10 lists, themed collections, and collaborative group lists

### Technology Stack

#### Frontend
- **Framework**: React
- **Styling**: Tailwind CSS
- **State Management**: Redux Toolkit
- **Features**: Progressive Web App (PWA) capabilities, responsive design
- **Build Tools**: Vite for fast development and optimized builds

#### Backend
- **Framework**: Laravel (PHP)
- **Architecture**: RESTful API with JWT authentication
- **Database**: MySQL with optimized indexing

#### Activity-Based Intelligence
- **Smart Activity Tracking**: User behavior analysis including viewing patterns, rating frequency, and interaction preferences
- **Contextual Suggestions**: Recommendations based on user activities like time spent on specific genres, rewatching patterns, and social interactions
- **Community Activity Integration**: Suggestions influenced by friend activities, group discussions, and trending content within user's network

#### External Integrations
- **Movie Data**: TMDB API, IMDB API
- **Social Authentication**: OAuth integration (Google, Facebook, Apple)

#### Development Tools
- **Version Control**: Git with GitHub
- **Code Quality**: ESLint, Prettier, PHP CodeSniffer

### Database Architecture

#### Core Entity Relationship Design
The platform employs a sophisticated relational database architecture designed for scalability, performance, and data integrity:

#### Primary Tables
- **Users Table**: 
  - Primary Key: user_id (UUID)
  - Fields: username, email, password_hash, profile_image, date_created, last_active, subscription_tier
  - Indexes: email (unique), username (unique), subscription_tier
  
- **Movies Table**:
  - Primary Key: movie_id (UUID) 
  - Fields: tmdb_id, imdb_id, title, release_date, genre_ids, director, cast, synopsis, poster_url, runtime
  - Indexes: tmdb_id (unique), release_date, genre_ids (composite)

- **Reviews Table**:
  - Primary Key: review_id (UUID)
  - Foreign Keys: user_id, movie_id
  - Fields: overall_rating, plot_rating, acting_rating, cinematography_rating, soundtrack_rating, review_text, review_type, media_urls, created_at, updated_at
  - Indexes: user_id, movie_id, overall_rating, created_at

#### Relationship Tables
- **User_Movies (Watchlist Management)**:
  - Composite Primary Key: (user_id, movie_id)
  - Fields: status (watched/watching/plan_to_watch), priority_level, date_added, date_watched, personal_notes
  
- **User_Friendships**:
  - Primary Key: friendship_id
  - Fields: requester_id, addressee_id, status, compatibility_score, created_at
  - Unique constraint: (requester_id, addressee_id)

- **Groups & Communities**:
  - Groups Table: group_id, name, description, privacy_level, created_by, member_count
  - Group_Members Table: group_id, user_id, role, joined_date
  - Group_Posts Table: post_id, group_id, user_id, content, post_type, created_at

#### Activity & Analytics Tables
- **User_Activities**:
  - activity_id, user_id, activity_type, target_id, metadata (JSON), timestamp
  - Optimized for real-time activity feeds and behavioral analysis

- **User_Achievements**:
  - achievement_id, user_id, achievement_type, earned_date, progress_data

### UI Design
**Figma Design Link**: [RedPill UI/UX Design](https://coal-prior-36046077.figma.site/)



### Project Architecture Design Principles

#### System Architecture Principles
- **Modular Design**: Component-based architecture with clear separation of concerns
- **Scalability First**: Horizontal scaling capabilities with load balancing support
- **Database Optimization**: Efficient indexing, query optimization, and data normalization
- **API-Driven Architecture**: RESTful services with consistent response formats
- **Security by Design**: Input validation, authentication layers, and data encryption

#### UI/UX Design Principles
- **User-Centric Design**: Intuitive workflows based on user journey mapping
- **Responsive Design**: Mobile-first approach with adaptive layouts
- **Accessibility Standards**: User-friendly design with proper color contrast and readable fonts
- **Performance Optimization**: Lazy loading, image optimization, and minimal bundle sizes
- **Consistent Design System**: Unified color schemes, typography, and component library

### Development Phases
1. **Phase 1**: Core infrastructure, user authentication, basic movie discovery
2. **Phase 2**: Activity-based recommendation system, review system, social features
3. **Phase 3**: Community features, gamification, advanced personalization
4. **Phase 4**: Analytics dashboard, admin tools, performance optimization

### Team Roles & Responsibilities
- **Frontend Developers**: React application, user interface, responsive design
- **Backend Developers**: Laravel API, database design, authentication systems
- **UI/UX Designers**: User experience design, visual design, prototyping

### Contributors

| Name | Student ID |
|------|------------|
| Sakibul Hassan Shovon | 2022204060 |
| Md Iftekhar Zawad | 2022204067 |
| Ariful Islam | 2022204071 |
| Mahfuza Sultana Borsha | 2022204084 |



### License
This project is proprietary and confidential. All rights reserved.

---

**RedPill** - Connecting movie lovers through intelligent discovery and meaningful community engagement.
