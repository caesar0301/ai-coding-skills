# Platonic Coding Skills

A professional collection of [Agent Skills](https://agentskills.io) for AI-powered Platonic Coding workflow.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Agent Skills Format](https://img.shields.io/badge/format-Agent%20Skills%201.0-blue)](https://agentskills.io)

## Overview

**Platonic Coding** is a coding style designed for complex projects and cross-team collaboration with AI agents. Instead of relying on prompts, vibes, or implicit assumptions, it treats specifications as abstract laws that define what can exist, what can change, and what must always hold. Agents operate inside a shared, closed spec world where meaning is explicit, violations are detectable, and evolution is traceable over time, making large systems reproducible, reviewable, and stable across teams, agents, and long development cycles.

![manifesto-infographic](./platonic-coding-manifesto.png)

See a full description in [PLATONIC_CODING_MANIFESTO.md](https://github.com/caesar0301/platonic-coding-skills/blob/main/PLATONIC_CODING_MANIFESTO.md).

## In Practice

### 🚀 Grism: Hypergraph Database in 3 Days

We built [**Grism**](https://github.com/mirasoth/Grism), an AI-native, neurosymbolic hypergraph database, from concept to *working prototype* in just **three days** using the Platonic Coding method.

Grism features:
- **Hypergraph-first architecture** with n-ary relations as the core primitive
- **Multi-layered engine** (Python API → Logical Plan → Optimizer → Storage)
- **Neurosymbolic integration** for combining symbolic reasoning with neural signals
- **Comprehensive RFC specifications** driving all design decisions

By defining the system's form through RFCs before writing code, agents operated within a closed, legally defined space. Every architectural decision was traceable, every component was spec-compliant, and the entire codebase remained coherent across rapid iteration cycles.

*This demonstrates that Platonic Coding doesn't slow you down, it accelerates complex system development by eliminating ambiguity and drift.*

## Available Skills

This repository provides production-ready Agent Skills that enhance Platonic Coding. All skills follow the [Agent Skills specification](https://agentskills.io/specification) for maximum compatibility across AI coding agents.

### 📋 platonic-code-specs

Manage RFC-style specifications with AI-driven operations.

**Capabilities:**
- Initialize new specification systems from templates
- Generate and maintain RFC history, index, and terminology files
- Validate consistency and cross-references
- Check taxonomy and standard compliance
- Comprehensive specification refinement

**Use when:** Managing technical specifications, RFCs, documentation standards, terminology systems

[**→ Full Documentation**](skills/platonic-code-specs/SKILL.md)

---

### 📐 platonic-impl-guide

Create concrete, project-specific implementation designs from RFC specifications.

**Capabilities:**
- Create implementation guides that translate RFC specs into implementation-ready designs
- Validate guides against RFCs for contradictions
- Update guides when RFCs change
- Language-aware and framework-aware technical architecture

**Use when:** Planning implementation of RFCs, creating detailed technical designs, documenting implementation architecture

[**→ Full Documentation**](skills/platonic-impl-guide/SKILL.md)

---

### ✅ platonic-code-review

Review code implementation against specifications for consistency validation.

**Capabilities:**
- Validate code matches RFC specifications and requirements
- Check feature completeness against specs
- Identify gaps (specs without code, code without specs)
- Find discrepancies where implementation differs from specs
- Generate detailed compliance reports (default: report-only, no code modification)

**Use when:** Validating implementation against specs, checking requirements compliance, ensuring spec-to-code consistency

[**→ Full Documentation**](skills/platonic-code-review/SKILL.md)

## Installation

### Method 1: Claude Code CLI Marketplace (Easiest)

If using Claude Code CLI with marketplace support:

```bash
# Add the skills marketplace
claude-code marketplace add caesar0301/platonic-coding-skills
```

### Method 2: Install using npx skills (Recommended for Most)

```bash
npx skills add caesar0301/platonic-coding-skills
```

### Method 3: Clone to Skills Directory

Clone this repository to your agent's skills directory:

```bash
git clone https://github.com/caesar0301/platonic-coding-skills.git ~/.claude/skills/platonic-coding-skills
```

## General Workflow

Platonic Coding follows a four-phase flow: **design specs → implementation guide → code → review**. Each phase uses one or more of the available skills.

| Phase | What you do | Skill(s) |
|-------|-------------|----------|
| **1. Create design specs** | Define requirements and architecture in RFCs. | platonic-code-specs |
| **2. Create implementation guide** | Turn RFCs into concrete, language- and framework-specific technical designs. | platonic-impl-guide |
| **3. AI agent writes code** | Implement the feature using the implementation guide (and RFCs) as the source of truth. | — |
| **4. Review code against spec** | Check that the implementation matches specs and the guide; fix gaps. | platonic-code-review |

This keeps meaning explicit, violations detectable, and evolution traceable. The **Examples** and **Practical Workflows** below show how to apply this flow with the available skills.

## Examples

Examples are ordered by the general workflow: specs → impl guide → code (manual) → review. Each shows a single skill in action.

### Example 1: Create design specs (Phase 1)

```
I'm starting a new project called "AI Assistant Platform".
Use the platonic-code-specs skill to initialize the
specification system in docs/specs/
```

**Result:** RFC specification system with standard, history, index, and namings files.

### Example 2: Create implementation guide (Phase 2)

```
Use the platonic-impl-guide skill to create an implementation guide for
RFC-001 (Authentication) targeting the auth module. Use TypeScript and
the existing Express patterns in this repo.
```

**Result:** Implementation guide with module structure, types, interfaces, and implementation details aligned with the RFC.

### Example 3: Implement from guide (Phase 3)

```
Implement the user authentication feature following docs/impl/rfc-001-auth-impl.md
and docs/specs/rfc-001-authentication.md. Do not deviate from the spec or the guide.
```

**Result:** Code that matches the implementation guide and the RFC (no separate skill; the agent uses the docs as source of truth).

### Example 4: Review code against spec (Phase 4)

```
Use the platonic-code-review skill to verify that src/auth/
correctly implements all requirements from docs/specs/rfc-001-authentication.md.
```

**Result:** Compliance report showing what is implemented, what is missing, and what is inconsistent.

### Example 5: Maintain specifications

```
Use the platonic-code-specs skill to refine all specifications in docs/specs/,
check consistency, and regenerate history, index, and namings.
```

**Result:** Validated specifications with updated history, index, and terminology files.

### Example 6: Gap analysis

```
Use the platonic-code-review skill to identify gaps between
all RFCs in docs/specs/ and the implementation in src/.
```

**Result:** Bi-directional analysis of unimplemented specs and undocumented code.

### Example 7: Validate implementation guide

```
Use the platonic-impl-guide skill to validate that docs/impl/rfc-001-auth-impl.md
does not contradict docs/specs/rfc-001-authentication.md.
```

**Result:** Validation report confirming the guide is spec-compliant or listing contradictions to fix.

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Author

**Xiaming Chen**
- Website: [https://xiaming.site/](https://xiaming.site/)
- GitHub: [@caesar0301](https://github.com/caesar0301)

---

*Built with ❤️ following the [Agent Skills](https://agentskills.io) standard*
