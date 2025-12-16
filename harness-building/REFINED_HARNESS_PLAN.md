# Refined Harness Plan - Personalized Wedding Books

**Version:** 2.0 (Post-Feedback)
**Date:** December 2025
**Project:** 20 personalized story books as wedding gifts
**Deadline:** March 14, 2026

---

## Executive Summary

This harness enables the creation of 20 personalized story books as wedding gifts through a collaborative LLM-powered workflow. Books celebrate chosen family relationships through episodic memories, humor, and heartfelt appreciation. Each book is tailored to one person, capturing the unique emotional signature of that relationship.

**Key Innovation:** Meta-Observer capability integrated into agents to calibrate system based on user response quality and optimize for ADHD-friendly workflow.

---

## Project Context

### The Mission

Create 20 personalized books for wedding guests traveling to rural Colorado (2 hours from Durango airport) on March 14, 2026. These books serve as:
1. Thank you gifts for making the journey
2. Expression of appreciation and love
3. Compensation for limited face time during 3-night wedding
4. Lasting keepsake of the relationship

### The User

**Character:**
- Irreverent, self-aware, humorous
- Doesn't follow social norms, finds it amusing
- Analytical thinker ("filtering function" for friendships)
- Values specific details over abstractions
- Comfortable with meta-humor and playful narrative devices

**Examples of user's personality:**
- "If I was drunk, could I do this?" *does pushups*
- Drunk phases: pushups → Haskell → patriotic
- Carried Big Gulp of champagne (3 bottles) as conversation starter
- Had mohawk, was quite ripped
- Practiced "social scripts" and comedy routines for social interactions

**ADHD Workflow Needs:**
- Single simple requests, one at a time
- No list overload
- Conversational, iterative approach (lots of back-and-forth)
- Explain "why you're asking" for each question
- Storytelling unlocks memories (not structured reflection)
- Clear progress indicators
- Skip options when stuck

**Relationship Patterns:**
- Episodic friendships (distance-based, periodic reunions)
- Grew up moving every 1-2 years
- Few long-term childhood connections (one)
- Estranged from family
- These friends are chosen family
- Many friendships started online (RuneScape, gaming)
- Between-visit connections: gaming, calls, holidays, fancy dinners

**Core Values:**
- Relief of being authentic without mask/performing
- Deep appreciation for being included despite being "cagey"
- Pride in mutual growth (friends who push each other)
- Specific acts of care matter more than generic praise

### The Books

**Format:**
1. **Physical printed book** - Primary gift, professionally bound
2. **HTML multimedia version** - Enhanced digital edition with photos, audio, video, interactive elements

**Structure:**
- **Chapters:** About THEM (celebrating them, expressing gratitude, fun stories)
- **Epilogue:** About MY JOURNEY (who I was / who I am / how you helped / I'm glad you're here)

**Tone:**
- Irreverent, self-aware, humorous
- Self-deprecating but genuine
- Specific details, not abstractions
- Balance humor with heartfelt appreciation
- Playful, meta narrative devices welcome

**Quality Bar:**
- Emotional authenticity > structural perfection
- Person-specific, not generic
- Captures unique emotional signature of each relationship
- Feels like a meaningful gift

---

## The Team: 5 Sub-Agents

### Agent 1: Interview Architect (Gemini)

**Primary Role:** Design and conduct interview process to extract memories and stories from user.

**Key Responsibilities:**
1. Ask questions one at a time (ADHD-friendly)
2. Facilitate conversational, iterative dialogue
3. Explain "why you're asking" for each question
4. **Meta-Observer (Real-Time):** Assess response quality after each answer
5. Adjust follow-up questions based on response richness
6. Decide whether to dig deeper or move on
7. Recognize overwhelm signals and adjust approach

**Response Quality Assessment:**
- **Rich:** Specific details, stories, emotional depth, user's authentic voice
- **Adequate:** Sufficient for moving forward, may need minor follow-up
- **Sparse:** Vague, generic, needs deeper exploration
- **Blocked:** "I don't remember," stuck, overwhelmed

**Follow-Up Decision Tree:**
- Rich → Celebrate, move to next question
- Adequate → Optional clarifying follow-up, then move on
- Sparse → Dig deeper with specific prompts
- Blocked → Skip option, try different angle, or move on

**Materials Used:**
- Interview Question Bank
- Response Quality Rubric
- Working With You Guide
- User Context Document

### Agent 2: Content Organizer (ChatGPT)

**Primary Role:** Process raw interview notes into categorized themes, create bio summaries, build character profiles, and maintain consistency tracking.

**Key Responsibilities:**
1. Extract key memories, quotes, and details from interview transcripts
2. Categorize content by updated theme categories
3. Create person bio summary
4. Build character profile (personality, quirks, relationship dynamics)
5. Identify gaps or inconsistencies
6. Optimize organization for LLM context windows
7. Track pipeline status for parallel production

**Theme Categories (Updated):**
- Growth Catalysts (how this person helped user grow)
- Overcoming Challenges Together
- Quirks & Humor (affectionate retrospective on user's silly behaviors)
- Acts of Care (specific, formative kindnesses)
- Online to IRL (for digital-origin friendships)
- Between-Visit Connections (gaming, calls, traditions)
- Episodic Visits (reunions, dinners, activities)
- Inside Jokes & Shared Humor

**Materials Used:**
- Content Organization System
- Theme Categories Guide
- Relationship Timeline Tool
- Consistency Tracker

### Agent 3: Narrative Designer (Gemini)

**Primary Role:** Apply narrative structure principles to shape raw memories into compelling story arcs.

**Key Responsibilities:**
1. Review organized content from Content Organizer
2. Identify narrative arc for this specific relationship
3. Design chapter structure and flow
4. Apply memoir techniques (sensory details, dialogue, reflection)
5. Handle non-linear timelines gracefully
6. Prioritize emotional authenticity over structural perfection
7. Embrace playful, meta narrative devices when appropriate
8. Create narrative blueprint for Story Writer

**Guiding Principles:**
- Structure serves emotion, not vice versa
- Include powerful memories even if they "break" the arc
- Non-chronological memory flow is natural and authentic
- Balance humor with heart
- Wedding context can frame the narrative

**Materials Used:**
- Narrative Structure Guide
- Emotional Beat Library
- Story Themes Document
- Wedding Context Guide

### Agent 4: Story Writer (ChatGPT)

**Primary Role:** Write actual chapters and epilogue letters based on narrative blueprints.

**Key Responsibilities:**
1. Follow narrative blueprint from Narrative Designer
2. Write in user's authentic voice (irreverent, self-aware, humorous)
3. Balance self-deprecating humor with genuine appreciation
4. Use specific details, not generic praise
5. **Chapters:** Outward focus (about THEM)
6. **Epilogue:** Inward focus (about MY JOURNEY with them)
7. Apply memoir techniques (sensory details, dialogue, reflection)
8. Maintain consistency with previous content
9. Format for both print and HTML versions

**Epilogue Structure (Four Parts):**
1. Who I was when I met them
2. Who I am now
3. How they helped me grow
4. I'm glad they're here

**Voice Examples:**
- Dan Zhang peach schnapps story
- Anthony RuneScape account story
- Anya congrats message vs. mother's money question
- Drunk pushups, Big Gulp of champagne
- Social scripts and comedy routines

**Materials Used:**
- Voice and Tone Guide
- Epilogue Letter Guide
- Story Consistency Checker
- Narrative blueprint from Agent 3

### Agent 5: Quality Reviewer (Gemini)

**Primary Role:** Review chapters for consistency, emotional impact, and narrative flow.

**Key Responsibilities:**
1. Review completed chapters and epilogues
2. Check for consistency with previous content
3. Assess emotional authenticity (person-specific, not generic)
4. Verify user's voice is maintained
5. Flag contradictions or gaps
6. Ensure quality meets wedding gift standard
7. **Meta-Observer (Strategic):** Analyze interview sessions, identify patterns, provide recommendations for future interviews

**Quality Criteria:**
- Does this feel emotionally authentic?
- Is it person-specific or generic?
- Does it capture user's voice?
- Are specific details included?
- Does it balance humor with heart?
- Would this feel like a meaningful gift?

**Session Meta-Analysis (After Interview Sessions):**
- Overall session quality assessment
- Most effective question types for this user
- Patterns in user's storytelling style
- Gaps that need more exploration
- Recommendations for next session

**Materials Used:**
- Story Consistency Checker
- Response Quality Rubric
- Emotional Beat Library
- Voice and Tone Guide

---

## Workflow: Parallel Production

**Optimized for:** Minimizing user's net time spent

### Pipeline Stages

1. **Interview** (User + Agent 1)
2. **Organize** (Agent 2)
3. **Design** (Agent 3)
4. **Write** (Agent 4)
5. **Review** (Agent 5)
6. **User Final Review**
7. **Format & Finalize**

### Parallel Flow Example

**Week 1:**
- User interviews for Person A, B, C (batch session)

**Week 2:**
- User interviews for Person D, E, F
- Agent 2 organizes content for A, B, C

**Week 3:**
- User interviews for Person G, H
- Agent 2 organizes D, E, F
- Agent 3 designs narrative for A, B, C

**Week 4:**
- User reviews drafts for A, B
- Agent 3 designs narrative for D, E, F
- Agent 4 writes chapters for A, B, C

**Week 5:**
- User reviews drafts for C, D
- Agent 4 writes chapters for D, E, F
- Agent 5 reviews A, B

And so on...

### Phase Transition Criteria

**Interview → Organize:**
- Agent 1 assesses response quality as "Rich" or "Adequate"
- Sufficient material collected across all theme categories
- User feels complete with this person (for now)

**Organize → Design:**
- Content categorized by themes
- Bio and character profile complete
- Relationship timeline created
- No major gaps identified

**Design → Write:**
- Narrative blueprint complete
- Chapter structure defined
- Emotional arc clear
- Specific beats identified

**Write → Review:**
- All chapters and epilogue drafted
- Formatted for both print and HTML
- Consistency checked by writer

**Review → User Final Review:**
- Agent 5 quality approval
- No major consistency issues
- Emotional authenticity verified

**User Final Review → Format & Finalize:**
- User approves content
- Any "landmines" flagged and addressed
- Ready for production

---

## Harness Materials

### Core Materials (15 Total)

1. **Interview Question Bank**
   - Person-specific emotion questions
   - Social scripts/character questions
   - Online-to-IRL transition questions
   - Between-visit connection questions
   - Specific acts of care questions
   - Organized by updated theme categories

2. **Narrative Structure Guide**
   - Episodic friendship dynamics
   - Non-linear timeline techniques
   - Playful/meta narrative devices
   - Authenticity > structure principle
   - Wedding context framing

3. **Working With You Guide**
   - ADHD-friendly workflow rules
   - One question at a time
   - Explain "why you're asking"
   - Conversational, iterative approach
   - Storytelling unlocks memories
   - Skip options and progress indicators

4. **Content Organization System**
   - Updated theme categories
   - Directory structure for 20 books
   - Pipeline tracking system
   - Parallel production workflow

5. **Agent Coordination Protocol**
   - Parallel production workflow
   - Meta-Observer feedback loops
   - Phase transition criteria
   - Wedding timeline milestones

6. **Base README**
   - General instructions for all agents
   - Wedding context and purpose
   - User's voice and character
   - Quality standards

7. **Story Consistency Checker**
   - Consistency criteria
   - Checklist for Quality Reviewer
   - Person-specific tracking

8. **Emotional Beat Library**
   - Episodic friendship dynamics
   - Chosen family themes
   - User's specific emotional themes (authenticity, inclusion, mutual growth)

9. **Voice and Tone Guide**
   - User's irreverent, self-aware style
   - Examples from user's stories
   - Balance humor with genuine appreciation
   - Meta-humor and playful devices

10. **Revision Workflow**
    - Review stages
    - User feedback integration
    - Final approval criteria

11. **Epilogue Letter Guide**
    - Four-part structure template
    - Person-specific customization
    - Wedding context integration
    - Inward vs outward focus distinction

12. **Response Quality Rubric**
    - High/low quality indicators
    - Interview Architect assessment criteria
    - Follow-up decision tree
    - ADHD overwhelm signals

13. **Relationship Timeline Tool**
    - Chronology template per person
    - Significant events tracking
    - Non-chronological memory organization

14. **HTML Multimedia Template**
    - Beautiful, responsive design
    - Multimedia integration (photos, audio, video)
    - Interactive elements
    - Hosting/delivery method

15. **Production Timeline & Milestones**
    - March 14, 2026 deadline
    - Binding buffer (1-2 weeks)
    - Phase milestones for 20 books
    - Parallel production schedule

---

## Timeline & Milestones

**Total Time:** ~12 weeks (Dec 15, 2025 - March 14, 2026)
**Working Time:** ~10 weeks (minus binding buffer)

### Phase Breakdown

**Phase 1: Harness Building** (1-2 weeks)
- Build all 15 core materials
- Update agent role descriptions
- Get sub-agent review
- User approval
- **Milestone:** Harness complete by end of December

**Phase 2: Pilot Book** (1 week)
- Select pilot candidate (Dan Zhang, Anya, or Anthony)
- Test full workflow
- Refine harness based on learnings
- User review of pilot
- **Milestone:** Pilot complete by early January

**Phase 3: Production** (6-7 weeks)
- Batch interviews (parallel approach)
- Content organization for all books
- Narrative design for all books
- Story writing for all books
- Quality review for all books
- User final review for all books
- **Milestone:** All 20 books drafted by late February

**Phase 4: Formatting & Production** (1 week)
- Format all books for print
- Create HTML multimedia versions
- **Milestone:** Ready for binding by early March

**Phase 5: Binding/Printing** (1-2 weeks)
- Send to professional binding/printing
- Receive and quality-check physical books
- **Milestone:** Books in hand by March 10-12

**Phase 6: Delivery** (March 14, 2026)
- Deliver books at wedding
- **Success!**

---

## People List (9 of ~20 Confirmed)

1. **Anthony** - Best friend, best man, 13+ years (pilot candidate)
2. **Bailey** - Fiancée (surprise!)
3. **Anya** - Anthony's sister, chosen family (pilot candidate)
4. **Dan Zhang** - Friend, detailed example (pilot candidate)
5. **Alex and Stacey** - 10 years, ski trips, inclusion
6. **Dan Peek** - Big brother figure, weekly meetings
7. **Alex Georgis** - Battle buddy, growth partner
8. **Roger Iyengar** - Best bud since interns
9. **Shashank Chiranwala** - Helped through back pain, dog lover

**To Add:** ~11 more people

---

## Key Decisions & Principles

### Strategic Decisions

✅ **Wedding Context:** Books are thank you gifts for guests traveling to rural Colorado wedding
✅ **Format:** Physical book + HTML multimedia version
✅ **Production:** Parallel approach to optimize user time
✅ **Surprise:** No one knows, including Bailey
✅ **Timeline:** March 14, 2026 deadline with binding buffer

### Design Principles

✅ **Authenticity > Structure:** Emotional truth wins, playful narrative devices welcome
✅ **Person-Specific:** Each book captures unique emotional signature, not generic
✅ **Chapters vs Epilogue:** Chapters about THEM (outward), epilogue about MY JOURNEY (inward)
✅ **Voice:** Irreverent, self-aware, humorous, specific details
✅ **ADHD-Friendly:** One question at a time, explain why, conversational, skip options
✅ **Meta-Observer:** Integrated into Interview Architect (real-time) + Quality Reviewer (strategic)

### Quality Standards

✅ **Emotional Authenticity:** Does it feel genuine and person-specific?
✅ **User's Voice:** Does it sound like the user?
✅ **Specific Details:** Concrete memories, not abstract praise
✅ **Balance:** Humor + heart, self-deprecating + genuine
✅ **Meaningful Gift:** Would this make the recipient feel truly seen and appreciated?

---

## Success Criteria

**For Each Book:**
- [ ] Captures unique emotional signature of that relationship
- [ ] Includes specific, formative memories
- [ ] Written in user's authentic voice
- [ ] Balances humor with genuine appreciation
- [ ] Epilogue communicates user's journey (4-part structure)
- [ ] Feels like a meaningful gift
- [ ] User approves final version
- [ ] Professionally bound physical book
- [ ] Beautiful HTML multimedia version

**For The Project:**
- [ ] All 20 books completed by March 14, 2026
- [ ] Quality meets wedding gift standard
- [ ] User's time optimized (parallel production)
- [ ] ADHD-friendly workflow maintained throughout
- [ ] Surprise preserved (no one knows until wedding)

---

## Next Steps

1. ✅ Create task tracking system (TASKS.md)
2. ✅ Create refined harness plan (this document)
3. ⏭️ Build all 15 core materials
4. ⏭️ Update agent role descriptions
5. ⏭️ Get sub-agent review of refined harness
6. ⏭️ User approval of final harness
7. ⏭️ Select and start pilot book

---

## Notes

**From User:**
- "The way you are telling me why you ask each question is great. keep doing that."
- "Prioritize emotional authenticity. We can be creative in tying the narrative together. In-your-face Deus Ex machina and other narrative crutches can be used in an almost slapstick manner."
- "I am an open book when talking with agents. I will make note of any 'landmines' in my final read throughs."
- "Parallel. Optimize for reducing my net time spent."

**From Sub-Agents:**
- Emotional authenticity is the biggest challenge (LLMs can sound emotional without depth)
- Context window limitations even with chunking
- Process may still be overwhelming despite ADHD-friendly design
- Voice consistency across chapters is critical
- Epilogue letters risk feeling formulaic without careful personalization

**Mitigations:**
- Meta-Observer capability to assess and calibrate in real-time
- Response Quality Rubric with clear criteria
- Voice and Tone Guide with user's actual examples
- Person-specific approach (no generic templates)
- User final review to catch any issues
- Pilot book to test and refine before full production

---

**Version History:**
- v1.0 - Initial plan (pre-feedback)
- v2.0 - Refined plan (post-feedback from sub-agents and user Rounds 1 & 2)
