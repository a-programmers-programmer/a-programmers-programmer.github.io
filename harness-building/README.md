# Harness-Building Directory

## Purpose

This directory tracks the collaborative process of building the LLM harness for personalized story books. The harness is the system of materials, guidelines, and workflows that enable sub-agents (Gemini and ChatGPT) to help create meaningful, personalized books.

## Process

We're treating harness development as a team effort:

1. **Initial Plan Created** - Base plan developed with user context
2. **Sub-Agent Input** - Each sub-agent reviews plan and provides strategic input
3. **Consolidated Questions** - Questions from sub-agents broken into ADHD-friendly chunks
4. **Feedback Rounds** - Up to 2 rounds of back-and-forth with user (facilitated by coordinator)
5. **Final Harness** - Integrated design incorporating all perspectives

## Philosophy

**Invest in the harness to leverage AI effectively.** A well-designed harness ensures:
- Consistent quality across all books
- ADHD-friendly workflow for user
- Optimal use of LLM context windows
- Clear coordination between sub-agents
- Authentic, emotionally resonant final products

## Directory Structure

```
/harness-building/
  README.md                          # This file
  personalized_books_plan.md         # Main plan document
  
  /context/                          # Background and updates
    plan_updates_summary.md          # Summary of changes based on user context
    user_context.md                  # Key details about user's life and relationships
    
  /sub-agent-input/                  # Strategic input from each sub-agent
    gemini_input.md                  # Gemini's questions and suggestions
    chatgpt_input.md                 # ChatGPT's questions and suggestions
    consolidated_questions.md        # All questions organized for user
    
  /feedback-rounds/                  # User feedback and iterations
    round_01_questions.md            # First round questions (chunked)
    round_01_responses.md            # User's responses
    round_02_questions.md            # Second round questions (if needed)
    round_02_responses.md            # User's responses
    
  /final/                            # Completed harness design
    final_harness_plan.md            # Integrated final version
    changes_log.md                   # What changed and why
```

## Current Status

**Phase:** Setting up structure and gathering sub-agent input

**Next Steps:**
1. Send plan to Gemini for strategic review
2. Send plan to ChatGPT for strategic review
3. Consolidate their questions
4. Present to user in manageable chunks

## Team Members

- **Coordinator (Manus):** Facilitates process, breaks questions into chunks, tracks context
- **Sub-Agent 1 (Gemini):** Interview Architect, Narrative Designer, Quality Reviewer
- **Sub-Agent 2 (ChatGPT):** Content Organizer, Story Writer
- **User:** Final decision-maker, provides context and feedback
