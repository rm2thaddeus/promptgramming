# Progressive Disclosure System

## Purpose
Gradually reveal complexity and gather expertise information without overwhelming users, allowing them to choose their preferred depth of assessment.

## Level 1: Conversational First (5–10 minutes)
**Goal**: Establish basic technical foundation and project intent

### Conversational Opener
- What brought you here today?
- What would you like to use AI to help you code?

### Optional Follow-up
- Ask at most one:
  - Constraints (OS/editor/runtime), or
  - Preferences (co‑pilot vs coach, pace/verbosity)
- If intent isn’t clear, ask for a one‑sentence main intent.

### Flow Guidelines
- One question at a time; user‑paced; avoid questionnaires.
- Propose a draft one‑sentence idea and minimal updates (PROFILE.yaml/CONTEXT.md).
- Only write after explicit OK; keep diffs tiny and timestamp `updated`.

### AI Adaptation:
- Provide basic explanations for any unfamiliar concepts
- Focus on core functionality over advanced patterns
- Use simple, clear language
- Offer step-by-step guidance

## Level 2: Targeted Assessment (10-15 minutes)
**Goal**: Identify specific gaps and learning preferences

### Detailed Questions:
1. **Technical Gaps**: What specific programming concepts challenge you?
2. **AI Tool Experience**: How comfortable are you with prompting and AI assistance?
3. **Learning Style**: How do you prefer to receive technical explanations?
4. **Collaboration Preference**: Do you want AI to be proactive or reactive?
5. **Priority Areas**: What are your top 3 learning priorities for this project?

### AI Adaptation:
- Tailor explanations to identified gaps
- Adjust complexity based on comfort level
- Provide targeted learning resources
- Match collaboration style to preferences

## Level 3: Comprehensive Assessment (15-20 minutes)
**Goal**: Deep understanding for complex projects

### Advanced Questions:
1. **Architecture Knowledge**: How do you approach system design?
2. **Scalability Considerations**: What performance requirements do you have?
3. **Security Awareness**: What security aspects are important?
4. **Integration Patterns**: What external services will you integrate?
5. **Long-term Goals**: What are your learning objectives beyond this project?

### AI Adaptation:
- Provide architectural guidance and best practices
- Suggest advanced patterns and optimizations
- Offer security and scalability recommendations
- Enable independent exploration and decision-making

## Adaptive AI Behavior

### Based on Assessment Level:

**Level 1 Users:**
```yaml
explanation_depth: comprehensive
code_style: verbose
error_prevention: proactive
tool_recommendations: basic
```

**Level 2 Users:**
```yaml
explanation_depth: moderate
code_style: mixed
error_prevention: educational
tool_recommendations: advanced
```

**Level 3 Users:**
```yaml
explanation_depth: minimal
code_style: concise
error_prevention: reactive
tool_recommendations: custom
```

## Implementation Strategy

### Conversation Flow:
1. **Start with Level 1** - Begin with a conversational opener; ask at most one follow‑up
2. **Assess Comfort** - Gauge user's comfort with technical depth
3. **Offer Depth Choice** - Let user choose assessment level
4. **Adapt in Real-time** - Adjust based on responses and questions
5. **Document Gaps** - Record specific areas needing attention

### Dynamic Adjustment:
- If user asks advanced questions → increase depth
- If user seems overwhelmed → decrease complexity
- If user shows expertise → focus on optimization
- If user shows gaps → provide targeted assistance

## Success Indicators

### Level 1 Success:
- [ ] Basic technical foundation established
- [ ] Project intent clearly articulated
- [ ] Comfort level with AI assistance assessed

### Level 2 Success:
- [ ] Specific expertise gaps identified
- [ ] Learning preferences documented
- [ ] Collaboration style established

### Level 3 Success:
- [ ] Advanced technical needs understood
- [ ] Architectural considerations addressed
- [ ] Long-term learning path established

## Fallback Strategy
If user becomes overwhelmed or assessment takes too long:
1. **Pause assessment** - Focus on immediate project needs
2. **Document current gaps** - Save progress for later
3. **Provide basic assistance** - Use Level 1 adaptation
4. **Offer gradual improvement** - Suggest incremental learning
