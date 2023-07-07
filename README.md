# apollo-inaccessible-bug

@inaccessible is not working as expected for interface.
When "newField: String @inaccessible" is added to accounts.graphql it throw the below error.
error[E029]: Encountered 1 build error while trying to build a supergraph.

Caused by:
    INTERFACE_FIELD_NO_IMPLEM: Interface field "Account.newField" is declared in subgraph "accounts" but type "RegularAccount", which implements "Account" only in subgraph "brokerage" does not have field "newField".

To Run Use: NO_PROXY=true rover supergraph compose --config config.yaml > supergraph.graphql
