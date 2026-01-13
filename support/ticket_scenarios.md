# Support Ticket Response Scenarios

## Instructions

For each scenario below, write a professional support ticket response as if you were responding to a real customer. Your response should be sent via email or ticketing system.

**What we're evaluating:**
- Clear, professional communication
- Empathy and customer focus
- Diagnostic thinking and problem-solving approach
- Ability to ask the right clarifying questions
- Setting appropriate expectations

**Submission Format:**
- Write your responses in a document named `your_name_support_responses.txt` or `.docx`
- Label each response clearly (Scenario 1, Scenario 2)
- There is no strict length requirement, but aim for responses that are thorough yet concise

---

## Scenario 1: Customer Reports Python Script Error

### Customer's Ticket:

**Subject:** Urgent - Data Export Script Failing

**From:** Sarah Martinez, Operations Manager at Acme Corp

**Message:**
> Hi Support Team,
>
> Our automated data export script stopped working this morning and we need this data for our weekly reports. I'm getting an error when I run it. Here's what it says:
>
> ```
> Traceback (most recent call last):
>   File "export_data.py", line 47, in <module>
>     process_records(data)
>   File "export_data.py", line 23, in process_records
>     formatted_date = record['date'].strftime('%Y-%m-%d')
> AttributeError: 'NoneType' object has no attribute 'strftime'
> ```
>
> This worked fine last week! Nothing has changed on our end. Please help ASAP as my team is waiting on this data.
>
> Thanks,
> Sarah

---



**Now, write your customer response using this answer, and make sure to:**
- Acknowledge the urgency and empathy for the customer's situation.
- Ask clarifying questions as needed to help diagnose (such as, "Are there any new records? Has the data format changed?").
- Offer the technical workaround above, mentioning you can help apply it.
- Explain next steps or set expectations for how you will follow up.
- Do not just copy-paste the above code or explanation; write it in your own words as if emailing the customer.


### Your Task:

Write a support ticket response to Sarah. Consider:
- How would you acknowledge her urgency while being realistic?
- What information do you need to diagnose this issue?
- What initial troubleshooting steps or explanations can you provide?
- How would you set expectations for resolution?

**Write your response below this line:**

**The answer to the technical problem is:**

The error is occurring because at least one of the records has a missing (`None`) value for the `date` field, so calling `.strftime()` on it fails. This may be due to new or changed data with null or blank dates. The script needs to check if `record['date']` is not `None` before calling `.strftime()`—for example:

```python
if record['date']:
    formatted_date = record['date'].strftime('%Y-%m-%d')
else:
    formatted_date = ''
```

**This is the answer for the technical issue. Write your response below this line providing the information above:**



---

## Scenario 2: Customer Asks "How Do I...?" Question

### Customer's Ticket:

**Subject:** Question about automating monthly reports

**From:** James Chen, Finance Analyst at TechStart Inc.

**Message:**
> Hello,
>
> I've been manually running the same report every month and exporting it to Excel, then doing some calculations and formatting before sending it to my manager. It's taking me about 2 hours each month.
>
> Someone mentioned that I might be able to use Python to automate this process, but I'm not really a programmer. Is this something your software supports? Can you help me set this up? I'd like to have it automatically email the formatted report to my manager on the first Monday of each month.
>
> Let me know what's possible.
>
> Thanks,
> James

### Your Task:

Write a support ticket response to James. Consider:
- How would you clarify what he's actually trying to accomplish?
- What questions do you need to ask to understand his requirements better?
- How would you explain the options available (even if you don't know the exact technical details)?
- How would you guide him toward next steps without overpromising?

**Write your response below this line:**

Good luck!
