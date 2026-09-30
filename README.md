# StudyMate AI

StudyMate AI is an AI-powered study assistant designed to help university students understand academic concepts, organize learning, and create personalized revision materials.

The product combines conversational AI with study-focused assistive actions such as summarization, flashcard generation, and practice quiz generation.

AI-generated content is not automatically treated as final. Students can review, edit, approve, reject, or regenerate generated materials before saving them.

## Core Experience

**Ask → Generate → Review → Approve/Modify → Save**

## Core Features

* **Conversational Study Assistant** — Ask academic questions and receive AI-generated explanations.
* **Content Summarization** — Summarize study materials into more manageable content.
* **Flashcard Generation** — Generate revision flashcards from provided study content.
* **Practice Quiz Generation** — Generate practice questions for revision.
* **AI Output Review** — Review, edit, approve, reject, or regenerate AI-generated content.
* **Fallback Handling** — Provide clear error messages and retry options when an AI request fails.

## Target Users

The primary users are university students who need support with:

* Understanding difficult academic concepts
* Reviewing course materials
* Preparing for exams and assessments
* Creating personalized revision materials
* Continuing learning with conversation context

The initial product scope prioritizes students.

## System Architecture

The planned architecture follows this flow:

**User → Next.js Frontend → Application Server → AI Provider → Application Server → Frontend → User**

The frontend is responsible for the user interface, interaction, forms, loading states, and displaying responses.

The application server handles request processing, validation, communication with the AI provider, and protection of private credentials.

The AI model provides explanations, summaries, flashcards, and practice quizzes.

A data layer is planned for saved study materials, conversation/session information, and user preferences when persistence is introduced.

> The complete system architecture diagram will be added to the `docs` directory.

## Technology Stack

* Next.js App Router
* React
* Vercel AI SDK
* OpenAI
* GitHub
* Vercel
* Future data storage layer

## AI Provider

StudyMate AI will initially use **OpenAI** as its AI provider.

The architecture is designed so that the AI provider can be replaced without requiring major changes to the frontend. The Vercel AI SDK provides an abstraction layer for the AI integration.

## State Management

The application will manage:

* Conversation history
* Current chat/session state
* Active AI actions
* Loading and error states
* AI-generated content under review
* Saved preferences as a future feature

Generated content follows a review lifecycle:

**Generating → Review → Approved / Edited / Rejected**

## Privacy & Security

StudyMate AI follows a data-minimization approach.

Private information such as:

* AI API keys
* Database credentials
* Private server environment variables
* Internal service credentials
* Sensitive server configuration

must remain on the server and must never be exposed to the browser.

AI-generated information will also be clearly identified, and users will be able to review generated study materials before saving or relying on them.

## Documentation

Project documentation is available in the `docs` directory:

* **Product Brief** — Product concept, target users, AI use cases, user journeys, architecture, acceptance criteria, and state-management decisions.
* **Risk Register** — Identified product, AI, privacy, security, accessibility, and UX risks with mitigation strategies.
* **System Diagram** — Visual representation of the planned system architecture.

## Project Status

**Phase 1: AI-Native Product Strategy & Frontend Architecture**

Current work focuses on defining the product concept, user journeys, system boundaries, AI integration strategy, security considerations, risk management, and frontend architecture.

The application implementation and deployment will follow the architecture defined during this phase.

## Deployment

The application will be deployed through **Vercel** with the GitHub repository connected for automatic deployments.

**Live URL:** Coming soon.
