---
layout: page
title: "Projects"
permalink: /projects.html
---

### Biodiversity Informatics Group, PI Claus Weiland, Senckenberg Society for Nature Research

I am currently a scientific software engineer in the Biodiversity Informatics group of Claus Weiland working mainly on projects related to the NFDI4Earth. This is a German consortium of more than 60 partner organisations (universities, research institutes, and public organisations), and *"a community-driven process providing researchers with FAIR, coherent, and open access to all relevant Earth System data, to innovative research data management and data science methods"*, quoting the [NFDI4Earth website](https://www.nfdi4earth.de/). I am a member of the working group for the NFDI4Earth Community Label in the section [2Interoperate](https://nfdi4earth.de/2interoperate) and also involved in the NFDI4Earth Knowledge Hub, the backend for the NFDI4Earth Portal based on a graph database with a SPARQL interface.

<br/><br/>

### Fries Lab, Ernst Strüngmann Institute (ESI) for Neuroscience

I was a scientific software developer in the [lab of Prof. Dr. Pascal Fries](https://www.esi-frankfurt.de/people/pascalfries/) at [ESI](https://www.esi-frankfurt.de/), working on the [Syncopy Python package](https://github.com/esi-neuroscience/syncopy) for electrophysiology data analysis (MEG, EEG, ECoG). Syncopy is easy-to-use, with an interface similar to [Fieldtrip](https://github.com/fieldtrip/fieldtrip), the standard Matlab package for the analysis of electrophysiology data. Syncopy is designed for large-scale data anaylysis and parallel computations, and can utilize multi-core machines and high-performance computing (HPC) systems like clusters running the Slurm job scheduler.

<img style="" src="assets/img/syncopy_signals.png" alt="Electrophysiology data in Syncopy" width="70%">
<figcaption>
Figure 1: Visualization of electrophysiological data, created with Syncopy.
</figcaption>

<br/><br/>

### Ecker Lab, University Hospital Frankfurt

I was a postdoc in Computational Neuroimaging at [University Hospital Frankfurt](https://kgu.de) in the Department of Child
and Adolescent Psychiatry, Psychosomatics and Psychotherapy in the [group of Prof. Dr. Christine Ecker](https://www.kgu.de/einrichtungen/kliniken/zentrum-fuer-psychische-gesundheit/psychiatrie-psychosomatik-und-psychotherapie-des-kindes-und-jugendalters/forschung/laboratory-of-neuroimaging) from 03/2018 - 04/2022. We used structural magnetic resonance imaging (sMRI) in combination with genetic data to better understand the mechanisms of autism spectrum disorders, and the complex interplay of neuroanatomy and brain function. We applied statistical and machine learning methods implemented in R, Python and Matlab to surface-based cortical reconstructions generated with [FreeSurfer](http://freesurfer.net).

<img style="" src="assets/img/fsbrain_vis_overview.jpg" alt="sMRI descriptor visualization" width="70%">
<figcaption>
Figure 2: Visualization of sMRI neuroimaging data, created with my <a href="https://github.com/dfsp-spirit/fsbrain">fsbrain package for R</a>. <b>A</b> Visualization of raw morphometry data (cortical thickness) from native space on the white surface of a subject. The view shows the data in tiles from 8 different angles. <b>B</b> Arbitrary data (p-values in this case) visualized on the regions of the Desikan atlas, using the surface of the fsaverage (standard space template) subject from FreeSurfer. The view shows the data in tiles from 4 different angles. <b>C</b> The regions of the Desikan atlas on the white surface of a subject. The colors were loaded from the respective annotation file.
</figcaption>

<br/><br/>

### Molecular Health GmbH, Heidelberg

I worked as a scientific software developer at [Molecular Health](https://www.molecularhealth.com), a bioinformatics company that produces software solutions for precision medicine, with the goal to make the latest research available to clinicians based on AI and curated data from publications.

The main project was an internal web application for biomedical data curation based on Python, [PostgreSQL](https://www.postgresql.org/) and [SQLAlchemy](https://www.sqlalchemy.org/) for the backend and [React.js](https://reactjs.org/) for the frontend. Another project was a high-throughput natural language processing system, which used Perl to orchestrate interdependent jobs in compute pipelines running on an HPC cluster.

<br/><br/>

### Koch Lab, Goethe University Frankfurt am Main


I finished my doctorate in the [lab of Prof. Dr. Ina Koch](http://www.bioinformatik.uni-frankfurt.de) in 2016 and mainly worked on the following two projects in the fields of digital pathology and structural biology:

<br/>

#### Digital pathology: The spatial distribution of immune cells in Hodgkin lymphoma


In this project, I worked on the analysis of Hodgkin lymphoma, a cancer of the lymphatic system, based on high-resolution images. We were interested in better understanding the way tumour cells interact with their environment, communicate and spread through the lymphatic system. We implemented a digital image analysis pipeline to perform cell detection, description and classification with the goal to aid pathologists during the diagnosis of the various sub types of lymphoma.

We used graphs to model and compare spatial cell distributions in different Hodgkin lymphoma subtypes as well as lymphadenitis. The project is a collaboration with [Prof. Dr. Dr. h.c. Martin-Leo Hansmann](https://de.wikipedia.org/wiki/Martin-Leo_Hansmann") at the [Senckenberg Institute of Pathology](https://www.kgu.de/pathologie) at [University Hospital Frankfurt](https://kgu.de).

<img style="" src="assets/img/cellgraph.jpg" alt="Cellgraph" width="70%">
<figcaption>
Figure 3: Part of a whole slide image from a Hodgkin lymphoma case. Cell nuclei are stained in blue, and CD30+ cells in red. A cell graph is displayed as an overlay. Each vertex represents a cell detected by our imaging pipeline. Edges are added between cells which are close to each other. The graphs can be used to quantify clustering and to compare cell distributions.
</figcaption>

<br/>

#### Structural biology: The new Protein Topology Graph Library (PTGL) webserver

My diploma thesis dealt with modeling protein structure topologies by graph-theoretical methods. A part of the thesis was the development of the <a href="http://www.bioinformatik.uni-frankfurt.de/tools/vplg/index.html">Visualization of Protein Ligand Graphs (VPLG) software</a>. VPLG computes and visualizes protein ligand graphs. It works on the super-secondary structure level and uses the atom coordinates from PDB files and the SSE assignments of the DSSP algorithm. The graphs can be saved to a database or exported in standard graph formats for further analysis, including protein structure comparison and evolutionary studies.

VPLG is free software and available from the [PTGL project website at GitHub](https://github.com/MolBIFFM/PTGLtools). It powers the [PTGL protein topology database](http://ptgl.uni-frankfurt.de), a web server which also supports motif detection and other advanced queries based on the graphs computed for all proteins of the RCSB Protein Data Bank.

<img style="" src="assets/img/ptgl_overview.png" alt="PTGL Protein graph creation" width="70%">
<figcaption>
Figure 4: From 3D atom data to protein graph. The 3D atom coordinates and the secondary structure assignments are used to compute contacts between secondary structure elements (SSEs). In the final cell graph, each vertex represents an SSE, and edges model spatial contacts and relative spatial orientations between SSEs.
</figcaption>

<br/><br/>

# Education

* PhD (Dr. rer. nat.), Bioinformatics, summa cum laude
  - Supervisor: [Prof. Dr. Ina Koch](http://www.bioinformatik.uni-frankfurt.de)
  - [Department of Molecular Bioinformatics](http://www.bioinformatik.uni-frankfurt.de), [Goethe University Frankfurt am Main](https://www.goethe-university-frankfurt.de), Germany
  - Thesis: Tim Schäfer. *Application of graph theory to the topologies of proteins and Hodgkin lymphoma.* Dissertation. Goethe University Frankfurt, Germany, 2016.

