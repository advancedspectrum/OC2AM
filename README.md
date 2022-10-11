# OC2AM
OC2AM or Organizational Capability to API Model is a repo that contains artifacts about an organization's capabilities and their underlying resources to drive API Strategy and Program. The purpose of this repo is to provide a machine-readable construct to document this model and generate a visual map when necessary. It also enables the organization to better understand how to categorize/tag/identify APIs to drive better insight or connectivity to KPIs. The model can be further modified to include dimensions of personas, security policies, consumer categories, domain data models and more.

The hierarchy is as follows

- **Org**  - > orgId maps to multiple domainIds
  - **Domain**  -> domainId maps to one orgId
    - **Level_1**  -> subLevelId maps to one domainId
      - **Level_2**
        - ....
          - **Level_N**          
            - **Capabilities**  -> capabilityId maps to one subLevelId
              - **Resource**   -> resourceid maps to 1 or more capabilityId(s) and apiId(s)
                - **API**  -> maps to 1 or more resourceId(s)
              - **Use Cases**         

**Org** is the name of the organization or company. In the case of university it would be the name of the university.

**Domains** are the top level business divisions based on the organizations criteria for divisions. Domains are non-overlapping in nature and must contain 1 or more sub-levels. For example, a University may use the following divisions: Academics, Research, Business Spport, etc. All domain must map to the same Org. Domains must be uniqueand have a 1 to 1 relationship to Org.

**Levels** are increasingly granular representation of what constitutes a Domain. For example, Student, Faculty, Teaching & Learning can be a sublevels below Academics. Sub-levels must be unique and have a 1 to 1 relationship to the parent level.

**Capabilities** are a managed aspect of the business that produce specific, desirable value or outcome. They are necessary non/operational requirements enabled by people, process and technologies. Capabilities in this model never discuss how they are implemented (whether using people, process and/or technology). They simply describe the what. Not the how. Capabilities can be as coarse-grained as a high-level business processes or as granular as specific activities within a unit of work. Capabilities can have have many to 1 relationship to sub level. Capabilities can only be attached to lowest sub-level of a Domain. Student Recruiting may be a capability under the Student sub-level.

**Resources** are digital business objects on which actions are performed. A resource can be made up of data describing the object. For example, a customer's address is an object. Street numbers, street name, city, state/province, and postal code describe the Address object. But in the same token the customer that lives at the address can also be represented as a digital object in a similar way.  Resources can only be attached Capabilities. Resources can have have a many to many relationship to Capabilities. Student, Application, Campus, Recruiting Event, Recruiting calendar, etc. may be Resources under the Student Recruiting capability.

**APIs** are the access points to Resources and expose operations (aka actions) that can be performed on them programmatically. APIs can have 1 to many relationship to Resources. APIs are a way to materialize Capabilities through software. 

**Use Cases** describe the conditions and actors that activate a Capability. A use case for Student Recruiting capability can be to "Allow students to register for a University show case event".

**commonProperties** file describes the schema of attributes that are reusable across all parts of the hierarchy.
