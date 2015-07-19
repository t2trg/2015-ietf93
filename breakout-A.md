# Thing-to-Thing Breakout A

- Talk: [12 CoRE Applications](https://github.com/t2trg/2015-ietf93/blob/master/slides/12-core-apps.pdf) (Klaus Hartke, Uni Bremen TZI) ([draft](http://tools.ietf.org/html/draft-hartke-core-apps))

## REST
- Collect accessable "authoritative" material on RESTful design
  - Roy Fielding's thesis and blog posts (less accessable)
  - Book references
  - Review other blog posts and convert to drafts?
- Assemble a cookbook with design patterns
  - Provide an "executive summary"
  - Focus on properties and implications (benefits, drawbacks)
  - Explain benefits in context of concrete use cases
  - Having parallel documents for each application domain might help
  - Keep abstract/general explanations
  - Initial items
    - Execute X (how to convert RPC style to REST)
    - Multi-user interaction with resources
- Define compliance levels? (see [Richardson Maturity Model](http://martinfowler.com/articles/richardsonMaturityModel.html))
  - Help with development contracts

## Agenda Items
### A1) Orchestration of Web Things
- About commissioning (i.e., configure devices to interact with each other to achieve goal)
- How to introduce intermediaries during runtime
  - Look at "cut" connections
  - Learn from classic Web applications (e.g., load balancers)
- Bindings with handles (resources) to synchronize resources might help
- Terming "choreography" might be more fitting?

### A2) Use cases, requirements and modeling of subscriptions
- Look at Observe attributes in [core-interfaces](http://tools.ietf.org/html/draft-ietf-core-interfaces) and [OMA LWM2M](http://member.openmobilealliance.org/ftp/public_documents/dm/LightweightM2M/Permanent_documents/OMA-TS-LightweightM2M-V1_0-20150707-D.zip)
- Have explicit handles
  - Resource to manage subscriptions in "/.well-known/subscriptions"
  - Rough consensus on such subscription handles
  - Handles could be managed with [CoMI](http://tools.ietf.org/html/draft-vanderstok-core-comi) to benefit from tooling
  - Possibility to batch multiple observe relations
- Also think about including other mechanisms (e.g., for HTTP) in the handles

### A3) Modeling of Web Thing as Typed Resources vs HATEOAS
- CoRE Apps provides some guidance for HATEOAS approach
- HATEOAS provides resilience for change
- Look into Internet Media Types / representation formats
  - Trade-off between being specific and reusable
  - For forward/backward compatibility look at physics behind things
  - ongoing discussions about needed resource types
- Look into link relations / form classes
- Start with reference framework
  - Agree on experimental use case (e.g., look at Lighting in ZigBee Cluster Library / IPSO; get an access token from an ACE-like service to access a pay-to-use resource)
  - Ensure "touching" properties of REST in use cases (not too trivial)
  - Implement experimental prototypes
  - Hold a plugtest to see different approaches and identify problems
- Evaluate properties of REST
  - Which constraints impact which (benefitial) properties

## Terms -- collect what it is and what it is not to arrive at definitions
- "origin" -- see Roy's thesis (origin server: "definitive source for representations of its resources and must be the ultimate recipient of any request that intends to modify the value of its resources")
- "binding"
- "orchestration" denotes a centralized controller
- "choreography" denotes a distributed approach

## Random Ideas
- Access Control
  - Hypermedia controls to gain access (request token)
  - Forms
  - Dynamic representations based on authorization?
- Make SenML mergable for batch observing
- Bookmarks as entry URIs -- just cacheing, restart from original entry URI on error
- serialization not enough, need semantics
- interoperable machines vs autonomous machines
- orchestrator, how to get information into devices
- standardized way to instantiate elements like proxies
- requirements differ per application domain -- see where it breaks

## Outlook
- Start definitions bottom-up from REST elements and constraints (client-server etc.)
- Add next step, small abstraction on top
- Thing descriptions as "beyond REST" approach

## Action Items
- Draft for subscriptions
- implementations for HATEOAS
- draft REST cookbook
