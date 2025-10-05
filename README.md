# Scrollify

Scrollify is an AI-powered short video generation platform that allows users to create realistic short videos from text prompts. Leveraging advanced AI technologies, Scrollify generates videos by combining images, audio, and captions to deliver engaging content at warp speed.

## Highlights

- AI-driven video generation from text prompts
- Multi-step generation process including image and audio creation
- User authentication and credit-based usage system
- Real-time video processing status updates
- Responsive and modern UI built with Next.js and Tailwind CSS

## Features

### User Features

- **User Authentication**
  - Secure sign-in and sign-up with Clerk
  - User credit management system
- **Video Creation**
  - Generate videos from custom text prompts
  - Multi-step progress loader to track generation stages
- **Video Management**
  - Dashboard to view created videos
  - Video status tracking and playback
- **Credits System**
  - Credit-based access to video creation
  - Pricing page to purchase additional credits

### Technical Features

- **Backend**
  - API routes for video creation, status, and Stripe payment integration
  - Queue management for video processing using BullMQ and Redis
  - PostgreSQL database managed with Prisma ORM
- **Frontend**
  - Built with Next.js 13 (App Router)
  - Tailwind CSS for styling
  - Clerk for authentication
  - Remotion for video rendering
- **AI Integrations**
  - OpenAI for text and audio generation
  - ElevenLabs for advanced audio synthesis
  - Replicate for image generation
- **Payments**
  - Stripe integration for credit purchases

## Tech Stack

- **Frontend:** Next.js, React, Tailwind CSS, Clerk
- **Backend:** Node.js, Next.js API Routes, Prisma, PostgreSQL
- **Queue:** BullMQ, Redis
- **AI Services:** OpenAI, ElevenLabs, Replicate
- **Video Rendering:** Remotion
- **Payments:** Stripe

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/scrollify.git
cd scrollify
```

2. Install dependencies:

```bash
npm install
```

3. Set up environment variables:

Create a `.env` file in the root directory with the following variables:

```env
DATABASE_URL=your_postgresql_database_url
REDIS_URL=your_redis_url
OPENAI_API_KEY=your_openai_api_key
ELEVENLABS_API_KEY=your_elevenlabs_api_key
REPLICATE_API_TOKEN=your_replicate_api_token
STRIPE_SECRET_KEY=your_stripe_secret_key
STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret
CLERK_FRONTEND_API=your_clerk_frontend_api
CLERK_API_KEY=your_clerk_api_key
```

4. Run database migrations:

```bash
npx prisma migrate deploy
```

5. Start the development server:

```bash
npm run dev
```

6. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Usage

- Sign up or sign in to your account.
- Use the prompt input to create a new video.
- Monitor the video generation progress.
- Access your videos in the dashboard.
- Purchase credits via the pricing page to continue creating videos.

## Project Structure

```
app/                # Next.js app directory with pages and API routes
components/         # Reusable UI components
lib/                # Utility functions and helpers
prisma/             # Prisma schema and migrations
worker/             # Background worker for video processing
public/             # Static assets
```
