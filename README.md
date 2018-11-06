# ExtendedProvJson

[PROV-JSON](https://www.w3.org/Submission/2013/SUBM-prov-json-20130424/) is a standard developed by the World Wide Web Consortium to provide an interchange format for data provenance that uses the [PROV data model](https://www.w3.org/TR/prov-dm/).  The PROV data model is intended to capture provenance of data as it moves between tools, such as when using a workflow tool.

This repository contains documentation about a version of PROV-JSON that is extended to support fine-grained provenance.  Fine-grained provenance describes how data moves within a tool, for example from statement to statement with a program or script.  

In this extension, a PROV activity corresponds to a line of code and includes details such as the line and column location of the code within the script.  A PROV entity represents either a data value (including variable values, input and output files, and plots), information about a library or a library function used, or information about the computing environment.  wasInformedBy edges are used to represent control flow between statements.  wasGeneratedBy edges connect statements to the values they output, while used edges connect data to the statements that use the data.  hadMember edges connect functions to the libraries that they come from.

[rdt](https://github.com/End-to-end-provenance/rdt) and [rdtLite](https://github.com/End-to-end-provenance/rdtLite) are examples of tools that collect provenance and write it using this extended PROV-JSON notation.  [provDebugR](https://github.com/End-to-end-provenance/provDebugR), [Rclean](https://github.com/ProvTools/Rclean), and [DDG Explorer](https://github.com/End-to-end-provenance/DDG-Explorer) are tools that use provenance written in this notation.

For full detail of this extension, please read the [document in the repository](JSON-format.md).
