# DICOM ZOO

Public repository of example DICOM studies and instances to support demonstrations, tutorials, and testing.

## Motivation

Medical imaging software developers constantly struggle to provide software that works robustly on DICOM data, yet many users are unable to supply test data due to confidentiality concerns.

This repository is meant to collect both valid and invalid (per the standard) datasets as a public resource.

## Considerations and Process

The Slicer community is working on workable process to collect, curate, and deliver this content.

Some issues to consider:
* We need to ensure there is no information shared that should not be shared.
* To be useful, some data will need to be large so git may be inappropriate as is.
* We need to be able to annotate and discuss the data.
* We need to be able to organize the data by attributes such as modality, encodings, reasons for invalidity etc.
* We need to host the datasets for easy access in CI tests, tutorial noteboooks, etc.
* We need a scalable solution that won't lead to high costs.

Strawman plan:
* Only a small set of expert maintainers are able to add data to this repository to ensure they are safe to share.
* We store data as binary assets to releases (to address concerns that git-lfs may be overly complex in practice).
* We store data descriptions in markdown files with links to the data download.
* We discuss data in github issues.
* We host the data in a Google Healthcare DICOM store behind the [IDC ThrottleProxy](https://github.com/ImagingDataCommons/ThrottleProxy) or maybe [nginx rate limiting](https://www.nginx.com/blog/rate-limiting-nginx/).


## Related Projects
* Some [early discussion about IPFS](https://docs.google.com/document/d/1DfQ3AZfXBuv51PP7shKi7QP0Nm90W0KRBVMI9-rIB5g/edit#) led to a list of datasets to start with.
* Something similar already exists in the [dcmjs-org/data](https://github.com/dcmjs-org/data) project, but with less ambitious goals and no DICOMweb hosting.
