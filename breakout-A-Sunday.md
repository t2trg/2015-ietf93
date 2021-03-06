# Breakout A2

## Framework scenario

- Lighting as "hello world"-scenario
- Group control?
- how to handle events?
- Entities
    - Lights
    - Switch
    - Presence Detection
    - Controller
    - Brightness sensor
    - energy measurement
- user stories
  - someone enters the room the light is to dim up to the last level
  - the user wants to control he light through a user interface
  - adding a device with more features
  - leavin the room triggers a timer to turn off the light
  - measure energy on a central point
- Smaller group to work out implementation details (bootstrapped by Klaus and Matthias)
  - requirement: single entry point - catalog
  - management of bindings
  - multiple rooms
  - Evolution proofing through actual evolution

## Cookbook / Pattern collection

generally: Guidelines/best practices doing WoT in a RESTful way

to keep in mind/avoid:
- TL;DR - effect
- explain, don't preach

### front matter
- terminology
- basic do and don't from gdoc
- topic index

### collection of patterns
- RPC-style "excute X"
- conversion
- multi-user (concurrent interaction on resources)
- subscription (model events as states -- doorbell example)
- bulletin boards (RESTful pub/sub)
- modelling of collections
- group communication ([RFC7390](http://tools.ietf.org/html/rfc7390) overlap?)
- Resource structure (URIs may change, no implicit relation between parent and child resources, made explicit with link relations)

Template will be provided on T2T github
