= Introduction =

This folder contains testing material for large external code systems;
these are the sources for the test cases on LOINC, SCT etc.

What follows is notes about how to prepare the subsets

== SNOMED CT ==

Take an international SNOMED distribution, and run:

```
java -jar --add-opens java.base/java.lang=ALL-UNNAMED snomed-owl-toolkit-5.3.0-executable.jar \
 -rf2-to-owl -rf2-snapshot-archives {zip-download} -version 20250801
java -jar --add-opens java.base/java.lang=ALL-UNNAMED snomed-subontology-extraction-2.2.0-SNAPSHOT-executable \
 -source-ontology ontology-20250801.owl -input-subset {snomed-subset.txt} -output-rf2 -rf2-snapshot-archive {zip-download} -include-inactive
```

where {subset.txt} is the file in this folder.

== LOINC CT ==

The subset is prepared by the code at https://github.com/HealthIntersections/nodeserver,
and running

```
npm install
tx-import loinc-subset
```

You then have to provide a reference to a downloaded LOINC source, 
and a list of LOINC codes to import, which is found in
loinc-subset.txt in this folder

== NDC ==

The test set is prepared by hand by taking subsets
from the first few lines of NDC

