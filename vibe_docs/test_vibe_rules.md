# VIBE RULES VALIDATION SPEC

**Purpose**: LLM Judge validation criteria for vibe_rules.md
**Usage**: Input this spec to LLM judge to validate vibe_rules.md compliance

## VALIDATION ALGORITHM

### TEST 1: REQUIRED TEXT PATTERNS
**PASS CONDITIONS**: vibe_rules.md MUST contain these exact text patterns:

```
REQUIRED_PATTERNS = [
    '🎯VIBING...',
    'pwd && date',
    'vibe_docs/task_on_hand.md',
    'project_knowledge_base',
    'ALWAYS search web BEFORE',
    'CLI FIRST',
    'User preference ALWAYS overrides AI suggestions',
    'tmp_scripts/',
    'frequency ≥ 3',
    'success_rate',
    'Commit when user expresses satisfaction'
]
```

**JUDGE INSTRUCTION**: Return FAIL if ANY pattern is missing from vibe_rules.md

### TEST 2: REQUIRED SECTION STRUCTURE
**PASS CONDITIONS**: vibe_rules.md MUST contain these sections in order:

```
REQUIRED_SECTIONS = [
    '<immutable_instructions>',
    '<development_environment>',
    '<project_knowledge_base>',
    '<vibe_docs_metadata>'
]
```

**JUDGE INSTRUCTION**: Return FAIL if any section is missing or out of order

### TEST 3: STARTUP SEQUENCE VALIDATION
**PASS CONDITIONS**: immutable_instructions MUST contain 5-step startup sequence:

```
REQUIRED_STARTUP_STEPS = [
    'Print "🎯VIBING..."',
    'Execute "pwd && date"',
    'Load context from "vibe_docs/task_on_hand.md"',
    'Apply learned patterns from project_knowledge_base',
    'Make plan and continue work'
]
```

**JUDGE INSTRUCTION**: Return FAIL if startup sequence is incomplete or reordered

### TEST 4: LEARNING LOOP COMPLETENESS
**PASS CONDITIONS**: learning_loop MUST contain ALL elements:

```
REQUIRED_LEARNING_ELEMENTS = [
    'Track: time, success, mistakes, approach',
    'vibe_docs/',
    'project_knowledge_base',
    'IMMEDIATE:',
    'EXTRACT:',
    'PROMOTE:',
    'RETIRE:'
]
```

**JUDGE INSTRUCTION**: Return FAIL if any learning element is missing

### TEST 5: ERROR PROTOCOL VALIDATION
**PASS CONDITIONS**: error_protocol MUST contain 4-step process:

```
REQUIRED_ERROR_STEPS = [
    'Fix immediately',
    'Classify',
    'Pattern frequency ≥ 3',
    'Document solution'
]
```

**JUDGE INSTRUCTION**: Return FAIL if error protocol incomplete

### TEST 6: KNOWLEDGE SYSTEM CATEGORIES
**PASS CONDITIONS**: project_knowledge_base MUST contain these categories:

```
REQUIRED_KB_CATEGORIES = [
    'project_identity',
    'decision_memory',
    'learned_efficiencies',
    'workflow_patterns',
    'project_constraints'
]
```

**JUDGE INSTRUCTION**: Return FAIL if any category is missing

### TEST 7: VIBE_DOCS CORE FILES
**PASS CONDITIONS**: vibe_docs_metadata MUST reference these files:

```
REQUIRED_VIBE_FILES = [
    'task_on_hand.md',
    'project_context.md',
    'technical_details.md',
    'development_log.md',
    'troubleshooting.md'
]
```

**JUDGE INSTRUCTION**: Return FAIL if any core file is not referenced

### TEST 8: FORBIDDEN PATTERNS
**PASS CONDITIONS**: vibe_rules.md MUST NOT contain these anti-patterns:

```
FORBIDDEN_PATTERNS = [
    'section 2',
    'section 3',
    'environment_context',
    'current_state',
    'execution_knowledge'
]
```

**JUDGE INSTRUCTION**: Return FAIL if ANY forbidden pattern is found

### TEST 9: CRITICAL WORKFLOWS
**PASS CONDITIONS**: ALL workflows must be present and correctly ordered:

```
REQUIRED_WORKFLOWS = {
    'CLI_FIRST': ['CLI FIRST', 'before opening heavy tools'],
    'GIT_SATISFACTION': ['Commit when user expresses satisfaction', 'User satisfaction drives'],
    'WEB_SEARCH': ['ALWAYS search web BEFORE', 'new tasks or troubleshooting'],
    'DUAL_KNOWLEDGE': ['vibe_docs/', 'project_knowledge_base', 'specifics → patterns']
}
```

**JUDGE INSTRUCTION**: Return FAIL if any workflow is incomplete

## SCORING ALGORITHM

```
TOTAL_TESTS = 9
PASS_THRESHOLD = 9  # All tests must pass

IF passed_tests == TOTAL_TESTS:
    RETURN "COMPLIANT"
ELSE:
    RETURN "NON_COMPLIANT: Failed tests " + failed_test_numbers
```

## JUDGE OUTPUT FORMAT

```json
{
  "status": "COMPLIANT" | "NON_COMPLIANT",
  "passed_tests": [1,2,3,4,5,6,7,8,9],
  "failed_tests": [],
  "total_score": "9/9",
  "details": "All validation tests passed" | "Specific failure descriptions"
}
```

**Version**: v2.0 (algorithmic validation)
**Last Updated**: 2024-01-XX