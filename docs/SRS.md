# Software Requirements Specification<br><br>Team 3

*December , 2019*

*Version 1*

*Prepared by: Bonoldi Enrico*

# Table of Contents

|     |
| --- |
|1 **INTRODUCTION**	|
| &nbsp;&nbsp; *1.1* Overview |
| &nbsp;&nbsp; *1.2* Goals and Objectives |
| &nbsp;&nbsp; *1.3* Scope |
| &nbsp;&nbsp; *1.4* Definitions |
|2 **GENERAL DESIGN CONSTRAINTS**|
| &nbsp;&nbsp; *2.1* PCTO Manager Environment |
| &nbsp;&nbsp; *2.2* User Characteristics |
| &nbsp;&nbsp; *2.3* Mandated Constraints |
|3 **NONFUNCTIONAL REQUIREMENTS** |
| &nbsp;&nbsp;*3.1* Operational Requirements|
| &nbsp;&nbsp;*3.2* Performance Requirements|
| &nbsp;&nbsp;*3.3* Security Requirements|
| &nbsp;&nbsp;*3.4* Documentation and Training|
| &nbsp;&nbsp;*3.5* External Interface|
| &nbsp;&nbsp;&nbsp;&nbsp; *3.5.1* User Interface|
| &nbsp;&nbsp;&nbsp;&nbsp; *3.5.2* Software Interface|
|4 **FUNCTIONAL REQUIREMENTS** |
| &nbsp;&nbsp;*4.1* Required Features|
| &nbsp;&nbsp;&nbsp;&nbsp; *4.1.1* Use Case: 1|
| &nbsp;&nbsp;&nbsp;&nbsp; *4.1.2* Use Case: 2|
| &nbsp;&nbsp;&nbsp;&nbsp; *4.1.3* Use Case: 3|
| &nbsp;&nbsp;&nbsp;&nbsp; *4.1.4* Use Case: 4|
| &nbsp;&nbsp;*4.2* Optional Features|
| &nbsp;&nbsp;&nbsp;&nbsp;*4.2.1* Use Case: 5|

Revision History

| **Version** | **Date** | **Name** | **Description** |
| --- | --- | --- | --- |
| 1 | 12/01/19 | Bonoldi Enrico | Initial Document |
___
*1* **Introduction**

*1.1* **Overview**

The PCTO manager will be a system that will be available for the ITIS G.Marconi to manage the PCTO activity.

The application will provide access to students data related to their PCTO activities.

The app will allow teachers to plan activities and students to report theirstatus about documentation .

This document provides information on the requirements for the PCTO manager software application.  Project goals, scope and definitions are given in the introduction.  Design constraints and application environment are described in the following section. Functional requirements are given to show the system features and expected user interaction.  Nonfunctional requirements give a better idea about the whole project.NonFunction

Project constraints will be included in separate documentation.  The Software Project Management Plan will give specifics on project budget and schedule.

*1.2* **Goals and Objectives**

The main objective of this project is to allow teachers a way to access PCTO schedules related to their students from any browser.

The PCTO Manager application is expected to:

1. Provide a system to manage data from and to Spaggiari (ETL).
2. Provide an API system to access PCTO data.
3. Provide a friendly web UI.

*1.3* **Scope**

The PCTO Manager application will provide users a method to access information about their students records about PCTO activities from any device via browser.

Users will be able to check and update their status about documentation or other legal stuffs through the web app.

*1.4* **Definitions**

**PCTO Manager**  **Application** – the product that is being described here; the software system specified in this document.

**Project** – activities that will lead to the production of the PCTO Manager application.

**Client** – the person or organization for which thisapplication is being built.

**User** – the person or persons who will actually interact with the PCTO Manager application.

**Use case** – describes a goal-oriented interaction between the system and an actor. A use case may define several variants called scenarios that result in different paths through the use case and usually different outcomes.

**Scenario** – one path through a user case

**Actor** – user or other software system that receives value from a user case.

**Developer** – the person or organization developing the system, also sometimes called the supplier.

**Stakeholder** – anyone with an interest in the project and its outcomes. This includes clients, customers, users, developers, testers, managers and executives.
___
*2* **General Design Constraints**

*2.1* **PCTO Manager Environment**

The PCTO Manager product will include a web app designed to work on any browser.

This application will interface with an API system served from a backend application of out design.

This API system will interface with the database.

The backend system will be designed to import and export data related to students and companies.

*2.2* **User Characteristics**

**PCTO Manager**  **Users** : ITIS G.Marconi students (3rd and 4th year), teachers and staff.

*2.3* **Mandated Constraints**

The application will run on any browser.

This platform was chosen based on experience with web development and backend systems.
___
*3* **Nonfunctional Requirements**

*3.1* **Operational Requirements**

Usability: Users will not need to read the user manual to be able to use the application as a prospective otherwise for a better usage is suggested to read the user manual.

Flexibility: the whole app is designed to support a lot of tabular data

*3.2* **Performance Requirements**

Maintainability: As any back/front system the app is splitted between presentation and business side, these are standalone.

*3.3* **Security Requirements**

The PCTO Manager app has a secury layer that allows to identify the entity as students or teacher.

Each User has is own pair of username and password.

The PCTO data is protected as private data and no other data is collected.

*3.4* **Documentation and Training**

The PCTO Manager application will be delivered to the school  as a web app.

A user guide and system documentation will be provided to project stakeholders.


*3.5* **External Interface**

*3.5.1* **User Interface**

The user interface will be friendly and clear.

When users access their accounts the interface will provide based on their entity type (student or teacher).

The interface will be intuitive.

As a web app it will be streamlined and simple to use.

Training will be provided to a close stakeholders group.

*3.5.2* **Software Interface**

The PCTO Manager API system will serve as an interface between the Web application and the frontend application.
___
*4* **Functional Requirements**

*4.1* **Required Features**

*4.1.1* **Use Case: 1**

**Description: User Login / Check**  **Entity Type**

Actors: Any application user

Value = high

Cost = medium

Basic Path

1. User access the URL for the web app.
2. If the user has a valid ID (token) the web App read it and authenticate the user otherwise shows up a login page.
3. The login page is defined by two text box with username and password.
4. If this pair is valid a new ID(token) is give to the user instance otherwise an error badge is prompt

*4.1.2* **Use Case: 2**

**Description:**  **Teacher companies/students view**

Actors: Any teacher

Value = high

Cost = medium

Basic Path

1. User clicks the user/company icon in the navbar.
2. User will be able to access/filter tabular that represents the selected resource.



*4.1.3* **Use Case: 3**

**Description: Teacher companies/students details view**

Actors: Any teacher

Value = high

Cost = medium

Basic Path

1. User clicks on any user/company row in the companies/students view table.
2. User will be able to access a section with details about the selected resource.

 *4.1.4* **Use Case: 4**

**Description: Student view**

Actors: Any student

Value = low

Cost = medium

Basic Path

1. User access the home page.
2. User will be able to access details about the account and the editable status of the his documentation.

*4.2* **Optional Features**

*4.2.1* **Use Case: 5**

**Description: Teacher edit companies/students details view**

Actors: Any teacher

Value = medium

Cost = high

Basic Path

1. User clicks on any user/company row in the companies/students view table.
2. User will be able to edit details about the selected resource.