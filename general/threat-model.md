# Threat Model

Threat Model is used to identify and explore threats and mitigations within the context of protecting something of value.

Threat Model is applicable to a wide range of things, including SW, hardware (HW), networks, distributed systems, and etc. There are very some technical products which cannot be threat modelled. Although threat modelling can be done at any stage of development, it is preferably to do it as early as possible, so that the findings can be applied to the design of the system.

Most thread modelling researches aim to answer the following questions:

1. What system are we building?
   - Application architecture
   - Application data flow
   - Application data type
   - Technologies used
2. What can go wrong?
   - "Branistorming" phase
   - Good stage to consult with STRIDE, Kill Chains, CAPEC and others structures models
3. What are we going to do about that?
   - Applying result of the question 2 to the system from the question 1
   - Also known as Threat Modeling Outputs
4. Did we do a good enough job?
   - Testing, and checking whether means from the question 3 are sufficient

[Lean more](https://owasp.org/www-community/Application_Threat_Modeling) about Threat Model.

---

Go back to the [section page](general/README.md).
