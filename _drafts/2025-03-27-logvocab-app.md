---
layout: single
title: "LogVocab: Feature Brief"
date: 2025-03-27
tags:
  - Ngôn ngữ
---

Here is a brief outlining the proposed features for "LogVocab," designed to assist learners using an input-heavy method like [Refold](https://refold.la/).

## Core Concept

LogVocab is a desktop/web application designed to enhance the processing of text-based language input and facilitate reflective output practice, aligning with acquisition-focused learning methodologies. It bridges the gap between encountering language in text and activating it for use, with a strong emphasis on understanding word meanings in context and encouraging confident, natural output.

## Key Features

### 1. Input Processing & Meaning-Focused Card Creation (Stages 1-2 Focus)

*   **Text Import:** User pastes target language text (from articles, books, subtitles, transcripts).
*   **Interactive Reading Interface:** Displays the imported text.
*   **Targeted Unknown Identification:** User clicks on any word or phrase they don't fully understand within the text.
*   **Contextual Lookup & Sense Disambiguation (AI-Assisted):**
    *   Integrates with selected dictionaries (TL monolingual & bilingual).
    *   Uses AI (WSD) to analyze the sentence context and suggest the most probable meaning(s) of the clicked word/phrase.
    *   User confirms or selects the relevant meaning.
*   **Streamlined SRS Card Export:**
    *   Facilitates creating flashcards (e.g., for Anki) pre-populated with:
        *   The original sentence (context).
        *   The specific target word/phrase.
        *   The user-confirmed *meaning/definition*.
        *   (Optional) Links to audio or other relevant metadata.
*   **Implicit User Knowledge Tracking (Internal/Hidden):** Words/phrases processed within LogVocab that the user *does not* click are internally marked as "processed/encountered by user." *This data is NOT displayed to the user as stats during the input phase to avoid analysis paralysis.*

### 2. Output Auditing & Self-Reflection Prompting (Stage 3 Focus)

*   **Text Input:** User pastes their own written target language text (or a speech transcript).
*   **Fluency/Naturalness Analysis (AI-Assisted):**
    *   Uses general language models to identify phrases or constructions that are grammatically plausible but may be statistically uncommon, potentially non-idiomatic, or indicative of NL interference.
*   **Targeted Flagging:** Highlights these potentially awkward phrases within the user's text.
*   **Guided Self-Reflection Prompt:**
    *   Instead of direct correction, prompts the user when a flagged phrase is detected: _"This phrasing seems a bit less common. Can you think of another way to express this idea, perhaps using words/phrases you feel more confident with or have encountered frequently?"_
    *   Does **not** explicitly suggest alternatives based on the internal "processed" database, but encourages the user to access their own acquired language.

Okay, here is the English expression for point 3, the AI Conversation Partner feature:

### 3. AI Conversation Partner (Optional Early Introduction - Late Stage 1 / Stage 2+, Core for Stage 3):**

*   **Core Function:** Provides a real-time **spoken conversation** environment with an AI partner.
*   **Speech I/O:** Integrates speech recognition (Speech-to-Text - STT) and high-quality text-to-speech (TTS).
*   **Adaptive Difficulty (i+1 Capability):**
    *   **Leverages Implicit Data:** The LLM utilizes the list of "processed/encountered" words/phrases from Module 1 to **adjust the complexity** (vocabulary, sentence structures) of its responses, aiming to provide comprehensible **"i+1" input** tailored to the user.
*   **New Word Introduction & Support:**
    *   Optional setting for the AI to highlight or briefly explain key new words/phrases it introduces.
    *   Allows the user to quickly query the definition of a word the AI has just used.
*   **Feedback Mechanisms (Considered Approach):**
    *   Prioritizes **ensuring successful communication**. If the AI doesn't understand the user, it will ask for clarification, prompting self-correction.
    *   *May* offer gentle, non-intrusive feedback on significant grammatical errors or very clear pronunciation issues (if STT analysis capabilities permit), but avoids constant interruption.
*   **Integration with Module 1:** Enables the user to easily flag or "send" new vocabulary/phrases encountered *during the AI conversation* to the Input Processing module for later review and potential SRS card creation.

## Target User & Stage

*   Language learners using input-heavy methods (like Refold).
*   **Input Module:** Primarily useful from late Stage 1 through Stage 2 (during intensive reading/sentence mining from text).
*   **Output Module:** Primarily useful during Stage 3 (when beginning writing/speaking practice).

## Key Differentiators

*   Focus on disambiguating and learning specific **word senses** in context during card creation.
*   Output feedback emphasizes **awareness and self-reflection** prompting active retrieval, rather than direct AI correction or suggestions based on logged data.
*   Designed to **complement immersion**, not replace it, by streamlining text processing and output review without distracting statistics during input phases.

## Limitations

*   Primarily designed for **text-based input** (requires text or accurate transcripts).
*   Does not directly measure language acquisition (implicit tracking is a heuristic based on user interaction).
*   Accuracy depends heavily on the quality of integrated dictionaries and underlying NLP/AI models (especially WSD and naturalness detection).
*   Complements, but does not replace, varied immersion and feedback from native speakers.

---

## LogVocab & Refold Stage 1

**LogVocab Relevance in Stage 1:** LogVocab is **primarily useful in late Stage 1C**. Its relevance in 1A and 1B is minimal.

### Overall Stage 1 Goal
Lay the foundation for comprehension through tools, habits, basic building blocks (sounds/script), and core vocabulary/grammar awareness. Prepare for Stage 2 (learning from native content).

---

### Adapting Features for Stage 1

#### 1. Stage 1A: Setting Up Tools and Habits
    ##### Goal:
    Start immersion habits, set up Anki, build tolerance for ambiguity.
    ##### LogVocab Use:
    **Minimal / Not Recommended.**
    *   Focus should be on *starting to consume* TL content (even with NL subs initially, then moving away) and establishing daily Anki reviews (perhaps with a pre-made frequency deck first).
    *   LogVocab processes specific texts, which is premature when the focus is just getting comfortable with the *act* of immersion and basic tool setup. Trying to analyze text at this point might add unnecessary complexity.

#### 2. Stage 1B: Learning the Building Blocks
    ##### Goal:
    Learn phonetics (sound awareness), learn the writing system.
    ##### LogVocab Use:
    **Minimal / Ancillary.**
    *   **Phonetics:** LogVocab is not designed to teach sounds. External resources are required.
    *   **Writing System:** LogVocab *assumes* basic script recognition. While pasting text provides exposure, dedicated script learning tools/methods are needed *before* LogVocab becomes practical for processing sentences.
    *   *Potential Minor Use:* Once a user can *recognize* characters/letters, they could *theoretically* paste individual words learned during script study into LogVocab to facilitate lookup or linking to audio, but this isn't its core function and other tools might be better.

#### 3. Stage 1C: Jumpstarting Your Comprehension
    ##### Goal:
    Study basic grammar (for understanding), learn ~1500 common words via SRS (recognition cards), practice SRS habits.
    ##### LogVocab Use:
    **Relevant & Potentially Valuable (Input Module Only).**
    *   **Primary Use Case:** Supplementing frequency list study by providing contextualized SRS cards from *very simple* texts.
    *   **Text Import:** User pastes **simple target language text** (e.g., from graded readers, simple children's stories, potentially basic textbook dialogues if used sparingly).
    *   **Interactive Reading:** User reads the simple text in the interface.
    *   **Targeted Unknown ID:** User clicks on common words they encounter in the text that they don't yet know (likely cross-referencing with the goal of learning the ~1500 common words).
    *   **Contextual Lookup (Stage 1 Focus):**
        *   LogVocab facilitates lookup of the clicked word.
        *   **Emphasis on TL -> NL (Bilingual) Dictionaries:** Provides simple, direct meaning/translation suitable for beginners. (Monolingual support is for later stages).
    *   **Streamlined SRS Card Export (Stage 1 Focus):**
        *   Exports a **recognition card** (TL word/sentence on front).
        *   Back of the card contains the **NL meaning/translation** obtained from the bilingual lookup.
        *   (Optional) May include basic audio if available/integrated.
    *   **Implicit Tracking:** Internally logs "processed" words, but this data remains hidden and unused at this stage.
    *   **Output Auditing Module:** **Completely Disabled / Irrelevant.** No output practice occurs in Stage 1.

### Summary for Stage 1 LogVocab Use

*   **Not needed for 1A/1B.** Focus on core Refold activities for those stages.
*   **In late 1C, LogVocab's Input Module can be used as a *supplementary* tool:**
    *   To process **very simple texts**.
    *   To easily look up **bilingual meanings** of unknown *common* words found in context.
    *   To quickly create **TL -> NL recognition flashcards** for Anki, complementing study from frequency lists or pre-made decks by adding contextual examples.
*   The tool should prioritize **bilingual dictionary integration** for Stage 1 use.
*   The advanced features (output auditing, monolingual support, complex stats) are **not used** in Stage 1.

LogVocab in Stage 1 essentially acts as a basic "Reading Assistant + Bilingual Lookup + Recognition Card Creator" specifically for processing simple texts and feeding an SRS like Anki with contextualized common words.

---

## LogVocab & Refold Stage 2

**LogVocab Relevance in Stage 2:** The **Input Processing & Card Creation Module** becomes the central, highly relevant feature throughout Stage 2. The Output Module remains disabled/irrelevant.

### Overall Stage 2 Goal
Build comprehension from basic (Level 1-3) up to comfortable understanding (Level 5) of native content within a specific domain, primarily learning directly from immersion materials via sentence mining.

---

### Adapting Features for Stage 2

#### 1. Stage 2A: Overcoming the Curve
    ##### Goal:
    Reach Level 3 comprehension (gist) in easier native content (e.g., adolescent shows, simple slice-of-life). Start basic sentence mining (1T cards). Drop NL supports. Focus on a domain.
    ##### LogVocab Use:
    **Core Tool for Basic Sentence Mining from Text.**
    *   **Text Import:** User pastes subtitle files (extracted from videos), simple web articles, or potentially OCR'd comic text related to their chosen domain.
    *   **Interactive Reading Interface:** User reads the text, likely encountering many unknowns.
    *   **Targeted Unknown Identification:** User clicks unknown words/phrases. **Focus is on finding 1T (one target) sentences.** LogVocab could *potentially* assist by highlighting sentences where only one word wasn't previously "processed" by the user (using the hidden internal data as a heuristic), but manual identification by the user remains primary.
    *   **Contextual Lookup (Still Bilingual Primary):**
        *   Defaults to **TL -> NL (Bilingual) lookup** for efficient understanding.
        *   AI-assisted WSD helps quickly find the relevant meaning for the context.
    *   **Streamlined SRS Card Export (Basic Sentence Cards):**
        *   Facilitates creating **Text Sentence Cards** (TL sentence on front).
        *   Back of card contains the **NL meaning/translation**.
        *   Emphasis on exporting cards based on 1T sentences found in the text.
        *   Audio linkage (if feasible) adds value.
    *   **Implicit Tracking:** Internal logging of "processed" words continues silently.

#### 2. Stage 2B: Expanding Your Domain
    ##### Goal:
    Reach Level 4 comprehension (story) in native adult content. Advanced sentence mining (varied card formats). Casual monolingual transition (for related languages). Handle more difficult content.
    ##### LogVocab Use:
    **Supports Advanced Mining & Monolingual Transition.**
    *   **Text Import:** Handles more complex texts (native adult subtitles, blog posts).
    *   **Interactive Reading:** User reads, ideally clicking fewer unknowns per sentence.
    *   **Targeted Unknown ID:** User continues clicking unknowns, still often seeking 1T sentences but potentially exploring other card formats.
    *   **Contextual Lookup (Transition Phase):**
        *   Integrates **TL Monolingual Dictionaries**.
        *   **Crucial Feature:** When user clicks an unknown, LogVocab **shows the Monolingual definition first**.
        *   Provides an easy toggle/button to **reveal the Bilingual definition** if the monolingual one is too difficult. Supports the "check mono first, fall back to bi" workflow.
    *   **Streamlined SRS Card Export (Advanced Formats & Monolingual):**
        *   Supports creating different card formats (Text Sentence, potentially Text Vocabulary if user prefers).
        *   **Key Feature:** Easily incorporates the **Monolingual definition** onto the card back (potentially alongside the bilingual one, perhaps using hidden HTML summary tags as discussed).
        *   User can choose which definition(s) to include.
    *   **Implicit Tracking:** Continues silently.

#### 3. Stage 2C: Mastering Comprehension
    ##### Goal:
    Reach Level 5 comprehension (comfortable, near-perfect) in the focused domain (e.g., slice-of-life), without supports. Structured monolingual transition (if needed). Optional pure listening/novel reading. Prepare for Stage 3 output.
    ##### LogVocab Use:
    **Primary Monolingual Tool & Advanced Mining.**
    *   **Text Import:** Handles native content, potentially including longer texts like novel excerpts (if user opts for reading).
    *   **Interactive Reading:** User reads with significantly fewer clicks, focusing on less common words, nuances, or confirming understanding.
    *   **Targeted Unknown ID:** Clicking is less frequent.
    *   **Contextual Lookup (Monolingual Default):**
        *   Defaults to **TL Monolingual lookup**. Bilingual lookup becomes a deliberate exception.
        *   **Structured Transition Support:** Supports recursive lookups (clicking words *within* a monolingual definition to see *their* definitions). Facilitates adding both definitions to cards for the structured approach.
    *   **Streamlined SRS Card Export (Monolingual Focus):**
        *   Focus is on creating cards with **Monolingual definitions** on the back.
        *   May assist in creating cards for words found *during* recursive definition lookups.
    *   **Implicit Tracking:** Continues silently. Its potential utility for later output analysis grows as more data accumulates, but remains hidden.

### Summary for Stage 2 LogVocab Use

*   LogVocab's **Input Module** is a central tool throughout Stage 2, evolving with the learner's needs.
*   It starts as a basic sentence miner using bilingual lookups (2A).
*   It transitions to support monolingual dictionary usage, offering bilingual as a fallback (2B).
*   It becomes a primary tool for monolingual understanding and card creation, supporting recursive lookups (2C).
*   It streamlines the creation of context-aware SRS cards (1T sentences initially, potentially more varied later, with evolving definition types).
*   The **Output Module remains disabled/unused**.

LogVocab acts as an intelligent reading and sentence mining assistant, adapting its dictionary priority and card creation options to match the learner's progression through the stages of comprehension building and the monolingual transition described in Refold Stage 2.

---

## LogVocab & Refold Stage 3

**LogVocab Relevance in Stage 3:** Both the **Input Processing Module** and the **Output Auditing Module** become highly relevant, supporting different aspects of Stage 3 goals.

### Overall Stage 3 Goal
Transition from comprehension mastery to speaking ability. This involves activating latent language, practicing pronunciation, and engaging in real conversation, focusing first on the "everyday conversation" domain.

---

### Adapting Features for Stage 3

#### 1. Stage 3A: Preparing for Output
    ##### Goal:
    Overcome output aversion, achieve Level 5 comprehension in the "everyday conversation" domain, adopt and understand a language parent.
    ##### LogVocab Input Module Use:
    **High Relevance for Domain Acquisition.**
    *   **Text Import:** User pastes text from conversational sources: chat logs (public or private exchanges), forum discussions, blog comments, social media posts, emails, simple messaging apps, transcripts of language parent (if available), transcripts of interviews/casual conversations.
    *   **Interactive Reading:** Read and process this often messy, informal language.
    *   **Targeted Unknown ID:** Click on slang, idioms, conversational fillers, abbreviations, discourse markers, and common expressions used in everyday speech.
    *   **Contextual Lookup (Monolingual Default):** Use monolingual lookups to understand nuances. Bilingual fallback remains available for very tricky slang/idioms.
    *   **Streamlined SRS Card Export:** Create cards specifically for conversational language encountered. Crucial for building the vocabulary/phrase bank needed for output.
    *   **Implicit Tracking:** Continues silently, building a richer profile of "processed" conversational language.
    ##### LogVocab Output Module Use:
    **Low Relevance / Optional.**
    *   While the user starts basic writing (journaling, simple chats), the focus is just *starting*. Formal auditing might be premature and add pressure. The self-reflection prompts aren't the priority yet; just getting words out is.

#### 2. Stage 3B: Deliberate Practice
    ##### Goal:
    Activate acquired language via writing practice, build pronunciation muscle memory (shadowing), reach Level 6 comprehension of language parent.
    ##### LogVocab Input Module Use:
    **Moderate Relevance (Targeted Input).**
    *   Continued use for reinforcing conversational language and parent's speech patterns (aiming for Level 6).
    *   May be used more selectively to analyze texts related to specific topics the user is trying to write/talk about, filling known gaps.
    ##### LogVocab Output Module Use:
    **High Relevance & Core Use Case.**
    *   **Text Input:** User pastes their practice writing (text chats with partners, iTalki messages, tutor corrections, journal entries, longer-form writing).
    *   **AI Flagging & Prompting:** The AI identifies potentially awkward/uncommon phrasing. The user is prompted to self-reflect: *"Can you think of another way... using words/phrases you feel more confident with?"*
    *   **Supports Language Activation:** This directly aids the process described in Refold 3B. It encourages retrieving known-but-perhaps-less-available language, calibrating certainty, and moving away from NL interference or simple guessing.
    *   **Feedback Loop:** Helps identify areas where activation is weak or acquisition is incomplete, guiding the user back to targeted input or confirming correct usage.

#### 3. Stage 3C: Speaking
    ##### Goal:
    Engage in real conversation, improve speaking performance (reduce gap with competence), refine pronunciation/intonation/mannerisms.
    ##### LogVocab Input Module Use:
    **Ongoing Relevance (Refinement & Expansion).**
    *   Analyze transcripts of native conversations (talk shows, podcasts, recorded exchanges) to specifically study features like fillers, backchanneling, interruptions, prosody cues.
    *   Process input related to *new* domains the user wants to start talking about (preparing for Stage 4).
    *   Continue processing language parent content for deeper imitation.
    ##### LogVocab Output Module Use:
    **High Relevance (Reviewing Spoken Output).**
    *   **Text Input:** User pastes **transcripts** of their *own recorded* monologues or conversations (obtained via transcription service or manual typing).
    *   **AI Flagging & Prompting:** Same function as 3B, but now applied to the nuances and pressures of spoken language. Helps identify performance errors (slips under pressure) vs. underlying competence gaps revealed during speech.
    *   **Supports Performance Improvement:** The self-reflection prompt helps the user analyze *why* they might have chosen a less-than-ideal phrase during speech. Was it pressure? Did the right word not come? Was it a competence gap?
    *   **Complements Native Feedback:** Allows for detailed self-review between sessions with tutors or partners, focusing attention on areas flagged by the AI before seeking external confirmation or correction.

### Summary for Stage 3 LogVocab Use

*   The **Input Module** remains crucial in 3A for mastering the conversational domain and understanding the language parent, then serves for targeted input and refinement in 3B/3C.
*   The **Output Module** becomes a central tool starting in 3B for writing practice review and continues strongly in 3C for analyzing transcribed spoken output.
*   Its core function in Stage 3 is **facilitating self-reflection on output**, prompting users to access their acquired language more effectively and naturally, rather than simply correcting errors.
*   It helps bridge theory (Refold roadmap stages/concepts) and practice (analyzing user's actual output and guiding improvement).

LogVocab in Stage 3 supports the transition to output by helping learners acquire the necessary conversational input, then providing a structured way to reflect on their own writing and transcribed speech, encouraging reliance on acquired language and fostering the development of natural phrasing intuition.
