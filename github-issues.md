## Issues and Pull Requests

- Create an Issue for a feature, bug, or idea.
- Use Pull Request to commit your code.

## Labels

### Black

Every issue should have one of the following labels:

- **Feature** - A distinguishing characteristic of a software item (e.g., performance, portability, or functionality).
- **Bug** - An error, flaw, failure, or fault _found in released version_.
- **Idea** - A question or suggestion.

### Green

Set of skills required to close the issue. Basically it's a type of work.

- **Design** - HTML/CSS.
- **Code** - JavaScript.
- **Content** - Text, photos, videos.
- **Admin** - Deployment.

### Orange and Red

A group of optional labels to indicate one of most frequent blockers or the next required step. Examples:

- **Product Requirements** - Clarification is needed.
- **Code Refactoring** - Quick and dirty code should be refactored.
- **Team: Sales** - Dependency on another team or 3rd party.

## Description

### Features

1. Summary: What this feature is? Why do you want it?
2. Description: Decompose into small small incremental steps. Attach helpful artifacts:
  - **HTML/CSS** - Wireframes.
  - **Frontend** - Use cases.
  - **Backend** - Data models and methods (arguments, returns, etc).
  - **Content** - Drafts or samples.

### Bugs

1. Expected: What was the expected outcome?
2. Actual: What happened instead? 
3. Reproduction: How to recreate the problem?
  - Link to demo or repository with reproduction code.
  - Include system details e.g. the browser, library, or operating system version.
  - Paste error output or logs. 

## Milestones

- There is always open `Backlog` Milestone for Issues that may require triage or scheduled for future Releases. Move Issues from `Backlog` to the next Release Milestone when it's time.
  - _Open issues_ — Incoming questions or suggestions.
  - _Closed issues_ — Declined ideas or Pull Requests.
 
- Create a Milestone for the next Release. The only open Milestone with a Due Date.
  - _Open issues_ — Work in progress.
  - _Closed issues_ — Code is merged into `master` and deployed to production. 
  - Link to the Release in the description.

- When Release is published close the Milestone.

Example:
- **Backlog** - Open
- **v0.2 Advanced Version** - Open - Due Date: June 1, 2014
- **v0.1 Proof of Concept** - Closed 

## Assignee

- The issue should be assigned to the person whose work is required as the next logical step.