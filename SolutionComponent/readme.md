# Query components in a solution Notes
The following blog posts deep div into how to query solution components 
- (https://www.d365freelancing.com/post/query-all-entities-in-a-dataverse-solutions)
- (https://www.d365freelancing.com/post/query-views-in-power-platform-using-fetchxml)

## ERD of _(Views(System)InASolution.xml)_ System Views in a Solution Query.
```mermaid
---
title: Views in a Solution FetchXml Query Structure
---
erDiagram
    SolutionComponent {
        guid solutionid fk
        guid objectid fk 

    }
    SavedQuery {
        guid savedqueryid pk
        string name
        guid returntypecode
    }
    Solution
    Solution {
        guid solutionid pk
        string friendlyname
        string uniquename
    }
SolutionComponent zero or more to one or zero Solution : ""
SolutionComponent zero or more to one or zero SavedQuery : ""
```
