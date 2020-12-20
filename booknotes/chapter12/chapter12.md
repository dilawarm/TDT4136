# 12 - Knowledge Representation
_In which we show how to use first-order logic to represent the most important aspects of the real world, such as action, space, time, thoughts, and shopping._

By delving into the deails of how represents a variety of knowledge, we hope we have given the reader a sense how real knowledge bases are constructed and a feeling for the interesting philosophical issues that arise. The major points are as follows:
* Large-scale knowledge representation requires a general-purpose ontology to organize and tie together the various specific domains of knowledge.
* A general-purpose ontology needs to cover a wide variety of knowledge and shoud be capable, in principle, of handling any domain.
* Building a large, general-puprose ontology is a significant challenge that has yet to be fully realized, although current frameworks seem to be quiet robust.
* We presented an __upper ontology__ based on categories and the event calculus. We covered categories, subcategories, parts, structured objects, measurements, substances, events, time and space, change, and beliefs.
* Natural kinds cannot be defined completely in logic, but properties of natural kinds can be represented.
* Actions, events, and time can be represented either in situation calculus or in more expressive representations such as event calculus. Such representations enable an agent to construct plans by logical inference.
* We presented a detailed analysis of the Internet shopping domain, exercising the general ontology and showing how the domain knowledge can be used by a shopping agent.
* Special-purpose representation systems, such as __semantic networks__ and __decription logics,__ have been devised to help in organizing a hierachy of categories. __Inheritance__ is an important form of inference, allowing the properties of objects to be deduced from their membership in categories.
* The __closed-world assumption,__ as implemented in logic programs, provides a simple way to avoid having to specify lots of negative information. It is best interpreted as a __default__ that can be overriden by additional information.
* __Nonmonotonous logics,__ such as __circumscription__ and __default logic,__ are intended to capture default reasoning in general.
* __Truth maintenance systems__ handle knowledge updates and revisions efficiently.