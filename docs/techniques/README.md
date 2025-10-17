# Reusable Prompt Techniques

> Battle-tested patterns and techniques applicable across domains

## Table of Contents

1. [Chain-of-Thought Techniques](#chain-of-thought-techniques)
2. [Few-Shot Learning](#few-shot-learning)
3. [Role-Based Prompting](#role-based-prompting)
4. [Template-Based Generation](#template-based-generation)
5. [Iterative Refinement](#iterative-refinement)
6. [Constraint-Driven Prompting](#constraint-driven-prompting)
7. [Multi-Step Reasoning](#multi-step-reasoning)
8. [Context Injection](#context-injection)

## Chain-of-Thought Techniques

### Basic Chain-of-Thought

Guide the AI through explicit reasoning steps:

```
Problem: [Describe problem]

Solve this step-by-step:
1. Identify the key components
2. Analyze each component
3. Determine relationships
4. Synthesize findings
5. Draw conclusions

Show your work for each step.
```

**When to Use:**
- Complex problem-solving
- Logical reasoning tasks
- Debugging and troubleshooting
- Decision-making scenarios

**Example Application:**

```
Analyze why our app's user engagement dropped 30% last month.

Step-by-step analysis:
1. Data examination: Review metrics (DAU, session length, feature usage)
2. Timeline correlation: Identify events coinciding with the drop
3. User segment analysis: Which cohorts were most affected?
4. Feature changes: What was released/modified?
5. External factors: Market changes, competitor actions
6. Root cause identification: Connect findings
7. Recommendation: Propose solutions based on analysis
```

### Structured Chain-of-Thought

```
[UNDERSTAND]
Restate the problem in your own words.

[ANALYZE]
Break down into sub-problems.

[SOLVE]
Address each sub-problem.

[VERIFY]
Check solution validity.

[CONCLUDE]
Present final answer with confidence level.
```

### Tree-of-Thought

Explore multiple reasoning paths:

```
Problem: [Describe]

Generate 3 different approaches:

Approach A: [Method 1]
- Steps: ...
- Pros: ...
- Cons: ...

Approach B: [Method 2]
- Steps: ...
- Pros: ...
- Cons: ...

Approach C: [Method 3]
- Steps: ...
- Pros: ...
- Cons: ...

Evaluate and recommend the best approach with rationale.
```

## Few-Shot Learning

### Basic Few-Shot Pattern

Provide examples to establish patterns:

```
Convert requirements to user stories using this format:

Example 1:
Input: Users need password reset
Output: As a user, I want to reset my password via email so that I can 
regain access to my account if I forget my credentials.

Example 2:
Input: Admins need usage reports
Output: As an admin, I want to generate monthly usage reports so that 
I can track system adoption and identify trends.

Example 3:
Input: Users need dark mode
Output: As a user, I want to enable dark mode so that I can reduce 
eye strain when using the app at night.

Now convert these:
1. [New requirement 1]
2. [New requirement 2]
3. [New requirement 3]
```

**When to Use:**
- Establishing specific formats
- Teaching style/tone
- Pattern recognition tasks
- Consistency requirements

### Progressive Examples

Build complexity gradually:

```
Write function docstrings following these examples:

Simple example:
def add(a, b):
    """Add two numbers and return the result."""
    return a + b

Moderate example:
def fetch_user(user_id, include_deleted=False):
    """
    Fetch user by ID from database.
    
    Args:
        user_id: Unique identifier for the user
        include_deleted: Whether to include soft-deleted users
        
    Returns:
        User object or None if not found
    """
    # implementation

Complex example:
def process_payment(amount, currency, payment_method, metadata=None):
    """
    Process a payment transaction.
    
    Args:
        amount: Payment amount in smallest currency unit (e.g., cents)
        currency: ISO 4217 currency code (e.g., 'USD', 'EUR')
        payment_method: Payment method identifier from payment provider
        metadata: Optional dict of additional transaction metadata
        
    Returns:
        Transaction object with status and reference ID
        
    Raises:
        PaymentError: If payment processing fails
        ValidationError: If input validation fails
        
    Example:
        >>> process_payment(1000, 'USD', 'card_123')
        Transaction(id='txn_456', status='succeeded')
    """
    # implementation

Now document these functions:
[Paste functions to document]
```

### Contrastive Examples

Show both good and bad examples:

```
Write error messages that are helpful and actionable.

❌ Bad:
"Error occurred"

✅ Good:
"Connection failed: Unable to reach database server at db.example.com:5432. 
Please check your network connection and verify the server is running."

❌ Bad:
"Invalid input"

✅ Good:
"Email format invalid: 'user@example' is missing a domain extension. 
Expected format: user@example.com"

Now improve these error messages:
1. [Current error message]
2. [Current error message]
```

## Role-Based Prompting

### Expert Role Assignment

```
[ROLE]
You are a [SPECIFIC EXPERT] with [X years] experience in [DOMAIN].

Your expertise includes:
- [Skill/area 1]
- [Skill/area 2]
- [Skill/area 3]

[CONTEXT]
[Provide relevant context]

[TASK]
[Specific task]

[APPROACH]
Apply your expert knowledge to provide [detailed/strategic/tactical] guidance.
```

**Example:**

```
[ROLE]
You are a senior database architect with 15 years of experience in 
high-traffic e-commerce systems.

Your expertise includes:
- Query optimization for millions of daily transactions
- Scaling PostgreSQL for global applications
- Data modeling for complex product catalogs

[CONTEXT]
Our e-commerce platform handles 50K orders/day with 2M SKUs. Current 
search queries take 3-5 seconds during peak traffic.

[TASK]
Design a solution to reduce search query latency to under 500ms.

[APPROACH]
Provide architectural recommendations with implementation priorities.
```

### Perspective Shifting

Get multiple viewpoints on the same issue:

```
Analyze [SITUATION] from three perspectives:

1. [ROLE 1] Perspective
   Focus: [What they care about]
   Analysis: ...
   Recommendation: ...

2. [ROLE 2] Perspective
   Focus: [What they care about]
   Analysis: ...
   Recommendation: ...

3. [ROLE 3] Perspective
   Focus: [What they care about]
   Analysis: ...
   Recommendation: ...

Synthesize: Find common ground and optimal path forward.
```

**Example:**

```
Our team is debating whether to rewrite our legacy system or refactor incrementally.

Analyze from three perspectives:

1. CTO Perspective
   Focus: Technical debt, scalability, risk
   
2. Product Manager Perspective
   Focus: Feature velocity, user impact, market timing
   
3. Engineering Manager Perspective
   Focus: Team capacity, skill development, delivery predictability

Synthesize findings and recommend an approach.
```

## Template-Based Generation

### Structural Templates

Define reusable structures:

```
Generate [OUTPUT] using this template:

# [Title]

## Overview
[2-3 sentence summary]

## Key Points
1. [Point 1]: [Details]
2. [Point 2]: [Details]
3. [Point 3]: [Details]

## Details
[Expanded explanation]

## Recommendations
- [Action 1]
- [Action 2]
- [Action 3]

## Next Steps
[Immediate actions]
```

### Variable-Based Templates

```
Create a [DOCUMENT TYPE] for:

VARIABLES:
- {{product_name}}: [value]
- {{target_audience}}: [value]
- {{key_benefit}}: [value]
- {{price_point}}: [value]

TEMPLATE:
Introducing {{product_name}} - the ultimate solution for {{target_audience}}.

{{key_benefit}} at just {{price_point}}.

[Continue with template structure...]
```

### Conditional Templates

```
Generate content based on conditions:

IF [condition A]:
  Use template A:
  [Template structure]
  
ELSE IF [condition B]:
  Use template B:
  [Template structure]
  
ELSE:
  Use default template:
  [Template structure]

INPUT:
[Provide input that determines condition]
```

## Iterative Refinement

### Feedback Loop Pattern

```
[INITIAL OUTPUT]
Generate: [Task description]

[EVALUATION]
Review the output for:
- [Criterion 1]
- [Criterion 2]
- [Criterion 3]

[REFINEMENT]
Based on evaluation, improve:
- [Aspect 1]
- [Aspect 2]

[FINAL OUTPUT]
Present the refined version.
```

### Progressive Enhancement

```
Version 1 (Basic):
[Generate minimal viable version]

Version 2 (Enhanced):
Improve Version 1 by adding:
- [Enhancement 1]
- [Enhancement 2]

Version 3 (Polished):
Refine Version 2 by:
- [Refinement 1]
- [Refinement 2]

Present all three versions for comparison.
```

### A/B/C Testing Pattern

```
Generate 3 variations optimized for different goals:

Variation A: Optimized for [GOAL A]
[Output]
Rationale: [Why this works for goal A]

Variation B: Optimized for [GOAL B]
[Output]
Rationale: [Why this works for goal B]

Variation C: Optimized for [GOAL C]
[Output]
Rationale: [Why this works for goal C]

Recommend best overall with trade-off analysis.
```

## Constraint-Driven Prompting

### Hard Constraints

```
Generate [OUTPUT] with these non-negotiable constraints:

MUST HAVE:
- [Constraint 1]
- [Constraint 2]
- [Constraint 3]

MUST NOT HAVE:
- [Anti-constraint 1]
- [Anti-constraint 2]

VALIDATION:
After generation, verify all constraints are met.
```

### Soft Constraints

```
Generate [OUTPUT] prioritizing these preferences:

HIGH PRIORITY:
- [Preference 1]
- [Preference 2]

MEDIUM PRIORITY:
- [Preference 3]
- [Preference 4]

NICE TO HAVE:
- [Preference 5]

Balance priorities based on trade-offs.
```

### Boundary Testing

```
Generate [OUTPUT] and test boundaries:

1. Minimum viable: Least that satisfies requirements
2. Optimal: Best balance of factors
3. Maximum: Push limits while maintaining quality

For each:
- Present the output
- Explain trade-offs
- Identify breaking points
```

## Multi-Step Reasoning

### Sequential Processing

```
Process this task in sequence:

STEP 1: [Subtask 1]
Input: [What you start with]
Process: [What to do]
Output: [What results]

STEP 2: [Subtask 2]
Input: [Output from Step 1]
Process: [What to do]
Output: [What results]

STEP 3: [Subtask 3]
Input: [Output from Step 2]
Process: [What to do]
Output: [Final result]

Execute each step, showing intermediate results.
```

### Parallel Processing

```
Analyze [SUBJECT] along multiple dimensions simultaneously:

DIMENSION 1: [Aspect 1]
[Analysis]

DIMENSION 2: [Aspect 2]
[Analysis]

DIMENSION 3: [Aspect 3]
[Analysis]

SYNTHESIS:
Combine findings from all dimensions.
```

### Recursive Decomposition

```
Solve [COMPLEX PROBLEM] by decomposition:

LEVEL 1: Break into major components
[Component A], [Component B], [Component C]

LEVEL 2: For each component, break into sub-components
Component A:
  - [Sub-component A1]
  - [Sub-component A2]
Component B:
  - [Sub-component B1]
  - [Sub-component B2]

LEVEL 3: Solve smallest units
[Detailed solutions]

INTEGRATION: Combine solutions bottom-up
```

## Context Injection

### Layered Context

```
[GLOBAL CONTEXT]
High-level information relevant to all tasks:
[Context that applies broadly]

[DOMAIN CONTEXT]
Specific domain knowledge:
[Domain-specific information]

[TASK CONTEXT]
Immediate task details:
[Specific task information]

[TASK]
[What to do with all this context]
```

### Just-In-Time Context

```
Main task: [Primary task]

When you encounter [SITUATION], apply this context:
[Situation-specific context]

When you encounter [DIFFERENT SITUATION], apply this context:
[Different situation-specific context]

Proceed with the main task, injecting context as needed.
```

### Context Prioritization

```
Consider these context layers in priority order:

P0 (Critical - Always consider):
[Must-know information]

P1 (Important - Usually consider):
[Should-know information]

P2 (Helpful - Consider if relevant):
[Nice-to-know information]

Task: [Task description]
```

## Combining Techniques

### Example 1: Chain-of-Thought + Few-Shot

```
Analyze user feedback using step-by-step reasoning.

Examples of analysis:

Feedback: "The app crashes when I upload photos"
Analysis:
1. Issue type: Technical - Stability
2. Severity: High (blocks core feature)
3. Affected feature: Photo upload
4. User impact: Cannot complete primary task
5. Priority: P0 - Fix immediately
6. Recommendation: Investigate crash logs, add error handling

Feedback: "Would be nice to have dark mode"
Analysis:
1. Issue type: Feature request - UI/UX
2. Severity: Low (enhancement)
3. Affected feature: Theme/appearance
4. User impact: Quality-of-life improvement
5. Priority: P2 - Backlog for future sprint
6. Recommendation: Gather more feedback, assess effort

Now analyze:
[New feedback items]
```

### Example 2: Role + Template + Constraints

```
[ROLE]
You are a technical documentation specialist.

[TEMPLATE]
Create API documentation following this structure:
- Endpoint
- Method
- Parameters
- Request body
- Response format
- Error codes
- Example

[CONSTRAINTS]
- Maximum 300 words per endpoint
- Include curl example
- Use JSON for examples
- Target audience: intermediate developers

[TASK]
Document these API endpoints:
[List endpoints]
```

### Example 3: Multi-Step + Iterative

```
PHASE 1: Initial draft
[Generate initial version]

PHASE 2: Expert review
[Apply expert role to review]

PHASE 3: Refinement
[Make improvements based on review]

PHASE 4: Validation
[Check against constraints and criteria]

Present the evolution through all phases.
```

## Technique Selection Guide

### By Task Type

**Analysis Tasks** → Chain-of-Thought, Multi-Step Reasoning

**Generation Tasks** → Template-Based, Few-Shot Learning

**Optimization Tasks** → Iterative Refinement, Constraint-Driven

**Complex Projects** → Combine Multiple Techniques

### By Output Requirements

**Need Consistency** → Templates, Few-Shot

**Need Depth** → Chain-of-Thought, Role-Based

**Need Variety** → Iterative Refinement, A/B Testing

**Need Precision** → Constraint-Driven, Validation

## Practice Exercises

### Exercise 1: Technique Identification

For each scenario, identify the best technique(s):

1. "Generate 10 social media posts with consistent brand voice"
   - Technique: ___________
   - Rationale: ___________

2. "Debug why this algorithm produces incorrect results"
   - Technique: ___________
   - Rationale: ___________

3. "Create a detailed project plan with dependencies"
   - Technique: ___________
   - Rationale: ___________

### Exercise 2: Technique Application

Take a basic prompt and enhance it using 3 different techniques:

Basic prompt: "Write a product description for a smartwatch"

Enhanced with Technique 1: ___________
Enhanced with Technique 2: ___________
Enhanced with Technique 3: ___________

Compare results.

### Exercise 3: Technique Combination

Combine 2-3 techniques to solve a complex task:

Task: "Create a comprehensive security audit report"

Techniques to combine:
1. ___________
2. ___________
3. ___________

Explain how they work together.

## Common Patterns Library

Save these patterns for quick reference:

1. **The Analyzer**: Chain-of-Thought + Role-Based
2. **The Generator**: Template-Based + Few-Shot
3. **The Optimizer**: Iterative + Constraint-Driven
4. **The Validator**: Multi-Step + Validation
5. **The Explorer**: Tree-of-Thought + Parallel Processing

## Resources

- [Best Practices Guide](../best-practices/README.md)
- [Meta-Prompts](../meta-prompts/README.md)
- [Templates Library](../../templates/README.md)
- [Examples](../../examples/README.md)

## Next Steps

1. **Practice**: Apply each technique to real tasks
2. **Experiment**: Combine techniques in new ways
3. **Document**: Record which combinations work best
4. **Share**: Contribute successful patterns
5. **Iterate**: Continuously refine your approach

---

**Remember**: These techniques are tools in your toolbox. The art is knowing which tool (or combination of tools) to use for each situation.
