

# API development governance lifecycle

## Alignemnt Stage
| Title | Description |
| ----------- | ----------- |
| Input       | API change request.       |
| Process        | 1. Define job story narrative to specify outcomes. Reference stories to the appropriate  feature, epic and story it is aligned to. <br /> 2. Define or update the digital capabilities required to fulfil the job. <br />  3. Define the activities and activity steps linked to the digital capability.      |
| Output       | - Alignment of API change with wider organizational goals and features documented.  <br />  - API business capabilities defined <br />  - API job description updated   |
| Checkpoint       | API business owner and API designer review the change. |
| Exit Pre Conditions       | - job-stories.md updated. <br /> - activities.md updated with business capabilities.  <br /> - activity-steps.md updated with activity steps. <br /> - API business owner approves the change.  |
| Roles involved       | - API business owner   <br /> - API designer <br />     |

## Definition Stage
| Title | Description |
| ----------- | ----------- |
| Input       | - Job story narrative <br />  - Activities   <br />  - Activity steps  <br />   |
| Process       | 1. Capture API profile basics: name, description and scope.  <br /> 2. Capture API operation names (using lowerCamelCase()) and participants based on activity steps.    <br />  3. Identify the resources. Resources are usually domain entities operated on by the API.   <br />  4. For each resource, create a table and caputre its description and essential properties (ignore others). <br /> 5. Define the resource taxonomy. A taxonomy is a classification of concepts and the reletionships between them. There are three relationship types for the API resources -  independent (exists standalone), dependent (existence tied to a parent resource) and associative (relationship between the resources requires additional information specified by a third resource). <br /> 6. Add operation events. Helpful for analytics and understanding the events other systems will react to. <br /> 7. Add operation details:  important input and output details. E.g is the operation synchronous or asynchronous ? Safe (no state change) or unsafe (state changes) ?  Idempotent ? Any important architectural SLAs or industry standards to be aware of (e.g open banking) ?  <br /> 8. Validate API model workflow against job stories with sequence diagram. Should show typical usage scenarios. Share model with stakholders and get feedback.|
| Output | - Public or Private API Profile. An API profile is a cohesive view of an API that specifies its name, scope, operations, participants , emitted events,  important architectural requirements and the workflow required to deliver the API outcome. Specifies API boundaries. <br /> - Resource model taxonomies <br /> - API usage sequence diagrams |
| Checkpoint | API business owner , API designer other stakholders review and approve the changes. |
| Exit Pre Conditions | - api.profile.md updated with API profile information <br /> - Updated API sequence diagram file <br /> - Updated resources.md file <br />| 
| Roles involved | - API business owner  <br /> API designer <br /> | 


## Design Stage