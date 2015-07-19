# Scenarios

(Ludwig: Pubsub
Sensors publish readings
Accessors want to read these readings
Clients want to make sure they get...)
Pay-per-view
Oxford Sensor Network
[an existing system -- good for demonstration]
+
Alex: city-scale networks, low-rate connectivity, rolled out by
different providers...
-- authenticate to the network
-- application layer security
Infrastructure, Street lighting
Air quality; mobile devices on transport infrastructure

* Existing description of structure (Eduardo -> links)
* Eduardo: Security and privacy considerations
* Alex: Security and privacy considerations for street lighting
* Everyone: throw their favorite protocols against the scenario and
  see what sticks

Home automation
(multi-stakeholder aspects)
(consumer end user)
[use Lemonbeat?]

* Daniel: Specific use case (including family)
* ___: Security and privacy considerations [see also ACE use case]
* Everyone: throw their favorite protocols against the scenario and
  see what sticks

Alex: building management (commercial)
(legal-entity end user)
... HR cannot get to know when I enter my office...
(Privacy!)

* Sandeep: Start from ACE use cases document, include s.a.p.c.
* Everyone: throw their favorite protocols against the scenario and
  see what sticks

Steve: Healthcare -- take-home monitoring devices need to deliver data
to systems in the hospital

* Steve might find someone... Justin Richer?

## common aspects to be added to multiple scenarios

Steve: Emergency first responder information
e.g., where is the power?
[Exceptions!]
-> home automation, building automation scenario

Most scenarios have managed/operated networks, except home automation
(single-domain vs. cross-domain as well)

## maybe too hard

Daniel: Smart Meter, billing...
[maybe too complicated/loaded?]

Daniel: car-to-car
real-time safety information
[would need experts]

Oliver: Predictive maintenance...
Factory-floor
ICS

## plugtests

make scenarios ready for implementation contributions that can be
taken to plugtest-type events

may need to emulate the scenarios ""

e.g., specific protocols:

* EAP over CoAP (method for now: EAP-PSK, Sim card)

# Required attributes

Alex: keep in mind evolvability of the system

Ownership transfer; custodians
(hotel room scenario)

Define "me" = personal area network

Resilience to crypto desasters (PQ etc.)

Separation of network access authorization and application layer
authorization processes:

* network setup process
* application setup process
* -> (network setup as a byproduct of applications setup?)

"Bring your own thermostat"

(vs. "Steal your own thermostat", "Sell your own thermostat")

Fog computing

Forms, actions
granularity of form fields wrt actions
-> granularity of authorization in general
(e.g., different resources for different access classes)

Do NOT define a new policy language
but need AIF-like format for operational authorization ("cache")

Oliver:

* things owned by legal entities can operate based on
pre-configured policies
* things owned by consumers need to operate on an "exception by
  exception" basis
(Ludwig: There are some UI issues here that we are not concerned with)

What do we expect from an OAuth implementation to be able to integrate it?

Visibility?  How to maintain that in a secure way, and what visibility
is required *for* security?

Security in a RESTful system
-- access control
-- privacy
What are the benefits of doing security in a RESTful way

Oliver:
"Provider gets simpler by a factor of ten" [Oliver -> refs]
"Consumer get simpler as well"
-> asymmetric philosophy: consumer can be simpler

Are the ways we have for a user to authenticate to the system sufficient?

Alex: hardening with time... (when you are happy and stop worrying
about it)

Reciprocity

Policies for authentication, negotiation...


# Other resources to look at

* ETSI M2M -> OneM2M (vs. FIWARE open-source implementation -- not RESTful)
  Alex: -> Links to relevant documents

# To do

Logistics for collecting information:

-- collect in the T2TRG repo
   -- relevant input documents
   -- snippets that will become the RG drafts at some point

What are the outputs:

-- Research Group drafts -> RFCs (after suitable time as a living document)
   (need editors per draft!)

(W3C: Landscape, Requirements)
