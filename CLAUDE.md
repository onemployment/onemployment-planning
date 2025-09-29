# onemployment Platform - AI Development Hub

## 🚀 AI Agent Quick Start

**Start here for all onemployment platform contributions**

### Choose Your Work Type:

**🏗️ Feature Request Development**
- Work Location: This repository (`onemployment-planning`)
- Template: [Feature Request](https://github.com/onemployment/onemployment-planning/issues/new?template=feature-request.yml)
- Process: Business requirements → User scenarios → Functional/non-functional requirements

**📐 Technical Design Work** 
- Work Location: This repository (`onemployment-planning`)
- Template: [Technical Design](https://github.com/onemployment/onemployment-planning/issues/new?template=technical-design.yml)  
- Process: 9-step collaborative architecture design → Implementation planning

**💻 Implementation Tasks**
- Work Location: Navigate to specific repository (see Repository Navigator below)
- Template: [Implementation Task](https://github.com/onemployment/onemployment-planning/issues/new?template=implementation-task.yml) or repository-specific
- Process: Code implementation → Testing → Deployment

**🔍 Weekly Reviews**
- Work Location: This repository (`onemployment-planning`)
- Template: [Weekly Review](https://github.com/onemployment/onemployment-planning/issues/new?template=weekly-review.yml)
- Process: Estimation accuracy tracking → Process improvement

### 🤖 Specialized AI Agents

**Product Manager Agent** (`@product-manager`)
- **Purpose**: Requirements engineering and user-centered design
- **Best For**: Feature Request development, user scenario definition, requirements gathering
- **Capabilities**: Auto-creates structured Feature Requests in GitHub, runs systematic requirement-gathering processes
- **Usage**: Available in Claude Code sessions started from this planning repository
- **Workflow**: Conversation-gated 6-step process (Problem → Solution → Scenarios → Requirements → Non-functional → Implementation)

**When to Use Product Manager Agent**:
- Creating new Feature Request issues with comprehensive requirements
- Translating business objectives into technical specifications  
- Defining user scenarios and acceptance criteria
- Gathering and analyzing user needs systematically

## 📊 Platform Overview

### System Architecture
```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│    Frontend     │    │     Backend      │    │ Infrastructure  │
│                 │    │                  │    │                 │
│ React + TS      │◄──►│ Node.js + TS     │◄──►│ AWS ECS/Fargate │
│ Redux Toolkit   │    │ Express.js       │    │ RDS PostgreSQL  │
│ Vite Build      │    │ Prisma ORM       │    │ Route 53 + ALB  │
│ Framer Motion   │    │ bcrypt + Zod     │    │ ECR Registry    │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

### Production Environment
- **Live Frontend**: https://www.onemployment.org (S3 + CloudFront)
- **Live API**: https://api.onemployment.org (ECS Fargate + ALB)
- **Health Check**: https://api.onemployment.org/health
- **Project Board**: https://github.com/orgs/onemployment/projects/1

### Platform Status
- **Frontend**: Production deployment (React 19, TypeScript, Redux Toolkit)
- **Backend**: Production-ready (Node.js API with JWT authentication)
- **Infrastructure**: Production deployment (AWS ECS, RDS PostgreSQL)
- **Planning**: Established GitHub-based workflow with issue templates

## 🗂️ Repository Navigator

| Repository | Purpose | Status | When to Use | CLAUDE.md Link |
|------------|---------|---------|-------------|----------------|
| **[planning](https://github.com/onemployment/onemployment-planning)** | Feature requests, technical designs, process coordination | ✅ Active | Feature requests, tech designs, cross-repo coordination | *This file* |
| **[frontend](https://github.com/onemployment/frontend)** | React/TypeScript user interface | ✅ Production | UI components, client-side logic, user experience | [`frontend/CLAUDE.md`](https://github.com/onemployment/frontend/blob/main/CLAUDE.md) |
| **[backend](https://github.com/onemployment/backend)** | Node.js/TypeScript API | ✅ Production | API endpoints, authentication, business logic | [`backend/CLAUDE.md`](https://github.com/onemployment/backend/blob/main/CLAUDE.md) |
| **[infrastructure](https://github.com/onemployment/infrastructure)** | AWS infrastructure as code | ✅ Production | Deployment, monitoring, cloud resources | [`infrastructure/CLAUDE.md`](https://github.com/onemployment/infrastructure/blob/main/CLAUDE.md) |

### Navigation Guide for AI Agents

**Starting a New Feature:**
1. Start here (`onemployment-planning`) → Create Feature Request
2. Stay here → Create Technical Design  
3. Navigate to implementation repositories → Create Implementation Tasks

**Working on Implementation:**
1. Read this file for context and coordination
2. Navigate to target repository directory
3. Read repository-specific CLAUDE.md for implementation details
4. Return here for cross-repository coordination

## 📋 GitHub-Based Development Workflow

### Complete Process Flow
```
Feature Request → Technical Design → Implementation Tasks → Weekly Review
     (planning)       (planning)      (target repositories)     (planning)
         ↓                ↓                   ↓                     ↓
  Business requirements → Architecture → Story-pointed tasks → Estimation accuracy
```

### 1. Feature Request Phase
**Template**: [Feature Request](https://github.com/onemployment/onemployment-planning/issues/new?template=feature-request.yml)

**Key Sections**:
- **Problem Definition**: What problem are we solving? Who has it? Why does it matter?
- **Solution Approach**: Chosen approach, alternatives considered, reasoning
- **User Scenarios**: Happy path, alternative flows, error cases
- **Functional Requirements**: MVP requirements vs future features
- **Non-functional Requirements**: Performance, security, scalability needs

**Labels Applied**: `feature-request`, `needs-triage`
**Next Step**: Create Technical Design issue with reference to Feature Request

### 2. Technical Design Phase
**Template**: [Technical Design](https://github.com/onemployment/onemployment-planning/issues/new?template=technical-design.yml)

**9-Step Collaborative Process**:
1. **Requirements Analysis & Scope Definition** - Clarify ambiguities, define boundaries
2. **Data Model Design** - Database schema, relationships, storage strategy  
3. **API Design & Integration Points** - Endpoints, request/response schemas, authentication
4. **Frontend Architecture & Components** - Component hierarchy, state management, user flows
5. **Technology Stack & Dependencies** - Technology choices, new dependencies, compatibility
6. **Testing Strategy** - Unit, integration, e2e test approaches and coverage
7. **Implementation Plan & Task Breakdown** - Story-pointed tasks, dependencies, sequencing
8. **Deployment & Infrastructure Plan** - Deployment strategy, infrastructure changes, rollback
9. **Design Review & Approval** - Final consistency review and stakeholder approval

**Labels Applied**: `technical-design`, `step-1-analysis` (progresses through steps)
**Next Step**: Create Implementation Tasks in appropriate repositories

### 3. Implementation Task Phase
**Templates**: 
- [Implementation Task](https://github.com/onemployment/onemployment-planning/issues/new?template=implementation-task.yml) (planning repo)
- Repository-specific templates (when available)

**Repository Placement Strategy**:
- **Frontend Tasks**: Create in [frontend repository](https://github.com/onemployment/frontend/issues/new)
- **Backend Tasks**: Create in [backend repository](https://github.com/onemployment/backend/issues/new)  
- **Infrastructure Tasks**: Create in [infrastructure repository](https://github.com/onemployment/infrastructure/issues/new)
- **Documentation Tasks**: Create in this planning repository
- **Cross-repository Tasks**: Create in planning repository with clear scope

**Key Components**:
- **Story Point Estimation**: 1 (half day), 2 (full day), 3 (two days)
- **Technical Specifications**: APIs, interfaces, configurations, code contracts
- **Implementation Approach**: Step-by-step development strategy
- **Dependencies & References**: Existing code patterns, integration points
- **Testing Requirements**: Unit, integration, manual testing approaches
- **Acceptance Criteria**: Complete definition of done checklist

### 4. Weekly Review Phase  
**Template**: [Weekly Review](https://github.com/onemployment/onemployment-planning/issues/new?template=weekly-review.yml)

**Review Components**:
- **Completed Tasks Analysis**: List with estimated vs actual story points
- **Accuracy Calculation**: (Estimated ÷ Actual) × 100% for each task
- **Pattern Identification**: Tasks consistently under/over/accurately estimated
- **Process Improvements**: Specific adjustments for next week's estimation

## 📏 Story Point System & Estimation Tracking

### Point Scale Definition
- **1 point** = Half day (~4 hours of focused development)
- **2 points** = Full day (~8 hours of focused development)  
- **3 points** = Two days (~16 hours of focused development)

### Completion Tracking Format
When finishing any implementation task, add this comment:
```
Completed - Actual effort: X story points
Brief note on what made it take more/less time than estimated
```

### Accuracy Calculation & Targets
```
Task Accuracy = (Estimated Points ÷ Actual Points) × 100%

Interpretation:
- 100% = Perfect estimate
- <100% = Underestimated (took longer than expected)  
- >100% = Overestimated (finished faster than expected)

Target Range: 80-120% (within 20% of estimate)
```

**Improvement Targets**:
- **Week 1**: Establish baseline accuracy across all task types
- **Week 2**: Achieve >70% average accuracy  
- **Week 3**: Achieve >80% average accuracy
- **Week 4**: Achieve >85% average accuracy with consistent patterns identified

## 🔗 Cross-Repository Coordination

### Issue Linking Convention
**Always include these references in implementation tasks**:
```markdown
**Epic:** onemployment-planning#X (Feature Request)
**Design:** onemployment-planning#Y (Technical Design)  
**Related Tasks:**
- Frontend: onemployment/frontend#A
- Backend: onemployment/backend#B
- Infrastructure: onemployment/infrastructure#C
```

### Project Board Management
**Organization Project**: https://github.com/orgs/onemployment/projects/1

**Column Workflow**:
- **Backlog** - New feature requests and designs awaiting prioritization
- **In Progress** - Active development work across all repositories
- **Review** - Technical designs awaiting approval, code reviews in progress
- **Done** - Completed work ready for deployment or deployed

**Adding Issues to Project Board**:
1. **During Issue Creation**: Use "Projects" sidebar to select "Development Process" project
2. **From Project Board**: Click "Add items" → Search `repo:onemployment/repository-name` → Select issues

## 💻 Cross-Repository Development Guide

### Local Development Setup Options

**Option 1 - Planning Focus** (Feature Requests & Tech Designs):
```bash
git clone https://github.com/onemployment/onemployment-planning.git
cd onemployment-planning
# Start Claude Code session here - this CLAUDE.md provides complete context
```

**Option 2 - Full Development** (Implementation Tasks):
```bash
mkdir onemployment-workspace && cd onemployment-workspace
git clone https://github.com/onemployment/onemployment-planning.git
git clone https://github.com/onemployment/frontend.git  
git clone https://github.com/onemployment/backend.git
git clone https://github.com/onemployment/infrastructure.git

# Always start Claude Code session from planning directory
cd onemployment-planning
# Use this CLAUDE.md for coordination, navigate to other repos for implementation
```

### Implementation Workflow
1. **Start Here**: Read this CLAUDE.md for platform context and task coordination
2. **Navigate to Target Repo**: `cd ../[repository-name]` for implementation work  
3. **Read Repo CLAUDE.md**: Get repository-specific setup, patterns, and validation requirements
4. **Implement & Test**: Follow repository-specific development and testing procedures
5. **Return for Coordination**: Come back to planning repo for cross-repository coordination

### Development Environment Requirements
**All Repositories**:
- **Node.js 18+** for JavaScript/TypeScript development
- **Git** for version control with standardized commit format
- **Docker** for containerized development environments (backend, infrastructure)

**Repository-Specific**:
- **Frontend**: npm, Vite, modern browser for development
- **Backend**: Docker Compose for PostgreSQL, Jest for testing  
- **Infrastructure**: AWS CLI, Docker for containerization, access to AWS account

## 🔧 Shared Platform Standards

### Commit Message Format (All Repositories)
```
<imperative title>

- <concise bullet point describing important change and brief why>
- <concise bullet point describing important change and brief why>
- <concise bullet point describing important change and brief why>
```

**Guidelines**:
- Title: Imperative mood, 50 characters or less
- Bullets: Explain what changed and briefly why
- No emojis, Claude collaboration lines, or extra formatting
- Focus on business value and technical necessity

**Example**:
```
Add user authentication flow

- Implement login/logout functionality to secure user access  
- Add JWT token management for session handling
- Create protected route wrapper for authenticated pages
- Add form validation to prevent invalid submissions
```

### Code Quality Requirements (All Repositories)
- **TypeScript strict mode** with full type safety
- **ESLint compliance** with repository-specific rules  
- **Prettier formatting** for consistent code style
- **Comprehensive test coverage** with unit and integration tests
- **Security best practices** - no secrets in code, input validation, secure authentication

### Deployment Principles (All Repositories)
- **Automated CI/CD** via GitHub Actions with proper testing gates
- **Environment parity** between development, staging, and production
- **Health monitoring** with proper logging and alerting
- **Rollback capability** for quick recovery from deployment issues
- **Cost optimization** staying within AWS Free Tier limits when possible

## 🎯 AI Agent Instructions

### Essential Workflow for Claude Code Agents

#### 1. Session Initialization
- **Always start** Claude Code sessions from `onemployment-planning` directory
- **Read this CLAUDE.md file first** for complete platform context
- **Understand your work type** (Feature Request, Tech Design, or Implementation)
- **Check project board** for current priorities and context

#### 2. Work Type Navigation
**Feature Requests & Technical Designs**:
- Stay in planning repository for entire workflow
- Use provided GitHub issue templates exclusively
- Add all issues to project board during creation
- Follow cross-repository linking conventions

**Implementation Tasks**:
- Start here for context and issue creation
- Navigate to target repository: `cd ../[repository-name]`  
- Read target repository CLAUDE.md for implementation details
- Return to planning repo for cross-repository coordination

#### 3. Repository-Specific Work
When working in implementation repositories:
- **Always read** repository-specific CLAUDE.md file first
- **Follow** repository validation sequences (lint → build → test)
- **Use** existing code patterns and architectural decisions
- **Test** thoroughly using repository-specific testing approaches
- **Reference** back to planning repository for issue coordination

#### 4. Cross-Repository Coordination
- **Link issues properly** using epic/design/task format
- **Update project board** as work progresses through columns
- **Track estimation accuracy** with completion comments including actual effort
- **Reference related issues** in commits and pull requests

#### 5. Quality Assurance
- **Run validation sequences** before committing (repository-specific)
- **Follow commit message format** consistently across all repositories
- **Update documentation** when introducing new patterns or processes
- **Participate in weekly reviews** with accurate estimation data

#### 6. Emergency Procedures
- **Production Issues**: Check health endpoints first, reference infrastructure CLAUDE.md
- **Deployment Problems**: Review GitHub Actions, check AWS console (us-east-2 region)
- **Integration Failures**: Verify cross-repository dependencies and API contracts

## 🔍 Quick Reference

### Essential URLs
- **Project Board**: https://github.com/orgs/onemployment/projects/1
- **Issue Templates**: https://github.com/onemployment/onemployment-planning/issues/new/choose
- **Production Frontend**: https://www.onemployment.org
- **Production API**: https://api.onemployment.org
- **API Health Check**: https://api.onemployment.org/health

### Documentation & Setup
- **Process Documentation**: [docs/index.md](docs/index.md) - Complete workflow details
- **Estimation Guide**: [docs/process/estimation-tracking.md](docs/process/estimation-tracking.md) - Story point methodology
- **Repository Setup**: [docs/setup-guide.md](docs/setup-guide.md) - First-time contributor setup

### Repository CLAUDE.md Files
- **Backend Development**: [`backend/CLAUDE.md`](https://github.com/onemployment/backend/blob/main/CLAUDE.md) - API patterns, testing, deployment
- **Frontend Development**: [`frontend/CLAUDE.md`](https://github.com/onemployment/frontend/blob/main/CLAUDE.md) - Component patterns, UI guidelines, build process  
- **Infrastructure Operations**: [`infrastructure/CLAUDE.md`](https://github.com/onemployment/infrastructure/blob/main/CLAUDE.md) - AWS deployment, monitoring, security

### Emergency Contacts & Resources
- **AWS Console**: us-east-2 (Ohio) region - ECS, RDS management
- **GitHub Actions**: Check workflow status for deployment issues
- **Database**: `onemployment-postgres.cr2ekyu0wmcb.us-east-2.rds.amazonaws.com:5432`
- **Container Registry**: `062440546828.dkr.ecr.us-east-2.amazonaws.com/onemployment/api`

---

**Instructions for AI Agents**: This file serves as the universal starting point for all onemployment platform development. Use the Repository Navigator to find specific implementation guidance, follow the established workflows for your contribution type, and maintain coordination through the planning repository for all cross-repository work.