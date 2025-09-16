# onemployment Planning Repository - AI Development Guide

## Repository Overview

The **onemployment-planning** repository serves as the central hub for project management and development process coordination across the entire onemployment platform. This repository implements a comprehensive GitHub-based workflow that bridges feature ideation to implementation across multiple repositories.

### Platform Integration

This planning repository coordinates development across three core repositories:
- **[onemployment/frontend](https://github.com/onemployment/frontend)** - React/TypeScript user interface
- **[onemployment/backend](https://github.com/onemployment/backend)** - Node.js/TypeScript API
- **[onemployment/infrastructure](https://github.com/onemployment/infrastructure)** - AWS infrastructure as code

### Key Technologies
- **GitHub Issues** with YAML templates for structured workflow
- **GitHub Projects v2** for visual project management
- **GitHub Pages** for process documentation
- **Cross-repository linking** for coordinated development
- **Story point estimation** with accuracy tracking

## GitHub-Based Development Process

### Complete Workflow: Feature → Design → Implementation → Review

```
Feature Request → Technical Design → Implementation Tasks → Weekly Review
     (planning)       (planning)      (all repositories)     (planning)
         ↓                ↓                   ↓                  ↓
   Business requirements → Architecture → Story-pointed tasks → Estimation accuracy
```

### 1. Feature Request Phase
**Template**: [Feature Request](https://github.com/onemployment/onemployment-planning/issues/new?template=feature-request.yml)

**Purpose**: Capture business requirements and user scenarios
**Key Sections**:
- Problem definition and target users
- Solution approach and alternatives considered
- User scenarios (happy path, alternatives, error cases)
- Functional requirements (MVP vs future)
- Non-functional requirements (performance, security, scalability)

**Labels Applied**: `feature-request`, `needs-triage`
**Next Step**: Create Technical Design issue

### 2. Technical Design Phase
**Template**: [Technical Design](https://github.com/onemployment/onemployment-planning/issues/new?template=technical-design.yml)

**Purpose**: 9-step collaborative technical architecture process
**Process Steps**:
1. **Requirements Analysis & Scope Definition** - Clarify feature request, define boundaries
2. **Data Model Design** - Database schema, relationships, storage strategy
3. **API Design & Integration Points** - Endpoints, schemas, authentication
4. **Frontend Architecture & Components** - Component hierarchy, state management
5. **Technology Stack & Dependencies** - Technology choices, version compatibility
6. **Testing Strategy** - Unit, integration, e2e test approaches
7. **Implementation Plan & Task Breakdown** - Story-pointed tasks, dependencies
8. **Deployment & Infrastructure Plan** - Deployment strategy, infrastructure changes
9. **Design Review & Approval** - Final consistency and completeness review

**Labels Applied**: `technical-design`, `step-1-analysis` (progresses through steps)
**Next Step**: Create Implementation Tasks in appropriate repositories

### 3. Implementation Task Phase
**Template**: [Implementation Task](https://github.com/onemployment/onemployment-planning/issues/new?template=implementation-task.yml)

**Purpose**: Development tasks with complete context across repositories
**Key Components**:
- **Story Point Estimation**: 1 (half day), 2 (full day), 3 (two days)
- **Component Type**: Frontend, Backend, Infrastructure, Documentation, Testing
- **Technical Specifications**: APIs, interfaces, configurations
- **Implementation Approach**: Step-by-step strategy
- **Dependencies & Code References**: Existing patterns and dependencies
- **Testing Requirements**: Unit, integration, manual testing
- **Acceptance Criteria**: Definition of done

**Repository Placement**:
- **Frontend tasks**: Create in [onemployment/frontend](https://github.com/onemployment/frontend/issues/new)
- **Backend tasks**: Create in [onemployment/backend](https://github.com/onemployment/backend/issues/new)
- **Infrastructure tasks**: Create in [onemployment/infrastructure](https://github.com/onemployment/infrastructure/issues/new)
- **Documentation tasks**: Create in this planning repository

### 4. Weekly Review Phase
**Template**: [Weekly Review](https://github.com/onemployment/onemployment-planning/issues/new?template=weekly-review.yml)

**Purpose**: Estimation accuracy tracking and process improvement
**Review Components**:
- **Completed Tasks**: List with estimated vs actual story points
- **Accuracy Calculation**: (Estimated ÷ Actual) × 100%
- **Patterns & Insights**: Underestimated, overestimated, accurate estimates
- **Next Week Focus**: Estimation improvements and process adjustments

## Story Point System

### Point Scale Definition
- **1 point** = Half day (~4 hours)
- **2 points** = Full day (~8 hours)
- **3 points** = Two days (~16 hours)

### Accuracy Tracking
**Completion Format**: Add comment when finishing tasks:
```
Completed - Actual effort: X story points
```

**Accuracy Calculation**:
```
Task Accuracy = (Estimated Points ÷ Actual Points) × 100%

Examples:
- Estimated 2, Actual 2 = 100% (perfect)
- Estimated 2, Actual 3 = 67% (underestimated)
- Estimated 3, Actual 2 = 150% (overestimated)
```

**Target Accuracy Range**: 80-120% (within 20% of estimate)

### Success Targets
- **Week 1**: Establish baseline accuracy
- **Week 2**: >70% average accuracy
- **Week 3**: >80% average accuracy
- **Week 4**: >85% average accuracy

## Cross-Repository Coordination

### Issue Linking Format
```markdown
**Epic:** onemployment-planning#1 (Feature Request)
**Design:** onemployment-planning#15 (Technical Design)
**Related Tasks:**
- Frontend: onemployment/frontend#23
- Backend: onemployment/backend#45
- Infrastructure: onemployment/infrastructure#12
```

### Repository Mapping
- **Planning & Coordination**: All feature requests and technical designs in this repository
- **Frontend Development**: React components, state management, UI/UX implementation
- **Backend Development**: APIs, authentication, business logic, database integration
- **Infrastructure Development**: AWS resources, deployment, monitoring, security
- **Documentation**: Process documentation in this repository, technical docs in implementation repositories

## Project Board Management

### Project Board URL
**Organization Project**: https://github.com/orgs/onemployment/projects/1

### Column Structure
- **Backlog** - New feature requests and designs awaiting prioritization
- **In Progress** - Active development work across all repositories
- **Review** - Technical designs awaiting approval and code reviews
- **Done** - Completed work ready for deployment

### Adding Issues to Project Board
**Method 1 - During Issue Creation**:
1. Create issue using appropriate template
2. On right sidebar, click "Projects"
3. Select "Development Process" project
4. Choose appropriate column based on issue type

**Method 2 - From Project Board**:
1. Navigate to project board
2. Click "Add items" or "+"
3. Search: `repo:onemployment/onemployment-planning` (or other repos)
4. Select issues to add

### Automation Options
- **Built-in Workflows**: Set up auto-add filters in project settings
- **GitHub Actions**: Use `actions/add-to-project` for advanced automation
- **Manual Management**: Add issues via Projects sidebar (current approach)

## AI Agent Instructions

### Essential Workflow for Claude Code Agents

#### 1. Before Starting Cross-Repository Work
- **Read this CLAUDE.md file** for planning context
- **Check related repository CLAUDE.md files** for implementation context:
  - `backend/claude.md` - API development patterns and deployment
  - `frontend/claude.md` - Component patterns and UI guidelines
  - `infrastructure/claude.md` - AWS deployment and infrastructure

#### 2. Feature Development Workflow
1. **Understand the Epic**: Read the Feature Request issue thoroughly
2. **Review Technical Design**: Ensure you understand the approved architecture
3. **Create Implementation Tasks**: Use appropriate repository and template
4. **Link Issues Properly**: Follow cross-repository linking format
5. **Add to Project Board**: Ensure visibility in Development Process project
6. **Estimate Story Points**: Use 1-3 scale based on complexity
7. **Track Actual Effort**: Add completion comments with actual story points

#### 3. Issue Template Usage
**Always use templates** when creating planning issues:
- Feature Request: Business requirements gathering
- Technical Design: Architecture and implementation planning
- Implementation Task: Development work with complete context
- Weekly Review: Estimation accuracy and process improvement

**Template URLs for Quick Access**:
- [Feature Request](https://github.com/onemployment/onemployment-planning/issues/new?template=feature-request.yml)
- [Technical Design](https://github.com/onemployment/onemployment-planning/issues/new?template=technical-design.yml)
- [Implementation Task](https://github.com/onemployment/onemployment-planning/issues/new?template=implementation-task.yml)
- [Weekly Review](https://github.com/onemployment/onemployment-planning/issues/new?template=weekly-review.yml)

#### 4. Repository Navigation
**For Cross-Repository Tasks**:
- Start with planning repository context (this file)
- Navigate to implementation repository
- Read repository-specific CLAUDE.md file
- Follow repository-specific patterns and validation requirements
- Link back to planning issues appropriately

#### 5. Project Management Integration
- **Always add issues to project board** using Projects sidebar
- **Move issues through columns** as work progresses
- **Update issue status** with comments and label changes
- **Reference related issues** in all cross-repository work

#### 6. Estimation and Tracking
- **Estimate story points** for all implementation tasks
- **Track actual effort** with completion comments
- **Participate in weekly reviews** by providing accurate data
- **Learn from estimation patterns** to improve accuracy over time

## Quick Reference

### Essential Links
- **Issue Templates**: https://github.com/onemployment/onemployment-planning/issues/new/choose
- **Project Board**: https://github.com/orgs/onemployment/projects/1
- **Current Issues**: https://github.com/onemployment/onemployment-planning/issues
- **Process Documentation**: https://onemployment.github.io/onemployment-planning (after GitHub Pages setup)
- **Setup Guide**: [docs/setup-guide.md](docs/setup-guide.md)

### Documentation Structure
- **Main Process**: [docs/index.md](docs/index.md) - Complete workflow overview
- **Estimation Tracking**: [docs/process/estimation-tracking.md](docs/process/estimation-tracking.md) - Detailed story point process
- **Setup Guide**: [docs/setup-guide.md](docs/setup-guide.md) - First-time repository setup

### Related Repository Context
- **Root Platform Guide**: `/mnt/c/Workspaces/onemployment/CLAUDE.md` - Multi-repository architecture
- **Backend Development**: `backend/claude.md` - API patterns and deployment
- **Frontend Development**: `frontend/claude.md` - Component patterns and UI guidelines
- **Infrastructure Operations**: `infrastructure/claude.md` - AWS deployment and infrastructure

## Commit Guidelines

Follow the same commit message format as other onemployment repositories:

```
<imperative title>

- <concise bullet point describing important change and brief why>
- <concise bullet point describing important change and brief why>
- <concise bullet point describing important change and brief why>
```

### Example
```
Add automated estimation tracking to weekly reviews

- Include accuracy calculation helper in review template for consistent measurement
- Add pattern identification prompts to improve estimation learning
- Link to story point guidelines for reference during reviews
```

## Process Evolution

This planning system is designed for continuous improvement:

### Current Phase (Established)
- ✅ Complete issue template workflow
- ✅ Cross-repository coordination
- ✅ Story point estimation system
- ✅ Project board integration
- ✅ Weekly review process

### Future Enhancements (Planned)
- 🔄 Automated issue-to-project board assignment
- 🔄 Velocity tracking across teams
- 🔄 Quality metrics integration
- 🔄 Milestone planning capabilities
- 🔄 Advanced estimation analytics

---

**Instructions for AI Agents**: This file provides complete context for the onemployment planning workflow. Always reference this file when working on cross-repository features, project coordination, or process improvements. Combine this planning context with repository-specific CLAUDE.md files for comprehensive development guidance.