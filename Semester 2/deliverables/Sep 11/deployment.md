# Deployment & DevOps

## What You Need to Deliver

A live production app that automatically deploys when you push code. Professional teams ship code multiple times per day with confidence.

## Key Questions

- How long does it take to deploy a change?
- What happens if a deployment fails?
- How do you know if your app is healthy?

## What You Need to Submit

### Technical Setup
- [ ] Live production app with custom domain
- [ ] Automated deployment (push code → live in < 5 minutes)
- [ ] Basic monitoring (uptime + error tracking)

### Documentation
- [ ] Simple deployment guide
- [ ] Architecture diagram

### Demo
- [ ] Show deployment process live
- [ ] Explain your setup in 5 minutes

## How to Get Started

### 1. Choose Your Platform
**Easiest Options:**
- **React/Next.js:** Vercel
- **Static Sites:** Netlify
- **Full Stack:** Heroku or Railway
- **Advanced:** AWS/Google Cloud

### 2. Set Up Automated Deployment
**Example GitHub Actions:**
```yaml
name: Deploy
on:
  push:
    branches: [main]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Deploy
        run: npm run deploy
```

### 3. Add Monitoring
- **Uptime:** UptimeRobot (free)
- **Errors:** Sentry (free tier)
- **Analytics:** Google Analytics

## Examples by Tech Stack

### React + Node.js
**Platform:** Vercel (frontend) + Railway (backend)
**Process:** Git push → automatic deployment

### Next.js Full Stack
**Platform:** Vercel with Vercel Postgres
**Process:** Git push → build → deploy

### Python + Django
**Platform:** Heroku
**Process:** Git push → deploy

## Success Criteria

- Can you deploy changes in under 5 minutes?
- Do you have zero-downtime deployments?
- Is your app up 99.9% of the time?
- Can you deploy with one command?

## Resources

### Hosting Platforms
- **Vercel:** Best for React/Next.js apps (free tier available)
- **Netlify:** Great for static sites and JAMstack (free tier available)
- **Heroku:** Simple platform-as-a-service (free tier available)
- **Railway:** Modern deployment platform (free tier available)
- **AWS:** Full cloud platform (free tier available)

### CI/CD Tools
- **GitHub Actions:** Built into GitHub, easy to start (free)
- **GitLab CI:** Integrated with GitLab (free)
- **CircleCI:** Powerful and flexible (free tier available)
- **Vercel:** Automatic deployments for frontend projects

### Monitoring Tools
- **UptimeRobot:** Free uptime monitoring
- **Sentry:** Error tracking and performance (free tier available)
- **Google Analytics:** User behavior tracking (free)
- **Vercel Analytics:** Built-in for Vercel apps
- **New Relic:** Application performance monitoring (free tier available)

### Documentation Tools
- **Notion:** Collaborative documentation
- **GitBook:** Technical documentation platform
- **Draw.io:** Free architecture diagrams
- **Lucidchart:** Professional diagramming tool

**Remember:** Start simple. A basic deployment that works is better than a complex system that doesn't.

## Grading Rubric

| Criteria | Excellent (4) | Good (3) | Satisfactory (2) | Needs Work (1) |
|----------|---------------|----------|------------------|----------------|
| **Production Setup** | Live app with custom domain, SSL, and professional setup | Live app with custom domain and basic security | Live app accessible via URL | App not live or major issues |
| **Automated Deployment** | Push-to-deploy works flawlessly in < 3 minutes | Push-to-deploy works in < 5 minutes | Manual deployment process works | Deployment process broken or unreliable |
| **Monitoring & Health** | Comprehensive monitoring with alerts and dashboards | Basic monitoring with uptime tracking | Simple health checks in place | No monitoring or health checks |
| **Documentation** | Clear, complete deployment guide with troubleshooting | Good deployment guide with basic troubleshooting | Basic deployment instructions | Poor or missing documentation |
| **Demo & Presentation** | Confident live demo with clear explanation of architecture | Good demo with explanation of key components | Basic demo showing deployment process | Poor demo or unable to explain setup |
