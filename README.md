# Dequeue Registration Service

DequeueRegistration is a web service whereby the registering entity becomes one of the dequeueing entities, and the ESRP managing the queue will begin to send calls to it. Often, an ESRP or PSAP will manage a queue for which it is the only dequeuer; explicit DequeueRegistration for a single dequeuer is NOT REQUIRED. When there is more than one dequeuer, each dequeuer MUST register with this service. If the ESRP that manages the queue is also a dequeuer, it need not register (to itself). The registration includes a value for DequeuePreference that is an integer from 1-5. When dequeueing calls, the ESRP MUST send calls to the highest DequeuePreference entity available to take the call when it reaches the head of the queue. If more than one entity has the same DequeuePreference, the ESRP SHOULD fairly distribute calls to the set of entities with the same DequeuePreference measured over tens of minutes. 

## Owner

The owner of this repository approves all changes to the repository. 

This repository is owned by the NENA Core Services Committee, i3 Architecture working group.

#### Rules:

Specification Required. 

#### Contact:

[https://www.nena.org/page/911CoreSvcs](https://www.nena.org/page/911CoreSvcs) 

## Version History

### Dequeue Registration Service v 1.0

Version 1 OpenAPI schema for this service was originally defined in NENA-STA-010.3.2021. See https://www.nena.org/page/i3_Stage
