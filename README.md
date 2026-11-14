# SigAnalyzer map data

Open terrain, road and ground data for **SigAnalyzer**, a radio-planning program. This repository
holds no program code and no plans: only public map data, repackaged so the program can
install it with one click.

## Using it

In SigAnalyzer, click **🗺 Map data**, tick the maps you need and press **Install selected**.
The program downloads the files from the
[`maps` release](../../releases/tag/maps) (`manifest.json` lists every item with its size and
SHA-256), checks them and unpacks them into its data folder. The same files on a USB stick work
offline: "From folder…".

| Item | Contents |
|---|---|
| `basics` | Roads, railways and place names (OpenStreetMap); ground maps for HF ground wave (GEUS, PROMICE) |
| `dk-10m` | Denmark: Danmarks Højdemodel terrain + surface 10 m; Copernicus DEM GLO-30 fallback |
| `dk-2m-<region>` | Denmark 2 m (DHM) per region: zealand, funen, jutland-north, jutland-south, bornholm |
| `faroes` | Faroe Islands: Umhvørvisstovan DTM 10 m + DSM 2 m on a 2 m grid; Copernicus GLO-30 fallback |
| `gl-base` | Greenland overview: Copernicus DEM GLO-90; the Nuuk area at GLO-30 |
| `gl-10m` | Greenland ice-free coast: ArcticDEM 10 m (sea-level heights) |
| `gl-2m-<town>` | ArcticDEM 2 m around nuuk, kangerlussuaq, narsarsuaq, qaqortoq |

Every item is one or more zip files under 2 GB with paths relative to the program's data folder.

## Sources, licences and attribution

The data is modified (cropped, resampled onto common grids, heights stored in 0.1 m or 0.2 m
steps, sea set to 0 m, ArcticDEM converted from ellipsoidal to EGM2008 heights, voids filled
from Copernicus). Each area pack's `pack.json` carries its licence text.

- **Danmarks Højdemodel (DHM)** © Klimadatastyrelsen, via Dataforsyningen. Free data, used under
  Klimadatastyrelsen's terms for free geographic data, with attribution.
- **Copernicus DEM GLO-30 / GLO-90** © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH
  2014-2018, provided under COPERNICUS by the European Union and ESA; all rights reserved.
- **ArcticDEM** v4.1 mosaic: DEM(s) courtesy of the Polar Geospatial Center under NSF-OPP awards
  1043681, 1559691, 1542736, 1810976 and 2129685. CC BY 4.0. Porter et al. (2023), ArcticDEM
  Version 4.1, Harvard Dataverse, doi:10.7910/DVN/3VDC4W.
- **Faroe Islands:** data from the Faroese Environment Agency, Umhvørvisstovan: FO_DTM_2009_10m and
  FO_DSM_2015_FOTM_2M (foroyakort.fo). Terms:
  https://www.foroyakort.fo/um-foroyakort/terms-and-conditions-in-english. No endorsement implied.
- **Map data** © OpenStreetMap contributors, available under the Open Database License (ODbL):
  https://www.openstreetmap.org/copyright. The roads and place names here are a derived database
  under the ODbL.
- **Danmarks Digitale Jordartskort 1:25 000** © GEUS, CC BY 4.0.
- **PROMICE-2022 Ice Mask** (doi:10.22008/FK2/O8CLRE) and the **PROMICE 1980s ice mask**
  (doi:10.22008/FK2/PRWITW), Geological Survey of Denmark and Greenland (GEUS), CC BY 4.0.

No warranty: check critical heights in the field.
