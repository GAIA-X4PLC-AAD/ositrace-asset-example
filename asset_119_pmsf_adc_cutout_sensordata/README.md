# 20240603T143803.535904Z_sd_370_3200_457_pmsf_ars548_054814_119_cutout

OSI SensorData trace of cut-out scenario on testing ground

## Digital Assets

This is a digital asset according to the ENVITED Ecosystem Specification [EVES-003](https://ascs-ev.github.io/EVES/EVES-003/eves-003.html) for the ENVITED-X Data Space. It can be used as a template for other dataspaces as well. It contains a fully described and consistent example of a digital asset including a **`manifest.json` - file** as content registry.

A complete **`digital asset`** in a specific domain includes the data itself and all necessary files for describing, evaluating, and visualizing the dataset.

## Example Asset Folder Structure

A sample **`digital asset`** can be downloaded from the [GAIA-X4PLC-AAD/ositrace-asset-example](https://github.com/GAIA-X4PLC-AAD/ositrace-asset-example) as artifact of the lastest release (**`asset.zip`**) containing the following structure:

📁 `asset`

- 📁 `simulation-data`
  - 📄 `assetName.osi` or `assetName.mcap`
- 📁 `documentation`
  - 📄 `assetName_Documentation.pdf`
  - 📄 *`assetName_[Name].[ext]`* <i style="color:gray;">(optional)</i>
- 📁 `metadata`
  - 📄 `ositrace_instance.json`
- 📁 *`validation-reports`* <i style="color:gray;">(optional)</i>
  - 📄 *`qcReport.txt`* <i style="color:gray;">(optional)</i>
- 📁 `media`
  - 📁 `preview` *-> preview files* <i style="color:gray;">(optional)</i>
  - 📄 `assetName_01.png` *-> eyecatcher*
  - 📄 *`assetName_[XX].png`* *-> impression* <i style="color:gray;">(optional)</i>
- 📄 `README.md`
- 📄 `manifest.json`

### Legend

- 📁 `folder-name`: A folder in the repo.
- 📄 `assetName`: A file in the repo.
-  <i style="color:gray;">(optional)</i> : This file or folder is optional and can be added or omitted as needed.

### Description of the respective folders

- 📁 `simulation-data` : *Contains all valuble data files of the asset.*
- 📁 `documentation` : *Contains an instruction as well as technical specification of the asset.*
- 📁 `metadata` :   *Contains all metadata which are necassary to describe this asset, that includes all domain sepcific metadata from the [Ontology Management Base Repository](https://github.com/GAIA-X4PLC-AAD/ontology-management-base) (and all GAIA-X metadata form the [gaia-x-compliant-claims-example](https://github.com/GAIA-X4PLC-AAD/gaia-x-compliant-claims-example) to be compliant with the [GAIA-X Trust Framework](https://docs.gaia-x.eu/policy-rules-committee/trust-framework/22.10/). -> needs to be defined in a next step)*
- 📁 `validation-reports` :   *Contains the results provided by a validation suite.*
- 📁 `media` : *Contains all viusalization content from the asset (e.g. images and videos).*

### Description of the respective files

📄 `manifest_reference.json`:

- *This manifest file defined the link structure depending on the domain sepecific asset.zip. It includes a context section defining namespaces for various terms, an identifier (`@id`) for the asset, and a type (`@type`) indicating it is a manifest. The `manifest:links` section contains multiple entries, each specifying a type of link (e.g., license, simulation-data, media) with details such as relative paths, formats, and access roles. Optional metadata and visualization files are also included, with different access roles like `isOwner`,`isRegistered`, and `isPublic`.*

📄 `ositrace_instance.json` (domain metadata):

- *This JSON file describes the metadata and links associated with a OSI traces used in the Gaia-X 4 PLC-AAD project. It includes a context section defining namespaces for various terms, an identifier (@id) for the OSI trace, and a type (@type) indicating it is an OSI trace. The `DataResource` section provides details such as the name, description, and the GAIA-X metadata from the [gaia-x-compliant-claims-example](https://github.com/GAIA-X4PLC-AAD/gaia-x-compliant-claims-example) to be compliant with the [GAIA-X Trust Framework](https://docs.gaia-x.eu/policy-rules-committee/trust-framework/22.10/). The `manifest` section contains multiple entries, each specified by a category of link (e.g., simulation-data, metadata, media, documentation, validation-report) with details such as URLs and types. The `format` section specifies the type and version of the OSITrace format. The `content` section describes contained road types, traffic direction, granularity of sensor data, timestamps and information on contained objects or events. The `quantity` section provides measurements like number of frames. The `quality` section details precision and accuracy metrics. The `dataSource` section lists the data sources and measurement system used. Finally, the `georeference` section provides geolocation information, including the bounding box and geodetic reference system.*

### Create an asset

You can use the GaiaX 4 PLC-AAD [Provider Services](https://github.com/GAIA-X4PLC-AAD/provider-services) and [Provider Tools](https://github.com/GAIA-X4PLC-AAD/provider-tools) to create your own digital asset.