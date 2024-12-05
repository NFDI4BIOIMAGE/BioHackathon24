| name | description |type|
| ----| ----|---|
|[OME data model](https://docs.openmicroscopy.org/ome-model/6.3.1/) |Technical metadata description of an imaging experiment|schema|
|[REMBI](https://doi.org/10.1038/s41592-021-01166-8) |Recommended Metadata for Biological Images|best practice|
| [4DN-BINA-OME-QUAREP](https://doi.org/10.1038/s41592-021-01327-9)| (BNO) tiered metadata guidelines|metadata schema|
| [3D-MMS](https://doryworkspace.org/metadata) |3D microscopy metadata standard||
| [BIDS](https://doi.org/10.3389/fnins.2022.871228) |(Brain Imaging Data Structure) for Microscopy|model|
| [MITI](https://doi.org/10.1038/s41592-022-01415-4) |Minimum Information for Highly Multiplexed Tissue Images||
| [MIHCSME](https://doi.org/10.1038/s41597-023-02367-w) |Minimum Information for High Content Screening Microscopy Experiments||
|||
| [OME-XML](https://ome-model.readthedocs.io/en/latest/ome-xml/index.html)     |  file format for storing microscopy information (both pixels and metadata) using the OME Data Model; superseded by OME-TIFF, which is the container format for image data  making use of the OME Data Model      |file format|
|   [OME-Zarr/NGFF](https://ngff.openmicroscopy.org/latest/)     | a specific implementation of the Zarr format tailored for bioimaging data for storing data in the cloud, incorporates metadata compliant with the OME model       |file format|
| HDF5 | (Hierarchical Data Format) Widely used for storing large datasets, it supports complex data models and is commonly utilized in bioimaging|file format|
|NetCDF|Suitable for multidimensional data, it is often used in scientific research for storing array-oriented data.||
|[ARC](https://github.com/nfdi4plants/ARC-specification/blob/main/ARC%20specification.md)| (Annotated Research Context), plant science|model|
|  [ISA](https://isa-specs.readthedocs.io/en/latest/index.html)      |  (Investigation/Study/Assay)  [ISA Abstract Model specification](https://isa-specs.readthedocs.io/en/latest/isamodel.html)    |model|
|   [ISA-TAB](https://isa-specs.readthedocs.io/en/latest/isatab.html)     |   key component of the ISA framework that provides a tabular format for representing the metadata associated with biological studies. It is designed to facilitate the organization and sharing of research data in a structured manner.      |file format|
