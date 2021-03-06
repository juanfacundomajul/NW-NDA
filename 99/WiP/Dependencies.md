Dependencies:

Dependencies are the things on which a proposition rests.  It is one of the theses of an object-oriented approach that all dependencies should be expressly linked to, rather than be implied. That is to say, the context of a Record should be explicit, not implicit. This addresses a problem pervasive in both law and software, particularly in law.

A Record expressing an event in transacting should reference the prior step in the transaction and any new structures that it depends on.  Sometimes the mere link will be most of what is needed, for instance in making a first draft of an NDA, the Demo links to the objects for the two Parties and the object for the Form of NDA.  But each of these referenced objects is composed of other objects - for instance the Parties are connected to types of identities, addresses and the like.  The Form is connected to objects for the various sections of the NDA, possibly to an object for things that are involved.  And each of these is dependent on the software that renders the objects into a full document, and that is dependent on the code for the web-engine, software languages, eventually even the operating system.  Ideally, a Record would permit tracing of all of these things. That is possible by a combination of Prose Objects and git, including "git include".

This contrasts with most systems of Records.  Most Records in most transacting systems are designed to be used in a particular environment, but that context (important concept) is implicit rather than explicit in the Records.

Ideally, the dependencies need to be modifiable.  One should be able to override a Dispute resolution clause with another one.  Similarly, if a code module supporting Notices is improved, it should be possible to both use the new module and to have all the old uses of Notices retain their pointers to the old version.  Interface can indicate that there is a new code module, and offer a chance to run under both the old and the new.  Same for all of the levels.  This has been called "malleability."  We take the absence of the discipline of explicitly linking to dependencies and offering malleability as being at the root of much of the entanglement of data and software - state and logic.  The entanblement of state and logic is at the core of much of "technical debt" in enterprise and banking software and organizations.  



