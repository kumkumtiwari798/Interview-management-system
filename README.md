# Interview Management System
The Interview Management System is an application built using the Frappe framework to facilitate end-to-end interview management. It enables companies to manage job postings, candidates, interview schedules, and interviewer details in a structured manner.

## Features
  ### Job Description (JD) Web Page
    Details Displayed:
      Company Name
      Job Details (Description of the job role)
      Location
      Role (e.g., Frontend Developer)
      Work Type: Remote or Office
      Openings: Number of available positions
      Apply Button: A form for candidates to submit their application.

## Candidate Management
  ### Candidate's Data Doctype:
      Fields:
        Name: Candidate's name
        Experience: Years of experience
        Skills: Candidate's skill set
        Applied Role: Role the candidate is applying for
      Filter: Filter candidates by experience or role for easy management.
## Interviewer Management
  ### Interviewer Doctype:
      Fields:
        Name: Interviewer's name
        Contact: Interviewer's contact details
        Position: Interviewer's job position
        Department: Department the interviewer belongs to
        Address: Interviewer's address
      Data Import: Import interviewer data using Google Sheets CSV for quick setup.
## Interview Scheduling
  ### Interview Schedule Doctype:
      Naming Rule: Naming convention is cdn-role-intName for easy identification.
      Fields:
        Candidate Name: Linked to the Candidate's Data Doctype
        Interviewer Name: Linked to the Interviewer Doctype
        Role Applied: Job role the candidate applied for
        Interview Date: Scheduled date of the interview
        Status: Options include "Hired," "Rejected," and "In Progress," with color-coded indicators:
          Green: Hired
          Red: Rejected
          Yellow: In Progress
## Additional Functionalities
    Date Validation: Validates interview dates to avoid scheduling conflicts.
    Custom Buttons: Custom "Hire" and "Reject" buttons for easy candidate status updates.
    Alerts & Notifications:
      Welcome notifications for candidates upon application submission.
      Alerts on deleting candidate records.
    Data Access Control: Candidate data is submittable only after hiring, and email login is removed for simplification.
    Kanban Board:
      Categories: Organizes tasks as "To Do," "In Progress," and "Completed" for visual tracking of tasks.

## Installation
  Clone the repository from GitHub:
    git clone https://github.com/yourusername/InterviewManagementSystem.git

Navigate to the project directory:
    cd InterviewManagementSystem

Install the app on your Frappe site:
    bench --site your-site-name install-app InterviewManagementSystem

Start the Frappe server:
    bench start

## Usage
  Job Posting: HR can create a job posting with details about the position, allowing candidates to apply.
  Candidate Management: Filter and view candidate data, including experience and skills.
  Interview Scheduling: Schedule interviews for candidates with designated interviewers and update interview statuses.
  Kanban Board: Track the interview process visually from "To Do" to "Completed."

## Directory Structure
    InterviewManagementSystem/
      doctype/: Contains all Doctype configurations.
      config/: Stores app configurations.
      public/: Assets for public-facing content.
      workflows/: Defines workflows for the interview process.
      permissions/: Role-based access control configurations.

## Contributing
  Fork the repository.
  Create a new branch:
    git checkout -b feature-branch-name
  Commit your changes:
    git commit -m 'Add new feature'
  Push to the branch:
    git push origin feature-branch-name
  Create a pull request on GitHub.

## License
  This project is licensed under the MIT License.
