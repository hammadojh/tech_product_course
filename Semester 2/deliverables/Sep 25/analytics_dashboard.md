# Analytics Dashboard

## What You Need to Deliver

Two analytics systems working together: (1) a custom dashboard tracking your database metrics, and (2) external user behavior tracking via Firebase Analytics or Amplitude. Combine internal data with user behavior insights.

## Key Questions

- How do users actually interact with your app?
- Which features are used most/least?
- Where do users drop off in critical flows?
- What data will help you improve your product?

## What You Need to Submit

### Implementation
- [ ] **Custom dashboard** built in your app showing database metrics
- [ ] **External analytics integration** (Firebase Analytics, Amplitude, etc.)
- [ ] **GitHub repository** with clear commit history for both systems

### Documentation
- [ ] **README.md** explaining both dashboard and external tracking setup
- [ ] **Dashboard features** documentation (what metrics you display)
- [ ] **Event tracking list** (what user behaviors you track)

### Demo
- [ ] **5-minute video** showing both your custom dashboard AND external analytics

## How to Get Started

### 1. Build Your Custom Dashboard
Create a dashboard page in your app that shows:
- **Database Metrics:** User count, posts created, active sessions
- **Business Data:** Signups per day, feature usage counts
- **App Performance:** Response times, error counts from your logs

### 2. Choose External Analytics Tool
**Recommended options:**
- **Firebase Analytics:** Free, easy setup
- **Amplitude:** Powerful user behavior tracking
- **Mixpanel:** Strong event tracking features

### 3. Plan Your Event Tracking
Identify key user actions for external tool:
- **Authentication:** Login, signup, logout
- **Core Features:** Button clicks, form submissions
- **User Journey:** Page navigation, feature discovery

### 4. Implement Both Systems
**Custom Dashboard:** Query your database for real metrics
**External Analytics:** Track user behavior events
```javascript
// External tracking example
analytics.track('Feature Used', {
  feature: 'create_post',
  user_type: 'premium'
});
```

## Implementation Examples

### Custom Dashboard (Database Metrics)
```javascript
// Dashboard component querying your database
const Dashboard = () => {
  const [metrics, setMetrics] = useState({});
  
  useEffect(() => {
    // Query your database for metrics
    fetchMetrics().then(data => {
      setMetrics({
        totalUsers: data.userCount,
        dailySignups: data.signupsToday,
        activeFeatures: data.featureUsage
      });
    });
  }, []);

  return (
    <div className="dashboard">
      <MetricCard title="Total Users" value={metrics.totalUsers} />
      <MetricCard title="Daily Signups" value={metrics.dailySignups} />
      <Chart data={metrics.activeFeatures} />
    </div>
  );
};
```

### External Analytics (Firebase Example)
```javascript
// Install: npm install firebase
import { getAnalytics, logEvent } from 'firebase/analytics';

const analytics = getAnalytics();

// Track user behavior
logEvent(analytics, 'feature_used', {
  feature_name: 'create_post',
  user_type: 'premium'
});
```

## What to Track in Each System

### Custom Dashboard (Internal Data)
- Total users, posts, transactions
- Daily/weekly signups and activity
- Database performance metrics
- Revenue or conversion data

### External Analytics (User Behavior)
- Page views and navigation
- Button clicks and interactions
- User journey and drop-off points
- Session duration and frequency



## Success Criteria

- Do you have a custom dashboard showing real database metrics?
- Is external analytics properly tracking user behavior?
- Can you compare internal data with user behavior patterns?
- Does your system help you make product decisions?

## Resources

### Analytics Tools
- **Firebase Analytics:** Free, easy setup, Google integration
- **Amplitude:** Advanced user behavior analytics
- **Mixpanel:** Event tracking and user segmentation  
- **Google Analytics 4:** Web analytics and conversion tracking

### Custom Dashboard Tools
- **Charts:** Chart.js, Recharts for React, D3.js
- **UI Libraries:** Material-UI, Ant Design for dashboard components
- **Database Queries:** SQL queries, ORM methods for metrics

### External Analytics Setup
- **Firebase:** [Web Analytics Setup Guide](https://firebase.google.com/docs/analytics/get-started?platform=web)
- **Amplitude:** [JavaScript SDK Documentation](https://www.docs.developers.amplitude.com/data/sdks/javascript/)

## Grading Rubric

| Criteria | Excellent (4) | Good (3) | Satisfactory (2) | Needs Work (1) |
|----------|---------------|----------|------------------|----------------|
| **Custom Dashboard** | Complete dashboard with database metrics and charts | Good dashboard with key metrics | Basic dashboard with some data | Missing or broken dashboard |
| **External Analytics** | Proper integration tracking meaningful user events | Good integration with key events | Basic tracking working | Poor or broken integration |
| **Documentation** | Clear setup guide for both systems | Good documentation with minor gaps | Basic documentation | Poor or missing documentation |

**Remember:** Combine your database insights with user behavior data to make better product decisions.
