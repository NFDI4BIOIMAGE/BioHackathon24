# de.NBI24 BioHackathon
## [Project 6](https://www.denbi.de/de-nbi-events/1763-3rd-biohackathon-germany-increasing-interoperability)
### Misc:
- **Communication**: Space NFDI4BIOIMAGE-HACKATHON2024 (join via https://matrix.to/#/!OPPIswBjILObXJmMLI:mpg.de?via=gitter.im)
- **OMERO instance:**
    - upload instance 10.14.28.137 with 2TB storage
    - developer instance 10.14.28.177 with 250GB storage
    - **Requires VPN. Requires some setup beforehand.**
      - VPN client installation (Cisco)
      - Linux instructions: https://www.uni-muenster.de/IT/services/kommunikation/vpn/linuxoc.html
      - [Cisco Client for MacOS](https://cloud.gerbi-gmb.de/f/1373896)
      - [Step-by-Step guides](https://www.uni-muenster.de/IT/services/kommunikation/vpn/index.html) from Uni Münster, how to set up VPN
      - VPN login credentials:***

#### Table of Content:     
1. [Subproject: Optimize RDF structure and URIs, packaging in subsets](#p1)
2. [Subproject: Use Cases for subsetting RDF](#p2)
3. [Subproject: Accessing RDF subsets](#p3)
---
#### P1: 
#### Reviewing RDF Structure and URIs: Analyze and refine the current RDF structure and URIs to ensure they are optimized for production environments 
#### Packaging subsets: Package subsets of RDF data in a RO-Crate format to foster sharing and data integration.

##### Role & Responsibilities:

- Josh Moore (lead)
- Susanne Kunis (lead)
- Niraj Kandpal
- Peter Zentis

##### Goal:

- A refined RDF structure in terms of used predicates and improved URIs ready for production deployment.

##### Requirements
- Knowlegde of [ro-crate](https://www.researchobject.org/ro-crate/)
- Knowledge of [LinkML](https://linkml.io/) for encoding the decisions

##### Environment:
- **Repositories**: [omero-rdf](https://github.com/German-BioImaging/omero-rdf), [ome-ld](https://github.com/joshmoore/ome-ld), [idr_metadata_model](https://github.com/khaledk2/idr_metadata_model/blob/main/idrmetadatamodels/models/antibody_schema.yaml)
- Login to the [IDR](https://idr.openmicroscopy.org/)
- necessary python modules: omero-rdf

##### Data:

- idr0054 (with zarr) https://idr.openmicroscopy.org/webclient/?show=project-701
- idr0056 https://idr.openmicroscopy.org/webclient/?show=screen-2303
- Create a Demo dataset with examples eg: finding annotations from all/multiple kind. 



##### Timeline & Activities:
- Identify fields that need discussion (Perhaps before hackathon)
- Loop through those fields. Discuss URI options and decide.
- Update omero-rdf to split out the URI
- Document the choice in the appropriate LinkML
- Schema specification for harmonization of OMERO metadata by omero-rdf
- Create test samples of data subsets from IDR based on defined criteria's
- Stretch goals (breakouts)
    - Discuss relationship to [ome-owl](https://gitlab.com/openmicroscopy/incubator/ome-owl)
    - Make all URIs resolvable
    - flexible customization and extraction of desired subsets of data by omero-rdf
- addon: import of/from ro-crate in OMERO

##### Judging criteria:

- Total number of agreed on URIs
- status of specification
- subset in ro-crate format

---
#### P2: 
#### Subsetting RDF for Various Use Cases: Identify effective strategies to create subsets of the RDF data that cater to different research and application needs.

##### Role & Responsibilities:

- Tom
- Torsten

##### Goal:

- Clearly defined guidelines and criteria to create useful subsets of RDF data, tailored for various research and application needs.
- usecases for subsets, query about the outcome/specification of P1

##### Requirements/Environment/Data:
- sparql/SHEX, 
- ontop
- data: IDR, OpenNeuro BIDS

##### Timeline & Activities:

##### Judging criteria:

- Prototypical SPARQL queries and/or SHEX (?)

---
#### P3: 
#### Endpoint Drafting and Testing: Develop endpoints for SPARQL and bioschemas formats, aiming to facilitate the consumption of RDF subsets. Curate (meta)datasets and queries for testing and performance profiling. Conduct performance and scalability testing of these endpoints.

#### Role & Responsibilities:

- Carsten (lead)
- Mariana (lead)

#### Goals:

- Development and documentation of SPARQL and bioschemas endpoints that facilitate efficient RDF data consumption.
- Curation of metadatasets and queries for testing and performance profiling
- Benchmarks that document the performance of the newly developed endpoints, ensuring the use of the most efficient databases.
- Performance and scalability results that guide future optimizations

#### Requirements/Environment/Data:

- Data: One Project/Dataset/Image hierarchy with metadata (e.g. from IDR). Have to experiment pre-hackathon what is a good size (number of triples)
- [github.com:German-BioImaging/omero-ontop-mappings](https://github.com:German-BioImaging/omero-ontop-mappings)
- ontop sparql endpoint and r2rml engine ("dynamic triplestore")
- other sparql endpoints: fuseki, virtuoso, ??? ("static triplestores")

#### Timeline & Activities:
- Populate static triplestores
- Define performance metrics
- Define benchmark queries
- Run benchmarks, collect data
    - Mari: Besides queries, I think it'd be important to clarify whether we're using specific tools or libraries to run benchmarks.
- Analyse data
- Report

##### Judging criteria:

- minimum success: - one benchmark query timed and profiled for two triplestore/endpoints
- maybe: description/guide HOW to benchmark
