# Setup Guide

This guide will help you set up the complete development process infrastructure.

## 1. Enable GitHub Pages

To make the documentation available at `https://onemployment.github.io/onemployment-planning`:

1. Go to [Repository Settings](https://github.com/onemployment/onemployment-planning/settings)
2. Scroll down to "Pages" section in the left sidebar
3. Under "Source", select "Deploy from a branch"
4. Choose "main" branch and "/docs" folder
5. Click "Save"
6. GitHub will build and deploy the site (takes a few minutes)

## 2. Create Organization Project Board

1. Go to [Organization Projects](https://github.com/orgs/onemployment/projects)
2. Click "New project"
3. Choose "Board" layout
4. Set these details:
   - **Name:** Development Process
   - **Description:** Cross-repository development workflow tracking
5. Create these columns:
   - **Backlog** - New feature requests and designs
   - **In Progress** - Active development work
   - **Review** - Technical designs awaiting approval
   - **Done** - Completed work

## 3. Repository Setup Verification

Verify these components are in place:

### Issue Templates
- [x] Feature Request template
- [x] Technical Design template  
- [x] Implementation Task template
- [x] Weekly Review template

### Documentation Structure
- [x] `docs/index.md` - Main process documentation
- [x] `docs/process/estimation-tracking.md` - Estimation process details
- [x] `docs/_config.yml` - GitHub Pages configuration

### Repository Files
- [x] `README.md` - Repository overview with direct template links
- [x] `.github/ISSUE_TEMPLATE/` - All issue templates

## 4. First Use

After setup is complete:

1. **Test issue templates:** Create a test feature request using the template
2. **Add to project board:** Verify the issue appears in your project board
3. **Verify GitHub Pages:** Check that documentation loads at the GitHub Pages URL
4. **Create first real feature request:** Start with your actual first feature

## 5. Troubleshooting

### GitHub Pages Not Loading
- Check Pages settings are enabled with "main" branch and "/docs" folder
- Verify `_config.yml` exists in docs folder
- GitHub Pages can take 5-10 minutes to deploy initially

### Project Board Issues
- Ensure you have admin access to the organization
- Issues may not appear in project board if not properly linked

### Issue Template Problems  
- Templates should appear at `https://github.com/onemployment/onemployment-planning/issues/new/choose`
- If templates don't show, check YAML syntax in template files

## 6. Maintenance

### Weekly Tasks
- Create weekly review using the template
- Update project board status for all active issues
- Review estimation accuracy and patterns

### Monthly Tasks
- Review and update process documentation
- Assess project board column effectiveness
- Update issue templates based on usage patterns