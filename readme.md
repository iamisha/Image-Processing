# Image Processing

A collection of Python notebooks for medical image analysis, focusing on bone segmentation and mask manipulation techniques.

## What's this about?

Working with medical imaging data (NIFTI format), I've developed tools for:
- Segmenting bone structures from CT/MRI scans
- Expanding segmentation masks with precise measurements
- Creating randomized mask variations for robustness testing

## Directory Structure

```
./
├── code/                     # Python notebooks
│   ├── task1.1&1.2.ipynb     # Bone segmentation & expansion
│   ├── Task_1_3.ipynb        # Randomized mask generation
│   └── task1.4.ipynb         # Landmark analysis
│
└── results/                  # Output files
    ├── Task 1.1/             # Original bone masks
    ├── Task 1.2/             # Expanded masks (2mm/4mm)
    ├── Task 1.3/             # Randomized masks
    ├── Task 1.4/             # Landmark coordinates
    └── output images/        # Visualization outputs
```

## Implementation Details

### Bone Segmentation
Isolates bone structures from volumetric medical images using thresholding and morphological operations. Produces clean binary masks suitable for further analysis.

### Mask Expansion
Takes the bone mask and expands it uniformly by 2mm and 4mm. Uses distance transforms to ensure accurate distance-based dilation.

### Randomized Boundary Generation
Creates masks with random boundaries that lie between the original bone mask and its 2mm expanded version. Useful for testing segmentation robustness.

### Landmark Analysis (NEW!)
Identifies key anatomical landmarks in each mask version and exports their coordinates for registration analysis.

## Getting Started

1. Clone this repo
2. Set up the environment:
   ```bash
   # Create and activate virtual env
   python -m venv env
   source env/bin/activate
   
   # Install dependencies
   pip install -r requirements.txt
   ```

3. Run the notebooks:
   ```bash
   jupyter notebook code/
   ```

## Key Results

Results are stored as NIFTI (.nii.gz) files in the results directory, with separate folders for each processing stage. Visualization images show key slice views for quick inspection.
