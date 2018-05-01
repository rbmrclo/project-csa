# Operational Excellence

The operational excellence pillar includes operational practices and procedures
used to manage production workloads.

This includes how planned changes are executed, as well as responses to
unexpected operational events.

Change execution and responses should be automated. All processes and procedures
of operational excellence should be documented, tested, and regularly reviewed.

#### Design Principles

- Perform operations with code
- Align operations processes to business objectives
- Make regular, small, incremental changes
- Test for responses to unexpected events
- Learn from operational events and failures
- Keep operations procedures current

#### 3 Areas for Operational Excellence

- Preparation
- Operation
- Response

#### Best Practices - Preparation

- Effective preparation is required to drive operational excellence. Operations
  checklists will ensure that workloads are ready for production operation and
  prevent unintentional production promotion without effective preparation.

- Workloads should have:
  - Runbooks - operations guidance that operations teams can refer to so they
    can perform normal daily tasks.
  - Playbooks - guidance for responding to unexpected operational events.
    Playbooks should include response plans, as well as escalation paths and
    stakeholder notifications.

- In AWS, there are several methods, services, and features that can be used to
  support operational readiness, and the ability to prepare for normal day to
  day operations as well as unexpected operational events.

- Be sure that documentations does not become stale or out of data as procedures
  change. Also make sure that it is thorough. Without application designs,
  environmental configurations, resource configurations, response plans, and
  mitigation plans, documentation is not complete.

- If documentation is not updated and tested regularly, it will not be useful
  when unexpected operational events occur. If workloads are not reviewed before
  production, operations will be affected when undetected issues occur. If
  resources are not documented, when operational events occur, determining how
  to respond will be more difficult while the correct resources are identified.

##### Questions

- What best practices for cloud operations are you using?
- How are you doing configuration management for your workload?

#### Best Practices - Operations

- Operations should be standardized and manageable on a routine basis. The focus
  should be on automation, small frequent changes, regular quality assurance
  testing, and defined mechanisms to track, audit, roll back, and review
  changes.

- Changes should not be large and infrequent, they should not require scheduled
  downtime, and they should not require manual execution. A wide range of logs
  and metrics that are based on key operational indicators for a workload should
  be collected and reviewed to ensure continuous operations.

- In AWS, you can set up a continuous integration / continuous deployment
  (CI/CD) pipeline (e.g source code repository, build systems, deployment and
  testing automation). Release management processes, whether manual or
  automated, should be tested and be based on small incremental changes, and
  tracked versions. You should be able to revert changes that introduce
  operational issues without causing operational impact.

##### Questions

- How are you evolving your workload while minimizing the impact of change?
- How do you monitor your workload to ensure it is operating as expected?

#### Best Practices - Responses

- Responses to unexpected operational events should be automated. This is not
  just for alerting, but also for mitigation, remediation, rollback, and
  recoverly. Alerts should be timely, and should invoke escalations when
  responses are not adequate to mitigate the impact of operational events.

##### Questions

- How do you respond to unplanned operational events?
- How is escalation managed when responding to unplanned operational events?

#### Key AWS Services

- Preparation: AWS Config, AWS Service Catalog, Auto Scaling, SQS
- Operations: CodeCommit, CodeDeploy, AWS CodePipeline, CloudTrail
- Responses: CloudWatch
