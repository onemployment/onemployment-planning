# onemployment Planning Repository

This repository serves as the central hub for project management and technical design coordination across the onemployment platform.

## Purpose

- **Feature Requests:** Capture and analyze new feature ideas
- **Technical Design:** Collaborative design process for approved features
- **Project Coordination:** Cross-repository task planning and tracking
- **Process Documentation:** Development workflow and estimation tracking

## Repository Structure

```
onemployment-planning/
  .github/ISSUE_TEMPLATE/     # Issue templates for workflow
  docs/                       # Process documentation (GitHub Pages)
  README.md                   # This file
```

## Related Repositories

- **[frontend](https://github.com/onemployment/frontend)** - React/TypeScript user interface
- **[backend](https://github.com/onemployment/backend)** - Node.js/TypeScript API
- **[infrastructure](https://github.com/onemployment/infrastructure)** - AWS infrastructure as code

## Quick Start

### Using Issue Templates
1. **Create Feature Request:** [Use Feature Request template](https://github.com/onemployment/onemployment-planning/issues/new?template=feature-request.yml)
2. **Technical Design:** [Use Technical Design template](https://github.com/onemployment/onemployment-planning/issues/new?template=technical-design.yml)
3. **Implementation Tasks:** [Use Implementation Task template](https://github.com/onemployment/onemployment-planning/issues/new?template=implementation-task.yml)
4. **Weekly Reviews:** [Use Weekly Review template](https://github.com/onemployment/onemployment-planning/issues/new?template=weekly-review.yml)

### Project Board Workflow
1. **Set up project board:** Go to [Organization Projects](https://github.com/orgs/onemployment/projects) and create "Development Process" board
2. **Add issues to board:** Use Projects sidebar when creating issues
3. **Track progress:** Move issues through Backlog → In Progress → Review → Done
4. **Cross-repo coordination:** Link related issues across repositories

## Documentation

**[Process Documentation](docs/index.md)** 
- **Note:** Enable GitHub Pages in repository settings to access at `https://onemployment.github.io/onemployment-planning`
- [Setup Guide](docs/setup-guide.md) - First-time repository setup instructions
- [Estimation Tracking Process](docs/process/estimation-tracking.md) - Story point tracking details
- Workflow Overview and Issue Template Usage Guide

## Current Focus

**Phase 1:** Establishing estimation accuracy baseline

- Simple story point tracking (1-3 scale)
- Weekly estimation reviews
- Process refinement based on actual usage

## Contributing

1. Use the provided issue templates for consistency
2. Follow the cross-repository linking conventions
3. Track actual effort vs estimates for all tasks
4. Participate in weekly estimation reviews

---

**Setup Instructions:** [docs/setup-guide.md](docs/setup-guide.md)  
**Live Documentation:** https://onemployment.github.io/onemployment-planning (after enabling GitHub Pages)