# Shashank Saxena

## Submission checklist
*Mark checks as explained on this [link](https://docs.github.com/en/free-pro-team@latest/github/managing-your-work-on-github/about-task-lists#creating-task-lists), and remove this instruction*

- [X] `Steps to run the project` AND a `documentation` have been included in a README.md file at root of your project.
- [X] No `binaries/compressed` files have been added
- [X] You understand that a submission here is publicly visible. 
- [X] You have not plagialised, or blatently copied work; and this submission is your original work. (Code of ethics)

## Briefly write about the project that you have submitted from the perspective of the user.
The user can create an account as a client or therapist.
- He cannot create two client accounts or two therapists accounts with the same email
- Though he can create a therapist account and a client account with the same email
- He can delete his account, edit his name, id, email address associated with that account

A client he can journal his emotions: time, feeling, intensity. He can view past entries and view/edit/delete an entry.

A Therapist can create slots for sessions.

As a client he can send/receive mappings requests to/from therapists. And vice-versa. But not to the same type.

User can remove his request, reject/accept a received request. 

Once accepted, it becomes a mapping and
- Either of the user delete the mapping
- Both users can send each other messages
- By default journal accesss to the client is off. A client can turn on/off journal access for a mapped therapist. If on, the therapist can view client's journal
- A client can view available slots of a therapist and apply in them

Therapists can view requests for slots and accept a client's request, then it becomes a session.

Therapist can create private or shared notes in the sessions. And mark present/absent in case the client turns up or not.

Client can view his past sessions and shared notes in the session.

## Assumptions you have made for this project?
The main assumption the users aren't malicious entity actively trying to deceive the system. For that a lot of guardrails would have to be put in check.

## Did you learn anything new while doing this assignment? Please explain.
It was a really insightful assignment for. Irrespective of the outome, I've learnt a lot. I was introduced to a lot of new concepts like REST APIs, OpenAPI structure, swagger documentation, AWS as service, CLI version of AWS, using AWS CDK to create and deploy models, serverless databases, NoSQL databases and how do they function, testing APIs, testing APIs using Postman. And also practically using Git. And Java app structure, maven, springboot, concept of pom.xml. And developped my own approach to tackle the problem.

The only regret I have is taking too much time for the assignment. I feel had I been introduced to even some concepts before, I would made the assignment much faster and better.

## If you had more time, what enhancements will you make?
- User log in and authentication hasn't been implemented due to lack of time
- I have only implemented the required API.
- Once a mapping or removed the is removed from the database, though it still exists in the other tables. A better approach would have been to change the status to "delete" to keep a record of past entries. But that would require to query table then filter out deleted entries which would make the project complicated.
- In the given there is no way for a therapist to delete past slots without bookings, so once the time for a slot is completed it can be put in "no booking" category, for the therapist to delete or filter
- A client cannot see his requested sessions, so session request handling can be made better and more efficient

Shortcoming
- It doesn't current verify if a user edits his email, whether the email already exists in the database, and deny the operation. This is lead errors along the way
