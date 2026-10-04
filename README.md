# 🎙️ WordWise — Voice Vocabulary Learning Agent

WordWise is a browser-based voice vocabulary learning prototype designed to help users learn new words through **voice interaction, contextual practice, instant feedback, and spoken responses**.

The prototype focuses on making vocabulary learning more interactive than traditional flashcards by allowing users to speak naturally and receive feedback based on how they use a word in context.

---

## 🚀 Project Overview

The goal of WordWise is to create a simple voice-based vocabulary coach that can:

- Introduce vocabulary words
- Explain word meanings
- Pronounce words
- Accept spoken responses
- Understand whether the user is asking for a meaning or an example
- Evaluate how the user uses a vocabulary word in a sentence
- Provide contextual feedback
- Give example sentences
- Track learning progress and accuracy
- Respond using voice

The current prototype contains **20 vocabulary words**.

---

## ✨ Features

### 🎙️ Voice Interaction

Users can click **"Speak Answer"** and speak naturally.

The browser converts speech into text using the Web Speech API.

Example:

> "I am curious to learn more about AI."

WordWise processes the spoken sentence and evaluates its usage.

---

### 🔊 Text-to-Speech

WordWise can speak:

- Vocabulary words
- Word meanings
- Example sentences
- Feedback
- Session completion messages

This creates a two-way voice learning experience.

---

### 📖 Meaning Mode

Users can ask questions such as:

> "What does resilient mean?"

or

> "What is curious?"

WordWise identifies the request and provides the meaning of the current vocabulary word.

---

### 💡 Example Mode

Users can ask:

> "Give me an example sentence."

or:

> "Use the word in a sentence."

WordWise provides an example relevant to the current vocabulary word.

---

### ✍️ Sentence Practice

Users can create their own sentence using the vocabulary word.

For example:

> "I am curious to learn more about AI."

The system checks whether:

1. The target vocabulary word was used.
2. The surrounding context reflects the meaning of the word.

It then provides feedback such as:

- ✅ Excellent
- ✅ Good use
- ⚠️ Almost
- 💡 Try again

---

### 🧠 Context-Based Evaluation

Instead of requiring the user to repeat the dictionary definition, WordWise uses groups of related concepts and expressions for each vocabulary word.

For example, for **Curious**, the system recognizes expressions related to:

- learning
- knowing
- discovering
- understanding
- asking questions
- being interested

Therefore, different natural sentences can be accepted.

Example:

> "I am curious to learn more about AI."

and

> "She was curious about how the machine worked."

can both be recognized as meaningful uses of the word.

---

### 📊 Progress Tracking

The prototype tracks:

- Current word
- Words completed
- Correct answers
- Total answered questions
- Accuracy percentage

A progress bar also shows the user's position in the 20-word session.

---

## 📚 Vocabulary Set

The current prototype includes:

1. Curious
2. Resilient
3. Concise
4. Adapt
5. Insight
6. Empathy
7. Ambiguous
8. Innovative
9. Persistent
10. Articulate
11. Versatile
12. Elaborate
13. Inevitable
14. Cautious
15. Significant
16. Efficient
17. Authentic
18. Proactive
19. Skeptical
20. Collaborate

Each word contains:

- Meaning
- Multiple example sentences
- Related concepts
- Contextual keywords
- A learning hint

---

# 🛠️ Technology Stack

### Frontend

- HTML5
- CSS3
- JavaScript
- Web Speech API
- Speech Recognition
- Speech Synthesis

### Backend / Initial AI Integration

- Node.js
- Express.js
- dotenv
- OpenAI JavaScript SDK

### Development Tools

- Visual Studio Code
- Git
- GitHub
- Chrome Browser

---

# 🏗️ Project Architecture

### Current Free Prototype

```text
                User
                  │
                  ▼
          🎙️ Voice Input
                  │
                  ▼
      Browser Speech Recognition
                  │
                  ▼
             JavaScript
                  │
          ┌───────┴────────┐
          │                │
          ▼                ▼
   Intent Detection   Context Evaluation
          │                │
          └───────┬────────┘
                  ▼
           Feedback Engine
                  │
          ┌───────┴────────┐
          ▼                ▼
     Text Feedback    Speech Synthesis
          │                │
          └───────┬────────┘
                  ▼
               User
