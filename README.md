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
- 

