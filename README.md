# ITIL-and-ITSM

What is ITIL?
-
- Information Technology Infrastructure Library
- Its a framework that provides best practices for delivering IT services
- It helps organizations manage risk, improve customer satisfaction, increase efficiency and ensure IT services align with business goals

- It includes processes like Incident management, Change management, Problem management and Service level management
- ITIL helps to
  - Provide structured and repeatable processes
  - Improve communication between IT and services
  - Supports digital transformation and Agile DevOps initiatives
  - Helps reduce costs, downtime and risks
 
--------------------------------------------------------------

Explain the difference between incident and problem
-
- Incident is an unplanned interruption or reduction in quality of IT service.
  - Its objective is to restore the service as quickly as possible
  - It focusses on immediate resolution
  - e.g :- User cant access mail (What aspect)
- Problem is underlying cause of one or more incidents
  - Its objective is to identify and eliminate root cause to prevent recurrence
  - It focuses on root cause analysis RCA and long term fix
  - e.g :- Mail server keeps crashing due to memory leaks (Why aspect)

- If server crashes its an incident. Investigating why server is crashed and implementing permanent solution is problem management
 
--------------------------------------------------------------

What is the purpose of SLA?
-
- Service Level Agreement
- Its a level of service a customer expects from service provider and metrics used to measure that service
- Its a formal agreement between service provider and customer that defines expected level of service.
- Its purpose is to set clear, measurable performance standards and ensuring accountability for service delivery
  - e.g :- SLA might specify that service desk will respond to critical incidents within 15 mins and resolve within 2 hrs
 
- In ITIL, Service Level Management (SLM) is a process that creates and monitors SLA
- e.g :-
  - 99.99% availability uptime per month of a system
  - Incident response time 15 mins for critical
  - Resolution time 4 hrs for medium priority
 
--------------------------------------------------------------

How to prioritize incidents?
-
- Incidents are basically prioritized based in impact and urgency, using matrix or predefined criteria
- Its essential to ensure most critical issues are resolved first, not just based on urgency but also on business impact
- Impact means the extent to which incident affects business, how many users or services are impacted
- Urgency means how quickly a resolution is required
- Critical incident affecting multiple users would be prioritized higher than minor incident affecting only one user
- P1 means it has highest priority and need immediate attention - Major app downtime, SLA getting violated
- P4 has lowest priority and can be scheduled or deferred - Service not working for one user
- P2 and P3 have medium priority - email service is slow for one department

--------------------------------------------------------------

What is CAB?
-
- Change Advisory Board
- Its a group responsible for accessing, prioritizing and authorizing changes to IT environment
- They evaluate, approve changes
- They ensure chanes are reviewed from all relevant perspectives like technical, business, security, risk and operations
- They review CRs (RFCs), assess impact and risk, approve/reject changes, recommend improvements to change process, schedule changes to avoid conflicts and downtimes

- e.g :- For prod DB upgrade - We propose change to CAB, they review, asks for rollback plans, impact on business hrs, test results and risk level. Based on this they approve change

--------------------------------------------------------------

How do you handle major incident?
-
- Major incidents are handled using a predefined process, involving rapid response, communication with stakeholders and co ordination of resources until incident is resolved. Minimizing businee impact
- During a major incident like data breach, incident manager would converge response team, update affected users and work to restore services as quickly as possible
- Steps
  - Identify the issue via monitoring tools, service desk, user query. Log it in ITSM tool. Categorize and assign the priority
  - Immediately communicate and escalate. Notify incident manager or on-call-lead. SAlert relevant app teams. Escalate to management and key stakeholders of business or IT heads
  - Form incident bridge
  - Technical investigation and workaround
  - Update the stakeholders
  - Implement the resolution and recovery
  - Conduct post incident review (PIR) or (RCA)
 
--------------------------------------------------------------

What is the purpose of problem management process?
-
- It aims to identify and resolve root causes of recurring incidents to prevent future disruptions
- It aims to minimize impact by implementing workarounds to reduce user impact while permanent fixes are developed
- It also provides insights and trends to improve infrastructure and processes over time
- 2 types of problem management :- Reactive and proactive

- If a web application crashes frequently, problem management would investigate underlying issues such as software bugs or inadequate server resources

--------------------------------------------------------------

What is known error?
-
- Its a problem that has a documented root cause and a workaround but has not yet been permanently resolved
- Its a part of problem management process. It comes after RCA of problem. Helps incident management quickly resolve future related incidents using documented workarounds

- Suppose we get incident related to known error, service desk can refer to them and apply workarounds.
- It avoids duplicate analysis and saves time as its already documented
- Lifecycle :- Incident occurs - Problem record created - Root cause identified as known error - Workaround documented - Create RFC for fix - Known error closed

--------------------------------------------------------------

What is a difference between service desk and help desk?
-
- Service desk provides single point of contact for users to request IT support and services to resolve IT issues
  - Focuses on overall service delivery and aligning IT with business needs
  - Its fully integrated with ITIL processes like incident, problem, change, SR and used ITSM platforms like ServiceNow, JIRA
- Help desk primarily focuses on resolving technical issues
  - It is primarily for incident resolution and technical troubleshooting
  - Handles basic support like password reset, printer issues
 
- Mail not working - Help desk troubleshoots and restores access. Service desk processes request and resolves incident while updating user and IT team

--------------------------------------------------------------

How to measure effectiveness of ITSM processes?
-
- Its essential to ensure IT services are delivering values to business, improving over time and aligned with customer expectations
- Using KPIs like MTTR, First call resolution rate, customer satisfaction scores, % of incidents resolved within SLA, no of reopened incidents - For incident management
- For change management KPIs are % successful changes, change failure rate, e changes count, time to implement changes

- A decrease in MTTR indicates incident management processes are improving, leading to less downtime for users

--------------------------------------------------------------

What is the purpose of change management process?
-
- It ensures changes in IT are planned, reviewed, approved and implemented with minimal disruption to services
- Before deploying change, CM would assess potential impact, obtain approval from stakeholders and schedule changes during maintenance window
- It ensures service continuity, improves communication with stakeholders in change

- Standard change :- Low risk pre approved and repeatable
- Normal change :- Goes through full assessment and approval process
- E change :- Implemented quickly to resolve major incidents

--------------------------------------------------------------

How to handle service outages outside of business hrs?
-
- Organization have predefined procedures for managing outages outside of business hrs like on call support and escalation process
- It requires clear plan, defined roles and effective communciation to minimize downtime and business impact

- Steps
  - Detect outages quickly
  - Trigger on call escalation (if no response within SLA)
  -  Log the incident
  -  Implement immediate workarounds
  -  Document all actions
  -  Perform PIR
 
- At midnight monitoring tool detects high CPU usage on prod DB. Cloudwatch alerts on call engineer. Engineer joins war room, rolls back recent patch and restores service. Then PIR is scheduled

--------------------------------------------------------------

What is the role of Config Management DB (CMDB) in ITSM ?
-


--------------------------------------------------------------

How to esnure continuous improvement in ITSM process?
-
- CI involves regularly reviewing processes, identifying areas of enhancement and implementing changes to increase efficiency and effectiveness
- It keeps IT services efficient. reliable and aligned with evolving business goals
- Its imp to enhance service quality and customer satisfaction. Adapt business needs and tech changes

- What is the vision
- Where are we now
- Where we want to be
- How to get there
- Take actions
- How to keep momentum going

--------------------------------------------------------------

What is role of automation in ITSM?
-
- It streamlines repetitive tasks, improves efficiency and reduces risk of human error in ITSM process
- Incident management :- auto assign tickets, route to correct team, trigger alerts
- SR management :- password reset, laptop provisioning
- Change enablement :- Auto create RFCs from devops tools, enforce approver flows, trigger change calender updates
- Problem management :- Auto detect trends from recurring incidents, create problem records
- SLA management :- Track response/resoution times, escalate before breach automatically


--------------------------------------------------------------

How have you implemented or managed Change Enablement processes in a CI/CD or DevOps environment?
-
- In my role as DevOps engineer, I was responsible for implementing and managing Change Enablement process in a CICD pipeline driven env wehre we pushed code to prod multiple times in a week
- We had risk-based and automated change classification approach :-
  - **Standard changes (Low risk)** :- Changes like config updates, security patches or IaC deployments were pre-approved
  - **Normal changes (Medium-high risk)** :- For major code deployments or DB migrations, we created CR like RFCs in Cherwell directly from GitLab pipeline using API integration. These changes were auto routed to CAB or pre-assigned approvers based on impact and risk
  - **Emergency changes** :- For hotfixes or critical prod issues, we followed e change process where approvals are obtained via ECAB on call and post validations are completed during PIR meetings
 
--------------------------------------------------------------

Write a change pipeline using jenkins declarative syntax
-
- Below pipeline is suited for env where Change enablement is integrated with devops practices
- It has change ID tracking enabled with staged deployment. Email notification is sent after post build actions.
- It also includes timeout for approvals to avoid stuck builds

--------------------------------------------------------------

Change pipeline for standard, normal and e change 
-

--------------------------------------------------------------

How do you ensure audit readiness and traceability in the change management process?
-
- Link every deployment to unique change ID from Cherwell
- Maintain detailed logs in CICD pipelines for all stages
- Store artifacts and approvals in VCS or ticketing tools
- Enable automated tagging in Git and jenkins for rollback/reference
- Coduct regular post change reviews

--------------------------------------------------------------

How have you integrated change management into a CI/CD pipeline? What challenges did you face?
-
- We've integrated CM into CICD by
  - Auto creating and updating CRs in Cherwell by jenkins
  - Triggering manual approvals (CAB/ECAB) using jenkins input steps for Normal/Emergency changes
  - Ensuring traceablity with Change ID in commit messages, build logs and deployment tags
 
- Challenges :-
  - Delays due to manual approvals slowing down delivery
  - Aligning fast devops cycles with traditional ITIL processes
  - Handling e changes without skipping audit trials
 
--------------------------------------------------------------

Describe your experience with Cherwell ticketing tool. How is the workflow?
-
- I have used Cherwell ITSM tool primarily for IM, CM, PM, SR

- **Initiation/Ticket creation** :- CR is created manually or triggered via integrated tools like Jenkins, serviceNow or email listeners
  - Key fields are Change type, requestor, description, implementation plan, rollback plan, start/end time, affected services
- **Initial review** :- Assigned a Change manager or co ordinator for validation
- Impact and risk assessment to be assessed by stakeholders
- Approval workflow for Standard (Auto), normal by CAB, E change by ECAB for expidited approval
- **Implementation** :- Upon approval chnage moves to scheduled and then in progress, Implementation team performs task
- **Reviews and closure** :- Post implementation review is conducted to verify success of change
- Then ticket is closed

--------------------------------------------------------------

How do you identify gaps in operational readiness before a change is implemented?
-
- Conduct a pre-implementation checklist like monitoring, backups, rollback plan, support handover
- Review change documentation for missing risk/impact analysis
- Validate if test results, signoffs, config updates are complete
- Ensure support teams and stakeholders are informed and ready

--------------------------------------------------------------

What kind of reports have you created for change governance meetings? What tools did you use?
-
- Change dashboard summary :- Total changes Normal, std, emergency. Status like open, approved, rejected, completed
- Change success/failure rate
- Pending approvals
- E change report :- Frequency, justification, success/failure. PIR summary
- Change collision and risk analysis :- High risk vs low risk count
- Compliance and SLA violations :- changed implemented without approvals. SLA breaches

--------------------------------------------------------------

How do you ensure all stakeholders are aligned and informed during a major system change?
-
- Identify stakeholders early like business people, IT ops, support teams and end users
- Send pre change communication
- Maintain central change record like any ticketing tool
- Hold pre change review calls
- Provide real time updates on slack, teams during implementation
- Port change review and rebrief to share outcomes, verify no open issues

--------------------------------------------------------------

Have you ever redesigned or improved an existing change enablement process? What was your approach and the result?
-
- Assessment of existing process :- Reviewed SLAs, identified delays, manual steps
- Stakeholder consultation :- to get feedback about practical challenges
- Process redesign :- Segregated normal vs emergency workflows clearly with proper ECAB routing. Integrated CICD pipelines with change tickets
- Automation :- For approvals of low-risk changes
