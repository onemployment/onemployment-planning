# Estimation Tracking Process

## Goal
Learn to estimate development tasks accurately through systematic tracking.

## Story Point Scale
- **1 point** = Half day (~4 hours)
- **2 points** = Full day (~8 hours)  
- **3 points** = Two days (~16 hours)

## Process Flow

### 1. Feature Request → Technical Design → Implementation Tasks
1. Create feature request with business requirements
2. Create technical design with 9-step collaborative process
3. Break design into implementation tasks with story point estimates

### 2. Task Completion Tracking
When finishing any task, add comment:
```
Completed - Actual effort: X story points
```

### 3. Weekly Estimation Review
Every Friday:
1. Create weekly review issue
2. List completed tasks with estimated vs actual points
3. Calculate accuracy and identify patterns
4. Plan improvements for next week

## Accuracy Calculation
```
Task Accuracy = (Estimated Points ÷ Actual Points) × 100%

Examples:
- Estimated 2, Actual 2 = 100% (perfect)
- Estimated 2, Actual 3 = 67% (underestimated)
- Estimated 3, Actual 2 = 150% (overestimated)
```

**Good Range:** 80-120% (within 20% of estimate)

## Success Targets
- **Week 1:** Establish baseline accuracy
- **Week 2:** >70% average accuracy
- **Week 3:** >80% average accuracy  
- **Week 4:** >85% average accuracy

## Repositories & Cross-Linking

### Feature Requests & Designs
- Created in: `onemployment-planning`
- Link to: All related implementation tasks

### Implementation Tasks
- **Frontend tasks:** Created in `onemployment/frontend`
- **Backend tasks:** Created in `onemployment/backend`
- **Infrastructure tasks:** Created in `onemployment/infrastructure`
- **Documentation tasks:** Created in `onemployment-planning`

### Linking Format
```markdown
**Epic:** onemployment-planning#1
**Design:** onemployment-planning#15
**Related Tasks:** 
- Frontend: onemployment/frontend#23
- Backend: onemployment/backend#45
```

## Common Patterns
*To be updated as you learn your estimation patterns*

### Tasks Often Underestimated:
- [Update based on experience]

### Tasks Often Overestimated:
- [Update based on experience]

### Accurate Estimate Indicators:
- [Update based on experience]

## Process Evolution
This is the first iteration focusing only on estimation accuracy. Future additions may include:
- Velocity tracking
- Quality metrics
- Process adherence measurements
- Milestone planning