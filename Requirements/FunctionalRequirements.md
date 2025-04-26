# Requirements List for Interview Scheduling and Resource Allocation System

## Functional Requirements

| **Requirement ID** | **Category** | **Requirement Name** | **Short Description** |
|:--|:--|:--|:--|       
| FR01      | Interviewer | Automatic WorkHourLogger filling         | The system should autofill WorkHourLoggers based on interviews conducted          |
| FR02      | Interviewer | Automatic  CandidateEvaluationSheet generation      | The system should create and pre-populate interview CandidateEvaluationSheets               |
| FR03      | Interviewer | Automatic comp-off allocation       | The system should automatically add leave days for interviews conducted outside regular hours |
| FR04      | Interviewer | Interview type preferences          | Interviewers should be able to set preferences for types of interviews  |
| FR05      | Interviewer | Tech stack preferences              | Interviewers should be able to specify and update their tech stack expertise and preferences |
| FR06      | Interviewer | Client calendar synchronization     | The system should sync with client calendars to accurately reflect availability |
| FR07      | Interviewer | Availability management             | Interviewers should be able to set and update their availability slots easily |
| FR08      | Interviewer | Interview capacity limits           | Interviewers should be able to set maximum interviews per week/month         |
| FR09      | Recruiter  | Interviewer search                  | Recruiters should be able to quickly search for suitable interviewers using natural language |
| FR10      | Recruiter  | Time Bound Interview Rescheduling   | The system should handle declined interviews by automatically finding alternatives within a stipulated time |
| FR11      | Recruiter  | Messengerbot assistance                  | A Messengerbot should help recruiters through natural language queries            |
| FR12      | Talent Ops | Panel pool management               | The system should maintain an up-to-date pool of interview panels with their skills |
| FR13      | Talent Ops | Messenger group creation                 | The system should automatically create google Messenger groups for interview coordination |
| FR14      | Talent Ops | Panel promotion tracking            | The system should track shadow-to-anchor promotions and update permissions |
| FR15      | Integration| MyMindComputeProfile integration                  | The system should rank skills from MyMindComputeProfile for accurate interview scheduling |
| FR16      | Integration| MindComputeScheduler integration                | The system should leverage and extend MindComputeScheduler functionality               |
| FR17      | Reporting  | Interviewer activity reports        | The system should generate reports on interviewer participation and metrics |
| FR18      | Reporting  | Interviewer leaderboards            | The system should display leaderboards at account, office, and country levels |
| FR19      | Reporting  | Process bottleneck identification   | The system should identify bottlenecks in the interview process             |
