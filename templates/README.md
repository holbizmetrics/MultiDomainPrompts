# Templates Library

> Ready-to-use prompt templates for rapid AI automation across domains

## Table of Contents

1. [Code Generation Templates](#code-generation-templates)
2. [Analysis Templates](#analysis-templates)
3. [Content Templates](#content-templates)
4. [Operations Templates](#operations-templates)
5. [Documentation Templates](#documentation-templates)
6. [How to Use Templates](#how-to-use-templates)

## Code Generation Templates

### Template: Function Generator

**Purpose**: Generate production-ready functions with tests and documentation.

```
Generate a [LANGUAGE] function that [PURPOSE].

SIGNATURE:
[function signature]

INPUTS:
- [param1]: [type] - [description]
- [param2]: [type] - [description]

OUTPUT:
- [return type] - [description]

REQUIREMENTS:
- Time complexity: [O notation]
- Space complexity: [O notation]
- Error handling: [specific errors]
- Edge cases: [list cases]

INCLUDE:
1. Implementation with clear comments
2. Docstring/documentation
3. Example usage
4. Unit tests (at least 5 test cases)
5. Type hints/annotations

CONSTRAINTS:
- [any limitations]
```

**Variables to Replace**:
- `[LANGUAGE]`: Programming language (Python, JavaScript, etc.)
- `[PURPOSE]`: What the function does
- `[function signature]`: Specific function signature
- `[param1/2]`: Parameter names and descriptions
- `[type]`: Data types
- `[O notation]`: Complexity requirements

---

### Template: API Endpoint Generator

**Purpose**: Generate complete REST API endpoints with validation and tests.

```
Create a [HTTP_METHOD] API endpoint for [RESOURCE].

ENDPOINT: [PATH]

PURPOSE: [What it does]

AUTHENTICATION: [Auth type]

REQUEST:
- Headers: [list]
- Path Parameters: [list with types]
- Query Parameters: [list with types]
- Body Schema:
  {
    [field definitions]
  }

RESPONSE:
- Success ([STATUS]): [schema]
- Errors: [error codes and formats]

VALIDATIONS:
- [validation rules]

INCLUDE:
1. Endpoint implementation
2. Request validation
3. Error handling
4. Database interactions
5. Unit tests
6. Integration tests
7. API documentation

FRAMEWORK: [Express/FastAPI/Flask/etc.]
DATABASE: [PostgreSQL/MongoDB/etc.]
```

---

### Template: Class/Module Generator

**Purpose**: Generate well-structured classes or modules with proper design patterns.

```
Generate a [LANGUAGE] [CLASS/MODULE] for [PURPOSE].

STRUCTURE:
- Name: [ClassName]
- Inherits: [base classes]
- Implements: [interfaces]

PROPERTIES:
- [property1]: [type] - [description]
- [property2]: [type] - [description]

METHODS:
- [method1]: [signature] - [purpose]
- [method2]: [signature] - [purpose]

DESIGN PATTERNS:
- [pattern name]: [how to apply]

REQUIREMENTS:
- [specific requirements]

INCLUDE:
1. Class/module implementation
2. Constructor with validation
3. All methods with documentation
4. Private helper methods (if needed)
5. Example usage
6. Unit tests
7. Type definitions/interfaces

Follow [LANGUAGE] best practices and conventions.
```

---

## Analysis Templates

### Template: Code Review

**Purpose**: Systematic code review for quality, security, and performance.

```
Review this code as a senior [LANGUAGE] engineer:

CODE:
[paste code]

REVIEW AREAS:
1. **Correctness**
   - Logic errors
   - Edge case handling
   - Type safety
   - Null/undefined handling

2. **Performance**
   - Time/space complexity
   - Inefficient operations
   - Memory leaks
   - Database query optimization

3. **Security**
   - Input validation
   - SQL injection risks
   - XSS vulnerabilities
   - Authentication/authorization
   - Sensitive data handling

4. **Maintainability**
   - Code clarity and readability
   - Function/method length
   - Code duplication
   - Design patterns usage
   - Documentation quality

5. **Best Practices**
   - Language idioms
   - Framework conventions
   - Error handling
   - Naming conventions
   - Testing coverage

FORMAT OUTPUT:
For each issue:
- **Severity**: [Critical/High/Medium/Low]
- **Category**: [Correctness/Performance/Security/Maintainability/Best Practices]
- **Line(s)**: [specific lines]
- **Issue**: [clear description]
- **Impact**: [what could go wrong]
- **Recommendation**: [how to fix]
- **Example**: [corrected code snippet]

Prioritize by severity. Include positive feedback for well-done aspects.
```

---

### Template: Performance Analysis

**Purpose**: Analyze code performance and identify optimization opportunities.

```
Analyze performance of this code:

CODE:
[paste code]

CONTEXT:
- Expected load: [requests/users/data volume]
- Current performance: [metrics]
- Performance targets: [targets]

ANALYZE:
1. **Time Complexity**
   - Current: [O notation]
   - Bottlenecks: [identify]
   - Potential improvements: [O notation]

2. **Space Complexity**
   - Current: [O notation]
   - Memory usage patterns
   - Optimization opportunities

3. **I/O Operations**
   - Database queries (N+1 problems?)
   - API calls
   - File operations
   - Caching opportunities

4. **Concurrency**
   - Parallelization opportunities
   - Thread safety issues
   - Resource contention

5. **Resource Usage**
   - CPU intensive operations
   - Memory allocations
   - Network bandwidth

PROVIDE:
1. **Quick Wins** (< 1 hour implementation)
   - Change
   - Expected improvement
   - Implementation

2. **Medium Improvements** (< 1 day)
   - Change
   - Expected improvement
   - Trade-offs

3. **Major Optimizations** (needs redesign)
   - Approach
   - Expected improvement
   - Effort required

Include benchmarking code and methodology.
```

---

### Template: Security Audit

**Purpose**: Comprehensive security review of code.

```
Perform a security audit on this code:

CODE:
[paste code]

CONTEXT:
- Application type: [web app/API/service]
- User data handled: [types]
- Compliance requirements: [GDPR/HIPAA/etc.]

CHECK FOR:
1. **Injection Vulnerabilities**
   - SQL injection
   - NoSQL injection
   - Command injection
   - LDAP injection

2. **Authentication & Authorization**
   - Weak authentication
   - Broken access control
   - Session management
   - JWT handling

3. **Data Exposure**
   - Sensitive data in logs
   - Information disclosure
   - Insecure data storage
   - Insufficient encryption

4. **Security Misconfiguration**
   - Default credentials
   - Unnecessary features enabled
   - Outdated dependencies
   - Missing security headers

5. **Input Validation**
   - Insufficient validation
   - Mass assignment
   - File upload issues

For each vulnerability:
- **Risk Level**: [Critical/High/Medium/Low]
- **Category**: [OWASP Top 10 reference]
- **Location**: [file:line]
- **Vulnerability**: [type and description]
- **Exploit Scenario**: [how it could be exploited]
- **Impact**: [potential damage]
- **Fix**: [specific mitigation]
- **Prevention**: [how to avoid in future]

Include security checklist for this code type.
```

---

## Content Templates

### Template: Blog Post Generator

**Purpose**: Create structured, SEO-optimized blog posts.

```
Write a blog post about [TOPIC].

SPECIFICATIONS:
- Length: [word count]
- Target audience: [description]
- Tone: [professional/casual/technical/etc.]
- SEO keywords: [list]
- Goal: [inform/persuade/educate/etc.]

STRUCTURE:
1. **Introduction** ([word count])
   - Hook: [attention-grabbing opening]
   - Problem statement: [reader's pain point]
   - Promise: [what they'll learn]

2. **Main Content** ([word count])
   - Section 1: [topic]
   - Section 2: [topic]
   - Section 3: [topic]
   [add more as needed]

3. **Conclusion** ([word count])
   - Summary: [key takeaways]
   - Call-to-action: [what to do next]

REQUIREMENTS:
- Include [number] subheadings (H2/H3)
- Add [number] examples or case studies
- Include [number] images (describe what to show)
- Use bullet points and lists for readability
- Add internal links to: [suggest topics]
- Include statistics or data: [specify]
- Add expert quotes (if applicable)

SEO OPTIMIZATION:
- Title tag: [under 60 characters]
- Meta description: [150-160 characters]
- Primary keyword in first paragraph
- Keyword density: 1-2%
- Use LSI keywords naturally

OUTPUT FORMAT: Markdown with proper formatting
```

---

### Template: Social Media Content

**Purpose**: Generate engaging social media content for multiple platforms.

```
Create social media content for [TOPIC/CAMPAIGN].

BRAND: [brand name]
VOICE: [description]
GOAL: [awareness/engagement/conversion]
TARGET AUDIENCE: [description]

PLATFORMS:
- [ ] LinkedIn
- [ ] Twitter/X
- [ ] Facebook
- [ ] Instagram

FOR EACH PLATFORM:

**LinkedIn Post**
- Length: 150-200 words
- Format: [thought leadership/case study/announcement]
- Include: [data/story/insight]
- Hashtags: 3-5 relevant
- Image suggestion: [description]
- Best posting time: [suggest]

**Twitter Thread**
- Tweets: 5-7
- Hook tweet: [attention-grabbing]
- Content tweets: [educational/entertaining]
- CTA tweet: [call-to-action]
- Hashtags: 1-2 per tweet
- Best posting time: [suggest]

**Facebook Post**
- Length: 100-150 words
- Format: [story/question/poll]
- Visual: [image/video description]
- Engagement tactics: [ask question/use emoji]
- Best posting time: [suggest]

**Instagram Post**
- Caption: 150-200 words
- Format: [storytelling/educational]
- Hashtags: 20-30 relevant
- Image description: [what to show]
- Story ideas: [3 slides]
- Best posting time: [suggest]

ENGAGEMENT STRATEGY:
- Response templates for common comments
- Cross-promotion approach
- Timing strategy
- Metrics to track
```

---

### Template: Email Campaign

**Purpose**: Create effective email campaigns for different goals.

```
Create an email for [PURPOSE].

CAMPAIGN: [campaign name]
AUDIENCE: [segment description]
GOAL: [conversion/engagement/information]

EMAIL SPECIFICATIONS:
- From: [sender name]
- Subject line options: [3 variations, max 50 chars each]
- Preheader text: [40-50 characters]

EMAIL BODY:

**Opening** (50 words)
- Personalization: [how to personalize]
- Hook: [attention-grabber]

**Value Proposition** (100-150 words)
- Main message: [what you're offering]
- Benefits: [3-5 bullet points]
- Social proof: [testimonial/statistic]

**Call-to-Action** (clear and prominent)
- Primary CTA: [button text]
- Secondary CTA: [alternative action]

**Closing** (50 words)
- Next steps
- Contact information
- Unsubscribe link

DESIGN NOTES:
- Layout: [single column/two column]
- Images: [descriptions]
- Color scheme: [brand colors]
- Mobile-friendly: yes

TESTING:
- A/B test variables: [subject/CTA/timing]
- Success metrics: [open rate/click rate/conversion]

OUTPUT: HTML email template with inline CSS
```

---

## Operations Templates

### Template: Incident Report

**Purpose**: Document incidents comprehensively for analysis and learning.

```
Create an incident report for:

INCIDENT DETAILS:
- Date/Time: [start - end]
- Duration: [hours/minutes]
- Severity: [Critical/High/Medium/Low]
- Status: [Resolved/Mitigated/Ongoing]
- Impact: [description]

AFFECTED SYSTEMS:
- [System 1]: [impact]
- [System 2]: [impact]

GENERATE:

## Executive Summary
[2-3 paragraphs summarizing incident and resolution]

## Impact Analysis
- **Users Affected**: [number/percentage]
- **Services Impacted**: [list]
- **Business Impact**: [quantify if possible]
- **Data Impact**: [any data loss/corruption]

## Timeline
[Detailed timeline with timestamps]
- [Time]: [Event description]
- [Time]: [Action taken]
- [Time]: [Result/observation]

## Root Cause Analysis
- **Immediate Cause**: [what directly caused the incident]
- **Contributing Factors**: [what made it possible/worse]
- **Detection Method**: [how was it discovered]
- **Why It Wasn't Prevented**: [gaps in prevention]

## Resolution Steps
1. **Immediate Mitigation**
   - [Actions taken]
   - [Results]

2. **Permanent Fix**
   - [Solution implemented]
   - [Verification]

## Prevention Measures
1. **Technical Improvements**
   - [Change 1]: [description]
   - [Change 2]: [description]

2. **Process Improvements**
   - [Change 1]: [description]
   - [Change 2]: [description]

3. **Monitoring Enhancements**
   - [Addition 1]: [description]
   - [Addition 2]: [description]

## Action Items
| Action | Owner | Due Date | Priority | Status |
|--------|-------|----------|----------|--------|
| [task] | [name] | [date] | [level] | [status] |

## Lessons Learned
- [Learning 1]
- [Learning 2]
- [Learning 3]

Format: Professional report suitable for stakeholders
```

---

### Template: Runbook/Procedure

**Purpose**: Create clear, actionable operational procedures.

```
Create a runbook for: [PROCEDURE NAME]

PURPOSE: [What this procedure accomplishes]

FREQUENCY: [How often executed]

PREREQUISITES:
- Access required: [systems/tools]
- Knowledge required: [skills]
- Tools needed: [software/scripts]

## Procedure Steps

**Step 1: [Step Name]**
- **Action**: [What to do]
- **Command/Code**: 
  ```
  [Actual command or code]
  ```
- **Expected Output**: [What you should see]
- **Duration**: [Approximate time]
- **If Something Goes Wrong**: [Troubleshooting]

**Step 2: [Step Name]**
[Same format as Step 1]

[Continue for all steps]

## Verification
- [ ] [Check 1]
- [ ] [Check 2]
- [ ] [Check 3]

## Rollback Procedure
In case of issues:
1. [Rollback step 1]
2. [Rollback step 2]
3. [Rollback step 3]

## Troubleshooting
**Issue**: [Common problem 1]
- **Symptoms**: [What you'll see]
- **Cause**: [Why it happens]
- **Solution**: [How to fix]

**Issue**: [Common problem 2]
[Same format]

## Success Criteria
- [Measurable outcome 1]
- [Measurable outcome 2]

## Contacts
- **Primary**: [Name/contact]
- **Escalation**: [Name/contact]
- **After Hours**: [Contact info]

## References
- [Related documentation]
- [Relevant tickets]
- [System diagrams]

Last Updated: [Date]
```

---

### Template: Status Report

**Purpose**: Generate regular status reports with consistent format.

```
Generate [WEEKLY/MONTHLY] status report for [TEAM/PROJECT].

REPORTING PERIOD: [Date range]

DATA:
[Paste relevant metrics and information]

GENERATE:

## Executive Summary
[2-3 paragraphs highlighting key points]

## Key Metrics
| Metric | Current | Previous | Change | Target |
|--------|---------|----------|--------|--------|
| [metric1] | [value] | [value] | [%] | [value] |
| [metric2] | [value] | [value] | [%] | [value] |

## Accomplishments
- ✅ [Achievement 1]: [Impact/details]
- ✅ [Achievement 2]: [Impact/details]
- ✅ [Achievement 3]: [Impact/details]

## In Progress
- 🔄 [Item 1]: [Status, % complete]
- 🔄 [Item 2]: [Status, % complete]

## Blockers & Risks
- 🚧 [Blocker 1]: [Impact, mitigation plan]
- ⚠️ [Risk 1]: [Probability, impact, mitigation]

## Incidents & Issues
- [Summary of any incidents]
- [Resolution status]
- [Prevention measures]

## Upcoming Priorities
1. [Priority 1]: [Expected completion]
2. [Priority 2]: [Expected completion]
3. [Priority 3]: [Expected completion]

## Resource Needs
- [Need 1]: [Why, when]
- [Need 2]: [Why, when]

## Recommendations
- [Recommendation 1]
- [Recommendation 2]

Format: Professional, suitable for leadership review
Include visual elements: ✅ ❌ 🔄 ⚠️ 📈 📉
```

---

## Documentation Templates

### Template: README Generator

**Purpose**: Create comprehensive README files for projects.

```
Generate a README.md for:

PROJECT: [Project name]
TYPE: [Application/Library/Tool/Service]
LANGUAGE/FRAMEWORK: [Technologies used]

INCLUDE:

# [Project Name]

> [One-line description]

[![License](badge-url)](link)
[![CI Status](badge-url)](link)
[Add relevant badges]

## Overview
[2-3 paragraphs explaining what, why, and how]

## Features
- ✨ [Feature 1]
- 🚀 [Feature 2]
- 🔒 [Feature 3]
[List key features]

## Quick Start

### Prerequisites
- [Requirement 1]
- [Requirement 2]

### Installation
```bash
[Installation commands]
```

### Basic Usage
```[language]
[Simple usage example]
```

## Documentation

### Configuration
[Environment variables, config files]

### API Reference
[Brief API overview or link to full docs]

### Examples
[Link to examples or include common use cases]

## Development

### Setup Development Environment
```bash
[Setup commands]
```

### Running Tests
```bash
[Test commands]
```

### Contributing
[Link to CONTRIBUTING.md or brief guidelines]

## Deployment
[Deployment instructions]

## Built With
- [Technology 1] - [Purpose]
- [Technology 2] - [Purpose]

## License
[License information]

## Support
- Documentation: [link]
- Issues: [link]
- Discussions: [link]

## Acknowledgments
[Credits, inspirations]

Ensure beginner-friendly, clear, and comprehensive.
```

---

### Template: API Documentation

**Purpose**: Document API endpoints comprehensively.

```
Generate API documentation for:

ENDPOINT: [METHOD] [PATH]

## [Endpoint Name]

**Description**: [What this endpoint does]

**Authentication**: [Requirements]

### Request

**HTTP Method**: [GET/POST/PUT/DELETE/PATCH]

**URL**: 
```
[BASE_URL][PATH]
```

**Headers**:
| Header | Type | Required | Description |
|--------|------|----------|-------------|
| [name] | [type] | [yes/no] | [description] |

**Path Parameters**:
| Parameter | Type | Description |
|-----------|------|-------------|
| [name] | [type] | [description] |

**Query Parameters**:
| Parameter | Type | Required | Default | Description |
|-----------|------|----------|---------|-------------|
| [name] | [type] | [yes/no] | [value] | [description] |

**Request Body**:
```json
{
  "field1": "type - description",
  "field2": {
    "nested": "type - description"
  }
}
```

### Response

**Success Response (200 OK)**:
```json
{
  [response schema]
}
```

**Error Responses**:

**400 Bad Request**:
```json
{
  "error": "Error message",
  "details": ["Validation errors"]
}
```

**401 Unauthorized**:
```json
{
  "error": "Authentication required"
}
```

[Include other relevant error codes]

### Examples

**cURL**:
```bash
curl -X [METHOD] \
  [URL] \
  -H "Authorization: Bearer TOKEN" \
  -H "Content-Type: application/json" \
  -d '[request body]'
```

**JavaScript (Fetch)**:
```javascript
[Fetch example]
```

**Python (Requests)**:
```python
[Requests example]
```

### Rate Limiting
[Rate limit information if applicable]

### Notes
- [Important note 1]
- [Important note 2]

### Related Endpoints
- [Link to related endpoint 1]
- [Link to related endpoint 2]
```

---

## How to Use Templates

### Step 1: Choose Your Template
Select the template that best matches your needs.

### Step 2: Fill in the Placeholders
Replace all `[PLACEHOLDERS]` with your specific information:
- `[LANGUAGE]` → "Python", "JavaScript", etc.
- `[PURPOSE]` → Your specific goal
- `[OTHER_VARS]` → Your context-specific details

### Step 3: Customize for Your Context
Adjust the template to fit your specific requirements:
- Add sections if needed
- Remove irrelevant parts
- Modify complexity level
- Adjust format preferences

### Step 4: Submit to AI
Copy the completed template and submit to your AI assistant.

### Step 5: Review and Refine
- Check the output
- Identify gaps or errors
- Refine the prompt if needed
- Re-submit with improvements

### Template Customization Guide

**Make Templates More Specific**:
```
BEFORE: Generate a function
AFTER: Generate a Python function that validates email addresses using regex
```

**Add Constraints**:
```
BEFORE: [no constraints]
AFTER: 
CONSTRAINTS:
- Maximum 50 lines of code
- No external libraries
- Must handle Unicode
```

**Provide Examples**:
```
BEFORE: [no examples]
AFTER:
EXAMPLE INPUT: "user@example.com"
EXAMPLE OUTPUT: true

EXAMPLE INPUT: "invalid-email"
EXAMPLE OUTPUT: false
```

### Template Variables Reference

Common placeholders used across templates:

- `[LANGUAGE]`: Programming language
- `[FRAMEWORK]`: Framework or library
- `[PURPOSE]`: What the code/content does
- `[TOPIC]`: Subject matter
- `[TYPE]`: Category or classification
- `[METHOD]`: HTTP method or approach
- `[PATH]`: URL path or file path
- `[DESCRIPTION]`: Detailed explanation
- `[AUDIENCE]`: Target readers/users
- `[GOAL]`: Desired outcome
- `[word count]`: Length specification
- `[date]`: Date or time period

### Combining Templates

You can combine multiple templates for complex tasks:

**Example: Complete Feature Development**
1. Use **Function Generator** for business logic
2. Use **API Endpoint Generator** for the API layer
3. Use **Documentation Template** for API docs
4. Use **Test Case Generator** for testing

### Best Practices

1. **Start Simple**: Use basic template, then enhance
2. **Be Specific**: More details = better results
3. **Iterate**: First output is rarely perfect
4. **Save Variations**: Build your personal library
5. **Document Success**: Note what works well

### Template Contributions

Create your own templates following this format:

```
### Template: [Template Name]

**Purpose**: [What it's for]

```
[Template content with [PLACEHOLDERS]]
```

**Variables to Replace**:
- `[VAR1]`: [Description]
- `[VAR2]`: [Description]
```

## Related Resources

- [Examples](../examples/README.md) - See templates in action
- [Best Practices](../docs/best-practices/README.md) - Prompt engineering principles
- [Techniques](../docs/techniques/README.md) - Advanced patterns
- [Workflows](../docs/workflows/README.md) - Step-by-step processes
- [Domain Guides](../docs/automation/) - Specialized guidance

---

**Start creating!** Pick a template, customize it for your needs, and generate high-quality AI outputs instantly.
