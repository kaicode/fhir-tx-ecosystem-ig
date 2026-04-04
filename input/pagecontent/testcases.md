

### Test cases 

These tests are a particular implementation of the requirements for a terminology 
server that can be used by the validator and IG publisher. 


The tests assume that the server can accept code systems on the fly.
If servers do not accept code systems on the fly, server authors will have to 
adapt these tests by rewriting them for their own actual support code systems. 
Either way, servers that do SHOULD pass all the tests, but the FHIR product director 
will review the test outcomes in order to approve a server. 

#### Registry

{% json tests/test-cases.json liquid/test-cases.liquid %}