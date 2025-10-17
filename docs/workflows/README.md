# Step-by-Step Workflows

> Comprehensive workflow guides for automating complex tasks with AI

## Table of Contents

1. [Software Development Workflows](#software-development-workflows)
2. [Content Creation Workflows](#content-creation-workflows)
3. [Operations Workflows](#operations-workflows)
4. [Cross-Functional Workflows](#cross-functional-workflows)
5. [Workflow Best Practices](#workflow-best-practices)

## Software Development Workflows

### Workflow 1: Feature Development End-to-End

**Goal**: Develop a complete feature from requirements to deployment.

**Duration**: 2-4 days (depending on complexity)

**Prerequisites**: 
- Feature requirements document
- Development environment setup
- Access to repository and deployment tools

---

#### Step 1: Requirements Analysis (30 minutes)

**Prompt**:
```
Analyze these feature requirements and create a technical specification:

REQUIREMENTS:
[Paste requirements]

GENERATE:

1. **Feature Overview**
   - Purpose and goals
   - User stories (3-5)
   - Success criteria

2. **Technical Design**
   - Architecture approach
   - Component breakdown
   - Data models needed
   - API endpoints required

3. **Implementation Plan**
   - Task breakdown
   - Dependencies
   - Estimated effort per task

4. **Testing Strategy**
   - Test scenarios
   - Edge cases to cover
   - Acceptance criteria

5. **Risks & Mitigations**
   - Potential issues
   - Mitigation strategies

Format as technical specification document.
```

**Output**: Technical specification with clear implementation path.

**Next**: Review and refine the specification.

---

#### Step 2: Database Schema Design (20 minutes)

**Prompt**:
```
Design database schema for this feature:

FEATURE: [Feature description]

REQUIREMENTS:
- Data entities: [list]
- Relationships: [describe]
- Query patterns: [common queries]
- Scale: [expected data volume]

DATABASE: [PostgreSQL/MongoDB/etc.]

GENERATE:

1. **Entity-Relationship Diagram** (describe in text)
2. **Table Definitions**:
   - Table name
   - Columns with types
   - Constraints
   - Indexes
   - Foreign keys

3. **Migration Script**:
   - Up migration
   - Down migration
   - Data seeding (if needed)

4. **Sample Queries**:
   - Create
   - Read (with common filters)
   - Update
   - Delete
   - Complex queries

Best practices: Normalization, indexing, constraints.
```

**Output**: Database schema with migration scripts.

**Validation**: Review schema for normalization and performance.

---

#### Step 3: API Endpoint Implementation (2-3 hours)

**Prompt**:
```
Implement REST API endpoints for [FEATURE]:

ENDPOINTS NEEDED:
- GET /api/[resource]
- POST /api/[resource]
- PUT /api/[resource]/:id
- DELETE /api/[resource]/:id

FRAMEWORK: [Express/FastAPI/etc.]

FOR EACH ENDPOINT:

1. **Route Handler**:
   - Request validation
   - Business logic
   - Error handling
   - Response formatting

2. **Middleware**:
   - Authentication
   - Authorization
   - Input validation
   - Rate limiting

3. **Database Layer**:
   - Query functions
   - Transaction handling
   - Connection pooling

4. **Documentation**:
   - OpenAPI/Swagger spec
   - Request/response examples

INCLUDE:
- Error handling for all edge cases
- Logging
- Security best practices
- Performance optimization
```

**Output**: Complete API implementation with all layers.

**Testing**: Use Postman/Insomnia to test each endpoint.

---

#### Step 4: Unit Test Generation (1 hour)

**Prompt**:
```
Generate comprehensive unit tests for these API endpoints:

CODE:
[Paste endpoint code]

FRAMEWORK: [Jest/Pytest/etc.]

GENERATE TESTS FOR:

1. **Happy Path**:
   - Valid requests
   - Expected responses
   - Proper status codes

2. **Edge Cases**:
   - Empty data
   - Maximum values
   - Boundary conditions

3. **Error Cases**:
   - Invalid input
   - Unauthorized access
   - Resource not found
   - Validation failures

4. **Integration**:
   - Database interactions
   - External service calls
   - Middleware behavior

INCLUDE:
- Test setup and teardown
- Mock database
- Mock external services
- Test data factories
- Clear test descriptions
- Assertions for all scenarios

Target: 90%+ code coverage
```

**Output**: Complete test suite.

**Validation**: Run tests and ensure all pass.

---

#### Step 5: Frontend Integration (2-3 hours)

**Prompt**:
```
Create frontend components for [FEATURE]:

FRAMEWORK: [React/Vue/Angular]

COMPONENTS NEEDED:
1. [ComponentName1]: [purpose]
2. [ComponentName2]: [purpose]
3. [ComponentName3]: [purpose]

FOR EACH COMPONENT:

1. **Component Structure**:
   - Props/inputs
   - State management
   - Lifecycle methods/hooks
   - Event handlers

2. **API Integration**:
   - Fetch data
   - Handle loading states
   - Error handling
   - Success feedback

3. **UI Implementation**:
   - Layout structure
   - Styling (CSS/styled-components)
   - Responsive design
   - Accessibility

4. **Validation**:
   - Form validation
   - User feedback
   - Error messages

5. **Tests**:
   - Component tests
   - Integration tests
   - User interaction tests

INCLUDE:
- Type definitions (TypeScript)
- Loading spinners
- Error boundaries
- Proper ARIA labels
```

**Output**: Complete frontend implementation.

**Testing**: Manual testing in browser and automated tests.

---

#### Step 6: Integration Testing (1 hour)

**Prompt**:
```
Create end-to-end tests for [FEATURE]:

FRAMEWORK: [Cypress/Playwright]

USER FLOW:
1. [Step 1: e.g., User logs in]
2. [Step 2: e.g., Navigates to feature]
3. [Step 3: e.g., Performs action]
4. [Step 4: e.g., Verifies result]

FOR EACH FLOW:

```javascript
describe('[Feature Name]', () => {
  beforeEach(() => {
    // Setup
  });

  it('should [test description]', () => {
    // Test steps with assertions
  });
});
```

INCLUDE:
- Setup and teardown
- Test data creation
- Page object models
- Screenshot on failure
- Network request assertions
- Database state verification

Test both happy paths and error scenarios.
```

**Output**: E2E test suite.

**Validation**: Run tests in CI environment.

---

#### Step 7: Documentation (30 minutes)

**Prompt**:
```
Create documentation for [FEATURE]:

GENERATE:

## Feature Documentation

### Overview
[What it does, why it exists]

### User Guide
1. **How to Use**:
   - Step-by-step instructions
   - Screenshots descriptions
   - Tips and best practices

2. **Common Use Cases**:
   - Scenario 1
   - Scenario 2
   - Scenario 3

### Technical Documentation

1. **API Reference**:
   - Endpoints
   - Request/response formats
   - Error codes

2. **Architecture**:
   - System design
   - Data flow
   - Component interactions

3. **Database Schema**:
   - Tables and relationships
   - Important queries

### Development Guide

1. **Setup**:
   - Prerequisites
   - Installation steps

2. **Testing**:
   - How to run tests
   - How to add new tests

3. **Deployment**:
   - Build process
   - Deployment steps
   - Environment variables

### Troubleshooting
- Common issues and solutions
- Debugging tips
- Known limitations

Format: Markdown, suitable for wiki or docs site
```

**Output**: Complete feature documentation.

---

#### Step 8: Code Review Preparation (15 minutes)

**Prompt**:
```
Create a code review checklist and PR description for [FEATURE]:

CHANGES:
[Summary of changes]

GENERATE:

## Pull Request Description

### What
[Brief description]

### Why
[Motivation and context]

### Changes
- [Change 1]
- [Change 2]
- [Change 3]

### Testing
- [ ] Unit tests pass
- [ ] Integration tests pass
- [ ] Manual testing completed
- [ ] Performance tested

### Screenshots
[Describe what screenshots to include]

### Deployment Notes
[Any special deployment considerations]

### Checklist
- [ ] Code follows style guidelines
- [ ] Self-reviewed the code
- [ ] Commented complex code
- [ ] Updated documentation
- [ ] Added tests
- [ ] All tests passing
- [ ] No console errors/warnings

## Self-Review Checklist

**Code Quality**:
- [ ] No code duplication
- [ ] Functions are small and focused
- [ ] Clear variable names
- [ ] Proper error handling

**Security**:
- [ ] Input validation
- [ ] No sensitive data in code
- [ ] SQL injection prevention
- [ ] XSS protection

**Performance**:
- [ ] No N+1 queries
- [ ] Efficient algorithms
- [ ] Proper caching
- [ ] Optimized bundle size

**Testing**:
- [ ] Edge cases covered
- [ ] Error scenarios tested
- [ ] Integration points tested
```

**Output**: PR description and review checklist.

---

**Workflow Complete!**

**Summary**:
- ✅ Requirements analyzed and spec created
- ✅ Database schema designed
- ✅ API endpoints implemented
- ✅ Tests written and passing
- ✅ Frontend integrated
- ✅ E2E tests passing
- ✅ Documentation complete
- ✅ Ready for code review

---

### Workflow 2: Bug Investigation and Fix

**Goal**: Systematically investigate, fix, and verify a bug.

**Duration**: 2-4 hours (depending on complexity)

---

#### Step 1: Bug Analysis (15 minutes)

**Prompt**:
```
Analyze this bug report:

BUG REPORT:
Title: [bug title]
Description: [what's wrong]
Steps to Reproduce:
1. [step 1]
2. [step 2]
3. [step 3]
Expected: [expected behavior]
Actual: [actual behavior]
Environment: [browser/OS/version]
Error Messages: [any errors]

ANALYZE:

1. **Understanding**:
   - What's happening
   - Why it's a problem
   - Who's affected

2. **Hypotheses**:
   - Likely causes (ranked by probability)
   - Areas of code to investigate

3. **Investigation Plan**:
   - What to check first
   - What logs to review
   - What to test locally

4. **Reproduction Strategy**:
   - How to reproduce consistently
   - Minimal reproduction steps
   - Test data needed

5. **Priority Assessment**:
   - Severity
   - Impact
   - Urgency
```

**Output**: Bug analysis with investigation plan.

---

#### Step 2: Code Investigation (30-60 minutes)

**Prompt**:
```
Help debug this issue:

PROBLEM:
[Describe the bug]

RELEVANT CODE:
[Paste suspicious code sections]

ERROR MESSAGES:
[Paste error logs/stack traces]

WHAT I'VE TRIED:
[List attempted solutions]

PROVIDE:

1. **Error Analysis**:
   - What the error means
   - Why it's happening
   - Related code paths

2. **Root Cause**:
   - Exact cause
   - Why it wasn't caught earlier
   - Contributing factors

3. **Debugging Steps**:
   - What to log
   - What to breakpoint
   - What values to inspect

4. **Fix Approaches**:
   - Quick fix (temporary)
   - Proper fix (permanent)
   - Trade-offs of each

Include debugging code/commands to use.
```

**Output**: Root cause analysis and debugging strategy.

**Action**: Implement debugging and confirm root cause.

---

#### Step 3: Fix Implementation (30-60 minutes)

**Prompt**:
```
Implement fix for this bug:

ROOT CAUSE:
[Describe the identified cause]

CURRENT CODE:
[Paste buggy code]

REQUIREMENTS:
- Fix the bug
- Maintain backward compatibility (if needed)
- Follow existing code patterns
- Handle edge cases
- Add error handling

PROVIDE:

1. **Fixed Code**:
   - Complete implementation
   - Inline comments explaining fix
   - Any helper functions needed

2. **Migration/Compatibility**:
   - Impact on existing data/users
   - Migration steps if needed
   - Backward compatibility approach

3. **Verification**:
   - How to verify fix works
   - Manual testing steps
   - Automated test approach
```

**Output**: Fixed code with explanation.

**Validation**: Test fix locally with various scenarios.

---

#### Step 4: Test Case Creation (30 minutes)

**Prompt**:
```
Create tests for this bug fix:

BUG: [Description]
FIX: [What was changed]

GENERATE:

1. **Regression Test**:
   - Tests that bug doesn't reoccur
   - Uses exact reproduction steps
   - Clear assertion

2. **Related Edge Cases**:
   - Similar scenarios that might fail
   - Boundary conditions
   - Error cases

3. **Integration Tests**:
   - Tests in context of larger system
   - With real dependencies
   - End-to-end validation

FRAMEWORK: [Testing framework]

INCLUDE:
- Test setup
- Clear test names
- Meaningful assertions
- Cleanup
```

**Output**: Test suite preventing regression.

**Validation**: Verify tests fail with old code, pass with fix.

---

#### Step 5: Documentation (15 minutes)

**Prompt**:
```
Document this bug fix:

BUG: [Description]
ROOT CAUSE: [Explanation]
FIX: [Solution]

GENERATE:

## Commit Message
[Conventional commit format]
[Clear, descriptive summary]

## PR Description

### Bug Description
[What was wrong]

### Root Cause
[Technical explanation]

### Solution
[How it was fixed]

### Testing
- Manual testing steps
- Automated tests added
- Verification results

### Impact
- Who's affected
- Breaking changes (if any)
- Migration needed (if any)

### Screenshots/Logs
[Describe before/after to show]

## Changelog Entry
[User-facing description for release notes]

## Knowledge Base Article (if needed)
[Document for future reference]
- Symptoms
- Cause
- Solution
- Prevention
```

**Output**: Complete documentation for the fix.

---

**Workflow Complete!**

---

## Content Creation Workflows

### Workflow 3: Blog Post Creation Pipeline

**Goal**: Create, optimize, and publish a high-quality blog post.

**Duration**: 3-4 hours

---

#### Step 1: Topic Research and Outline (30 minutes)

**Prompt**:
```
Research and create blog post outline for: [TOPIC]

TARGET AUDIENCE: [Description]
GOAL: [Inform/persuade/educate]
LENGTH: [Word count]
SEO FOCUS: [Primary keyword]

GENERATE:

1. **Topic Analysis**:
   - Why this topic matters now
   - Audience pain points addressed
   - Unique angle/perspective

2. **Keyword Research**:
   - Primary keyword: [search volume, competition]
   - Secondary keywords (5-10)
   - LSI keywords (10-15)
   - Long-tail opportunities

3. **Competitive Analysis**:
   - Top 5 ranking articles
   - What they cover well
   - Content gaps to fill
   - Differentiation opportunities

4. **Detailed Outline**:

   **Title Options** (3 variations):
   1. [Title 1]
   2. [Title 2]
   3. [Title 3]

   **Introduction** (100 words):
   - Hook
   - Problem statement
   - Article promise

   **Section 1**: [Heading] (300 words)
   - Key points to cover
   - Examples needed
   - Data/statistics to include

   **Section 2**: [Heading] (300 words)
   [Same structure]

   [Continue for all sections]

   **Conclusion** (100 words):
   - Summary
   - Call-to-action

5. **Content Requirements**:
   - Images needed: [descriptions]
   - Examples to include: [list]
   - External sources to reference
   - Internal links to include
```

**Output**: Comprehensive outline with research.

---

#### Step 2: First Draft (1-2 hours)

**Prompt**:
```
Write the blog post based on this outline:

[Paste outline from Step 1]

WRITING GUIDELINES:
- Tone: [Professional/casual/technical]
- Reading level: [Grade level]
- Paragraph length: 2-4 sentences max
- Use active voice
- Include transition phrases
- Incorporate storytelling elements

FOR EACH SECTION:
- Lead with the main point
- Support with examples/data
- Use subheadings for scannability
- Include bullet points/lists
- Add relevant analogies
- End with clear takeaway

INCLUDE:
- Meta title (55-60 characters)
- Meta description (150-160 characters)
- Primary keyword in first 100 words
- Keywords distributed naturally
- Internal linking opportunities marked
- Image placement suggestions

Write in markdown format.
```

**Output**: Complete first draft.

**Review**: Read through for flow and completeness.

---

#### Step 3: Content Enhancement (30 minutes)

**Prompt**:
```
Enhance this blog post draft:

DRAFT:
[Paste first draft]

IMPROVEMENTS NEEDED:

1. **Readability**:
   - Simplify complex sentences
   - Break up long paragraphs
   - Add more subheadings
   - Improve transitions

2. **Engagement**:
   - Strengthen hooks
   - Add compelling examples
   - Include relevant statistics
   - Add expert quotes (suggest what quotes)
   - Incorporate questions for readers

3. **Visual Elements**:
   - Describe images/screenshots needed
   - Suggest infographic topics
   - Identify opportunities for charts/graphs
   - Pull quotes to highlight

4. **SEO Optimization**:
   - Verify keyword placement
   - Optimize heading hierarchy
   - Add schema markup suggestions
   - Improve internal linking

5. **Credibility**:
   - Add sources for claims
   - Include case studies
   - Reference research/studies
   - Add author expertise indicators

Maintain the core message and structure.
```

**Output**: Enhanced, more engaging version.

---

#### Step 4: SEO Optimization (20 minutes)

**Prompt**:
```
Perform SEO optimization on this article:

ARTICLE:
[Paste enhanced draft]

PRIMARY KEYWORD: [keyword]
SECONDARY KEYWORDS: [list]

OPTIMIZE:

1. **Title Tag**:
   - Current: [current title]
   - Optimized: [include keyword, under 60 chars, compelling]

2. **Meta Description**:
   - Current: [current description]
   - Optimized: [include keywords, 150-160 chars, CTA]

3. **URL Slug**:
   - Suggested: [keyword-rich, short, readable]

4. **Heading Structure**:
   - H1: [one only, with primary keyword]
   - H2s: [list with keywords where natural]
   - H3s: [list]

5. **Keyword Optimization**:
   - Primary keyword density: [target 1-2%]
   - Primary keyword placements: [first 100 words, H2, conclusion]
   - Secondary keywords: [naturally distributed]
   - LSI keywords: [incorporated]

6. **Image SEO**:
   - File names: [keyword-rich suggestions]
   - Alt text: [descriptions for each image]

7. **Internal Linking**:
   - Anchor texts: [contextual, keyword-rich]
   - Target pages: [relevant content to link]
   - Link placement: [where in content]

8. **Schema Markup**:
   - Article schema: [provide JSON-LD]
   - Other relevant schema: [FAQ, HowTo, etc.]

9. **Readability Score**:
   - Target: [Flesch reading ease 60+]
   - Improvements: [suggestions]

Provide optimized version with all changes.
```

**Output**: SEO-optimized article.

---

#### Step 5: Proofreading and Editing (30 minutes)

**Prompt**:
```
Proofread and edit this article:

ARTICLE:
[Paste SEO-optimized version]

CHECK FOR:

1. **Grammar and Spelling**:
   - Grammatical errors
   - Spelling mistakes
   - Punctuation issues
   - Capitalization

2. **Style and Consistency**:
   - Consistent tone
   - Consistent formatting
   - Consistent terminology
   - Style guide compliance

3. **Clarity**:
   - Ambiguous statements
   - Unclear references
   - Complex jargon
   - Missing context

4. **Factual Accuracy**:
   - Verify claims
   - Check statistics
   - Validate examples
   - Confirm technical details

5. **Flow and Structure**:
   - Logical progression
   - Smooth transitions
   - Proper pacing
   - Balanced sections

6. **Final Polish**:
   - Strengthen weak sentences
   - Improve word choice
   - Remove redundancy
   - Ensure active voice

Provide:
- List of issues found
- Corrected version
- Suggestions for improvement
```

**Output**: Polished, publication-ready article.

---

#### Step 6: Social Media Promotion (30 minutes)

**Prompt**:
```
Create social media promotion for this blog post:

ARTICLE TITLE: [title]
ARTICLE URL: [url]
KEY TAKEAWAYS:
- [Takeaway 1]
- [Takeaway 2]
- [Takeaway 3]

CREATE:

**Twitter/X Posts** (5 variations):
1. [Tweet 1: Hook with statistic]
2. [Tweet 2: Problem/solution angle]
3. [Tweet 3: Quote or key insight]
4. [Tweet 4: Question to audience]
5. [Tweet 5: Visual description + link]

**LinkedIn Post**:
- Length: 150-200 words
- Professional tone
- Value-driven hook
- Key insights
- Call-to-action
- Hashtags: [5 relevant]

**Facebook Post**:
- Length: 100-150 words
- Engaging question
- Relatable angle
- Link with preview
- Call-to-action

**Instagram Caption**:
- Length: 150 words
- Storytelling approach
- Emoji usage
- Link in bio reference
- Hashtags: [20-30 relevant]
- Carousel idea: [5 slides description]

**Email Newsletter**:
- Subject line (3 options)
- Preview text
- Email intro (50 words)
- Article summary
- CTA button text

INCLUDE:
- Best posting times
- Engagement tactics
- Response templates
```

**Output**: Complete social media promotion package.

---

**Workflow Complete!**

---

## Operations Workflows

### Workflow 4: Incident Response and Post-Mortem

**Goal**: Respond to, resolve, and learn from production incidents.

**Duration**: Varies (incident response) + 2 hours (post-mortem)

---

#### Step 1: Initial Incident Assessment (5 minutes)

**Prompt**:
```
Create initial incident assessment:

ALERT:
[Paste alert details]

OBSERVABLE SYMPTOMS:
[What's currently visible]

ASSESS:

1. **Severity Classification**:
   - Critical/High/Medium/Low
   - Criteria for classification

2. **Impact Analysis**:
   - Users affected: [estimate]
   - Services down: [list]
   - Business impact: [describe]

3. **Immediate Actions**:
   - Priority 1: [action]
   - Priority 2: [action]
   - Priority 3: [action]

4. **Team Assembly**:
   - Incident Commander: [who]
   - Technical Lead: [who]
   - Communications: [who]
   - Additional support: [who]

5. **Communication Plan**:
   - Stakeholders to notify
   - Status page update
   - Customer communication

6. **Investigation Strategy**:
   - Where to look first
   - What logs to check
   - What metrics to review

TIME-BOXED: Complete in 5 minutes maximum.
```

**Output**: Quick assessment with action plan.

**Action**: Execute immediate response actions.

---

#### Step 2: Root Cause Investigation (Varies)

(During incident response, use debugging prompts from bug workflow)

---

#### Step 3: Post-Mortem Report (1 hour)

**Prompt**:
```
Create post-mortem report for:

INCIDENT: [Title]

DETAILS:
- Start time: [timestamp]
- End time: [timestamp]
- Duration: [hours:minutes]
- Severity: [level]

TIMELINE:
[Paste detailed timeline]

ROOT CAUSE:
[Paste identified root cause]

GENERATE:

# Post-Mortem Report

## Executive Summary
[2-3 paragraphs for leadership]

## Incident Overview
- **Date**: [date]
- **Duration**: [time]
- **Severity**: [level]
- **Status**: Resolved

## Impact Analysis

### Quantitative Impact
- Users affected: [number/percentage]
- Requests failed: [number]
- Revenue impact: [if applicable]
- SLA breach: [yes/no, details]

### Qualitative Impact
- User experience: [description]
- Brand reputation: [assessment]
- Team morale: [impact]

## What Happened

### Timeline
[Detailed, minute-by-minute timeline]

### Detection
- How discovered: [method]
- Time to detect: [duration]
- Who detected: [person/system]

## Root Cause Analysis

### Immediate Cause
[What directly caused the incident]

### Contributing Factors
1. [Factor 1]
2. [Factor 2]
3. [Factor 3]

### Why It Wasn't Prevented
[Analysis of gaps]

## Resolution

### Immediate Mitigation
[What was done to stop the bleeding]

### Permanent Fix
[Long-term solution implemented]

### Verification
[How we confirmed it's fixed]

## What Went Well
- [Positive aspect 1]
- [Positive aspect 2]
- [Positive aspect 3]

## What Went Wrong
- [Issue 1]
- [Issue 2]
- [Issue 3]

## Lessons Learned
1. [Learning 1]
2. [Learning 2]
3. [Learning 3]

## Action Items

| Action | Type | Owner | Due Date | Priority | Status |
|--------|------|-------|----------|----------|--------|
| [Action 1] | [Prevent/Detect/Mitigate] | [Name] | [Date] | [P0/P1/P2] | [Status] |

### Prevention Actions
[Actions to prevent similar incidents]

### Detection Actions
[Actions to detect similar issues faster]

### Mitigation Actions
[Actions to reduce impact if it happens again]

## Supporting Information
- [Link to incident channel]
- [Link to metrics dashboard]
- [Link to relevant tickets]
- [Link to code changes]
```

**Output**: Comprehensive post-mortem report.

---

#### Step 4: Action Item Tracking (Ongoing)

**Prompt**:
```
Create action item tracking system for post-mortem:

POST-MORTEM ACTIONS:
[Paste action items from post-mortem]

GENERATE:

## Action Item Details

For each action item:

### [Action Item Name]

**Description**: [Detailed description]

**Rationale**: [Why this is important]

**Success Criteria**:
- [ ] [Criterion 1]
- [ ] [Criterion 2]

**Implementation Plan**:
1. [Step 1]
2. [Step 2]
3. [Step 3]

**Dependencies**:
- [Dependency 1]
- [Dependency 2]

**Risks**:
- [Risk 1]: [Mitigation]

**Effort Estimate**: [time]

**Progress Tracking**:
- [ ] Requirements defined
- [ ] Design approved
- [ ] Implementation started
- [ ] Testing completed
- [ ] Deployed
- [ ] Verified in production

**Status Updates**:
- [Date]: [Update]

## Weekly Check-in Template

**Completed This Week**:
- [Item 1]

**In Progress**:
- [Item 2]: [% complete]

**Blocked**:
- [Item 3]: [Blocker]

**Coming Next Week**:
- [Item 4]
```

**Output**: Detailed action items with tracking.

---

**Workflow Complete!**

---

## Cross-Functional Workflows

### Workflow 5: Product Launch Coordination

**Goal**: Coordinate a product launch across development, marketing, and operations.

**Duration**: 8-12 weeks

---

(Outline similar to previous workflows with phases for:
- Planning and requirements
- Development sprints
- Marketing content creation
- Beta testing coordination
- Launch preparation
- Go-live execution
- Post-launch monitoring)

---

## Workflow Best Practices

### 1. Start with Clear Goals

Before beginning any workflow:
- Define success criteria
- Identify deliverables
- Set time constraints
- Assign responsibilities

### 2. Use Checkpoints

After each major step:
- [ ] Validate output quality
- [ ] Verify against requirements
- [ ] Get necessary approvals
- [ ] Document decisions

### 3. Iterate and Improve

After completing a workflow:
- Document what worked well
- Note pain points
- Refine prompts
- Update workflow steps

### 4. Build Your Library

Create personal workflow variations:
- Save successful prompt sequences
- Adapt workflows to your context
- Combine steps for efficiency
- Share with team

### 5. Automate Where Possible

Look for automation opportunities:
- Scripted prompt sequences
- Template workflows
- Integration with tools
- Scheduled execution

## Related Resources

- [Examples](../../examples/README.md) - Individual use cases
- [Templates](../../templates/README.md) - Reusable prompts
- [Best Practices](../best-practices/README.md) - Prompt engineering
- [Techniques](../techniques/README.md) - Advanced patterns
- [Domain Guides](../automation/) - Specialized automation

---

**Start with a workflow!** Follow the steps, adapt to your needs, and streamline your work with AI automation.
