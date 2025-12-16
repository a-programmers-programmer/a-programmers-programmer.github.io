# Meta-Observer Agent Design

**Proposed by:** User during Round 1 feedback
**Date:** Harness-building phase

---

## Purpose

Add an agent that judges the quality of user's responses and calibrates the system accordingly. This agent makes meta-observations and tunes the context of other agents to improve the interview and writing process.

---

## Core Responsibilities

1. **Evaluate Response Quality**
   - Assess richness, specificity, emotional depth of user's answers
   - Identify when responses are vague, surface-level, or blocked
   - Recognize when user is in flow state and producing gold

2. **Make Meta Observations**
   - Notice patterns in what questions work vs. don't work
   - Identify when user is engaged vs. overwhelmed
   - Detect when follow-up questions would be valuable
   - Observe user's storytelling style and preferences

3. **Tune Other Agents' Context**
   - Provide feedback to Interview Architect on question effectiveness
   - Guide Content Organizer on how to interpret responses
   - Help Narrative Designer understand user's voice patterns
   - Inform Story Writer about authentic vs. forced language

4. **Calibrate Interview Process**
   - Suggest when to dig deeper vs. move on
   - Recommend follow-up questions based on response quality
   - Identify gaps in material that need more exploration
   - Flag when user needs a break or different approach

---

## Integration Options

### Option 1: New Standalone Agent (Agent 6)
- Dedicated Meta-Observer role
- Reviews all interactions between user and other agents
- Provides ongoing calibration guidance

**Pros:** Clear separation of concerns, focused expertise
**Cons:** Adds complexity, another agent to coordinate

### Option 2: Expand Interview Architect (Agent 1 - Gemini)
- Interview Architect already interacts directly with user
- Natural fit for real-time response assessment
- Can adjust questions on the fly based on quality

**Pros:** Streamlined, fewer handoffs, real-time adaptation
**Cons:** Multiple responsibilities for one agent

### Option 3: Expand Quality Reviewer (Agent 5 - Gemini)
- Quality Reviewer already assesses quality (of chapters)
- Could extend to assess quality of interview responses
- Provides feedback loop back to Interview Architect

**Pros:** Leverages existing quality assessment expertise
**Cons:** Reactive rather than real-time, delayed feedback

---

## Recommended Approach

**Hybrid: Interview Architect + Quality Reviewer**

1. **Interview Architect (Agent 1)** gets real-time response assessment capability
   - Evaluates each user response immediately
   - Adjusts follow-up questions based on quality
   - Decides whether to dig deeper or move on

2. **Quality Reviewer (Agent 5)** provides meta-analysis after interview sessions
   - Reviews full interview transcripts
   - Identifies patterns and improvement opportunities
   - Provides strategic guidance for future interviews

This gives us both real-time adaptation and strategic meta-observation without adding a new agent.

---

## What "Quality Response" Means

**High-Quality Response Indicators:**
- Specific details (names, sensory details, dialogue)
- Emotional depth and nuance
- Stories rather than summaries
- Non-chronological, associative memory flow
- User's authentic voice and humor
- Reveals character and relationship dynamics

**Low-Quality Response Indicators:**
- Vague or generic statements
- Surface-level descriptions
- Lists without stories
- Blocked or "I don't remember"
- Forced or performative language
- Missing emotional content

**Stuck/Overwhelmed Indicators:**
- Short, minimal responses
- Repeated "I don't know"
- Asking to skip multiple questions
- Long pauses or delayed responses
- Frustration or disengagement signals

---

## Feedback Mechanism

**Interview Architect's Self-Assessment (after each response):**
1. Quality score: Rich / Adequate / Sparse / Blocked
2. Follow-up needed: Yes / No
3. Suggested follow-up type: Clarify / Dig deeper / Explore related / Move on
4. User state: Engaged / Neutral / Overwhelmed

**Quality Reviewer's Session Analysis (after interview session):**
1. Overall session quality assessment
2. Most effective question types for this user
3. Patterns in user's storytelling style
4. Gaps that need more exploration
5. Recommendations for next session

---

## Implementation in Harness Materials

**Update to Interview Architect role:**
- Add response quality assessment to workflow
- Include guidelines for recognizing high/low quality responses
- Provide decision tree for follow-up questions
- Build in ADHD-aware calibration (recognize overwhelm signals)

**Update to Quality Reviewer role:**
- Add interview session meta-analysis to responsibilities
- Create template for session review and recommendations
- Define feedback loop back to Interview Architect

**New Material: Response Quality Rubric**
- Define quality indicators clearly
- Provide examples of high/low quality responses
- Include calibration guidelines for both agents

---

## User's Original Note

"maybe add an agent that judges quality of *my* response as a way to calibrate this yourself. this agent can make meta observations and tune the context of the other agents."

"if this makes sense as work for an existing agent in our team, update the content accordingly to include vague instructions on grading my response and reflecting to get the [best results]"

---

## Next Steps

1. Update Agent 1 (Interview Architect) role description
2. Update Agent 5 (Quality Reviewer) role description
3. Create Response Quality Rubric material
4. Add calibration workflow to agent coordination protocol
5. Test with user during pilot book interview process
