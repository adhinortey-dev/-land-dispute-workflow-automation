# Land Dispute Workflow Automation

This project demonstrates a cloud GIS and workflow automation prototype for land dispute and lease application processing. It was developed as an academic land administration exercise at the University of Twente.

The repository contains a ProcessMaker/WFMS workflow export, digital form definitions, supporting documentation, and saved interface evidence showing the workflow design environment.

## Project Objectives

- Design a digital workflow for land dispute complaint handling.
- Model lease and land administration application forms.
- Connect form-based workflows with web map interaction.
- Use OpenLayers and OGC web services to support area-of-interest selection and lot identification.
- Support structured review steps including survey, recommendation, accountancy, record update, and final outcome.

## Repository Structure

```text
.
├── workflow/                 # ProcessMaker/WFMS exported workflow package
├── forms/
│   ├── land-dispute/         # Land dispute workflow form definitions
│   └── lease/                # Lease workflow form definitions
├── docs/                     # Workflow report and assignment documentation
├── evidence/
│   └── wfms-page/            # Saved WFMS designer page evidence
└── README.md
```

## Main Components

- `workflow/land-dispute-processmaker-export.pmx`: exported ProcessMaker/WFMS workflow package.
- `forms/land-dispute/`: JSON form definitions for complaint intake, survey review, recommendation, accountancy, outcome, and record update stages.
- `forms/lease/`: JSON form definitions for lease application, analysis, survey, and lot allocation.
- `docs/workflow-summary.md`: concise explanation of the workflow logic.
- `evidence/wfms-page/wfms-designer-page.html`: saved evidence of the WFMS/ProcessMaker designer environment.

## Workflow Logic

The workflow begins when an applicant submits a land dispute complaint or lease application. The intake form captures identity, contact, parcel, title, dispute, and supporting-document information. A map panel allows the user to interact with spatial layers, identify a lot or area of interest, and pass selected map attributes into workflow form fields.

The back-office stages then support survey review, administrative recommendation, accountancy checks, record updates, and final outcome documentation.

## GIS and Cloud Integration

The workflow uses OpenLayers inside a digital form to connect with OGC services. The form script references WMS/WFS-style services for city, district, and lot layers, allowing cadastral or administrative features to be selected in the browser and used inside the workflow.

This demonstrates how land administration workflows can combine:

- Digital case intake
- Web GIS interaction
- Parcel/lot selection
- Spatially enabled decision support
- Structured back-office processing

## Tools and Technologies

- ProcessMaker/WFMS
- OpenLayers
- OGC WMS/WFS services
- JavaScript
- JSON form definitions
- Cloud GIS concepts
- Land administration workflow design

## Reproducibility

To inspect the project:

1. Review `docs/workflow-summary.md` for the process overview.
2. Inspect the JSON form definitions in `forms/`.
3. Import `workflow/land-dispute-processmaker-export.pmx` into a compatible ProcessMaker/WFMS environment.
4. Open `evidence/wfms-page/wfms-designer-page.html` to view saved evidence of the workflow designer page.
5. Review the academic report in `docs/` for the broader assignment context.

## Note

All forms, names, parcel references, and records in this repository are instructional/demo materials used for academic purposes.
