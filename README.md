GWAS Liftover Tool (GRCh37 ↔ GRCh38)

Convert SNP / GWAS summary statistic coordinates between genome builds
Supports both: GRCh37 → GRCh38 and GRCh38 → GRCh37

This repository provides Python scripts and Jupyter notebooks to convert genome coordinates between:
	•	GRCh37 (hg19)
	•	GRCh38 (hg38)

The conversion uses:
	•	UCSC liftover chain files
	•	pyliftover Python library

Supports both directions:

✔ GRCh37 → GRCh38
✔ GRCh38 → GRCh37

All original GWAS columns are preserved.
New coordinate columns such as Chr_37, bp_37 (or Chr_38, bp_38) are appended.


liftover/
│
├── chains/
│     ├── hg19ToHg38.over.chain.gz
│     └── hg38ToHg19.over.chain.gz
│
├── scripts/
│     └── liftover_gwas.py
│
├── demo/
│     └── liftover_demo.py
│
├── notebooks/
│     └── liftover_gwas_37_38.ipynb
│
└── README.md


You must download 2 chain files from UCSC:
1. GRCh37 → GRCh38
https://hgdownload.soe.ucsc.edu/goldenPath/hg19/liftOver/hg19ToHg38.over.chain.gz
2. GRCh38 → GRCh37
https://hgdownload.soe.ucsc.edu/goldenPath/hg38/liftOver/hg38ToHg19.over.chain.gz

Place them into:
chains/
    hg19ToHg38.over.chain.gz
    hg38ToHg19.over.chain.gz
