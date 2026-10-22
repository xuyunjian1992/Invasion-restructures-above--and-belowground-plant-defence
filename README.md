# Data and figures for: Invasion drives coordinated restructuring of above- and belowground defence strategies in plants

This repository contains the raw data and figure source file accompanying the manuscript:

> Xu Y., Xu C., Chen J., Zhou J., Siemann E. & Wang Y. **Invasion drives coordinated restructuring of above- and belowground defence strategies in plants.** (manuscript under submission)

Corresponding author: Yi Wang (yiwang@ynu.edu.cn), Yunnan University, Kunming, China.

---

## 1. Study overview

Eight native (USA) and eight invasive (China) populations of *Phytolacca americana* were grown in a fully factorial glasshouse experiment (Chenggong Campus, Yunnan University; 24°49′58″N, 102°51′5″E; April–July 2025) with three factors:

- **Origin**: native (USA) vs. invasive (China), 8 populations each;
- **Aboveground herbivory**: no-feeding control vs. feeding by one third-instar *Spodoptera litura* larva per plant (each fed-upon leaf damaged to ~25% of leaf area; feeding lasted three weeks);
- **Belowground herbivory**: no-nematode control vs. inoculation with *Meloidogyne enterolobii* at low (2,500 second-stage juveniles, J2, per pot) or high (7,500 J2 per pot) density, applied one week before aboveground herbivory.

Each population × treatment combination had six replicate pots: 2 origins × 8 populations × 2 aboveground levels × 3 belowground levels × 6 replicates = **576 pots**.

## 2. Treatment codes

| Treatment code | Meaning |
|---|---|
| CK | No-herbivory control |
| SL | *S. litura* feeding only |
| N1 | Low-density nematodes (2,500 J2) only |
| N1-SL | Low-density nematodes + *S. litura* |
| N2 | High-density nematodes (7,500 J2) only |
| N2-SL | High-density nematodes + *S. litura* |

In the `Pot_ID` column, the trailing digit (1–6) is the replicate number within each population × treatment combination. The letter prefix of `Pot_ID` is the original pot label used during the experiment; it maps to treatment codes as follows: **CK → CK, B → SL, Y → N1, P → N1-SL, G → N2, R → N2-SL**.

## 3. Population codes

| Code | Province/State | Country | Origin | Latitude | Longitude |
|---|---|---|---|---|---|
| BJ | Beijing | China | Invasive | 39.88°N | 116.37°E |
| LN | Liaoning | China | Invasive | 38.90°N | 121.62°E |
| SD | Shandong | China | Invasive | 36.05°N | 120.34°E |
| SX | Shaanxi | China | Invasive | 33.06°N | 106.97°E |
| SC | Sichuan | China | Invasive | 32.58°N | 106.85°E |
| HB | Hubei | China | Invasive | 32.05°N | 111.92°E |
| FJ | Fujian | China | Invasive | 27.58°N | 117.97°E |
| GX | Guangxi | China | Invasive | 24.86°N | 107.67°E |
| MA-GT | Massachusetts | USA | Native | 42.73°N | 71.01°W |
| MA-CC | Massachusetts | USA | Native | 41.62°N | 70.59°W |
| SC-HV | South Carolina | USA | Native | 32.16°N | 81.09°W |
| GA-DA | Georgia | USA | Native | 31.36°N | 81.45°W |
| LA-NO | Louisiana | USA | Native | 29.91°N | 90.01°W |
| TX-HT | Texas | USA | Native | 29.76°N | 95.45°W |
| FL-SA | Florida | USA | Native | 29.71°N | 81.23°W |
| FL-UF | Florida | USA | Native | 29.65°N | 82.35°W |

## 4. File inventory

### 4.1 `growth_reproduction_data.xlsx` (sheet: `growth_reproduction`)

Growth, reproductive and leaf functional/physical trait data for all 576 pots.

| Column | Description | Unit |
|---|---|---|
| Origin | Population origin (Native / Invasive) | — |
| Population | Population code (see Section 3) | — |
| Treatment | Treatment code (see Section 2) | — |
| Pot_ID | Original pot label (treatment prefix + replicate number) | — |
| Plant_height_cm | Plant height before harvest, measured with a measuring tape | cm |
| Base_diameter_mm | Basal stem diameter | mm |
| Leaf_chlorophyll_content_SPAD | Relative chlorophyll content (SPAD value) of the third fully expanded leaf from the apex (TYS-A chlorophyll meter, Zhongke Weihe, Beijing, China) | SPAD |
| Specific_leaf_area_cm2_g | Leaf area / leaf dry mass (leaf area measured in ImageJ) | cm² g⁻¹ |
| Leaf_toughness_N | Mean puncture force of three leaf discs (texture analyser ZQ-990, Zhiqiu Precision Instruments, China) | N |
| Leaf_biomass_g | Oven-dried leaf mass (105 °C for 30 min, then 65 °C to constant mass) | g |
| Stem_biomass_g | Oven-dried stem mass | g |
| Reproductive_biomass_g | Oven-dried mass of flowers/fruits/infructescences | g |
| Aboveground_biomass_g | Leaf + stem + reproductive biomass | g |
| Root_biomass_g | Oven-dried root mass | g |
| Total_biomass_g | Aboveground + root biomass | g |
| Root_shoot_ratio | Root biomass / aboveground biomass (natural-log transformed before analysis in the manuscript) | — |
| Inflorescence_number | Number of inflorescences per plant | count |

**Missing data:** 9 of 576 plants lack `Specific_leaf_area_cm2_g` and `Leaf_toughness_N` values because the designated leaf was damaged or lost before measurement (blank cells). This corresponds to the reduced denominator degrees of freedom (541 vs. 550) for these two traits in Table 1 of the manuscript. 133 plants had not produced inflorescences by harvest (`Inflorescence_number` = 0, `Reproductive_biomass_g` = 0).

### 4.2 `defence_metabolites_data.xlsx`

Chemical defence and oxidative physiology data. Because chemical assays are destructive, three plants per population × treatment combination were used (288 samples in total; these were the 2nd–4th replicate pots of each combination).

- **Sheet `Summary`**: final trait values used in the manuscript analyses.
- **Sheets `Raw_*` (12 sheets)**: original microplate absorbance readings (SpectraMax iD5, Molecular Devices, USA) and the intermediate differences from which the final values were calculated, one sheet per trait. Total phenolics, total flavonoids and lignin were determined with commercial assay kits (Suzhou Grace Biotechnology Co., Ltd., China) in oven-dried, ball-milled tissue; peroxidase (POD) activity and malondialdehyde (MDA) content were determined in fresh tissue with commercial kits (Aidisheng Biotechnology Co., Ltd., China) following the manufacturers' protocols.

| Summary column | Description | Unit |
|---|---|---|
| Origin / Population / Treatment / Pot_ID | as above | — |
| Root_total_phenolics_mg_g_DW / Leaf_total_phenolics_mg_g_DW | Total phenolics in root / leaf tissue | mg g⁻¹ DW |
| Root_total_flavonoids_mg_g_DW / Leaf_total_flavonoids_mg_g_DW | Total flavonoids in root / leaf tissue | mg g⁻¹ DW |
| Root_total_alkaloids_per_kit_protocol / Leaf_total_alkaloids_per_kit_protocol | Total alkaloids in root / leaf tissue, expressed as defined by the kit protocol (data not analysed in the manuscript; shared here for completeness) | per kit protocol |
| Root_lignin_mg_g_DW / Leaf_lignin_mg_g_DW | Lignin in root / leaf tissue | mg g⁻¹ DW |
| Root_POD_activity_U_g_FW / Leaf_POD_activity_U_g_FW | Peroxidase activity in root / leaf fresh tissue | U g⁻¹ FW |
| Root_MDA_nmol_g_FW / Leaf_MDA_nmol_g_FW | Malondialdehyde content in root / leaf fresh tissue | nmol g⁻¹ FW |

Note: chemical samples were bulked from all leaves or the entire root system (including gall tissue in nematode treatments); values are tissue-level averages.

### 4.3 `root-knot_gall_count_data.xlsx` (sheet: `gall_counts`)

Root-knot gall counts for the 384 plants in the four nematode treatments (N1, N1-SL, N2, N2-SL); no galls occurred in CK and SL plants.

| Column | Description |
|---|---|
| Origin / Population / Treatment / Pot_ID | as above |
| Gall_count_small_diameter_1mm_or_less | Number of galls ≤ 1 mm in diameter |
| Gall_count_medium_diameter_1_to_2mm | Number of galls 1–2 mm in diameter |
| Gall_count_large_diameter_over_2mm | Number of galls > 2 mm in diameter |
| Gall_count_total | Total gall number per plant (sum of the three size classes) |

### 4.4 `Manuscript_Figures_SigmaPlot.JNB`

SigmaPlot notebook file containing the source graphs and plotted data for the manuscript figures (Fig. 1, Fig. 2, Fig. S1 and Fig. S2). Requires SigmaPlot (Systat Software) to open.

## 5. Data curation notes

Relative to the internal working files, the following non-destructive curation steps were applied (no data values were altered):

1. Column headers were renamed to self-explanatory, publication-ready names (e.g. `Tatol biomass(g)` → `Total_biomass_g`, `Leaf bimass(g)` → `Leaf_biomass_g`); 
2. A decoded `Treatment` column (CK / SL / N1 / N1-SL / N2 / N2-SL) was added alongside the original `Pot_ID`;
3. The population code `TXHT` in the growth dataset was harmonised to `TX-HT` as used elsewhere;
4. The gall-count file contains only the four nematode treatments because gall number was invariably zero in CK and SL.

## 6. License and citation

These data are released under **CC BY 4.0** (https://creativecommons.org/licenses/by/4.0/). If you use these data, please cite the manuscript and this repository.

## 7. Contact

Yi Wang, School of Ecology and Environmental Science, Yunnan University, Kunming 650091, China — yiwang@ynu.edu.cn
