# Seed Metrics Dashboard

As part our application process, we'd like to see what you can produce by giving you an assignment to develop a real-time dashboard that should consume fake server metrics using websocket connection.

## Websocket Documentation

Please refer to websocket documentation [here](./websocket.md)

## Requirements

- You should use the following technologies:
    - Typescript
    - React (or Next.js)
    - Websocket (not socket.io)
- Git is a must, please make sure you commit your work throughout the process.
- You're free to use whatever UI library you prefer.

## User Stories

- [ ] 1. Consume Real-Time Server Metrics
    - As a user, I want to view real-time memory and CPU metrics from all five servers so that I can monitor their performance continuously.
- [ ] 2. Responsive Dashboard Design
    - As a user, I need the dashboard to be responsive to different screen sizes so that I can view the metrics clearly on any device.
- [ ] 3. Metric Visualization
    - As a user, I want to see each server's metrics displayed in time-series, and gauge charts so that I can easily understand the data at a glance.
- [ ] 4. Individual Server View
    - As a user, I want the option to view each server's metrics in a separate detailed view so that I can focus on a single server's performance when needed.
- [ ] 5. Aggregate Server Metrics View
    - As a user, I want to be able to view all servers' metrics in a single comprehensive view to get an overview of the overall system health.
- [ ] 6. Server Selection
    - As a user, I want to select a specific server from a list to view its metrics so that I can quickly navigate to the data I am interested in.
- [ ] 7. Metric Toggling
    - As a user, I want to toggle CPU or memory metrics on and off so that I can control which data is displayed according to my current needs.
- [ ] 8. Preference Persistence
    - As a user, I expect my selections and toggles for displayed metrics to be remembered so that I do not have to set them up each time I access the dashboard.
- [ ] 9. Initial Load Historical Data
    - As a user, I expect to see the last 2 seconds of historical metrics data for each server loaded immediately after the initial dashboard load so that I can quickly assess recent server performance.

## Bonuses

- [ ] Highly reusable components
- [ ] Polish and UX
- [ ] Tests
- [ ] Deployment

## Delivery

To complete your work, please add `omarahm3` as a contributer to your github repo when you're done, send an email to let us know.
