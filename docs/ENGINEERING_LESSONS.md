# Selected Engineering Lessons

This page contains a few public-safe examples of problems found during AI-assisted development and how they were turned into reusable engineering rules.

## 1. Text inserted is not the same as message sent

A browser automation could place text into a composer but did not reliably complete submission.

The workflow was split into independently verifiable stages:

```text
composer found
→ text inserted
→ usable send control found
→ submit action
→ successful submission observed
```

**Lesson:** UI automation should verify the actual final state, not an intermediate visual state.

---

## 2. Model proposal is not trusted file provenance

An AI-generated file-change proposal contained a stale base hash.

Instead of weakening verification, the architecture was changed so that the model remains the proposal source while trusted file identity comes from verified project context.

**Lesson:** AI output can propose an action, but integrity/provenance should come from trusted application state.

---

## 3. A backend PASS did not prove the desktop runtime was healthy

Backend-oriented acceptance succeeded, but the normal desktop application still launched incorrectly.

The first hypothesis was rejected after reading the real build configuration. The problem came from using the wrong production build path for the everyday runtime.

**Lesson:** every test has an evidence boundary. A passing backend test proves the backend path tested, not the health of every product layer.

---

## 4. Generated automation exposed PowerShell 5.1 edge cases

AI-generated Windows automation encountered parser, quoting, parameter-binding and scalar/collection issues.

The workflow was improved with parser validation, exact input checks, explicit collection handling, fail-closed behavior and rollback.

**Lesson:** AI-generated automation must be validated in the exact target runtime, not only reviewed conceptually.

---

## 5. Attachment found is not the same as download verified

A UI automation found the correct attachment but clicked the file/preview surface instead of the real download control.

The success criteria became:

```text
attachment found
→ download control found
→ download observed
→ resulting file verified
```

**Lesson:** break UI actions into observable contracts and verify the physical result.

---

These examples are intentionally summarized and sanitized. Internal paths, credentials, private transport details and operational control artifacts are excluded from this portfolio repository.
