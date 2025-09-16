# onemployment Platform - AI-Powered Development Guide

**The definitive guide for contributing to the onemployment platform using AI agents like Claude Code**

---

## 🚀 Quick Start

### For New Contributors
1. **Clone this repository**: `git clone https://github.com/onemployment/onemployment-planning.git`
2. **Start your AI agent session**: `cd onemployment-planning/` 
3. **Load context**: Your AI agent will automatically access [`CLAUDE.md`](CLAUDE.md) for complete platform context
4. **Choose your contribution type** below and follow the step-by-step workflow

### Prerequisites
- **Node.js 18+** (for all repositories)
- **Git** with GitHub account access
- **AI Agent** (Claude Code, GitHub Copilot, or similar)
- **AWS CLI** (optional, for infrastructure work)

---

## 🏗️ Platform Architecture

### Repository Overview
| Repository | Purpose | Status | AI Context |
|------------|---------|--------|------------|
| **[planning](https://github.com/onemployment/onemployment-planning)** | Feature requests, designs, coordination | ✅ Active | [`CLAUDE.md`](CLAUDE.md) |
| **[backend](https://github.com/onemployment/backend)** | Node.js API with Redis authentication | ✅ Production | [`backend/CLAUDE.md`](https://github.com/onemployment/backend/blob/main/CLAUDE.md) |
| **[frontend](https://github.com/onemployment/frontend)** | React/TypeScript user interface | ✅ Production | [`frontend/CLAUDE.md`](https://github.com/onemployment/frontend/blob/main/CLAUDE.md) |
| **[infrastructure](https://github.com/onemployment/infrastructure)** | AWS deployment and monitoring | ✅ Production | [`infrastructure/CLAUDE.md`](https://github.com/onemployment/infrastructure/blob/main/CLAUDE.md) |

### Live Environment
- **Production Frontend**: https://www.onemployment.org
- **Production API**: https://api.onemployment.org  
- **Health Check**: https://api.onemployment.org/health
- **Project Board**: https://github.com/orgs/onemployment/projects/1

---

## 🤖 AI Agent Workflow

### Starting Your Development Session

**The Golden Rule**: Always start AI agent sessions from this planning repository directory.

```bash
# Recommended workflow
cd onemployment-planning/
# Start Claude Code, GitHub Copilot, or your preferred AI agent here
# Your agent will automatically load CLAUDE.md with complete platform context
```

**Why this works:**
- ✅ **Universal Context**: [`CLAUDE.md`](CLAUDE.md) provides complete platform overview
- ✅ **Specialized Agents**: Access to `@product-manager` agent for requirements engineering
- ✅ **Navigation Guidance**: Clear paths to repository-specific implementation details
- ✅ **Cross-Repository Coordination**: Central hub for linking issues and tracking progress

### Using Specialized AI Agents

**Product Manager Agent** (`@product-manager`)
- **When to use**: Creating Feature Requests, gathering requirements, defining user scenarios
- **How to use**: Type `@product-manager` in Claude Code after starting session from planning repo
- **Capabilities**: Auto-creates structured Feature Requests in Notion, runs 6-step requirement gathering process
- **Output**: Complete Feature Request with user scenarios, acceptance criteria, and technical specifications

### Navigation Between Repositories

**For Cross-Repository Work:**
1. **Start here** (planning repo) → Load universal context
2. **Navigate to target repo** → `cd ../frontend` (or backend/infrastructure)  
3. **Agent reads repo CLAUDE.md** → Gets implementation-specific context
4. **Return to planning** → `cd ../onemployment-planning` for coordination

**Example Navigation Flow:**
```bash
cd onemployment-planning/          # Start with universal context
# Create Feature Request using @product-manager agent
cd ../frontend/                    # Move to implementation
# Agent reads frontend/CLAUDE.md for React-specific patterns  
cd ../onemployment-planning/       # Return for cross-repo coordination
```

---

## 📋 Contribution Workflows

### 1. 🏗️ Feature Request Development

**Goal**: Transform business ideas into comprehensive technical requirements

**Step-by-Step Process:**

1. **Initialize AI Session**
   ```bash
   cd onemployment-planning/
   # Start Claude Code or similar AI agent
   ```

2. **Use Product Manager Agent**
   ```
   @product-manager create a new feature request for [your feature idea]
   ```

3. **Follow 6-Step Requirements Process**
   - **Problem Definition**: What problem, who has it, why it matters
   - **Solution Brainstorming**: Chosen approach, alternatives, reasoning  
   - **User Scenarios**: Happy path, secondary flows, error cases
   - **Functional Requirements**: MVP vs nice-to-have with Given-When-Then criteria
   - **Non-Functional Requirements**: Performance, security, scalability needs
   - **Implementation Notes**: Dependencies, risks, success metrics

4. **GitHub Issue Creation**
   - Agent creates structured GitHub issue using [Feature Request template](https://github.com/onemployment/onemployment-planning/issues/new?template=feature-request.yml)
   - Automatic linking to Notion documentation
   - Addition to project board

**Expected Outcome**: Comprehensive Feature Request ready for technical design phase

---

### 2. 📐 Technical Design Work

**Goal**: Translate Feature Requests into detailed architecture and implementation plans

**Step-by-Step Process:**

1. **Create Technical Design Issue**
   - Use [Technical Design template](https://github.com/onemployment/onemployment-planning/issues/new?template=technical-design.yml)
   - Reference Feature Request: `Epic: onemployment-planning#X`

2. **Follow 9-Step Design Process**
   1. Requirements Analysis & Scope Definition
   2. Data Model Design (database schema, relationships)
   3. API Design & Integration Points (endpoints, authentication)
   4. Frontend Architecture & Components (React patterns, state management)
   5. Technology Stack & Dependencies (new libraries, compatibility)
   6. Testing Strategy (unit, integration, e2e approaches)
   7. Implementation Plan & Task Breakdown (story-pointed tasks)
   8. Deployment & Infrastructure Plan (AWS resources, rollback strategy)
   9. Design Review & Approval (stakeholder sign-off)

3. **Cross-Repository Planning**
   - Identify which repositories need changes
   - Plan task dependencies and sequencing
   - Estimate story points (1 = half day, 2 = full day, 3 = two days)

**Expected Outcome**: Detailed technical design ready for implementation task creation

---

### 3. 💻 Implementation Tasks

**Goal**: Execute technical designs with proper testing and deployment

**Step-by-Step Process:**

1. **Task Creation Strategy**
   - **Frontend Tasks**: Create in [frontend repository](https://github.com/onemployment/frontend/issues/new)
   - **Backend Tasks**: Create in [backend repository](https://github.com/onemployment/backend/issues/new)
   - **Infrastructure Tasks**: Create in [infrastructure repository](https://github.com/onemployment/infrastructure/issues/new)
   - **Cross-Repository Tasks**: Create in planning repository with clear scope

2. **Repository-Specific Development**

   **Backend Development** (`cd ../backend/`):
   ```bash
   npm run setup                    # Complete database setup
   npm run dev                      # Start development server
   npm run lint                     # ESLint validation
   npm run build                    # TypeScript compilation  
   npm run test:unit                # Unit tests
   npm run test:int                 # Integration tests
   npm run format                   # Prettier formatting
   ```

   **Frontend Development** (`cd ../frontend/`):
   ```bash
   npm install                      # Install dependencies
   npm run dev                      # Vite development server
   npm run lint                     # ESLint validation
   npm run type-check               # TypeScript compilation
   npm run build                    # Production build
   npm run test                     # Unit tests (when available)
   npm run format                   # Prettier formatting
   ```

   **Infrastructure Operations** (`cd ../infrastructure/`):
   ```bash
   aws ecs describe-services --cluster onemployment-cluster --services backend-service
   curl https://api.onemployment.org/health
   aws s3 sync dist/ s3://www.onemployment.org
   aws cloudfront create-invalidation --distribution-id E2AR0Y5IQCACIR --paths "/*"
   ```

3. **Code Quality Validation**
   - **Backend**: lint → build → test:unit → test:int → format
   - **Frontend**: lint → type-check → build → test → format
   - **Infrastructure**: Manual validation → AWS CLI verification → health checks

4. **Commit and Deploy**
   - Follow shared commit message format (see [Standards](#commit-standards))
   - Link issues: `Epic: onemployment-planning#X`, `Design: onemployment-planning#Y`
   - Automated deployment via GitHub Actions

**Expected Outcome**: Production-ready code with comprehensive testing and documentation

---

### 4. 🔍 Weekly Reviews

**Goal**: Track estimation accuracy and improve development velocity

**Step-by-Step Process:**

1. **Create Weekly Review Issue**
   - Use [Weekly Review template](https://github.com/onemployment/onemployment-planning/issues/new?template=weekly-review.yml)

2. **Analyze Completed Tasks**
   - List all completed implementation tasks
   - Compare estimated vs actual story points
   - Calculate accuracy: `(Estimated ÷ Actual) × 100%`

3. **Pattern Identification**
   - Tasks consistently under/over/accurately estimated
   - Repository-specific estimation patterns
   - Technology-specific complexity factors

4. **Process Improvements**
   - Specific adjustments for next week's estimation
   - Documentation updates based on learnings
   - Tool or workflow enhancements

**Expected Outcome**: Improved estimation accuracy and development process optimization

---

## 🔧 Development Standards

### Commit Standards

**Format** (consistent across all repositories):
```
<imperative title>

- <concise bullet point describing important change and brief why>
- <concise bullet point describing important change and brief why>
- <concise bullet point describing important change and brief why>
```

**Example**:
```
Add user authentication flow

- Implement login/logout functionality to secure user access
- Add JWT token management for session handling
- Create protected route wrapper for authenticated pages
- Add form validation to prevent invalid submissions
```

**Guidelines**:
- Title: Imperative mood, 50 characters or less
- Bullets: Explain what changed and briefly why
- No emojis, collaboration lines, or extra formatting
- Focus on business value and technical necessity

### Issue Linking Conventions

**Always include in implementation tasks**:
```markdown
**Epic:** onemployment-planning#X (Feature Request)
**Design:** onemployment-planning#Y (Technical Design)  
**Related Tasks:**
- Frontend: onemployment/frontend#A
- Backend: onemployment/backend#B
- Infrastructure: onemployment/infrastructure#C
```

### Story Point System

- **1 point** = Half day (~4 hours of focused development)
- **2 points** = Full day (~8 hours of focused development)  
- **3 points** = Two days (~16 hours of focused development)

**Completion Tracking**: Add this comment when finishing tasks:
```
Completed - Actual effort: X story points
Brief note on what made it take more/less time than estimated
```

---

## 🎯 Practical Examples

### Example 1: End-to-End Feature Development

**Scenario**: Adding user profile photo upload feature

**Step 1 - Feature Request** (in `onemployment-planning/`):
```bash
cd onemployment-planning/
# Start Claude Code
@product-manager create a new feature request for "user profile photo upload"
```
- Agent guides through 6-step requirements process
- Creates comprehensive Feature Request in GitHub + Notion
- Defines user scenarios, acceptance criteria, security requirements

**Step 2 - Technical Design** (in `onemployment-planning/`):
- Create Technical Design issue referencing Feature Request
- Design file upload API endpoints (backend)
- Plan image component and upload UI (frontend)
- Specify S3 storage and CloudFront integration (infrastructure)
- Break down into story-pointed tasks

**Step 3 - Implementation** (multi-repository):
```bash
# Backend API development
cd ../backend/
# AI agent reads backend/CLAUDE.md for API patterns
# Implement file upload endpoints, validation, S3 integration
npm run lint && npm run build && npm test && npm run format

# Frontend UI development  
cd ../frontend/
# AI agent reads frontend/CLAUDE.md for React patterns
# Create upload component, image preview, error handling
npm run lint && npm run type-check && npm run build && npm run format

# Infrastructure updates
cd ../infrastructure/ 
# AI agent reads infrastructure/CLAUDE.md for AWS patterns
# Configure S3 bucket, CloudFront, security policies
aws s3 mb s3://onemployment-user-photos
```

**Step 4 - Integration & Deployment**:
- Automated deployment via GitHub Actions
- Production health checks and monitoring
- Weekly review with estimation accuracy analysis

### Example 2: Bug Fix Workflow

**Scenario**: Users report authentication timeout issues

**Investigation** (in `onemployment-planning/`):
```bash
cd onemployment-planning/
# Start Claude Code with full platform context
# Create bug report issue, analyze production logs
# Check backend health: curl https://api.onemployment.org/health
```

**Implementation** (in `backend/`):
```bash
cd ../backend/
# AI agent reads backend/CLAUDE.md for authentication patterns
# Analyze JWT token expiration, Redis session management
# Fix timeout configuration, add monitoring
npm run lint && npm run build && npm test:int && npm run format
```

**Verification**:
- Deploy to production via automated pipeline
- Monitor authentication metrics
- Update documentation and preventive measures

---

## 🚨 Troubleshooting & Resources

### Common Issues

**AI Agent Can't Access Context**
```bash
# Solution: Always start from planning repository
cd onemployment-planning/
# AI agent automatically loads CLAUDE.md with complete platform context
```

**Repository Setup Issues**
```bash
# Backend: Database connection problems
cd backend/
npm run setup:db               # Reset database setup

# Frontend: Build failures  
cd frontend/
npm run type-check             # Check TypeScript errors
npm run build                  # Verify production build

# Infrastructure: AWS access issues
aws configure                  # Verify credentials
aws sts get-caller-identity    # Check account access
```

**Cross-Repository Coordination Problems**
- **Missing Issue Links**: Always reference Epic and Design issues
- **Project Board Sync**: Add issues to [organization project board](https://github.com/orgs/onemployment/projects/1)
- **Dependency Management**: Check task dependencies in Technical Design

### Emergency Procedures

**Production Outage**
1. **Check Health Endpoints**: https://api.onemployment.org/health
2. **AWS Console**: Monitor ECS service status (us-east-2 region)
3. **Restart Services**: `aws ecs update-service --cluster onemployment-cluster --service backend-service --desired-count 1`
4. **Check Logs**: CloudWatch logs for error diagnosis

**Cost Overruns**  
1. **AWS Cost Explorer**: Review unexpected charges
2. **Stop Non-Essential Services**: Scale down development resources
3. **Monitor Free Tier**: Check ElastiCache, ECS Fargate usage limits

**Deployment Failures**
1. **GitHub Actions**: Check workflow status for build errors
2. **Code Quality**: Run validation sequences locally before pushing
3. **Dependency Issues**: Verify package.json changes and compatibility

### Resource Links

**Production Monitoring**:
- **Frontend**: https://www.onemployment.org
- **API**: https://api.onemployment.org
- **Health Check**: https://api.onemployment.org/health

**Development Tools**:
- **Project Board**: https://github.com/orgs/onemployment/projects/1
- **Issue Templates**: https://github.com/onemployment/onemployment-planning/issues/new/choose
- **Repository Navigator**: See [platform overview](#platform-architecture) table above

**AWS Console Access** (us-east-2 region):
- **ECS Console**: Search "onemployment-cluster"  
- **ElastiCache**: Search "onemployment-redis"
- **S3**: Bucket "www.onemployment.org"
- **CloudFront**: Distribution E2AR0Y5IQCACIR

---

## 🎓 Advanced Workflows

### Multi-Repository Feature Development

For features spanning multiple repositories:

1. **Coordination Phase** (in `onemployment-planning/`):
   - Create Epic-level Feature Request
   - Design cross-repository architecture
   - Plan task dependencies and timing

2. **Parallel Development**:
   - Backend API development (authentication, data models)
   - Frontend UI development (components, integration)  
   - Infrastructure updates (resources, monitoring)

3. **Integration Testing**:
   - Backend integration tests with real databases
   - Frontend end-to-end tests with real API
   - Infrastructure deployment verification

4. **Coordinated Deployment**:
   - Infrastructure changes first
   - Backend API updates
   - Frontend deployment with feature flags

### AI Agent Optimization

**Context Management**:
- Start sessions from planning repo for universal context
- Navigate to specific repos only when implementing
- Return to planning repo for cross-repository coordination

**Specialized Agent Usage**:
- Use `@product-manager` for requirements engineering
- Leverage repository-specific CLAUDE.md files for implementation patterns
- Maintain conversation context across repository navigation

**Quality Assurance**:
- Always run validation sequences before committing
- Use AI agents to review code quality and test coverage
- Automate repetitive tasks while maintaining human oversight

---

**Next Steps**: Choose your contribution type above and start building! The AI-powered development workflow is designed to maximize your productivity while maintaining high code quality and thorough documentation.

---

*This guide is a living document. Updates and improvements are tracked through the [planning repository issues](https://github.com/onemployment/onemployment-planning/issues) and implemented collaboratively by the development community.*