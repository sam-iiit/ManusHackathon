Delegatr — AI-Powered Task Delegation for Teams
The problem: Managers waste hours figuring out who should do what — manually reading resumes, guessing at strengths, and chasing status updates.
The solution: Delegatr lets you drop in a task, your team's resumes, and GitHub profiles — and the AI handles the rest.

A manager enters a task in detail 
Enters employees and their resumes, git hub 
AI extracts the information by parsing
Automatically assigns roles to certain people based on their strengths
Shows a dashboard to show when people are finishing their tasks
Has a checklist format so that each employee can keep track of their work and check the work done to update the dashboard 





























Role and Objective: Act as an expert full-stack developer and AI systems architect. Your objective is to build a fully functional MVP of a web application called "Delegatr." This app uses AI to parse employee profiles and automatically assign project sub-tasks based on their strengths, while providing a real-time tracking dashboard.
Preferred Tech Stack:
Frontend: Next.js (App Router), React, Tailwind CSS, Shadcn UI (for clean, fast dashboard components).
Backend: Node.js (NestJS or Express) OR Python (FastAPI) to handle the AI orchestration smoothly.
Database: PostgreSQL (using Prisma or Drizzle ORM).
AI Integration: Use an LLM API (e.g., Gemini or OpenAI) for the parsing and matching engine.
Core Application Flows to Implement:
1. The Manager Flow (Input & Delegation):
Project Creation: A form where the manager inputs a detailed master task/project description (e.g., "Build a full-stack e-commerce site with Stripe integration").
Team Roster Input: A module where the manager adds employees. For each employee, the manager can input their Name, paste their Resume/CV text, and provide their GitHub profile URL.
The AI Delegation Engine (Crucial): Create a backend service that takes the master task and the array of employee profiles.
Step A (Extraction): The AI must parse the resumes and GitHub data to extract key skills, strengths, and experience levels for each employee.
Step B (Task Breakdown): The AI breaks the master task down into discrete sub-tasks.
Step C (Matching): The AI matches sub-tasks to the employees whose extracted strengths best fit the requirements.
Output: A proposed project plan showing who is doing what, and why (a brief 1-sentence AI justification for the assignment). The manager must be able to approve or manually edit this plan.
2. The Employee Flow (Execution):
Task View: A personalized checklist format for each employee showing their assigned sub-tasks.
Interaction: Employees can click checkboxes to mark sub-tasks as "In Progress," "Blocked," or "Completed."
3. The Global Dashboard (Tracking):
A central view for the manager displaying the overall project completion percentage.
Visual indicators (like progress bars or status badges) showing which employees have finished their tasks and who is currently working.
The dashboard must update dynamically as employees check off items on their individual lists.
Required Data Models (Schema outline):
Project: id, title, description, managerId, status, createdAt.
Employee: id, name, resumeText, githubUrl, extractedSkills (JSON array).
Task: id, projectId, assigneeId (foreign key to Employee), title, description, aiJustification, status (Pending, In Progress, Completed).
Execution Instructions for Manus:
Initialize the project: Set up the repository with the requested stack.
Database & Schema: Scaffold the database and implement the Prisma/ORM schema.
UI Components: Build the layouts for the Manager Dashboard, the Project Setup Wizard, and the Employee Checklist view.
AI Logic: Write the specific prompt logic and API call necessary to take the project description and employee array, and return a structured JSON response containing the matched tasks.
State Management: Ensure that when a task status is updated in the database by an employee, the manager's dashboard reflects the change.
Please generate the complete, deployable codebase for this MVP, including the necessary API routes for the LLM integration.



