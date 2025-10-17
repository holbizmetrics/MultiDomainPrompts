# Software Development Automation

> AI-powered automation for software development workflows

## Table of Contents

1. [Code Generation](#code-generation)
2. [Code Review & Analysis](#code-review--analysis)
3. [Testing Automation](#testing-automation)
4. [Documentation](#documentation)
5. [Debugging & Troubleshooting](#debugging--troubleshooting)
6. [Refactoring](#refactoring)
7. [API Design](#api-design)
8. [DevOps & CI/CD](#devops--cicd)

## Code Generation

### Boilerplate Generation

```
Generate a [FRAMEWORK] application with:

STRUCTURE:
- [Component 1]
- [Component 2]
- [Component 3]

REQUIREMENTS:
- Language: [Language/version]
- Framework: [Framework/version]
- Patterns: [Design patterns to use]
- Best practices: [Specific practices]

Include:
- Project structure
- Configuration files
- Basic implementations
- README with setup instructions
```

**Example: REST API Boilerplate**

```
Generate a Node.js REST API with Express:

STRUCTURE:
- User authentication (JWT)
- CRUD operations for resources
- Error handling middleware
- Request validation
- Database connection (PostgreSQL)

REQUIREMENTS:
- Language: Node.js 18+
- Framework: Express 4.x
- Patterns: MVC, Repository pattern
- Best practices: async/await, error handling, security headers

Include:
- /src/routes, /src/controllers, /src/models, /src/middleware
- .env.example
- package.json with scripts
- Basic auth and users endpoints
- README with API documentation
```

### Function Implementation

```
Implement a function that:

PURPOSE: [What it does]

SIGNATURE:
[Language-specific function signature]

INPUTS:
- [param1]: [type] - [description]
- [param2]: [type] - [description]

OUTPUT:
- [return type] - [description]

REQUIREMENTS:
- Time complexity: [O notation]
- Space complexity: [O notation]
- Error handling: [specific errors to handle]
- Edge cases: [list edge cases]

Include:
- Implementation with clear comments
- Docstring/JSDoc
- Example usage
- Unit tests
```

**Example:**

```
Implement a function that merges overlapping time intervals.

SIGNATURE:
Python: def merge_intervals(intervals: List[Tuple[int, int]]) -> List[Tuple[int, int]]

INPUTS:
- intervals: List of (start, end) tuples representing time intervals

OUTPUT:
- List of merged intervals with no overlaps

REQUIREMENTS:
- Time complexity: O(n log n)
- Space complexity: O(n)
- Error handling: Empty list, invalid intervals
- Edge cases: Single interval, no overlaps, complete overlaps

Include:
- Implementation with comments
- Docstring
- Example: [[1,3], [2,6], [8,10]] → [[1,6], [8,10]]
- 5 unit tests covering edge cases
```

### Algorithm Implementation

```
Implement [ALGORITHM] for [USE CASE].

CONTEXT:
[Why this algorithm, what problem it solves]

REQUIREMENTS:
- Input format: [description]
- Output format: [description]
- Constraints: [size limits, value ranges]
- Performance: [time/space requirements]

DELIVERABLES:
1. Algorithm explanation in plain English
2. Pseudocode
3. Production-ready implementation
4. Complexity analysis
5. Test cases with expected outputs
```

## Code Review & Analysis

### Comprehensive Code Review

```
Review this code as a senior [LANGUAGE] developer:

CODE:
[Paste code]

REVIEW AREAS:
1. Correctness
   - Logic errors
   - Edge case handling
   - Type safety

2. Performance
   - Time/space complexity
   - Optimization opportunities
   - Bottlenecks

3. Security
   - Vulnerabilities
   - Input validation
   - Authentication/authorization

4. Maintainability
   - Code clarity
   - Documentation
   - Design patterns
   - DRY principle

5. Best Practices
   - Language idioms
   - Error handling
   - Naming conventions

FORMAT OUTPUT:
For each issue:
- **Severity**: [Critical/High/Medium/Low]
- **Line(s)**: [Line numbers]
- **Issue**: [Description]
- **Recommendation**: [How to fix]
- **Example**: [Code snippet if helpful]

Prioritize by severity.
```

### Security Audit

```
Perform a security audit on this code:

CODE:
[Paste code]

CHECK FOR:
- SQL injection vulnerabilities
- XSS attack vectors
- CSRF vulnerabilities
- Authentication weaknesses
- Authorization flaws
- Sensitive data exposure
- Insecure dependencies
- Hardcoded secrets
- Improper error handling

For each vulnerability:
- **Risk Level**: [Critical/High/Medium/Low]
- **Location**: [File:line]
- **Vulnerability**: [Type and description]
- **Exploit Scenario**: [How it could be exploited]
- **Fix**: [Specific mitigation]
- **Prevention**: [How to avoid in future]
```

### Performance Analysis

```
Analyze performance of this code:

CODE:
[Paste code]

ANALYZE:
1. Time Complexity
   - Current: [O notation]
   - Bottlenecks: [Identify]
   - Optimization potential: [O notation]

2. Space Complexity
   - Current: [O notation]
   - Memory usage patterns
   - Optimization opportunities

3. I/O Operations
   - Database queries (N+1 problems?)
   - API calls
   - File operations

4. Concurrency
   - Thread safety
   - Race conditions
   - Deadlock potential

RECOMMENDATIONS:
- Quick wins (< 1 hour implementation)
- Medium improvements (1 day)
- Major optimizations (needs redesign)

Include benchmarking approach.
```

## Testing Automation

### Test Case Generation

```
Generate comprehensive test cases for:

FUNCTION/MODULE:
[Description or code]

TEST CATEGORIES:
1. Happy Path
   - Normal inputs
   - Expected outputs

2. Edge Cases
   - Boundary values
   - Empty inputs
   - Maximum sizes

3. Error Cases
   - Invalid inputs
   - Null/undefined
   - Type mismatches

4. Integration
   - Dependencies
   - Side effects
   - State changes

FORMAT:
For each test:
- Test name
- Setup/preconditions
- Input
- Expected output
- Assertions
- Cleanup (if needed)

Include actual test code in [FRAMEWORK].
```

**Example:**

```
Generate test cases for a user registration function:

FUNCTION:
async registerUser(email, password, username) {
  // Validates input, hashes password, creates user in DB
  // Returns user object or throws error
}

FRAMEWORK: Jest

GENERATE:
- 3 happy path tests
- 5 edge case tests
- 8 error case tests
- 2 integration tests

Include:
- Mock database
- Mock email service
- Test data factories
```

### Test Data Generation

```
Generate realistic test data for:

ENTITY: [Entity name/type]

SCHEMA:
[Describe fields and types]

REQUIREMENTS:
- Count: [Number of records]
- Variety: [Data diversity requirements]
- Constraints: [Validation rules to follow]
- Relationships: [Foreign keys, references]

FORMAT: [JSON/SQL/CSV/Code]

Include:
- Valid records (80%)
- Edge case records (15%)
- Invalid records for negative testing (5%)
```

### End-to-End Test Scripts

```
Create E2E test script for:

USER FLOW:
[Describe the user journey]

STEPS:
1. [Step 1]
2. [Step 2]
3. [Step 3]

FRAMEWORK: [Cypress/Playwright/Selenium]

INCLUDE:
- Setup and teardown
- Page object models (if applicable)
- Assertions at each step
- Error handling
- Screenshots on failure
- Data cleanup
```

## Documentation

### Code Documentation

```
Generate documentation for this code:

CODE:
[Paste code]

INCLUDE:
1. Overview
   - Purpose
   - High-level functionality

2. Function/Method Documentation
   - Description
   - Parameters with types
   - Return value
   - Exceptions/errors
   - Examples
   - Complexity (if relevant)

3. Usage Examples
   - Basic usage
   - Advanced usage
   - Common patterns

4. Edge Cases & Gotchas
   - Known limitations
   - Common mistakes
   - Best practices

FORMAT: [JSDoc/Docstring/XML comments/Markdown]
```

### API Documentation

```
Generate API documentation for:

ENDPOINT: [HTTP method] [path]

INCLUDE:

**Description**
[What this endpoint does]

**Authentication**
[Auth requirements]

**Request**
- Headers: [Required headers]
- Path Parameters: [Parameters in URL]
- Query Parameters: [Optional/required query params]
- Request Body: [JSON schema]

**Response**
- Success (200): [Response schema]
- Created (201): [Response schema if applicable]
- Error (4xx/5xx): [Error format]

**Examples**
- cURL example
- JavaScript/Python example
- Response examples

**Rate Limiting**
[If applicable]

**Changelog**
[Version history]
```

### README Generation

```
Generate a comprehensive README.md for:

PROJECT: [Project name and brief description]

INCLUDE:

# [Project Name]

## Overview
[2-3 paragraphs]

## Features
[Bullet list of key features]

## Installation
[Step-by-step setup]

## Usage
[Basic examples]

## Configuration
[Environment variables, config files]

## API Reference
[Link or brief overview]

## Development
[How to contribute, local development setup]

## Testing
[How to run tests]

## Deployment
[Deployment instructions]

## License
[License information]

## Support
[How to get help]

Ensure clear, concise, and beginner-friendly.
```

## Debugging & Troubleshooting

### Error Analysis

```
Analyze this error and provide solution:

ERROR MESSAGE:
[Paste error message/stack trace]

CONTEXT:
- Language/Framework: [specify]
- What I was trying to do: [description]
- What happened: [actual behavior]
- Environment: [dev/staging/production]

PROVIDE:
1. Error Explanation
   - What the error means
   - Root cause

2. Solution
   - Step-by-step fix
   - Code changes needed

3. Prevention
   - How to avoid in future
   - Best practices

4. Related Issues
   - Similar errors to watch for
```

### Debugging Assistant

```
Help me debug this issue:

PROBLEM:
[Describe the issue]

CODE:
[Relevant code]

EXPECTED BEHAVIOR:
[What should happen]

ACTUAL BEHAVIOR:
[What actually happens]

WHAT I'VE TRIED:
[Attempted solutions]

PROVIDE:
1. Hypothesis
   - Likely causes ranked by probability

2. Debugging Strategy
   - Steps to isolate the issue
   - What to check/log

3. Potential Fixes
   - Multiple approaches
   - Trade-offs of each

4. Long-term Solution
   - Prevent recurrence
   - Improve debugging for similar issues
```

### Performance Debugging

```
Help diagnose performance issues:

SYMPTOM:
[Describe the slow behavior]

METRICS:
- Current: [response time/throughput/etc.]
- Expected: [target metrics]
- Environment: [specs]

CONTEXT:
- Code: [relevant code]
- Architecture: [system design]
- Load: [current load patterns]

ANALYZE:
1. Profiling approach
2. Likely bottlenecks
3. Quick wins
4. Long-term optimizations

Provide monitoring/profiling code.
```

## Refactoring

### Code Refactoring

```
Refactor this code to improve [GOAL]:

CODE:
[Paste code]

GOAL: [Readability/Performance/Maintainability/Testability]

CONSTRAINTS:
- Maintain exact same functionality
- Preserve public API
- [Other constraints]

PROVIDE:
1. Analysis
   - Current issues
   - Improvement opportunities

2. Refactored Code
   - With explanatory comments

3. Changes Summary
   - What changed and why
   - Impact assessment

4. Testing Strategy
   - How to verify correctness
```

### Design Pattern Application

```
Refactor this code to use [PATTERN]:

CURRENT CODE:
[Paste code]

PATTERN: [e.g., Strategy, Factory, Observer]

CONTEXT:
[Why this pattern is appropriate]

PROVIDE:
1. Pattern Explanation
   - How it applies here
   - Benefits

2. Refactored Implementation
   - Class structure
   - Relationships
   - Code

3. Usage Examples
   - Before/after comparison
   - How it simplifies usage

4. Trade-offs
   - Added complexity vs benefits
```

### Legacy Code Modernization

```
Modernize this legacy code:

LEGACY CODE:
[Paste old code]

CURRENT STACK:
- Language: [version]
- Framework: [version]
- Patterns: [current patterns]

TARGET STACK:
- Language: [new version]
- Framework: [new version]
- Patterns: [modern patterns]

REQUIREMENTS:
- Phased migration (if large)
- Backward compatibility (if needed)
- Test coverage

PROVIDE:
1. Migration Plan
2. Modernized Code
3. Migration Scripts (if applicable)
4. Risk Assessment
```

## API Design

### RESTful API Design

```
Design a RESTful API for [DOMAIN]:

ENTITIES:
- [Entity 1]: [Description]
- [Entity 2]: [Description]

OPERATIONS:
[List required operations]

DESIGN:
1. Resource URLs
   - [Resource paths]
   - [Nesting structure]

2. HTTP Methods
   - GET: [endpoints]
   - POST: [endpoints]
   - PUT/PATCH: [endpoints]
   - DELETE: [endpoints]

3. Request/Response Formats
   - [JSON schemas]

4. Status Codes
   - Success: [codes used]
   - Error: [codes and meanings]

5. Authentication
   - [Auth approach]

6. Versioning
   - [Strategy]

7. Rate Limiting
   - [Limits and headers]

Include OpenAPI specification.
```

### GraphQL Schema Design

```
Design a GraphQL schema for [DOMAIN]:

REQUIREMENTS:
[Describe data and operations]

PROVIDE:
1. Type Definitions
   - Types
   - Queries
   - Mutations
   - Subscriptions (if applicable)

2. Resolvers Structure
   - [Resolver organization]

3. Authentication/Authorization
   - [Directive or approach]

4. Pagination
   - [Strategy]

5. Error Handling
   - [Error format]

6. Examples
   - Common queries
   - Mutations

Include schema.graphql file.
```

## DevOps & CI/CD

### CI/CD Pipeline Configuration

```
Create a CI/CD pipeline for:

PROJECT: [Project type]
STACK: [Technologies]

STAGES:
1. Build
   - [Build steps]
2. Test
   - [Test types]
3. Security Scan
   - [Checks]
4. Deploy
   - [Environments]

PLATFORM: [GitHub Actions/GitLab CI/Jenkins/CircleCI]

REQUIREMENTS:
- Environment variables
- Secrets management
- Deployment strategy (blue/green/canary)
- Rollback capability

PROVIDE:
- Complete pipeline configuration
- Setup instructions
- Best practices implemented
```

### Docker Configuration

```
Create Docker setup for:

APPLICATION: [Description]
STACK: [Technologies]

REQUIREMENTS:
- Multi-stage build
- Production-ready
- Security best practices
- Minimal image size

PROVIDE:
1. Dockerfile
   - Optimized layers
   - Security scanning

2. docker-compose.yml
   - All services
   - Networks
   - Volumes

3. .dockerignore
   - Optimized for build

4. Documentation
   - Build instructions
   - Run instructions
   - Environment variables
```

### Infrastructure as Code

```
Create [TERRAFORM/CLOUDFORMATION] for:

INFRASTRUCTURE:
[Describe required infrastructure]

REQUIREMENTS:
- [Cloud provider]
- [Regions]
- [Scalability needs]
- [Security requirements]

PROVIDE:
1. Main configuration
2. Variables file
3. Outputs
4. Modules (if complex)
5. Documentation
6. Cost estimation
```

## Advanced Automation Examples

### Code Generation from Specifications

```
Generate complete implementation from this specification:

SPECIFICATION:
[Formal or informal spec]

GENERATE:
1. Data models/entities
2. Business logic
3. API endpoints
4. Database migrations
5. Tests (unit + integration)
6. Documentation

STACK: [Specify technologies]

Ensure production-ready code with error handling and validation.
```

### Automated Refactoring Suggestions

```
Analyze this codebase and suggest refactorings:

CODEBASE STRUCTURE:
[Describe structure]

FOCUS AREAS:
- Code duplication
- Complex functions
- Tight coupling
- Missing abstractions
- Performance bottlenecks

PROVIDE:
1. Issues List (prioritized)
2. Refactoring Recommendations
3. Impact Analysis
4. Implementation Effort Estimates
5. Sample refactored code for top 3 issues
```

## Best Practices

1. **Always provide context**: Include language, framework, constraints
2. **Specify quality criteria**: Performance, security, maintainability
3. **Request complete solutions**: Working code, tests, documentation
4. **Ask for explanations**: Understand why, not just what
5. **Iterate and refine**: Start simple, add complexity progressively

## Resources

- [General Best Practices](../../best-practices/README.md)
- [Reusable Techniques](../../techniques/README.md)
- [Templates Library](../../../templates/README.md)
- [Examples](../../../examples/README.md)

---

**Next**: Explore [Content Creation Automation](../content-creation/README.md) or [Operations Workflows](../operations/README.md)
