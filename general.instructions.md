---
description: 'Universal coding principles and documentation standards for all projects'
applyTo: '**'
---

# General Development Guidelines

Universal principles for writing clean, maintainable code and documentation
across all projects and technologies.

## Core Principles

### Simplicity and Conciseness

- Prefer shorter alternatives that achieve the same result
- Remove unnecessary code, comments, and complexity
- Less is more - every line should serve a purpose

### Trust Tooling

- Rely on compilers, linters, and validators for correctness
- Use automated formatting tools instead of manual formatting
- Let tools catch errors rather than manual review

### YAGNI (You Aren't Gonna Need It)

- Remove code that isn't currently needed
- Don't implement features for hypothetical future requirements
- Keep the codebase lean and focused on current needs

### DRY (Don't Repeat Yourself)

- Refactor duplicated code into reusable functions or modules
- Extract common patterns into shared utilities
- Prefer composition over inheritance
- Prefer inheritance over copying code

## Code Examples

### Good Example - Simple and DRY

```python
def calculate_total(items):
    return sum(item.price for item in items)

def calculate_tax(total, rate=0.08):
    return total * rate
```

### Bad Example - Verbose and repetitive

```python
def calculate_total(items):
    total = 0
    for item in items:
        total = total + item.price
    return total

def calculate_order_total(items):
    total = 0
    for item in items:
        total = total + item.price
    return total
```

## Documentation Standards

### Plain Text Formatting

- Use plain ASCII characters in all documentation
- Avoid emojis, unicode symbols, and special characters
- Never use emdash (—) or endash (–); use hyphen (-) instead

### Line Length

- Wrap all lines at 80 characters maximum
- This includes comments, commit messages, and documentation
- Exception: URLs or code that cannot be reasonably wrapped

### Writing Style

- Write clear, concise sentences
- Use active voice
- Be direct and specific
- Avoid unnecessary words

## Commit Messages

- Use imperative mood: "Add feature" not "Added feature"
- Keep first line under 50 characters when possible
- Wrap body text at 80 characters
- Separate subject from body with blank line
- Use plain ASCII only

### Good Commit Message Example

```
Fix null pointer exception in user service

Check for null user before accessing properties. This prevents crashes
when the database returns no results for invalid user IDs.
```

### Bad Commit Message Example

```
fixed bug 🐛

added some checks for when user is null or whatever
```

## Comments

- Write comments that explain "why", not "what"
- Keep comments up to date with code changes
- Remove commented-out code; use version control instead
- Use plain ASCII in all comments
- Wrap at 80 characters

### Good Comment Example

```javascript
// Cache results for 5 minutes to reduce database load during peak hours
const CACHE_TTL = 300;
```

### Bad Comment Example

```javascript
// Set cache time to 300
const CACHE_TTL = 300; // this is the cache time
```
