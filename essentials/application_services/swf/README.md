# Simple Workflow

- SWF is a fully-managed "work flow" service provided by AWS.
- A SWF workflow allows an architect/developer to implement distributed,
  asynchronous applications as a work flow.
- A workflow coordinates and manages the execution of activities that can be run
  asynchronously across multiple computing devices.
- SWF has consistent execution.
- Guarantees the order in which tasks are executed.
- There are no duplicate tasks.
- The SWF service is primarily an API which an application can integrate it's
  work flow service into. This allows the service to be used by non-AWS
  services, such as an on-premiuse data center.
- A workflow execution can last up to 1 year.

### Components of SWF

##### Workflow

A sequence of steps required to perform a specific task.
- A workfow is alos commonly referred to as a decider.

##### Activities

A single step (or unit of work) in the workflow.

##### Tasks

What interacts with the "workers" that are part of a workflow.

- Activity Task - tells the worker to perform a function.
- Decision Task - tells the decider the state of the work flow execution, which
  allows the decider to determine the next activity to be performed.

##### Worker

Responsible for receiving a task and taking action on it.
- Can be any type of component such as an EC2 instance, or even a person.
