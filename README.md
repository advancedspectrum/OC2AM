# OC2RM
OC2RM or Organizational Capability to Resource Model is repo that contains artifacts about an organization's capabilities and their underlying resources to drive API Strategy and Program. 

The hierarchy

- Org  - > orgId and multiple domainIds
  - Domain  -> domainId & orgId
    - Level_1  -> subLevelId & domainId
      - Level_2
        - ....
          - Level_N          
            - Capabilities  -> capabilityId & subLevelId
              - Resource   -> resourceid & subLevelId / multiple apiIds
                - API  -> multiple resourceIds
                        
Org is the name of the organization or company. 

Domains are the top level business divisions based on the organizations criteria for divisions. Domains are non-overlapping in nature and must contain 1 or more sub-levels. For example, a University may use the following divisions: Academics, Research, Business Spport, etc. All domain must map to the same Org. Domains must be unique
and have a 1 to 1 relationship to Org.

Sub-levels are increasingly granular representation of what constitutes a Domain. For example, Student, Faculty, Teaching & Learning can be a sublevels below Academics. Sub-levels must be unique and have a 1 to 1 relationship to the parent level.

Capabilities are necessary non/operational requirements enabled by people, process and technologies. Capabilities in this model never discuss how they are implemented (whether using people, process and/or technology). They simply describe the what. Not the how. Capabilities can be as coarse-grained as a high-level business processes or as granular as specific activities within a unit of work. Capabilities can have have 1 to 1 relationship to sub level. Capabilities can only be attached to lowest sub-level of a Domain.

Resources are business objects on which actions are performed. For example, a customer's address is an object. Street numbers, street name, city, state/province, and postal code describe the Address object. But in the same token the customer that lives at the address can also be represented as a business object in a similar way. A resources is made of data describing the object.  Resources can only be attached Capabilities. Resources can have have a 1 to many relationship to Capabilities.

APIs are the access points to Resources and expose operations (aka actions) that can be performed on them programmatically. APis can have 1 to many relationship to Resources.
