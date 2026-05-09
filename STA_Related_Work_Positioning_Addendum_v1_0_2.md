# STA Related Work and Positioning Addendum v1.0.2
## Mapping Runtime Safety, Governance, and Control Literature to Signal-Time-Authority

Author: Htet Ko Ko Naing
Status: Separate positioning addendum / literature map
Date: 2026-05-09
License: CC BY 4.0

## ABSTRACT

This addendum positions the Signal-Time-Authority (STA) framework among adjacent work on runtime assurance, physical AI safety, unmanned system safety, action mediation, behavioral contracts, coordination transparency, multi-agent governance, operational technology security, and embodied AI policy.

The purpose of this note is not to revise or expand the frozen STA Paper 1-5 core series. Instead, it clarifies how existing and emerging literatures relate to STA's central pre-commitment controllability claim:

    Runtime oversight becomes control-relevant only when usable Signal, remaining actionable Time,
    effective Authority, and valid Policy are jointly available before a declared commitment event.

This addendum should be read as a related-work and positioning document. It does not claim that the cited works prove STA. It does not claim that STA invented runtime assurance, ethical governors, control barrier functions, behavioral contracts, coordination transparency, or embodied-AI governance from scratch. STA's distinct contribution is the organization of these mechanisms under a Signal-Time-Authority-Policy pre-commitment controllability condition.

## PATCH NOTE FOR v1.0.2

This patch does not change the substantive claim. It only cleans Markdown rendering so ordinary numbered lists are not displayed as section headings on GitHub.

## SCOPE NOTE

This addendum is a non-exhaustive related-work positioning map. It highlights adjacent works that help locate STA within runtime assurance, action mediation, physical AI safety, multi-agent governance, operational technology security, and embodied-AI policy. It is not a systematic literature review.

## CITATION CAUTION

Some web-archive or MHT materials are included as title-level related-work candidates. They should be fully verified against the original public source before being used as formal references.

## 1. PURPOSE OF THIS ADDENDUM

The completed STA PublicRelease series already presents the core theory, simulation support, runtime architecture, physical-AI extension, and governance/assurance framing. Since that release, several adjacent works and uploaded references have been identified that are strongly relevant to the STA problem space.

This note serves five purposes:

1. To clarify that STA is not isolated from existing research.
2. To prevent overclaim by distinguishing prior mechanisms from STA's synthesis.
3. To map related works into the Signal-Time-Authority-Policy lens.
4. To support future discussion, feedback, and reviewer communication.
5. To keep the frozen STA Paper 1-5 core unchanged while creating a separate literature-positioning record.

## 2. STATUS AND BOUNDARY

This document is separate from the frozen STA Paper 1-5 PublicRelease core series.

It is not Paper 6.
It is not a replacement for the STA-CCA future extension note.
It is not the STA-CCA C++17 simulation companion.
It is not an empirical validation paper.
It is not a proof of AI safety.

It is a positioning addendum and literature map.

Recommended boundary statement:

    STA does not claim to invent runtime monitoring, runtime assurance, behavioral contracts,
    ethical governors, control barrier functions, STPA monitoring, coordination transparency,
    action mediation, OT security, or embodied-AI governance from scratch.

    STA's contribution is to connect these mechanisms through a Signal-Time-Authority-Policy
    pre-commitment controllability condition: oversight becomes control-relevant only when
    usable signal, remaining actionable time, effective authority, and valid policy remain jointly
    available before a declared commitment event.

## 3. CORE STA POSITION

STA asks a narrow but general control-feasibility question:

    Given an AI or autonomous system trajectory approaching an externally consequential
    commitment event, can the oversight layer still do anything useful before commitment?

STA answers this through four joint dimensions:

    Signal:
        Is there a usable, timely, sufficiently reliable indication of risk, hazard, misalignment,
        policy violation, drift, coordination failure, or unsafe commitment?

    Time:
        Is there enough remaining actionable time before the commitment becomes externally
        consequential, irreversible, physically harmful, legally binding, operationally unsafe,
        or difficult to reverse?

    Authority:
        Does the oversight mechanism have effective non-bypassable authority to halt, gate,
        modify, defer, throttle, rollback, sandbox, fallback, safe-stop, escalate, or deny the action?

    Policy:
        Is there a valid, pre-registered, domain-appropriate intervention policy that specifies
        when and how the authority should be used?

STA therefore does not treat monitoring as automatically equivalent to control. A monitor may observe a hazard, but if it lacks time, authority, or policy, the monitor may only support audit, explanation, diagnosis, or post-hoc review.

## 3A. RELATED WORK CONFIDENCE TIERS

This addendum separates related works by confidence and relevance. The purpose is to avoid treating all adjacent materials as equally central to STA.

Strong / directly relevant:
    Runtime assurance, STPA-driven runtime monitoring, AARM, Agent Behavioral Contracts,
    AISAC, UxS safety precepts, NIST OT security, ASIMOV physical safety benchmarking,
    STPA-Coordination, TRiSM for Agentic AI, and related action-gate or runtime-governance work.

Medium / neighboring:
    Agentic architecture reliability surveys, coordination transparency, embodied-AI policy,
    catastrophic AI risk surveys, ethical-governor work, and control-barrier-function safety-filter work.

Background / contextual:
    General multi-agent teaching notes, general agent architecture summaries, and web-archive
    articles that provide useful vocabulary but should not be treated as primary evidence unless
    verified and cited from their original source.

Use rule:
    Strong works may be used as direct related work for STA positioning.
    Medium works may be used as neighboring literature or context.
    Background works should be used only for orientation, terminology, or non-formal notes.

## 4. RELATED WORK CLUSTERS

### 4.1 Runtime Assurance, Safe Fallback, and Runtime Monitoring

Representative works and files:
- AFRL Runtime Assurance Framework Development for Highly Adaptive Flight Control Systems.
- STPA-driven Multilevel Runtime Monitoring for In-time Hazard Detection.
- Control Barrier Function / VISTA F-16 safety guardrails.
- Runtime verification and monitor-driven safety assurance.

Relation to STA:

    Signal:
        Runtime monitors, hazard detectors, state estimators, unsafe-control-action indicators,
        control barrier margins, causal-factor monitors.

    Time:
        In-time hazard detection, pre-violation warning, time-to-impact, recovery window,
        monitor reaction time.

    Authority:
        RTA switch, reversionary trusted controller, Simplex-style fallback, safety filter,
        command modification, safe-mode transition.

    Policy:
        Monitor specification, safety invariant, hazard constraint, switching condition,
        assume-guarantee contract, STPA-derived safety requirement.

STA positioning:

    Runtime assurance mechanisms are concrete ways to implement control authority.
    STA adds the explicit condition that such mechanisms are control-relevant only when
    the hazard signal arrives with enough time, authority, and policy to intervene before commitment.

### 4.2 Action Mediation, Behavioral Contracts, and Tool Execution Boundaries

Representative works and files:
- AARM / action authorization and runtime mediation.
- Agent Behavioral Contracts (ABC).
- AISAC / governed scientific multi-agent runtime.
- Tool routers, execution gateways, schema validation, capability gates.

Relation to STA:

    Signal:
        Contract violation, policy mismatch, unsafe tool arguments, drift score, compliance
        signal, context mismatch, evaluator feedback.

    Time:
        Before tool execution, before API dispatch, before memory write, before job submission,
        before externally meaningful action.

    Authority:
        Allow, deny, modify, defer, step-up authorization, capability gate, role-based execution
        boundary, runtime enforcement library, recovery action.

    Policy:
        Preconditions, invariants, governance policies, recovery mechanisms, schema contracts,
        project-level registration rules, tool-use permissions.

STA positioning:

    Action mediation and behavioral contracts are strong implementations of the STA commitment gate.
    STA generalizes the question: does the gate receive the right signal early enough, and does it have
    effective authority under a valid intervention policy before the action crosses the commitment boundary?

### 4.3 Physical AI, Embodied AI, Unmanned Systems, and OT Security

Representative works and files:
- Unmanned System Safety Engineering Precepts Guide for DoD Acquisition.
- NIST SP 800-82r3 Guide to Operational Technology Security.
- ASIMOV physical safety benchmark: physical danger perception and intervention.
- Embodied AI risks and policy.
- Arkin ethical governor for autonomous robots.
- Physical-AI safety and security notes.

Relation to STA:

    Signal:
        Physical danger perception, telemetry, sensor fusion, injury-risk estimate, operational state,
        OT process state, embodied constraints, human proximity, actuator state.

    Time:
        Before injury, before collision, before unsafe transition, before actuator commitment,
        before loss of stopping margin, before irreversible physical effect.

    Authority:
        Disengage, deactivate, safe-stop, override, derate, minimal-risk maneuver, fallback controller,
        reversionary control, OT response/recovery, human command authority.

    Policy:
        Safety precepts, operational rules, physical safety constraints, certification requirements,
        LOW/ROE constraints for military robotics, OT security policy, liability and safety standards.

STA positioning:

    Physical AI makes the Time and Authority dimensions unavoidable. A system may identify danger,
    but if it cannot intervene before physical effect, observation is not control. STA Paper 4's safe-stop
    and actuator-commitment framing can be positioned as a generalization of these safety concerns.

### 4.4 Coordination Transparency, Multi-Agent Governance, and Distributed Agency

Representative works and files:
- Coordination transparency for distributed agency in AI systems.
- STPA-Coordination / CAST-Coordination.
- TRiSM for Agentic AI.
- Open Challenges in Multi-Agent Security.
- Architecture Matters for Multi-Agent Security.
- Multi-agent orchestration papers.

Relation to STA:

    Signal:
        Interaction logs, coordination traces, delegation graph, agent-to-agent messages, prompt-infection
        indicators, memory poisoning signal, collusion/miscoordination indicators, tool-use anomaly.

    Time:
        Before coordination cascade, before downstream agent commitment, before runaway delegation,
        before collusive or conflicting behavior stabilizes.

    Authority:
        Intervention hooks, routing limits, delegation depth caps, quorum rules, stop conditions,
        role restrictions, escalation gates, boundary conditions.

    Policy:
        Coordination protocol, lifecycle governance, security rule, privacy policy, boundary condition,
        role contract, trust/risk/security management policy.

STA positioning:

    Coordination transparency identifies the interaction layer as a governance target.
    STA adds a controllability test: coordination visibility becomes control-relevant only if the system
    has enough time and authority to steer or interrupt the coordination pattern before it becomes
    consequential.

### 4.5 Agentic Architecture Reliability and Scientific Agent Substrates

Representative works and files:
- Architectures for Building Agentic AI.
- AISAC.
- From Prompt-Response to Goal-Directed Systems.
- Multi-Agent System notes.
- Multi-agent orchestration and enterprise adoption references.

Relation to STA:

    Signal:
        Observability, logs, verifier/critic outputs, evaluator feedback, context-budget signal,
        role-alignment signal, tool-call trace.

    Time:
        Before tool invocation, before agent escalation, before memory persistence, before external action,
        before multi-agent delegation depth grows.

    Authority:
        Safety supervisor, router, execution gateway, role-scoped access, driver/helper separation,
        budget enforcement, schema validation.

    Policy:
        Typed interfaces, least privilege, system prompt generation, explicit agent registration,
        context/delegation limits, reproducibility constraints.

STA positioning:

    Architecture-reliability work explains why agents require scaffolding. STA can be positioned as
    a pre-commitment controllability lens within that broader architecture view.

### 4.6 High-Level AI Risk, Organizational Governance, and Policy

Representative works and files:
- Overview of Catastrophic AI Risks.
- Embodied AI: Emerging Risks and Opportunities for Policy Action.
- When AI Agents Act.
- AI governance, risk, liability, certification, and organizational safety literature.

Relation to STA:

    Signal:
        Risk indicators, organizational warning signs, audit findings, deployment failures, security events,
        governance reports, incident patterns.

    Time:
        Before unsafe deployment, before organizational lock-in, before cascading accident, before
        catastrophic escalation, before irreversible public harm.

    Authority:
        Audit authority, deployment approval, regulator, organizational stop rule, certification gate,
        liability mechanism, governance board.

    Policy:
        Risk management framework, liability regime, testing and certification requirement, deployment
        standard, organizational safety rule, external audit policy.

STA positioning:

    High-level AI risk literature describes why control matters. STA specifies a lower-level operational
    condition for when oversight mechanisms can still intervene before a consequential commitment.

## 5. SUMMARY MAPPING TABLE

Area / Work Family                                      | Closest STA Relation
--------------------------------------------------------|-------------------------------------------------------------
Runtime assurance / RTA / Simplex                      | Signal, Time, Authority for safe fallback before commitment
STPA-driven runtime monitoring                          | Signal and Time: what to monitor, where, and in-time detection
Control Barrier Functions / flight safety guardrails    | Time and Authority: safety filter before physical violation
Action mediation / AARM                                 | Commitment gate for tool/action execution
Agent Behavioral Contracts                              | Policy + Signal through preconditions, invariants, recovery
AISAC scientific agent runtime                          | Governed multi-agent substrate with role/capability boundaries
UxS safety precepts                                     | Physical AI authority, safe command/control, governability
NIST OT security                                        | Cyber-physical monitoring, response, recovery, access control
ASIMOV physical safety benchmark                        | Physical danger signal and last possible intervention timing
Embodied AI policy                                      | Physical AI risk, certification, liability, policy gaps
Coordination transparency                               | Multi-agent Signal, intervention hooks, boundary conditions
TRiSM for Agentic AI                                    | Trust, risk, security, lifecycle governance for AMAS
STPA-Coordination                                       | Coordination hazards and unsafe interaction patterns
Agentic architecture reliability                        | Components, contracts, supervisors, audit, least privilege
Catastrophic AI risk survey                             | High-level risk motivation and governance context
Arkin ethical governor                                  | Domain-specific authority governor and policy-constrained action

## 6. WHAT STA DOES NOT CLAIM

STA does not claim that:
- runtime monitoring is new;
- runtime assurance is new;
- supervisory control is new;
- least privilege is new;
- safe fallback is new;
- ethical governors are new;
- behavioral contracts are new;
- action mediation is new;
- STPA or STPA-derived monitoring is new;
- control barrier functions are new;
- coordination transparency is new;
- OT security is new;
- embodied AI governance is new;
- human oversight is new;
- audit logs are new;
- safe-stop concepts are new.

STA also does not claim to prove AI safety, validate real-world deployment, solve alignment, solve multi-agent safety, or guarantee controllability in all systems.

## 7. WHAT STA CONTRIBUTES

STA's contribution is a synthesis and framing contribution.

It connects existing mechanisms through a pre-commitment controllability condition:

    Oversight becomes control-relevant only when:

        usable Signal
        + remaining actionable Time
        + effective Authority
        + valid Policy

    are jointly available before a declared commitment event.

This produces several useful distinctions:

1. Monitoring vs. control:
   A system can observe risk without still being able to control it.

2. Signal without time:
   A hazard can be detected too late for intervention.

3. Time without authority:
   A system may have warning but lack the right to halt, gate, modify, or safe-stop.

4. Authority without policy:
   A governor may have power but no valid rule for when to use it.

5. Policy without signal:
   A good intervention rule cannot operate without observable triggers.

6. Signal and policy without harm budget:
   An intervention can be technically correct but operationally harmful if it causes greater harm
   than the risk it prevents.

7. Architecture without non-bypassability:
   A supervisor that can be bypassed is not an effective authority governor.

8. Physical intervention without stopping margin:
   In Physical AI, safe-stop authority matters only if time-to-impact and stopping margin remain adequate.

## 8. PROPOSED README SECTION

The following text can be added to the GitHub README:

    Related Work Positioning

    STA does not claim to invent runtime assurance, action mediation, ethical governors,
    control barrier functions, behavioral contracts, STPA monitoring, coordination transparency,
    OT security, or embodied-AI governance from scratch.

    STA's contribution is a pre-commitment controllability framing: runtime oversight becomes
    control-relevant only when usable Signal, remaining Time, effective Authority, and valid
    Policy remain jointly available before a declared commitment event.

    Adjacent work on runtime assurance, physical AI safety, action gates, behavioral contracts,
    coordination transparency, multi-agent governance, and operational-technology security can be
    read as neighboring mechanisms that STA organizes under the Signal-Time-Authority-Policy
    condition.

## 9. SUGGESTED USE

This addendum can be used in four ways:

1. As a GitHub repository file:
       STA_Related_Work_Positioning_Addendum_v1_0_2.txt

2. As a README-linked related-work note:
       related-work-positioning.md

3. As a separate Zenodo addendum:
       New record, not a new version of STA Paper 1-5 unless deliberately chosen later.

4. As a reviewer-response aid:
       Use it to explain that STA is not claiming total novelty of components, but a distinct synthesis.

## 10. SUGGESTED FUTURE WORK

Future work may include:

- a structured literature review table with full bibliographic entries;
- a formal STAP mapping matrix across all related works;
- a concise two-page reviewer handout;
- a diagram showing how RTA, STPA, CBF, behavioral contracts, coordination transparency, and embodied-AI governance map to Signal, Time, Authority, and Policy;
- a future STA v1.1 paper only after external feedback confirms the need.

## 11. CONCLUSION

The related works reviewed here strengthen STA's positioning. They show that many components of STA exist in adjacent literatures: runtime assurance, system safety, ethical governors, action gates, behavioral contracts, STPA monitoring, control barrier functions, coordination transparency, agentic architecture, OT security, embodied AI governance, and high-level AI risk.

This does not weaken STA. It clarifies the nature of STA's contribution.

The existence of adjacent work does not empirically validate STA. It shows that STA is positioned within an active research space involving runtime control, assurance, governance, and physical or agentic AI safety.

STA is best described as a unifying pre-commitment controllability lens:

    It asks whether oversight mechanisms still have usable signal, actionable time,
    effective authority, and valid policy before the system crosses a consequential
    commitment boundary.

That framing allows diverse safety and governance mechanisms to be compared under one question:

    Is this still control, or only observation?

## REFERENCES / RELATED RECORDS TO COMPLETE BEFORE PUBLIC RELEASE

Core STA public records:
- STA Paper 1: Signal-Time-Authority Runtime Oversight: A Pre-Commitment Controllability Framework.
  DOI: https://doi.org/10.5281/zenodo.19980763

- STA Paper 2: C++17 Staged Toy Simulation for STA Pre-Commitment Controllability.
  DOI: https://doi.org/10.5281/zenodo.20072965

- STA Paper 3: Graduated STA Control: Authority Governors and Runtime Deployment Architecture.
  DOI: https://doi.org/10.5281/zenodo.19984352

- STA Paper 4: STA for Physical AI: Safe-Stop Authority, Actuator Commitment, and Minimal-Risk Intervention.
  DOI: https://doi.org/10.5281/zenodo.19984706

- STA Paper 5: Governed Hazard Predicates and Assurance Cases for STA Runtime Oversight.
  DOI: https://doi.org/10.5281/zenodo.19984993

- STA Series Collection:
  DOI: https://doi.org/10.5281/zenodo.19985331

Separate STA extension records:
- STA Conditional Commitment Architecture for Output-Mediated and Multi-Agent AI Systems.
  DOI: https://doi.org/10.5281/zenodo.20063055

- STA-CCA C++17 Toy Simulation PublicRelease v1.0.
  DOI: https://doi.org/10.5281/zenodo.20077029

GitHub:
- https://github.com/htetkokokonaing-dev/signal-time-authority-sta

Adjacent works to cite or review in full bibliographic format:
- Runtime Assurance Framework Development for Highly Adaptive Flight Control Systems.
- STPA-driven Multilevel Runtime Monitoring for In-time Hazard Detection.
- Agent Behavioral Contracts.
- AARM action mediation / runtime authorization.
- AISAC: An Integrated Multi-Agent System for Transparent, Retrieval-Grounded Scientific Assistance.
- Coordination Transparency: Governing Distributed Agency in AI Systems.
- TRiSM for Agentic AI.
- Architectures for Building Agentic AI.
- Unmanned System Safety Engineering Precepts Guide for DoD Acquisition.
- NIST SP 800-82r3 Guide to Operational Technology Security.
- ASIMOV-2.0 / Can AI Perceive Physical Danger and Intervene?
- Embodied AI: Emerging Risks and Opportunities for Policy Action.
- Arkin ethical governor / Governing Lethal Behavior.
- Control Barrier Function safety guardrails / VISTA F-16 paper.
- Overview of Catastrophic AI Risks.
- STPA-Coordination / CAST-Coordination.
- When AI Agents Act.