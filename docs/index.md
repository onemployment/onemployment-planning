# onemployment Development Process

## Overview
This repository manages the development process for the onemployment platform across three main repositories:
- [onemployment/frontend](https://github.com/onemployment/frontend) - React/TypeScript user interface
- [onemployment/backend](https://github.com/onemployment/backend) - Node.js/TypeScript API
- [onemployment/infrastructure](https://github.com/onemployment/infrastructure) - AWS infrastructure as code

## Workflow

### 1. Feature Request
**How to Create:**
1. Go to [New Issue](https://github.com/onemployment/onemployment-planning/issues/new/choose)
2. Select "Feature Request" template
3. Fill out all required sections:
   - Problem definition and user scenarios
   - Functional and non-functional requirements
   - Business value and MVP priority
4. Add to project board (see Project Board Setup below)

### 2. Technical Design  
**How to Create:**
1. Go to [New Issue](https://github.com/onemployment/onemployment-planning/issues/new/choose)
2. Select "Technical Design" template
3. Complete the 9-step collaborative process:
   1. Requirements Analysis & Scope Definition
   2. Data Model Design
   3. API Design & Integration Points
   4. Frontend Architecture & Components
   5. Technology Stack & Dependencies
   6. Testing Strategy
   7. Implementation Plan & Task Breakdown
   8. Deployment & Infrastructure Plan
   9. Design Review & Approval
4. Link to the original Feature Request issue

### 3. Implementation Tasks
**How to Create:**
1. Go to the appropriate repository:
   - Frontend tasks: [onemployment/frontend](https://github.com/onemployment/frontend/issues/new)
   - Backend tasks: [onemployment/backend](https://github.com/onemployment/backend/issues/new)
   - Infrastructure tasks: [onemployment/infrastructure](https://github.com/onemployment/infrastructure/issues/new)
   - Documentation tasks: Use "Implementation Task" template in this repository
2. Use the "Implementation Task" template if available, or create detailed issues with:
   - Story point estimate (1-3 scale)
   - Complete context and acceptance criteria
   - Links to related Feature Request and Technical Design issues

### 4. Development & Tracking
- Work on tasks using provided context
- Update task status on the project board
- Track completion with actual effort comments
- Conduct weekly estimation reviews using the Weekly Review template

## Story Point Scale
- **1 point** = Half day (~4 hours)
- **2 points** = Full day (~8 hours)  
- **3 points** = Two days (~16 hours)

## Current Process Status
- **Phase:** Initial implementation and testing
- **Focus:** Estimation accuracy improvement
- **Review Cadence:** Weekly for first month, then monthly

## Project Board Setup

### Creating the Project Board
1. Go to [GitHub Organizations Projects](https://github.com/orgs/onemployment/projects)
2. Click "New project"
3. Choose "Board" layout
4. Name: "Development Process"
5. Description: "Cross-repository development workflow tracking"

### Project Board Columns
Set up these columns for workflow tracking:
- **Backlog** - New feature requests and designs
- **In Progress** - Active development work
- **Review** - Technical designs awaiting approval
- **Done** - Completed work

### Adding Issues to Project Board
1. When creating any issue, click "Projects" on the right sidebar
2. Select the "Development Process" project
3. Choose appropriate column based on issue type and status

## Quick Links
- [Process Documentation](process/estimation-tracking.md)
- [Current Issues](https://github.com/onemployment/onemployment-planning/issues)
- [New Issue Templates](https://github.com/onemployment/onemployment-planning/issues/new/choose)
- [Organization Projects](https://github.com/orgs/onemployment/projects)
- [Weekly Review Template](https://github.com/onemployment/onemployment-planning/issues/new?template=weekly-review.yml)

## Getting Started

### Initial Setup Required
**First time setup:** Follow the [Setup Guide](setup-guide.md) to:
- Enable GitHub Pages for this documentation
- Create the organization project board
- Verify all issue templates are working

### Development Workflow
1. **Read the process:** Review [estimation tracking process](process/estimation-tracking.md)
2. **Create first feature request:** Use the [Feature Request template](https://github.com/onemployment/onemployment-planning/issues/new?template=feature-request.yml)
3. **Follow technical design:** Use the [Technical Design template](https://github.com/onemployment/onemployment-planning/issues/new?template=technical-design.yml)
4. **Break into implementation tasks:** Create tasks in appropriate repositories
5. **Track on project board:** Add all issues to the Development Process project
6. **Start weekly reviews:** Use the [Weekly Review template](https://github.com/onemployment/onemployment-planning/issues/new?template=weekly-review.yml)