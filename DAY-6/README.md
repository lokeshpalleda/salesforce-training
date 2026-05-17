Triggers, SOQL, & Ecosystem Basics
Repository Structure

/day6-triggers-soql/ - Core technical tasks and deep dives.
/light-completion-day/ - Ecosystem exposure and quick reflections.

Part 1: Core Technical Learning
What is SOQL?

SOQL (Salesforce Object Query Language) is used to search your organization’s Salesforce data for specific information. Unlike SQL, it is specifically designed for Salesforce objects and is used only for retrieving records (SELECT operations) rather than modifying them.

What is an Apex Trigger?

An Apex Trigger is a piece of code that executes before or after specific data manipulation language (DML) events occur, such as inserting, updating, or deleting records. They allow for custom automated actions that aren't possible through standard configuration.

Key Differences
Flow vs. Trigger

Flows are declarative (point-and-click) and preferred for simple automation like email notifications.

Triggers are programmatic (code) and used for complex logic, high-performance bulk processing, or external API integrations.

Before vs. After Trigger

Before triggers: Used to update or validate record values before they are saved to the database.

After triggers: Used to access field values set by the system (like a Record ID) and to affect changes in other related records.

Trigger Use Cases (College Management System)

Based on a College Management System, here are 5 automated cases:

Student Registration:

After a student record is created, automatically send a welcome email and generate a student ID.

Course Enrollment:

After a course reaches its maximum capacity, automatically notify the faculty head to open a new section.

Low Attendance:

After attendance data is updated, if it falls below 75%, trigger a warning notification to the student.

Fee Payment:

After a successful payment record is inserted, automatically update the student's "Eligibility Status" to active.

Faculty Assignment:

Before a course record is saved, verify if the assigned faculty is already teaching more than 3 courses.

5. English Query Examples
Find all students currently enrolled in "Course A".
List all courses currently handled by "Faculty X".
Retrieve all students whose attendance percentage is below 75%.
Reflection: Why Event-Driven Behavior?

Enterprise systems need event-driven behavior to ensure data integrity and real-time responsiveness. Instead of users manually checking for changes (polling), the system reacts instantly to data changes, reducing manual errors and increasing organizational efficiency.

Part 2: Ecosystem Exposure
Modules Completed

Search Solution Basics: Learned how Salesforce indexes data to find records efficiently.

Agentforce 360 Platform Events Basics: Explored how different systems communicate asynchronously through events.

Key Learnings
Search:

Fast, accurate search is vital in enterprise systems to maintain user productivity when dealing with thousands of records.

Platform Events:

A single action (like a "Payment Completed") can notify multiple internal and external systems simultaneously without them being directly linked.

CLI:

Developers prefer CLI because it allows for scripting, automation, and handling complex tasks much faster than clicking through multiple GUI screens.

Command-Line Interface (CLI):

Understood why developers use terminal-based tools for faster workflows.
