## Figure Out Which Tool To Use 

Salesforce provides multiple tools to automate your org’s repetitive business processes: Lightning Process Builder, Visual Workflow, Workflow, and Approvals. The automation tool that you need depends on the type of business process that you’re automating.

What to do when a record has certain values
Example: Notify the account owner when a related case is escalated.

Collecting information from users or customers and then doing something with that information
Example: Customer support uses a wizard to step through a call script, and cases are created based on the information that they enter.

How a record gets approved
Example: Managers approve their direct reports’ requests for vacation.


### What to Do When a Record Has Certain Values

Three of our tools can address this use case: Workflow, Process Builder, and Visual Workflow. Respectively, these tools create workflow rules, processes, and flows.

We recommend starting with Process Builder, especially for business processes that can be simplified to if/then statements. For example: if a case is escalated, then notify the account owner.

Process Builder includes almost all the functionality that’s available in workflow rules, and more. In fact, a single process can do what it would normally take multiple workflow rules to do. The only thing you can do with workflow that you can’t do with processes is send outbound messages without code. However, you can work around this limitation by calling Apex code from a process.

If the process is too complicated for the Process Builder or requires more advanced functionality, create a flow by using Visual Workflow. For example, create a flow to:
Use complex branching logic (if certain conditions are true, evaluate for further conditions)
Example: First, check whether a case is escalated. If the case is escalated, check the account’s region and route the case accordingly.

Sort through, iterate over, and operate on several records
Example: After an opportunity is closed and won, calculate the opportunity’s discount. Then apply that discount to all the related opportunity products.

### Get Information from Users or Customers and Do Something with It

If you need to build a wizard to collect information, Visual Workflow is the tool for you. Create a flow that displays information to and requests information from a user. Then take the information that they enter and perform actions in Salesforce with it.

For example, create a flow that walks customer support representatives through a call script. The flow uses information that the representative entered, such as the caller’s name and account number, to create a case that’s assigned to the right person.

You can add more complexity to the flow to match your business process. For example:
Route the representative to different screens, depending on earlier choices. This prevents the representative from doing things like trying to upsell a product to a customer who already bought that product.
Check whether the reported problem is blocking the customer’s business and the account is high-value. If so, the flow notifies the region director.

### How a Record Gets Approved
For example, when an employee requests time off, that time has to be approved by the employee’s manager. You need to ensure that when a time-off request is submitted for approval, the right person (the employee’s manager) receives the request.

To automate your organization’s processes for approving records, create approval processes.
