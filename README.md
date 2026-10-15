# CareerForge: All-in-One Job Portal & Placement Preparation Platform

A full-stack web application designed for engineering students, freshers, and experienced software engineers to discover tech jobs and prepare for technical & HR interviews.

---

## 🌟 Key Modules

### 1. 💼 Job Portal
- **Browse & Filter Opportunities**: Filter jobs by role, work style (Full-time, Remote, Hybrid), and experience (Freshers, 0-2 yrs, 1-3 yrs).
- **Search Capabilities**: Instant search by company, job title, or required skills (React, Java, SDE, etc.).
- **Job Details Modal**: Comprehensive breakdown of responsibilities, requirements, CTC/compensation, and eligibility.
- **Easy Apply**: Submit candidacies with resume links, portfolio profiles, and personal cover notes.
- **My Applications Tracker**: Monitor submitted application status (`Applied`, `In Review`, `Shortlisted`).
- **Post a Job Form**: Recruiter portal for publishing new openings with instant persistence.

### 2. ⚡ Dedicated DSA Topic-Wise Sheet
- **Curated Problem Set**: Covering Arrays, Strings, Linked Lists, Stacks & Queues, Binary Trees, Graphs, and Dynamic Programming.
- **Interactive Checkbox Tracker**: Mark solved/unsolved with **confetti celebrations** on completion!
- **Multi-Language Solutions**: Interactive language switcher providing production-ready code snippets in **C++**, **Java**, **Python**, and **JavaScript** with one-click copy.
- **Complexity Breakdown**: Explicit Time & Space complexity analysis for every problem.
- **Direct Practice Links**: One-click shortcuts to **LeetCode**, **GeeksForGeeks**, and **YouTube video solutions** (Striver/NeetCode style).
- **Personal Revision Notes**: Built-in editor to jot down edge cases, intuition, and formulas, persisted to disk.

### 3. 🧠 Preparation Hub
- **Aptitude & Reasoning**:
  - **Quantitative Aptitude**: Time & Work, Speed Distance & Time, Percentages, and core formulas cheat sheet.
  - **Logical Reasoning**: Blood Relations, Syllogisms, and deduction patterns.
  - **Verbal Ability**: Sentence correction, grammar rules, and spotting errors.
  - **Interactive Practice**: Immediate feedback, option-checking, and step-by-step explanations.
- **Technical Core CS Subjects**:
  - **Operating Systems**: Processes vs Threads, Deadlocks, Bankers Algorithm, Paging & Virtual Memory.
  - **Database Management Systems (DBMS)**: ACID properties, Normalization (1NF to BCNF), Indexing, B+ Trees.
  - **Computer Networks**: OSI 7 Layers, TCP vs UDP, 3-Way Handshake, DNS & HTTP/HTTPS.
  - **Object-Oriented Programming (OOP)**: 4 Pillars (Encapsulation, Abstraction, Inheritance, Polymorphism) and SOLID principles.
  - **Subject Quizzes**: Interactive self-assessment quizzes with score calculation and answers.
- **HR Behavioral Interview Preparation**:
  - **The STAR Method Masterclass**: Situation, Task, Action, and Result structured blueprint.
  - **Top Frequent HR Questions**: "Tell me about yourself", "Why our company?", "Conflict resolution", "Strengths and Weaknesses".
  - **Sample High-Impact Answers**: Proven response scripts with rationale and traps to avoid.
  - **Smart Questions to Ask Interviewers**: Thoughtful questions to stand out in the final round.

### 4. 🏢 Company Hiring Process Directory
- **Company Profiles**: Detailed dossiers for top product companies (Google, Amazon, Microsoft) and IT service giants (TCS, Infosys, Accenture).
- **CTC & Roles**: Package tiers (e.g. TCS Ninja vs Digital vs Prime; Infosys SE vs DSE vs Specialist Programmer).
- **Eligibility Criteria Checklist**: Academic percentages (10th/12th/Graduation), active backlog rules, allowable study gaps, and eligible degrees.
- **Exam Patterns & Selection Rounds**: Test duration, platforms (TCS iON, HackerRank, Codility, CoCubes), negative marking, and round breakdowns.
- **Topic-wise Syllabus**: Quantitative, Coding, Core CS, and Behavioral expectations.
- **Candidate Strategy & Tips**: Practical insider advice from previously placed engineers.

---

## 🛠️ Tech Stack & Architecture

- **Frontend**: React (Vite), Tailwind CSS, Lucide React Icons, Canvas-Confetti
- **Backend**: Express.js REST API, Node.js
- **Persistence**: JSON-backed local storage file system (`jobs.json`, `dsaSheet.json`, `preparation.json`, `companyHiring.json`, `applications.json`, `userProgress.json`)

---

## 🚀 Quick Start Guide

### Prerequisites
- Node.js (v18+ or v24+)
- npm (v9+)

### Installation & Running

1. **Install dependencies**:
   ```bash
   cd server && npm install
   cd ../client && npm install
   ```

2. **Run the Full-Stack Application**:
   - **Option A: Production / Standalone Server (Port 5000)**:
     ```bash
     cd client && npm run build
     cd ../server && node src/index.js
     ```
     Access: **[http://localhost:5000](http://localhost:5000)**

   - **Option B: Vite Dev Server with Live Reload (Port 5173)**:
     ```bash
     # In terminal 1 (Express API):
     cd server && npm run dev
     
     # In terminal 2 (Vite Client):
     cd client && npm run dev
     ```
     Access: **[http://localhost:5173](http://localhost:5173)**

---

## 📡 REST API Reference

| Endpoint | Method | Description |
|---|---|---|
| `/api/jobs` | `GET` | List all tech jobs with search, type, and experience filters |
| `/api/jobs` | `POST` | Post a new job opportunity |
| `/api/jobs/:id/apply` | `POST` | Submit an Easy Apply application for a job |
| `/api/applications` | `GET` | Retrieve submitted job applications |
| `/api/dsa` | `GET` | Get topic-wise DSA problems with solve status and notes |
| `/api/dsa/:id/toggle` | `POST` | Toggle problem completion (solved/unsolved) |
| `/api/dsa/:id/note` | `POST` | Save personal revision notes for a DSA problem |
| `/api/prep/aptitude` | `GET` | Get aptitude formulas and practice MCQs |
| `/api/prep/technical` | `GET` | Get CS notes, interview Q&As, and quizzes |
| `/api/prep/hr` | `GET` | Get HR behavioral questions, STAR blueprint, and answers |
| `/api/companies` | `GET` | Get company hiring processes, exam patterns, and syllabi |
