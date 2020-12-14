## The Open Ecosystem Federation

### Table of Contents

* [Background](background#background)
* [An Introduction to the Ecosystem Toolkit](background#an-introduction-to-the-ecosystem-toolkit)
* [An Overview of the Ecosystem Toolkit](background#an-overview-of-the-ecosystem-toolkit)
* [Design Goals of the Ecosystem Toolkit](background#design-goals-of-the-ecosystem-toolkit)

### Authors

* Ben Helps
* Ross McDonald
* Sid Kalita

### Background

During the summer of 2019, the Open Identity Exchange (OIX) facilitated a Discovery Project involving HMRC, DWP, GDS, banks, other commercial entities and representatives from academia that sought to explore event-based data assurance.

The underlying premise was that during the course of day-to-day business, entities interact with other entities (such as their customers, staff, suppliers, etc.) in ways that can be used to assure the quality of the data associated with the latter.  The Discovery Project’s incoming hypothesis was that managed access to a digital record of such interactions would constitute a valuable service to others - that the borrowing of due diligence would open up new possibilities.

The findings, conclusions and recommendations from the Discovery Project were published as an OIX Whitepaper “Building a Trusted Environment: Event-based Attribute Assurance” which can be found on the OIX website.

The Whitepaper recommended the establishment of an OIX Alpha Project with the objective of agreeing a set of common requirements to support the provision, exchange and consumption of Events. The common requirements would be adopted by collaborating entities willing to share the value of the processes, activities and claims that the Events represent, using them to meet their own – potentially different – data assurance needs.

Following the completion of the Discovery Project, several organisations (HMRC, Future Borders, Food Standards Agency (FSA), GDS, Idemia and other commercial and academic entities) put forward resources to deliver an OIX facilitated Alpha Project to meet this brief, with the intention of taking the work forward into a subsequent Beta Project, where the generalised standards and rules of engagement developed in the Alpha could be deployed in the context of a specific use case that would be of value to those organisations, to act as a reference ecosystem deployment.

Two of these organisations, Future Borders and HMRC created the Open Ecosystem Federation in late January 2020 as a new initiative under the stewardship of the Distributed Systems Group (a large set of collaborating entities comprising government, industry and academia). FSA joined the OEF right after this in February taking the core members to three.

The outputs from the OEF are part of a set of complementary pieces co-created and co-evolved by the Distributed Systems Group an example of which is the Utility Trade Platform (UTP).

The OEF maintains an association with OIX in order to protect the co-design and evolution of the open standards and artefacts which are created through the various phases of the project.

The Alpha Project was launched towards the end of January 2020 and ran until the end of March. The target content was discussed over the course of nine workshops, the last of which took place on 25th March.

Over the course of the summer, a smaller group of project participants then set out to detail the “Ecosystem Toolkit”, which comprises both a Technical Specification and – importantly – Rules of Engagement to provide a configurable framework for collaboration.

### An Introduction to the Ecosystem Toolkit

#### Purpose of the Ecosystem Toolkit

There are many situations and contexts in which entities that share a common domain of interest could create value by collaborating with one another. Identity and eligibility assurance is one such use case, in which the benefits of collaboration are clear cut.

The primary objective of the Alpha Project was to develop a generalised and repeatable toolkit that can be easily deployed by any given entity to facilitate collaboration with other any other entity over any given domain of interest.

This is referred to as the Ecosystem Toolkit.

The ideas contained within the Ecosystem Toolkit aim to connect expertise across collaborating entities without unnecessary friction. The Ecosystem Toolkit aims to remove barriers to collective action that prevent the emergence of collaborative ecosystems, reducing the incremental effort required either to set up a new ecosystem or to extend an existing one. It also allows for a greater level of interoperability between ecosystems.

We envisage a future state in which the Ecosystem Toolkit helps significantly more collaborative ecosystems to emerge – and thereby create value.

In the same way, the Ecosystem Toolkit can be seen as setting out an architectural style that can be used to implement a Trust Framework, constraining some design decisions in order to elicit a number of beneficial qualities, as described later under 'Design Goals'.

The Ecosystem Toolkit should not be confused with an instance of a trust framework or scheme that has been deployed to deliver a particular use case, and which has made its own specific implementation choices.

#### Components of the Ecosystem Toolkit

The Ecosystem Toolkit can be seen as setting out an architectural style that can be used to implement Trust based and other Collaborative Frameworks, constraining some design decisions in order to elicit a number of beneficial qualities, as described in 'Design Goals'.

Many initiatives set out to establish technical standards . However, a key feature of the Ecosystem Toolkit is that it seeks to specify an approach for tackling those elements of collaboration and trust that go beyond the deployment of technical standards and is technology and vendor agnostic.

The heterogeneity of the different situations and contexts which might benefit from collaboration inevitably means that the legal, operational and behavioural aspects require as much – if not more – effort to specify and configure as any technical standard.

The Ecosystem Toolkit therefore comprises two major artefacts:

* **Rules of Engagement** to facilitate the agreement required for scalable, interoperable and extensible collaboration between participants within a given ecosystem.
* **Technical Specification**, offering a generic approach based on open standards, to implement the execution of scalable, interoperable and extensible collaboration over the Events that – for example – might be used to record proof of identity or eligibility.

The Rules of Engagement comprises of different areas of concern, referred to in the Rules of Engagement itself as components: legal basis (e.g. consent), liability framework, assurance levels, service levels and issue resolution.

Each of these components is configurable (e.g. different levels of liability can be set), and the Rules of Engagement includes a default configuration for a minimum set of components which provides a basic framework agreement for collaboration between entities.

Of course, this basic framework will not meet the needs of entities looking to collaborate in situations that require relatively high levels of trust. The Rules of Engagement allow for new components to be added and for different configurations of each component.

Importantly, specific instances (e.g. a defined level of liability, or a given issue resolution mechanism) of any component can be easily referenced by the machines (known as Expert Systems) that implement the Technical Specification.

The intention is for easily repeatable patterns to emerge, as ecosystems compose and configure components to meet their needs for specific levels of assurance and trust. These patterns can be exposed in a machine-readable way to other entities looking to participate in the ecosystem, or by participants looking to create their own ecosystems operating in a different situation or context.

#### Event Schema

One of the most important constraints imposed by the Technical Specification is the requirement to implement a universal and standardised Event schema.

The Event schema is divided into Data Assertions and Metadata Assertions, where the Metadata Assertions capture the provenance of the Event and the Data Assertions expresses its content.

The standardised Data Assertions ensure that the role of Event Producer (akin to that of the Issuer in a Verifiable Credential) is systematically captured as an integral part of the information itself . The Data Assertions of an Event are standardised in the form of an N-Tuple construct which may for example be an RDF triple.

All Events therefore take the form of an attestation (“X says that Y is true”), whose provenance provides a basis for trust: at its simplest, an Event Consumer can decide how much confidence to place in the content of the Event based on the entity attesting to it.

This standardised Event schema also means that:
* The information exchanged between Expert Systems can be about anything – as a result, ecosystems are not restricted to any particular domain of interest
* A universal API can be used to move information between Expert Systems – there is no need to re-work or extend the client which consumes the API as circumstances change

These properties hugely increase interoperability (both internally within an ecosystem and externally between ecosystems) and extensibility of solutions that are deployed in a way that conforms to the Ecosystem Toolkit. See 'Design Goals' for more detail.

### An Overview of the Ecosystem Toolkit

Here we provide a short overview of the components that comprise each of the two major artefacts of the Ecosystem Toolkit.

For more detail, please refer to the artefacts themselves which are located in the Open Ecosystem Federation Github repository.

#### Rules of Engagement

As indicated above, the Rules of Engagement set out a composable and configurable collaboration framework. This comprises of ten separate components, together with a set of default parameters that provide a minimum basis for collaboration between entities.

Some form of legal instrumentation is required to govern a given instance of collaboration. This may take the form of a bilateral contract between two entities, a multi-lateral collaboration agreement between several entities, a series of contracts with a legal entity tasked with operating a scheme, etc.

The ten components (which represents a non-exhaustive list) are:
* **Legal Basis**: the legal basis on which entities are collaborating over information. The default setting is consent.
* **Liability Framework**: the level of liability linked to the quality of information being shared. The default setting is zero.
* **Assurance Framework**: the level of assurance over the quality of information being shared. The default setting is zero.
* **Issue Resolution**: the mechanisms used to resolve issues and disputes, as well as sanctions for ecosystem members that fail to observe them. The default is the general body of national and international law and regulation relevant to each participant.
* **Terms of Service**: these might include service levels, feedback loops, revocation rights, etc. There are no default terms of service.
* **Scope of Service**: the default scope of service is the provision of access to write information in the form of Events.
* **Ecosystem Intent**: intent goes beyond the immediate transaction and may be used to capture what is expected of participants. There is no default expression of intent.
* **Membership Administration**: the people, entities, policies, mechanisms and tools used to administer membership of an ecosystem. There are no default settings.
* **Value Exchange Framework**: the motivation for collaboration, expressed as a value on the information being shared. The default motivation is altruism, and the default value is therefore zero.
* **Settlement Framework**: the mechanism through which value is exchanged to settle for the sharing of information. The default setting is psychic reward, meaning that unless configured otherwise no settlement framework is in place.

The defaults contained within the Rules of Engagement provide a basic pattern for such legal instrumentation. The intention is to test a more evolved collaboration agreement – which can in turn be published as a pattern of collaboration – in a subsequent Beta Project.

#### Technical Specification

The Technical Specification sets out the technical considerations that must be deployed in order to implement an Expert System. An Expert System can be implemented by any entity that sees value in collaborating with other entities also deploying Expert Systems.

The Technical Specification contains the following responsibilities:
* **Exchange**: the gateway that connects the Expert System to the outside world (including other Expert Systems), and through which the Owning Entity (which operates an Expert System) configures and instructs that Expert System
* **Administration**: the instruction set used to provision the Expert System, configure the Owning Entity's entitlements, instantiate an Ecosystem and specify a knowledge base
* **Refinery**: the transformation of information (including Administration instructions) into a machine-readable representation in the form of an Event
* **Event Store**: the persistent storage of Events written to the Expert System
* **Registry**: a registry of all the 'things' that have been declared (i.e. nodes), including the Participants that form part of an Ecosystem and their entitlements
* **Ontology**: a conceptual model of the domain of interest shared by the Participants of an Ecosystem, expressed in a machine-readable logic-based language

These responsibilities may be implemented to varying levels depending on the requirements of any given ecosystem. With the exception of a number of clearly articulated Architecture Constraints, implementation details are not part of the Technical Specification.

### Design Goals of the Ecosystem Toolkit

The Ecosystem Toolkit aims to elicit six beneficial qualities:
* **Privacy**: participants must be in control of when and how they contribute the results of deploying their expertise and what is done with it by others - we are working towards a goal of data minimisation while maximising local processing
* **Scalability**: after a relatively modest initial investment to configure it, an Expert System must have minimal marginal costs for executing the tasks of collaboration within an ecosystem
* **Configurability**: Expert Systems must be configurable across different contexts, fostering reuse and discouraging repeated development of the same core functionalities
* **Extensibility**: Expert Systems must be able to easily accommodate an extension – or indeed change – of the domain of interest over which entities choose to collaborate
* **Interoperability**: Expert Systems that have been deployed using different underlying technologies must be able to communicate with each other
* **Traceability**: every actor and action within an ecosystem must be traceable through the Event history, so that there is a basis for trust that is accessible to other participants

#### Privacy

A high level of duplication in administration over and storage of a body of data has repeatedly proven to be a problem in terms of privacy, security, ethics and cost.

Sooner or later the wrong kind of party will get access to the data.

Duplicating inference over the same bodies of 'raw' data can have a significant impact on the environment and is wasteful. Worse it does not capitalise on the expertise brought to bear on the information by other parties.

The OEF believe that it is better to identify expertise across a graph of collaborating participants, and that the result of those participants deploying that expertise yields a smaller and more useful footprint of insight. We move less and process more locally.

Cutting out middle men and waste, we can raise the bar in expertise across networks of government, commercial and academic collaborators.

#### Scalability

Machine-to-machine collaboration is inherently scalable. The Ecosystem Toolkit therefore leverages machines to execute collaboration between entities, by acting on behalf of the entities that are responsible for them.

However, as noted above, a technical specification alone is not enough to define the legal, procedural and behavioural aspects that govern the collective action within an ecosystem.

The Alpha Project sought to address this by requiring that the Rules of Engagement be formulated as a set of configurable components, instances of which can be easily referenced by the Expert Systems which deploy the Technical Specification.

This is intended to encourage the emergence of easily repeatable patterns – starting with the default collaboration agreement contained within the Rules of Engagement – that can be scaled as part of machine-to-machine interactions.

#### Configurability

Just as the Rules of Engagement must be configurable, so too the entitlements that govern access to information must be configurable. Configuration of entitlements is therefore at the epicentre of the Administration of an Expert System.

The Owning Entity (i.e. the entity operating an Expert System) needs to be able to specify the entitlements of the other entities that it is collaborating with. The scope of action that is afforded to each ecosystem participant can therefore be tailored to each specific need.

Entitlements can be codified as a distinct data shape. Entitlements can therefore not only be deployed by an Expert System but they can also easily be shared with other Expert Systems, reducing the need to rebuild the same set of entitlements for different entities or contexts.

Just as the Rules of Engagement encourage patterns of collaboration agreement, so too the Technical Specification encourages the configuration of entitlements into repeatable data shapes that can be easily shared and implemented as a matter of best practice.

#### Extensibility

The real world involves an endless flow of information across and between different contexts, and along many different extended value chains and user journeys. A “user” wants to be able constantly to assert and re-assert core attributes or properties about themselves as they move from one context to the next, without having to re-establish trust in them.

As importantly, a “user” will acquire new attributes and properties as they interact with entities in one context, and the accretion of these new attributes and properties can be used as ‘signals’ that streamline their interaction with entities in a subsequent context.

As discussed above, the Ecosystem Toolkit requires all information to be expressed using an Event, conforming to standardised schema. This allows information of any kind to flow to wherever it is needed, with both the content of the information and the basis of its assurance able to permeate different contexts.

Practically speaking, this implies that the Ecosystem Toolkit must have the capability to create and edit a machine-readable Ontology: i.e. the ability to develop, evolve and communicate from one machine to another the meaning of the information being shared.

#### Interoperability

The Technical Specification imposes “API First” as an Architectural Constraint on the deployment of Expert Systems. All interaction with the Expert System takes place through a gateway referred to as the Exchange, which must be deployed as an API that is self-describing, negotiable and evolvable (borrowing elements from REST, and minimising the need for out of band information). All interactions must use the standardised Event schema.

This means that Owning Entities can deploy Expert Systems using different technical topologies, and that they will still be able to communicate with other Expert Systems. The “API First” approach ensures that Expert Systems can cope with today’s rapidly evolving technical landscape, and the standardised Event schema protects against the systemic fragility inherent in the context-specific data schema often used as API standards.

To achieve these benefits, the Expert System must provide the ability to convert information that is pushed into it (from outside) into the standardised Event schema. This responsibility is referred to as the Refinery.

#### Traceability

As explored in detail in the Whitepaper, one of the biggest barriers to collective action is the ability to agree how to trust the quality of the information over which entities collaborate.
Most efforts to address this facet of collective action have focused on the definition of assurance standards, whereby entities either converge on a common due diligence process or rely on an “authoritative source” that undertakes such processing on their behalf.

In this approach, the frameworks that govern the relationships between collaborating entities are paramount. The information over which the entities collaborate (e.g. the “user” attributes and properties) often does not need to be supported by any further metadata (i.e. information about the information) – it is usually sufficient to know that it has come from an authoritative source that delivers against a known assurance level.

This approach places a high burden on those entities acting as authoritative sources: their operations must align with a given standard, and they must be sufficiently financially robust to warrant the high levels of trust placed in them to meet assurance standards.

The reliance on such authoritative sources can act as a barrier to widespread collective action. Where there is a strong business case, entities (usually large institutions) are willing to act as authoritative sources. However, it is very difficult to extend or replicate the same level of reliance into other contexts where the business case may not be so clear cut.

Although the Ecosystem Toolkit does not preclude the role of authoritative sources, as a default it encourages a fundamentally different model of assurance based on traceability.

The Technical Specification requires that each and every step in the Administration of every Expert System (such as its provisioning and configuration, the declaration of other entities participating in an ecosystem, the editing of an ontology, the creation of a knowledge base, etc.) is recorded as an Event, and persisted within an Event Store.

This means that every actor and action within an ecosystem is traceable through the history of Events, and can always be linked to the Events containing the “user” attributes and properties information over which collaboration primarily occurs.

Since entities deploying the Ecosystem Toolkit are able to collaborate over any Event, they can collaborate over the history of Events that led to the assertion of a particular “user” attribute or property.

Entities that are able to contribute signals into an ecosystem (e.g. because they have interacted with the “user”) are able to do so, with their assertions supported by a fully traceable audit trail of Events.

The metadata-centric nature of the Ecosystem Toolkit amplifies the quality of signals from a (much wider) network of (potentially less trusted) sources, without introducing the burdens imposed by the need to become an authoritative source.

In contrast, the burden shifts to the Event Consumer, who are made responsible for interpreting the information they receive, including the audit trail of Events. To do so, they must deploy reasoning models to determine if that audit trail is sufficient to satisfy the assurance levels that they require.

This approach – in common with other event-driven architectures – allows Event Producers and Event Consumers to scale independently of each other, and so reduces barriers to collective action.

In addition, the Ecosystem Toolkit actively encourages (without imposing) the emergence of assurance models that draw on the fully traceable audit trail of events to derive a basis for trust. Such assurance models leverage network effects and pattern recognition, providing powerful and robust alternatives to those that are anchored on authoritative sources.
