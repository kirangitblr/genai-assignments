# CodeSentinel AI --- GitHub Code Reviewer Prompt Master Roadmap 🚀

> **For AI Trainers & Learners:** This document provides a step-by-step
> prompt roadmap to build the complete **CodeSentinel AI --- GitHub Code
> Reviewer** dashboard from scratch. Each prompt is written naturally
> from a user's perspective and can be copied directly into Visual
> Studio Code GitHub Copilot or another AI coding assistant.

------------------------------------------------------------------------

## 📌 How to Use This Roadmap

1.  Follow each **Phase** sequentially from 1 to 6.
2.  Copy the prompt inside **"📋 Copy-Paste Prompt for AI Assistant"**
    and paste it into GitHub Copilot Chat.
3.  After the AI completes that phase, run the **"🧪 User-Facing
    Verification Steps"** in your browser before moving to the next
    phase.
4.  Keep the UI source code clean, responsive, and easy to maintain.
5.  Use your existing n8n GitHub Code Reviewer workflow as the backend.
6.  Before final submission, test the complete flow: **UI → n8n Webhook
    → AI Code Review → UI Results**.

------------------------------------------------------------------------

# Phase 1: Creating the Application & Visual Design System

## 🎯 Phase Goal

Build the initial visual foundation for a professional AI-powered GitHub
Code Reviewer dashboard called **CodeSentinel AI**. Establish a modern
dark developer-focused theme, organization branding, typography,
responsive layout, and visual design system.

## 📋 Copy-Paste Prompt for AI Assistant

``` text
Build the foundation for an AI-powered GitHub Code Reviewer dashboard called "CodeSentinel AI".

Tagline:
"Intelligent Code Review. Better Software."

Create a modern, professional dark developer dashboard inspired by premium SaaS products and developer tools.

Use a deep navy background with subtle technical grid patterns, soft ambient blue and cyan background lights, clean high-contrast typography, and modern cards.

Brand colours:
Primary Blue: #2563EB
Accent Cyan: #06B6D4
Dark Background: #0F172A
Card Background: #1E293B
Secondary Background: #111827
Primary Text: #F8FAFC
Secondary Text: #94A3B8
Success: #22C55E
Error: #EF4444
Warning: #F59E0B

Use modern typography such as Inter, Outfit, or another professional developer-friendly font.

Create the main application structure including:
- A responsive page layout
- Header placeholder
- Main dashboard area
- GitHub review form area
- AI review results workspace placeholder
- Footer placeholder

Make the design responsive for desktop, tablet, and mobile devices.

Do not connect the UI to the backend yet. Focus only on the visual design system and application foundation.
```

## 🧪 User-Facing Verification Steps

-   [ ] Open the application in a web browser.
-   [ ] **Theme Check:** Confirm the application has a professional dark
    developer-focused appearance.
-   [ ] **Brand Check:** Confirm "CodeSentinel AI" and its visual
    identity are clearly represented.
-   [ ] **Layout Check:** Confirm the main dashboard sections are
    visible and well spaced.
-   [ ] **Responsive Check:** Resize the browser and confirm the layout
    adapts without horizontal overflow.

------------------------------------------------------------------------

# Phase 2: Building the Professional Header, Navigation & Review Controls

## 🎯 Phase Goal

Add a professional navigation system and the main GitHub Code Review
input controls.

## 📋 Copy-Paste Prompt for AI Assistant

``` text
Add a sleek, professional navigation bar to the existing CodeSentinel AI dashboard.

On the left, display a custom CodeSentinel AI logo or code/security-inspired icon and the brand name "CodeSentinel AI".

In the navigation area, include:
- Dashboard
- New Review
- About

On the right, add a small status badge showing that the AI Code Reviewer service is ready, with a subtle animated status indicator.

Make the navigation responsive and easy to use on desktop, tablet, and mobile devices.

Below the navigation, create the main GitHub Code Review control area.

Include:

1. GitHub Repository URL
   Placeholder:
   https://github.com/username/repository

2. Review Type dropdown with:
   - Full Code Review
   - Security Review
   - Performance Review
   - Code Quality Review
   - Best Practices Review

3. Additional Instructions textarea
   Placeholder:
   Add any specific review requirements or areas you want the AI to focus on.

4. A prominent button:
   "Start Code Review"

Design the form as a premium card with clear labels, useful helper text, accessible focus states, and suitable developer-related icons.

Do not connect the form to n8n yet.
```

## 🧪 User-Facing Verification Steps

-   [ ] **Header Check:** Scroll the page and verify the header remains
    professional and easy to access.
-   [ ] **Brand Check:** Confirm the CodeSentinel AI name and logo/icon
    are visible.
-   [ ] **Navigation Check:** Hover over navigation links and verify
    clear interaction feedback.
-   [ ] **Form Check:** Confirm all required input controls are visible
    and easy to understand.
-   [ ] **Responsive Check:** Confirm the form remains usable on mobile
    screens.

------------------------------------------------------------------------

# Phase 3: Building the Dashboard Workspace & Review States

## 🎯 Phase Goal

Create a clear AI review workspace with default waiting, loading,
success, and error states.

## 📋 Copy-Paste Prompt for AI Assistant

``` text
Create a professional AI Review Workspace for the CodeSentinel AI dashboard.

The workspace should be the main area where GitHub code review results are displayed.

By default, show a friendly waiting state with a code-review or AI-related icon and a message such as:

"Ready to review your code"

"Enter a GitHub repository URL, choose a review type, and start the AI analysis."

Create a loading state for when a code review is running.

During loading:
- Show a professional animated spinner or AI processing animation
- Display:
  "CodeSentinel AI is analysing your repository..."
- Show rotating progress messages such as:
  "Connecting to repository..."
  "Reviewing code quality..."
  "Checking for security concerns..."
  "Analysing performance..."
  "Generating recommendations..."

Create visual areas for:
- Success messages
- Validation messages
- Server errors
- Network errors

Use subtle professional animations. Avoid excessive visual effects.

Keep the workspace responsive and maintain the existing CodeSentinel AI branding.
```

## 🧪 User-Facing Verification Steps

-   [ ] **Waiting State Check:** Confirm the workspace displays clear
    instructions before a review starts.
-   [ ] **Loading State Check:** Confirm the loading animation and
    progress message area are visible.
-   [ ] **Error State Check:** Confirm the design has a clear place for
    friendly error messages.
-   [ ] **Responsive Check:** Confirm the workspace remains readable on
    smaller screens.

------------------------------------------------------------------------

# Phase 4: Interactive Validation & User Feedback

## 🎯 Phase Goal

Add client-side validation and professional feedback before sending data
to the n8n workflow.

## 📋 Copy-Paste Prompt for AI Assistant

``` text
Make the CodeSentinel AI GitHub review form interactive with client-side validation.

When the user clicks "Start Code Review":

1. Validate that the GitHub Repository URL is not empty.

2. Validate that the value is a valid URL.

3. Validate that the URL contains github.com.

4. Validate that a Review Type is selected.

For validation failures:
- Highlight the relevant field
- Show a clear inline validation message
- Keep the message friendly and understandable
- Do not send a request to the backend

When validation passes:
- Remove previous validation errors
- Prepare the interface for the loading state

Also support keyboard accessibility where appropriate.

Do not connect the n8n webhook yet if the API integration has not been implemented.

Keep all existing CodeSentinel AI design elements unchanged.
```

## 🧪 User-Facing Verification Steps

-   [ ] **Empty URL Test:** Click "Start Code Review" with an empty
    repository field.
    -   Verify a helpful validation message appears.
-   [ ] **Invalid URL Test:** Enter invalid text instead of a URL.
    -   Verify the field is rejected with a clear message.
-   [ ] **Non-GitHub URL Test:** Enter a valid URL that is not a GitHub
    URL.
    -   Verify the user is asked to provide a GitHub repository URL.
-   [ ] **Valid Input Test:** Enter a valid GitHub URL and select a
    review type.
    -   Verify validation messages disappear.

------------------------------------------------------------------------

# Phase 5: n8n Webhook Connection, Loading & Error Handling

## 🎯 Phase Goal

Connect the CodeSentinel AI frontend to the existing n8n GitHub Code
Reviewer workflow using a POST request and handle the complete request
lifecycle professionally.

## 📋 Copy-Paste Prompt for AI Assistant

``` text
Connect the existing CodeSentinel AI dashboard to an n8n GitHub Code Reviewer workflow using the JavaScript Fetch API.

Create a clearly visible configuration constant near the top of the JavaScript code:

const WEBHOOK_URL = "PASTE_N8N_PRODUCTION_WEBHOOK_URL_HERE";

When the user submits a valid form:

1. Disable the submit button to prevent duplicate requests.

2. Change the button state to show that the review is processing.

3. Activate the loading workspace.

4. Cycle through progress messages every few seconds:
   - "Connecting to repository..."
   - "Reviewing code quality..."
   - "Checking for security concerns..."
   - "Analysing performance..."
   - "Generating AI recommendations..."

5. Send a POST request to the n8n webhook with Content-Type application/json.

Send this JSON structure:

{
  "repositoryUrl": repositoryUrl,
  "reviewType": reviewType,
  "instructions": instructions
}

6. Handle successful responses.

7. Handle unsuccessful HTTP responses.

8. Handle network failures gracefully.

9. Handle empty API responses.

10. Do not expose raw technical stack traces to the user.

The UI should show a clear, friendly error message if the n8n service is unavailable or the request fails.

The application must support both plain-text and JSON responses from the webhook where possible.

Use the existing CodeSentinel AI visual design and keep the application responsive.
```

## 🧪 User-Facing Verification Steps

-   [ ] **Validation Test:** Confirm invalid input does not trigger a
    webhook request.
-   [ ] **Loading Test:** Submit valid data and verify the button
    becomes disabled.
-   [ ] **Progress Test:** Verify progress messages change while the
    request is running.
-   [ ] **Network Test:** Open Browser Developer Tools and verify a POST
    request is sent to the configured webhook URL.
-   [ ] **Error Test:** Temporarily use an invalid webhook URL and
    verify a friendly error message is shown.
-   [ ] **Duplicate Request Test:** Confirm multiple rapid clicks do not
    create duplicate requests.

------------------------------------------------------------------------

# Phase 6: Automatic Formatting of AI Code Review Results

## 🎯 Phase Goal

Display the AI-generated code review in a polished, readable, and
professional results dashboard.

## 📋 Copy-Paste Prompt for AI Assistant

``` text
Build the final CodeSentinel AI results experience.

When the n8n workflow returns a successful AI code review, display a prominent success state:

"CODE REVIEW COMPLETE"

Show the review in a clean, structured workspace.

Include sections where the AI response provides them:

- Overall Summary
- Critical Issues
- Security Analysis
- Performance Analysis
- Code Quality
- Best Practices
- Recommendations

The n8n response may be plain text, JSON, or a nested response object.

Create flexible response handling that safely extracts the review content.

Format the review content clearly:
- Recognize headings and display them with strong visual hierarchy
- Format bold text
- Format bullet and numbered lists
- Display code blocks in dark monospace containers
- If markdown tables are present, render them as readable responsive tables where practical
- Preserve useful line breaks

Add:
- A success badge
- Review completion timestamp
- Copy Review button
- Start New Review button

Copy Review should copy the complete review result to the clipboard.

Start New Review should reset the form, clear the previous result, and return the user to the initial review state.

Reveal the completed review with a smooth fade-in animation.

Re-enable the form after the review is complete or after an error occurs.

Keep the interface accessible and responsive on desktop, tablet, and mobile.
```

## 🧪 User-Facing Verification Steps

-   [ ] **Success Badge Check:** Confirm a clear success message appears
    after the AI review finishes.
-   [ ] **Formatting Check:** Confirm headings, lists, bold text, code
    blocks, and line breaks are readable.
-   [ ] **Copy Button Check:** Click "Copy Review" and confirm the
    result is copied to the clipboard.
-   [ ] **New Review Check:** Click "Start New Review" and confirm the
    form resets correctly.
-   [ ] **End-to-End Test:** Submit a valid GitHub repository, wait for
    n8n and the AI workflow, and confirm the final review appears in the
    UI.

------------------------------------------------------------------------

# 🎨 Organization Branding Summary

## Organization Name

**CodeSentinel AI Labs**

## Application Name

**CodeSentinel AI**

## Tagline

**Intelligent Code Review. Better Software.**

## Suggested Brand Personality

-   Professional
-   Intelligent
-   Secure
-   Developer-focused
-   Modern
-   Reliable

## Suggested Visual Style

-   Premium dark SaaS dashboard
-   Deep navy background
-   Blue and cyan accent lighting
-   Security and code-inspired icons
-   Clean cards with subtle borders
-   Clear visual hierarchy
-   Minimal but polished animations

------------------------------------------------------------------------

# 🧩 Suggested Project Structure

``` text
CodeSentinel-AI/
│
├── CodeSentinel_UI_Implementation.md
├── UI_Development_Prompt.md
├── README.md
│
├── index.html
├── style.css
├── app.js
│
├── n8n/
│   └── github-code-reviewer-workflow.json
│
└── screenshots/
    ├── n8n-workflow.png
    ├── ui-dashboard.png
    ├── ui-loading.png
    ├── ui-validation.png
    └── ui-review-results.png
```

------------------------------------------------------------------------

# 🧪 Final Application Testing Checklist

Before submission, test the complete application.

-   [ ] The n8n workflow starts with a Webhook node.
-   [ ] The workflow ends with a Respond to Webhook node.
-   [ ] The Webhook uses POST.
-   [ ] The frontend sends valid JSON to the webhook.
-   [ ] Invalid repository URLs are rejected by the UI.
-   [ ] The loading state appears during processing.
-   [ ] Duplicate submissions are prevented.
-   [ ] Successful AI reviews appear in the UI.
-   [ ] Errors are displayed clearly.
-   [ ] The application works on desktop.
-   [ ] The application works on tablet.
-   [ ] The application works on mobile.
-   [ ] The final n8n workflow screenshot is captured.
-   [ ] Final UI screenshots are captured.
-   [ ] Code review result screenshots are captured.
-   [ ] The complete source code is pushed to GitHub.

------------------------------------------------------------------------

# 🛠 Summary of Architecture & Technologies Used

-   **Frontend Core:** HTML5, CSS3, Vanilla JavaScript
-   **Frontend Logic:** Async/Await, Fetch API, DOM Manipulation,
    Client-side Validation
-   **Design System:** CSS Variables, Flexbox, Grid, Responsive Design,
    Animations, Accessible UI
-   **Typography:** Professional web fonts such as Inter or Outfit
-   **Backend Integration:** n8n Webhook using HTTP POST and JSON
-   **AI Processing:** Existing GitHub Code Reviewer workflow with the
    configured AI model
-   **Response Flow:** CodeSentinel AI UI → n8n Webhook → GitHub/HTTP
    Processing → AI Code Review → Respond to Webhook → CodeSentinel AI
    Results

------------------------------------------------------------------------

## 🚀 Final End-to-End Flow

``` text
User enters GitHub Repository URL
            ↓
User selects Review Type
            ↓
UI validates the input
            ↓
Frontend sends POST request
            ↓
n8n Webhook receives request
            ↓
GitHub Code Reviewer workflow processes repository data
            ↓
AI generates the code review
            ↓
Respond to Webhook returns the result
            ↓
CodeSentinel AI formats and displays the review
```

**Project:** CodeSentinel AI --- GitHub Code Reviewer\
**Organization:** CodeSentinel AI Labs\
**Tagline:** Intelligent Code Review. Better Software.
