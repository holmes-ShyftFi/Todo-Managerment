### TODO MANAGEMENT – ODOO TRAINING MODULE SPEC 

Module name: training_todo
Purpose: This module is designed as a learning project for Odoo developers. It covers core Odoo concepts such as models, views, workflows, wizards, security, record rules, activities, cron jobs, and basic reporting. 

## 1. Functional Specification 
Overview: The module provides a Todo / Task management system where users can create, assign, track, and complete tasks. 

**User Roles:**
- Todo User: Manages only tasks related to them 
- Todo Manager: Manages all tasks and has full control 

**Core Features:**
- Task Management: Users can create, update, assign tasks, set priority and deadlines, and track progress. 
- Task Workflow: Draft → In Progress → Done → Cancelled 

**Rules:** 
- Done tasks cannot be edited 
- Only Todo Managers can cancel tasks 
- State changes must be logged 

**Views:** 
- List view with status and deadline 
- Form view with action buttons and chatter 
- Kanban view grouped by status 
- Search view with filters and group by options 

**Bulk Update Wizard: **
- Allows updating assigned user, deadline, and priority for multiple tasks. 
- Done tasks cannot be updated. 

**Notifications & Activities:** 
- Activities are created on state changes and approaching deadlines. 
- Overdue Handling: A daily cron job marks overdue tasks and creates reminder activities. 
- Reporting: Pivot and graph views for task analysis. 

## 2. Technical Specification 

**Todo Task Fields:**
- Title: Task name 
- Description: Task details 
- Owner: Task creator 
- Assigned User: Responsible person 
- Priority: Low / Normal / High 
- Deadline: Completion date 
- State: Task status 
- Is Overdue: Overdue indicator 
- Created Date 
- Last Updated 

**Bulk Update Wizard Fields:** 
- Assigned User 
- Deadline 
- Priority 

**Security:** 
Todo Users can only access their own or assigned tasks. 
Todo Managers can access all tasks. 

**Menus:** 
Todo 
- My Tasks 
- All Tasks (Manager only) 
- Reporting 
- Task Analysis 

**Non-Functional Requirements:**
- Follow Odoo best practices 
- No hardcoded IDs 
- Extendable and testable 

### Learning Objectives: Developers completing this module will understand Odoo fundamentals and be ready for real projects. 
