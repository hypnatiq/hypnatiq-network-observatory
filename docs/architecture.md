# Public Architecture Overview

## Product model

```text
Windows event sources
        |
        v
Local collection and normalization
        |
        v
Application identity + destination context + retained evidence
        |
        +--> Optional user-approved information sources
        +--> Windows-reported antivirus state
        +--> Current firewall policy view
        |
        v
Investigation record -> proposed response -> attended verification -> recovery
```

## Evidence layers

1. **Observed locally:** process identity, executable context, connection endpoints, timestamps, and Windows-reported state.
2. **Derived locally:** grouping, correlation, labels, and review suggestions.
3. **Optional online context:** results from a user-selected provider after disclosure of the data sent.
4. **Response state:** current firewall authority, proposed action, applied action, verification, and recovery record.

## Public repository boundary

The website describes the architecture and shows interface screenshots. Private implementation details, service code, provider credentials, signing material, and test captures remain outside this repository.
