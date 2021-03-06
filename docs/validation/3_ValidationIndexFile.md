## Index dataset validation
The Index.rdf file lists the documents that can be found in NEN-EN-ISO 21597-1:2020 containers. This Index.rdf must comply with the standard. A checklist can be developed for this compliance.

The following list contains a set of validation checks regarding the index.rdf file within the container. 

id   | check   |description   |
--- | --- | ---
ID1|valid syntax Index.rdf| validate if Index.rdf is a valid RDF file*
ID2|serialisation|check for allowed serialisations**.  
ID3|schema validation |check if the index.rdf file complies with the Container.rdf file*. Additional properties are allowed.
ID4|check listed files | check if the internal documents are present in the 'Payload documents'
ID5|check listed folders|check if listed folder documents folders are present in the 'Payload documents'
ID6|check not listed | check for unlisted files and folders. These are not allowed.
ID7|conformanceIndicator| check the ct:conformanceIndicator property for the value "ICDD-Part1-Container".
ID8|check external files| check if external documents are resolvable. This could prove to be difficult.
ID9|import Container.rdf|check if an owl:import statement to Container.rdf is present and correct.
ID10|existence link datasets| check if referred link datasets are available. Old and superseded linksets do not have to be present in the ICDD container. A linkset reference is superseded when a new linkset reference refers to it with the previous relations. 


*more details on schema validation in the schema validation chapter.

**the standard mentions XML or any other equivalent RDF serialisations recommended by W3C can be used. Limiting the supported serialisations to XML,turtle and json-ld can be recommended for an ICDD validation service.  

