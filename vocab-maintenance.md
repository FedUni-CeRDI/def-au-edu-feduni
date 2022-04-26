# Vocabulary Maintenance

## Content maintenance
The goal is for each controlled vocabulary to be stored and published using a 'semantic web' representation - typically using [SKOS](https://www.w3.org/TR/skos-primer/) for basic terms, definitions and (optionally) hierarchy; else using a domain-specific ontology if available. 
However, while it is eminently suitable for this application, it is a rather esoteric technology, unfamilar to most scientists and developers, and generally unsuitable for the development and maintenance of vocabaularies by subject-matter experts. 

For most users, the most convenient tool for development and maintenance of vocabaulary content is an Excel file (.xls or .xlsx format). 
Provided this is set up using a suitable template, the semantic web representation can be generated directly using [SKOS Play!](https://skos-play.sparna.fr/play/convert), 

## Generating RDF (SKOS)
Go to https://skos-play.sparna.fr/play/convert 
Check **In a local file on my computer** and select the xslx file.

**Convert**

Copy result into xxxx.ttl file.

**Edit for Loading in RVA**
In your editor of choice, in the .ttl file delete all `skos:inScheme` links (e.g. `skos:inScheme s:swcm-1992;`) that are associated with resources of `rdf:type skos:Collection`. 
(This deals with the fact that RVA applies a more rigorous interpretation of the SKOS conformance than SKOS-Play!.)

**Loading in RVA**

To edit or upload a new version of FedUni created collections of soil concepts to RVA
(at 07-04-2022 was titled 'Soil Vocabularies coordinated through Federation Universiy)

In demo mode: 
If you want to do a test, load the vocabulary in development mode. To to this, 
log on to https://demo.vocabs.ardc.edu.au

alternativly log in in production mode - 
Login to https://vocabs.ardc.edu.au and go to 'My Vocabs'.

Each of the steps below have to be done in both demo and production

Select 'My Vocabs Login'
- Login using your Australian Access Federation Credentials. Contact ARDC if you require credentials 
- Login to Federated Services - Search for Federation University Australia
- Enter your Username and Password

Demo video
Of creation and upload of a different vocabulary to RVA (out of demo mode). 
The production and demo RVA interfaces are much the same

*+ To edit of add metadata viewable in RVA interface of an existing vocabulary:*
Note, this is only the metadata viewable in RVA interface - there are also other metadata fields you can add or edit direct in the vocabulary .ttl file. This would require uppload of a new version (see below). 
- Select the Published Vocabulary 'Soil Vocabularies coordinated through Federation University' (or whatever the current title)
- Here, you can edit the metadata 
- 'publish' - this will publish metadata changes (ie will not need a new vocabulary version number)

*+ To add a New Version*
to 'Versions' > '+ Add a version'Add a version - give the version a Title that is short 
- Add Access Point - TTL
- Upload file xxx.ttl
- Add
- select - Display Collections (not ConceptScheme)
- Import, make available
- Add this version
- Publish

*+ To add a New Vocabulary*
- Select owner
- Make sure the Vocabulary Acronym is short  - the purpose is for use in the URL ie it is not for the end user to see at the inferface 
- Enter metadata
- Then, as per instructions to add a New Version

