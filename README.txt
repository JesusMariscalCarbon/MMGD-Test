MMGD-Test
=========

Directory structure
-------------------

MMGD-Test/
|-- README.txt
|-- 01_original_images/
|-- 02_harmonised_images/
|-- 03_manual_masks/
|-- 04_csv/
|   |-- complete_dataset.csv
|   |-- upper_subset.csv
|   |-- lower_subset.csv

Dataset description
-------------------

MMGD-Test is an external evaluation dataset for automatic meibomian gland segmentation in infrared meibography.

The dataset comprises 100 anonymised infrared meibography images acquired using a Keratograph 5M device without the Meibo Analytics software:

- 50 upper-eyelid images
- 50 lower-eyelid images

The images were cropped to a spatial resolution of 1,280 x 640 pixels to match the dimensions of the MGD-1K images used for model development.

Repository contents
-------------------

The repository contains three corresponding sets of files:

- original_images/: the original cropped infrared meibography images;
- harmonised_images/: the corresponding images after deterministic appearance harmonisation; and
- manual_masks/: the manually delineated reference masks of the meibomian glands.

The manual masks are stored as binary PNG images with the following pixel values:

- 0: background
- 255: meibomian gland

The CSV/ directory contains:

- complete_dataset.csv: filenames for the complete MMGD-Test dataset;
- upper_subset.csv: filenames for the 50 upper-eyelid cases; and
- lower_subset.csv: filenames for the 50 lower-eyelid cases.

The filenames recorded in the CSV files identify the cases included in each dataset or subset.

Appearance harmonisation
------------------------

The harmonised images were generated using the deterministic procedure described in the associated manuscript and supplementary materials. The procedure combines bilateral filtering, contrast-limited adaptive histogram equalisation (CLAHE), unsharp masking, and intensity normalisation. Image geometry and spatial resolution are not modified by this procedure.

Anonymisation and ethics
------------------------

All images were anonymised before inclusion in the repository. No directly identifying participant information is provided.

The collection and use of the data were conducted in accordance with the study protocol approved by the relevant research ethics committee.

Contact
-------

For questions concerning the dataset or the associated study, please contact the corresponding author: jesus.mariscal@dem.uhu.es
