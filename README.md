
## TCtracer - ICSE 2020 - Artefacts
This repository provides the data artefacts for the experiments conducted using our tool TCtracer for the ICSE 2020 paper "Establishing Multilevel Test-to-Code Traceability Links".

TCtracer is a tool that that establishes code traceability links in Java projects using the JUnit framework at the method level (function-to-test) and at the class level (test-class-to-tested-class), using a variety of techniques.
#### Artefact Types
This artefacts provided are the ground truth links for evaluating the techniques and the produced predicted links, specifically:

 - A manually curated method-level ground truth set for three projects (Commons IO, Commons Lang, and JFreeChart) - corresponding to RQ1 and RQ4 in the paper
 - A manually curated class-level ground truth set for four projects (Apache Ant, Commons IO, Commons Lang, and JFreeChart) - corresponding to RQ2 and RQ3 in the paper
 - The predicted method-level links for each project and each technique - corresponding to RQ1 and RQ4 in the paper
 - The predicted class-level links for each project and each technique - corresponding to RQ2 and RQ3 in the paper

#### File Structure
At the top level, the files are split into ground-truth and predicted-links. These categories are further split into class-level and method-level, which are then split by subject. These folders contain the CSV data files.

#### Data Format

The data is provided in CSV files, where for the ground truth: 

 - At the class-level, the fields provide the name of the test class, the name of the tested class, and the raters that created/inspected the link.
 - At the method-level, the fields provide the fully-qualified name of the test, the fully-qualified name of the tested function, and the raters that created/inspected the link.
 - The raters are identified either as J[n], where [n] is the ID of the judge, DEV where the links were created by the developers, or a reference is provided where links were taken from previous published work.

For the predicted links:

 - At the class-level, the fields provide the fully-qualified name of the test class and the fully-qualified name of the tested class for the predicted link
 - At the method-level, the fields provide the fully-qualified name of the test and the fully-qualified name of the tested function for the predicted link
 - The file names provide the name of the technique used to generate the predictions and which research question the predicted links correspond to.
