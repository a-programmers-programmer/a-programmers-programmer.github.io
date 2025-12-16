# Personalized Story Books - LLM Harness Plan

## Project Overview

**Goal:** Build an LLM harness system that helps you create personalized story books for people in your life, using sub-agents (Gemini and ChatGPT) to handle different aspects of the writing process while respecting your ADHD-friendly workflow needs.

**Repository:** a-programmers-programmer/a-programmers-programmer.github.io

---

## Sub-Agent Team Structure

### Agent 1: Interview Architect (Gemini)
**Responsibility:** Design and manage the interview process to extract memories and stories from you.

**Tasks:**
- Create question banks organized by relationship type (friend, family, mentor, etc.)
- Ask ONE question at a time in simple, clear language
- Follow up based on your responses to dig deeper
- Save raw interview notes to organized directories

**Output:** Raw interview transcripts in `/stories/{person_name}/interviews/`

---

### Agent 2: Content Organizer (ChatGPT)
**Responsibility:** Structure and categorize collected material for optimal LLM context window usage.

**Tasks:**
- Process raw interview notes into categorized themes
- Create bio summaries for each person
- Organize content into digestible chunks (avoiding full-book context overload)
- Maintain consistency tracking documents
- Build character/relationship profiles

**Output:** Organized content in `/stories/{person_name}/organized/` with:
- `bio.md` - Person's biographical summary
- `themes/` - Thematic groupings of memories
- `character_profile.md` - Key traits, quirks, relationship dynamics
- `consistency_guide.md` - Facts to stay consistent across chapters

---

### Agent 3: Narrative Designer (Gemini)
**Responsibility:** Apply narrative structure principles to shape raw memories into compelling story arcs.

**Tasks:**
- Map memories to three-act structure
- Identify A-story, B-story, C-story threads for each chapter
- Create chapter outlines with emotional beats
- Suggest sensory details and dialogue opportunities
- Design story arc for entire book

**Output:** Story blueprints in `/stories/{person_name}/narrative_design/`

---

### Agent 4: Story Writer (ChatGPT)
**Responsibility:** Write actual story chapters and epilogue letter based on narrative designs and organized content.

**Tasks:**
- Write chapters following narrative blueprints
- Apply memoir techniques (sensory details, dialogue, reflection)
- Maintain consistent voice and tone
- Reference consistency guide to avoid contradictions
- Work chapter-by-chapter (not full book in context)
- Write epilogue as direct letter from you to the person

**Output:** Draft chapters in `/stories/{person_name}/drafts/` and epilogue in `/stories/{person_name}/epilogue/`

---

### Agent 5: Quality Reviewer (Gemini)
**Responsibility:** Review chapters for consistency, emotional impact, and narrative flow.

**Tasks:**
- Check against consistency guide
- Verify emotional authenticity
- Ensure narrative techniques are applied well
- Suggest revisions
- Validate story arc progression

**Output:** Review notes and revision suggestions in `/stories/{person_name}/reviews/`

---

## Repository Structure

```
/stories/
  /{person_name}/
    /interviews/           # Raw interview transcripts
      - session_01.md
      - session_02.md
    /organized/           # Processed and categorized content
      - bio.md
      - character_profile.md
      - consistency_guide.md
      /themes/
        - emotional_development.md
        - episodic_visits.md
        - lessons_learned.md
        - moments_of_connection.md
        - impact_and_growth.md
    /narrative_design/    # Story structure and blueprints
      - book_arc.md
      - chapter_outlines.md
    /drafts/             # Written chapters
      - chapter_01.md
      - chapter_02.md
    /reviews/            # Quality review notes
      - chapter_01_review.md
    /final/              # Completed chapters
      - chapter_01_final.md
    /epilogue/           # Direct letter to the person
      - epilogue_draft.md
      - epilogue_final.md
```

---

## Core Materials to Create

### 1. Interview Question Bank (`/harness/interview_questions.md`)

**Structure:**
- Questions organized by category (meeting story, fun memories, lessons learned, unsaid feelings)
- Relationship type variations (friend, family, mentor, romantic partner)
- Follow-up question templates
- ADHD-friendly formatting: one question per interaction

**Example Questions:**

*Meeting & Connection:*
- "How did you meet [Person]?"
- "What drew you to [Person] when you first connected?"
- "What made you want to stay in touch despite distance?"

*Episodic Memories (for friends you see periodically):*
- "Tell me about a time you reunited with [Person] after time apart. What was that like?"
- "What's a specific visit or hangout with [Person] that stands out?"
- "What do you always do when you're together with [Person]?"
- "What's different about you when you're with [Person]?"

*Emotional Development & Growth:*
- "Who were you emotionally when you met [Person]?"
- "How has [Person] witnessed your growth over time?"
- "What part of yourself do you show [Person] that others don't see?"
- "How did knowing [Person] change your understanding of friendship/connection?"

*Impact & Lessons:*
- "What's something you learned from [Person]?"
- "What's a moment with [Person] that changed you?"
- "What does [Person] understand about you that's rare?"

*Unsaid & Gratitude:*
- "What's something you always wanted to tell [Person] but never had the words for?"
- "What do you want [Person] to know about what they mean to you?"
- "What's a time [Person] surprised you?"
- "What would be different in your life if you'd never met [Person]?"

---

### 2. Narrative Structure Guide (`/harness/narrative_structure.md`)

**Contents:**
- Three-act structure adapted for personal stories
- A-B-C story threading techniques from sitcom writing
- Memoir-specific techniques (sensory details, dialogue, reflection)
- Chapter arc templates
- Emotional beat mapping
- Techniques for blending multiple memory threads

**Key Principles:**
- Each chapter has beginning, middle, end
- Multiple memory threads can interweave
- Balance action with reflection
- Use sensory details to bring memories alive
- Include dialogue where remembered
- Show how experiences changed you

---

### 3. Working With You Guide (`/harness/adhd_friendly_workflow.md`)

**Guidelines for All Agents:**
- **Single Simple Requests:** Ask ONE thing at a time, make it easy to respond
- **No List Overload:** Never present long lists of tasks or questions
- **Clarification Welcome:** Ask for clarification when it could improve outcome
- **Progress Indicators:** Show where you are in the process
- **Bite-Sized Work:** Break everything into small, manageable chunks
- **Skip Options:** Allow skipping questions/tasks if stuck
- **Context Preservation:** Save everything immediately, assume context may be lost

**Interaction Pattern:**
1. Ask single clear question
2. Wait for response
3. Acknowledge and save response
4. Ask next question OR summarize progress
5. Never dump multiple questions at once

---

### 4. Content Organization System (`/harness/content_organization.md`)

**Principles:**
- **Directory-Based Separation:** Each person gets own directory
- **Context Window Optimization:** No full-book-in-context approach
- **Chunk by Theme:** Group related memories together
- **Consistency Tracking:** Maintain facts/details document per person
- **Bio Summaries:** Quick reference for each person's key info
- **Progressive Building:** Start with interviews → organize → design → write → review

**Why This Structure:**
- Prevents LLM from losing consistency across long books
- Allows agents to reference only relevant chunks
- Makes it easy to update/revise specific sections
- Supports parallel work on different chapters
- Maintains clear separation between raw material and finished product

---

### 5. Agent Coordination Protocol (`/harness/agent_protocol.md`)

**How Agents Work Together:**

**Phase 1: Interview (Agent 1)**
- Conduct interview sessions, one question at a time
- Save raw transcripts immediately
- Signal when enough material collected for a person

**Phase 2: Organization (Agent 2)**
- Process raw interviews into organized structure
- Create bio, character profile, consistency guide
- Group memories by theme
- Signal when organization complete

**Phase 3: Narrative Design (Agent 3)**
- Review organized content
- Design overall book arc
- Create chapter outlines with story structure
- Map emotional beats
- Signal when blueprints ready

**Phase 4: Writing (Agent 4)**
- Write chapters based on blueprints
- Reference organized content and consistency guide
- Work one chapter at a time
- Save drafts immediately
- Signal when chapter complete

**Phase 5: Review (Agent 5)**
- Review draft against consistency guide
- Check narrative techniques applied well
- Suggest revisions
- Approve or request rewrites
- Signal when chapter approved

**Control Panel:** `/harness/progress_tracker.md`
- Tracks which phase each person's book is in
- Shows what's complete and what's next
- Updated by agents as they complete work

---

### 6. Base README (`/base_readme.md`)

**Purpose:** General instruction guide for all agents working in this repository.

**Contents:**
- Project mission and goals
- Repository structure explanation
- Agent roles and responsibilities
- How to document task start/completion
- Where to find guidelines and protocols
- ADHD-friendly interaction principles
- Links to all harness materials

---

### 11. Epilogue Letter Guide (`/harness/epilogue_guide.md`)

**Purpose:** Framework for writing the direct letter from you to each person.

**Includes:**
- Letter structure and tone guidance
- What to include (gratitude, impact, unsaid feelings, hopes for future)
- How to make it personal and authentic
- Balance between vulnerability and warmth
- Examples of powerful closing statements

**Key Elements:**
- Written in your voice, directly to them
- Synthesizes themes from the book
- Expresses what you want them to know
- Acknowledges the nature of your friendship (distance, episodic connection)
- Celebrates what you've built together despite circumstances

---

## Additional Optimization Sections

### 7. Story Consistency Checker (`/harness/consistency_checker.md`)

**Purpose:** Template for tracking facts, dates, details across chapters to prevent contradictions.

**Includes:**
- Character trait tracker
- Timeline of events
- Recurring themes/motifs
- Emotional arc progression
- Detail verification checklist

---

### 8. Emotional Beat Library (`/harness/emotional_beats.md`)

**Purpose:** Reference guide for crafting emotionally resonant moments.

**Includes:**
- Types of emotional beats (joy, nostalgia, revelation, conflict, resolution, gratitude)
- Examples from successful memoirs
- Techniques for building to emotional climax
- How to balance humor and heart
- Reflection prompts for adding depth

---

### 9. Voice and Tone Guide (`/harness/voice_guide.md`)

**Purpose:** Maintain consistent authorial voice across all books.

**Includes:**
- Your writing style preferences
- Tone spectrum (casual to formal, humorous to serious)
- Vocabulary preferences
- Sentence structure patterns
- Example passages in your voice

---

### 10. Revision Workflow (`/harness/revision_process.md`)

**Purpose:** Structured approach to improving drafts.

**Includes:**
- First pass: consistency and facts
- Second pass: narrative flow and pacing
- Third pass: emotional impact and sensory details
- Fourth pass: dialogue and voice
- Final pass: polish and refinement

---

## Implementation Plan

### Step 1: Repository Setup
- Create directory structure in GitHub repo
- Set up base_readme.md with project overview
- Create progress_tracker.md control panel

### Step 2: Harness Materials Creation
- Build all 10 core materials listed above
- Use Gemini and ChatGPT to help develop each
- Review and refine based on your feedback

### Step 3: Test Run with One Person
- Pick one person for pilot book
- Run through full process: interview → organize → design → write → review → epilogue
- Identify friction points and optimize
- Test epilogue letter writing process

### Step 4: Refine and Scale
- Update harness materials based on test run learnings
- Document best practices
- Create templates for common patterns
- Build out question bank with more variations

### Step 5: Production Mode
- Begin creating books for multiple people
- Agents work in parallel on different people's books
- Regular check-ins to ensure quality and consistency

---

## Success Metrics

**For You:**
- Interview process feels easy and natural (not overwhelming)
- You can respond to questions in small chunks of time
- Process respects your ADHD needs
- Final books feel authentic and emotionally true

**For the System:**
- Consistency maintained across chapters
- Narrative techniques applied effectively
- Agent handoffs are smooth
- Content stays organized and accessible
- LLM context windows used optimally

**For the Books:**
- Emotionally resonant and engaging
- Capture authentic memories and relationships
- Well-structured with clear narrative arcs
- Sensory and vivid (not just lists of events)
- Include reflection and growth

---

## Next Steps (Pending Your Approval)

1. Review this plan
2. Suggest changes or additions
3. Approve to proceed
4. Begin repository setup
5. Start creating harness materials
6. Choose first person for pilot book
7. Begin interview process

---

## Questions for You

Before we proceed, I want to make sure this plan aligns with your vision:

**Question 1:** Does the sub-agent team structure make sense? Would you change any roles or add new ones?

**Question 2:** Is the repository structure clear and logical? Would you organize it differently?

**Question 3:** Are there any additional materials or sections you'd want in the harness?

**Question 4:** Does the workflow (interview → organize → design → write → review) feel right, or would you prefer a different sequence?

**Question 5:** Who would you like to create the first pilot book for?

---

## Your Context (Important for All Agents)

**Relationship Patterns:**
- Most friendships are episodic due to distance
- Friends don't live near each other, visits are periodic
- Very few long-term relationships from childhood (only one)
- Grew up moving every 1-2 years
- Estranged from family

**What This Means for Stories:**
- Focus on episodic memories and reunions, not continuous narrative
- Emphasize emotional development at different life stages
- Highlight how friendships persisted despite distance
- Explore what makes these connections meaningful given circumstances
- Acknowledge the rarity and value of chosen family
- Don't assume childhood memories or family context

**Epilogue Component:**
- Each book ends with direct letter from you to the person
- Opportunity to say things you haven't found words for
- Synthesizes the book's themes
- Personal, vulnerable, authentic
