# 2.1 ADD Step 1: Review Inputs

| Category        | Details           |
| ------------- |:-------------|
| Design Purpose      | The purpose is to produce an efficient and sufficiently detailed design to support the construction of the Course Management System. |
| Primary Functional Requirements     | The primary use cases were determined to be: <br> UC-1: Because it directly supports the primary requirements of the system <br> UC-4: Because it directly supports the primary requirements of the system <br> UC-6: Because it directly supports the primary requirements of the system <br> UC-13: Because it directly supports the primary requirements of the system <br> UC-16: Because of the technical issues associated <br> UC-20: Because of the technical issues associated    |

### Quality Attribute Scenarios: The scenarios were described in Section 1.2. They have now been prioritized as follows:

| Scenario ID        | Importance to the Customer           | Difficulty of Implementation According to the Architect  |
| ------------- |:-------------:| :-----:|
| QA-1      | High | High |
| QA-2      | High      |   Low |
| QA-3 | High      |    Medium |
| QA-4 | Medium    | Medium |
| QA-5 | High | High|

### Constraints: All of the constraints discussed in Section 1.3 are included as drivers.

# 2.2 Iteration 1

### Selecting drivers
This is the first iteration of the ADD process on the CMS system. The iteration goal is to establish an overall system structure. The following influence that structure:

QA-1: Performance <br>
QA-2: Modifiability <br>
QA-3: Availability <br>
CON-2: Must be user friendly. Support Dutch and English. Max 3 clicks to reach any content. Single login to access all content. Consistent UI<br>
CON-3: All content must be accessible by disabled users <br>
CON-5: Must work and synchronize with secondary universities <br>

![Context Diagram](ContextDiagram.jpg)
**FIGURE 2.1** Context Diagram for the CMS System

**2.2.2 Elements of the System to Refine** <br>
This is a greenfield development effort (Cervantes, 2016). So the element to refine is the CMS system as a whole. See Figure 2.1 for details on this system. Using the textbook, refinement is done through decomposition.

**2.2.3 Design Concepts that Satisfy the Selected Drivers** <br>
In order to establish an overall structure the following design decisions were made:


| Design Decisions and Location | Rationale |
| :---------- | :---------- |
| Logically Structure the client and server part of the system using the Web based application architecture. | The rationale behind selecting this is we do not want to deploy the application on every students machine (CON-2), and students should be able to access this system where ever they want (QA-3 and QA-2). It needs to be accessible over the internet and we want to minimize client-side resources. <table><tr> <th>Alternative</th> <th>Reason for Discarding</th> </tr> <tr> <td>Rich Client Application</td> <td>Has to be deployed on users machine and we want portability</td> </tr> <td>Rich Internet Application</td> <td>Restricted Access to local resources and out performed when compared to Web based </td> <tr> </tr> <tr> <td>Mobile application</td> <td> The limitations that make this option not viable is the screen size, and resources available. </td> </tr> <tr> <td>Service Applications</td> <td>Application is used by humans so needs user interface.</td> </tr></table> |
| Physically structure the application using the Four-Tier Deployment | This deployment has the best security as due to accessibility needs, it allows the web server to reside in a publicly accessible network. <table><tr> <th>Alternative</th> <th>Reason for Discarding</th> </tr> <tr> <td>>4 Tier Deployment</td> <td>Not necessary for our application. Will increase complexity for little increased performance results</td> </tr> <td>< 3 Tier Deployment</td> <td>Not complex enough, need at least three tiers for the web based application as complex as ours. </td> <tr> </tr> <tr> <td>Distributed Deployment</td> <td>  The downside is that making modifications like adding tiers is expensive </td> </tr></table> |
| Code the User Interface using HTML, PHP, and Javascript | HTML and PHP is easy to code and Javascript allows easy access to server. HTML and Javascript is also very easy to code and make changes. |
| Creating relational database using MySQL | MySQL is easy to work with HTML and PHP to make connections directly to the database. |

**2.2.5 Sketch Views and Record Design Decisions** <br>

The diagram in figure 2.2 shows the sketch of the module view of the two reference architectures that were selected for the client and server applications. These have now been adapted according to the design decisions we have made. <br>

![Views Diagram](ViewsDiagram.jpg)
