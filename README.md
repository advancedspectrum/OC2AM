# OCRM
This repo contains artifacts about an organization's capabilities and their underlying resources to drive API Strategy and Program. 

The hierarchy

Org - > orgId
- Domain  -> domainId & orgId
  - Level_1    -> subLevelId & domainId
    - Level_2
      - ....
        - Level_N          
          - Capabilities -> capabilityId & subLevelId
            - Resource  -> resourceid & subLevelId
              - API -> resourceId
                        
Org is the name of the organization or company. 

Domains are the top level business divisions based on the organizations criteria for divisions. Domains are non-overlapping in nature and must contain 1 or more sub-levels. For example, a University may use the following divisions: Academics, Research, Business Spport, etc. All domain must map to the same Org. Domains must be unique
and have a 1 to 1 relationship to Org.

Sub-levels are increasingly granular representation of the constituents of Domains. For example, Student, Faculty, Teaching & Learning can be a sublevels below Academics. Sub-levels must be unique and have a 1 to 1 relationship to the parent level.

Capabilities are necessary XXX as coarse as a business processes and as granular as specific activities. Capabilities can have have a 1 to many relationship to the parent levels. Capabilities can only be attached to lowest sub-level of a Domain.

Resources are business objects on which actions are performed. For example, a customer's address is an object. Street numbers, street name, city, state/province, and postal code describe the Address object. But in the same token the customer that lives at the address can also be represented as a business object in a similar way. A resources is made of data describing the object.  Resources can only be attached Capabilities. Resources can have have a 1 to many relationship to Capabilities.

APIs are the access points to Resources and expose operations (aka actions) that can be performed on them programmatically.
