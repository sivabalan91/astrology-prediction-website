# Astrology Prediction Website

## Project Description

This project is an AI-powered Astrology Prediction Website that collects
user birth details through a web form, processes them using an n8n
automation workflow, generates personalized astrology predictions using
Groq AI, and delivers the results to the user's email.

------------------------------------------------------------------------

## Live Demo

**GitHub Pages URL:**\


**GitHub Repository:**\
https://github.com/sivabalan91/astrology-prediction-website.git

------------------------------------------------------------------------

## Architecture Overview

The system is built with the following components:

-   **Frontend:** HTML, CSS, JavaScript\
-   **Automation:** n8n Workflow\
-   **AI Engine:** Groq AI (llama-3.1-8b-instant)\
-   **Email Delivery:** SMTP through n8n Email Node

### Workflow Diagram

User → Web Form → n8n Webhook → Set Node → Groq AI → Email → User Inbox

------------------------------------------------------------------------

## Frontend to n8n Data Flow Explanation

1.  User enters:

    -   Name\
    -   Date of Birth\
    -   Time of Birth\
    -   Place of Birth\
    -   Gender\
    -   Focus Area\
    -   Email

2.  JavaScript sends POST request to:
    http://localhost:5678/webhook/astro

3.  n8n receives JSON data via Webhook node.

4.  Set node converts input into AI prompt (chatInput).

5.  Groq AI node generates astrology prediction.

6.  Email node sends formatted HTML email to user.

7.  Respond node returns confirmation to frontend.

------------------------------------------------------------------------

## AI Usage Explanation

-   **Model Used:** llama-3.1-8b-instant\
-   **Purpose:** Generate personalized astrology interpretation\
-   **Input Parameters:**
    -   Birth details\
    -   Focus area (Career, Health, Relationships, Education)
-   **Output:**
    -   Structured prediction text\
    -   Sun sign, moon sign interpretation\
    -   Guidance related to selected focus
-   **Formatting:**
    -   Output converted to HTML for Gmail alignment\
    -   Preserved paragraphs using
        ```{=html}
        <pre>
        ```
        styling

------------------------------------------------------------------------

## n8n Workflow Proof

Included in repository:

-   Exported workflow JSON:\
    /n8n/astro-workflow.json

-   Screenshots showing:

    -   Webhook node\
    -   Set node (chatInput)\
    -   Groq AI node\
    -   Email node\
    -   Respond node

------------------------------------------------------------------------

## Known Limitations and Assumptions

-   Predictions are AI-generated, not certified astrology calculations.\
-   Accuracy depends on user-provided birth details.\
-   Emails may go to spam depending on provider.\
-   System supports English language only.\
-   Requires active n8n instance and SMTP configuration.

------------------------------------------------------------------------

## How to Run Locally

1.  Open index.html in browser or use Live Server.\
2.  Start n8n workflow.\
3.  Submit form with valid email.\
4.  Check inbox for prediction.

------------------------------------------------------------------------

## Technologies Used

-   HTML5\
-   CSS3\
-   JavaScript\
-   n8n Automation\
-   Groq AI\
-   SMTP Email

------------------------------------------------------------------------

## Author

Astrology Prediction Project -- Academic Submission
