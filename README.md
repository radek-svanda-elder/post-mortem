# Post Mortem Template

Based on article [Incident Postmortem Template](https://medium.com/the-cloud-architect/incident-postmortem-template-7b0e0a04f7a8). You should read it first!

## Title:

*Descriptive title (Service XYZ failed, affecting customers in the EU region)*

## Incident date:

*Date of the event.*

## Owner:

*Name of the owner of the postmortem process.*

## Peer-review committee:

*List of people that will verify the quality of the postmortem before publishing it.*

## Tags:

*List of tags or keywords to classify the event and facilitate future search and analysis.*

*Example: Configuration, Database, Dependency, Latent*

## Summary:

*A summary of the event.*

## Supporting data:

*Metric graphs, tables, or other data, that best illustrate the impact of this event.*

## Customer Impact:

*Discuss customer-impact during the event. Explicitly mention the number of impacted customers.*

## Incident Response Analysis:

*Example of questions you could address:*

* *Was the event detected within the expected time?*
* *How was it detected? (e.g., alarm, customer ticket)*
* *How could time to detection be improved?*
* *Did the escalation work appropriately?*
* *Would earlier escalation have reduced or prevented the event?*
* *How did you know how to mitigate the event?*
* *How could time to mitigation be improved?*
* *How did you confirm the event was entirely mitigated?*

## Post-Incident Analysis:

*Example of questions you could address:*

* *How were the contributing factors diagnosed?*
* *How could time to diagnosis be improved?*
* *Did you have an actual backlog item that could’ve prevented or reduced the impact of this event? If yes, why was this item not done?*
* *Could a programmatic verification rule (e.g., AWS Config) be used to prevent this event?*
* *Did a change trigger this event?*
* *How was that change deployed — automatically or manually?*
* *Could safeguards in the deployment have prevented or reduced the impact of this event?*
* *Could this have been caught and rolled back during the deployment?*
* *Was this tested in a staging environment? If yes, why did this pass through? Could more tests have prevented or reduced the impact of this event?*
* *If this change was manual, was there a playbook? Was that playbook practiced, tested, and reviewed recently?*
* *Did a specific tool/command trigger the event? Could safeguards have prevented or reduced the impact of this event? Was there any safeguard triggered? If not, why none were in place?*
* *Was a production operation readiness or well-architected review performed on the system(s)? If not, why? When was the last evaluation done?*
* *Could a review have prevented or reduced the impact of the event?*

## Timeline:

*Detail all major event points with their time (included the timezone) with a short description.*

*Example:*

* *09:19 EEST — database run out of connections.*

*Link graph & log*

## Diving deep on contributing factors:

*Start with the problem.*

*Keep asking questions (e.g., why?) until you get to multiple contributing factors. **There is no single cause for failure**. So, keeping going!*

*Probe into different directions — tools, culture, and processes.*

***NEVER stop at human errors** (e.g., if an operator enters a wrong command, ask why no safeguards were in place, or why wasn’t the action peer-reviewed, and why didn’t that command have roll-back?)*

*Define action items against all contributing factors.*

## Lessons Learned:

*Describe what your team is taking away from this event.*

* *What did you learn that will help you in the future to prevent similar events?*
* *What unexpected things happened?*
* *What process broke down?*

*Lessons learned should correlate directly, if possible, with an action item.*

## Action items:

*List of action items with a title, an owner, due date, a priority, and a link to the backlog item created to follow up.*

*Example:*

* Evaluate shorter timeout for GET API 123, adhorn, July 3rd- 2020, high priority, link to a backlog item.
