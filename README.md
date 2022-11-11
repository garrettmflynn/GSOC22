# gsoc
Work Summary for Google Summer of Code 2022

## An Open-Source Software Suite for EEG Artifact Annotation on Web Browsers

### Summary
From May 22nd to November 14th, I worked with [Jorge Bosch-Bayard](https://scholar.google.com/citations?user=-wVncXgAAAAJ&hl=en) and [Pedro Valdes-Sosa](https://scholar.google.com/citations?user=0M2PVJIAAAAJ&hl=en) from the[ Global Brain Consortium](https://globalbrainconsortium.org/) (GBC) to produce novel web-based annotation applications for the [Brain Imaging Data Structure](https://bids.neuroimaging.io/) (BIDS) under their [Global EEG Norms](https://globalbrainconsortium.org/project-norms.html) project.

### Actual Timeline
Our initial work focused on the development of [gen](https://github.com/garrettmflynn/gen): a Progressive Web Application (PWA) for the annotation of EEG data on the browser. 

In preparation for the [2022 International Congress of Clinical Neurophysiology](https://ifcn.site-ym.com/mpage/ICCN2022) (ICCN), however, we decided to leverage [AnyWave](https://gitlab-dynamap.timone.univ-amu.fr/anywave/anywave)—an existing annotation tool developed by Bruno Columbet and Christian Benar at the The Institut de Neurosciences des Systèmes (INS) in Marseille, France.

From July through November 2022, then, the GBC and INS teams closely collaborated to update the AnyWave application to natively support annotation with [Hierarchical Event Descriptor](https://bids-specification.readthedocs.io/en/stable/99-appendices/03-hed.html) (HED) tags ([anywave_hed](https://github.com/garrettmflynn/anywave_hed)) and be distributed to clinical neurophysiologists following ICCN 2022 ([anywave_gen](https://github.com/garrettmflynn/anywave_gen), in progress).

Near the end of the project, I've also been put into contact with a trainee who will take over the majority of the work following the GSOC 2022 project period.

### Outcomes


On a personal note, I was able to secure a contract with the [Kavli Foundation](https://kavlifoundation.org/) to produce a JavaScript API for [Neurodata without Borders](https://www.nwb.org/) files—in part due to my work of developing a JavaScript API for reading and writing BIDS files as part of [gen](https://github.com/garrettmflynn/gen).


### Reflections
Throughout this project, I've learned a lot about the challenges of working with large, distributed teams and the importance of clear communication and consensus-building before writing any code.

I put much time into the development of [gen](https://github.com/garrettmflynn/gen) at the early stages of the project, we collectively decided that our time would be best spent focusing on the distribution of AnyWave to clinical neurophysiologists—not on development of the application itself. As such, the majority of the development was outsourced to the INS team, while myself and my mentors focused on determining the appropriate integrations that we'd need to acheive our goals of simple distribution of AnyWave for the collection of huge amount of EEG annotations.

While this looked significantly different than the original plan, I'm happy with the outcome and the work that I was able to do. In the coming months, I'm also excited to see the AnyWave application be used by clinical neurophysiologists around the world to annotate EEG data for the GBC project!

----

## Appendix
### Official Project Description
> Artifacts are parts of a measured signal generated from sources other than those of interest. For electroencephalography (EEG) data, artifacts from a variety of physiological and environmental sources must be excluded or repaired to ensure that appropriate interpretations are applied during clinical evaluation and downstream analyses. We will develop a suite of web-based tools for facilitating artifact annotations for the Global EEG Norms project of the Global Brain Consortium (GBC). This project will enable clinical neurophysiologists to upload EEG data in standardized formats; annotate data with artifacts, such as electrical noise and movement artifacts, using a novel ontology that is interoperable with the Hierarchical Event Descriptors specification; and export this data to the Brain Imaging Data Structure standard. While the resulting libraries of this project will be integrated into a Progressive Web Application for clinical neurophysiologists, they will also be released standalone as tools to further facilitate the development of neuroscience tools on the Open Web. This could reduce the barriers to entry for neurophysiology research by enabling standalone data management and analysis applications to be released on modern browsers. In the long run, this may enable the rapid diagnosis of neurological disorders in lower to middle-income countries with unreliable internet connections.

### Additional Resources
To view my [official project page](https://summerofcode.withgoogle.com/programs/2022/projects/WOkMdu9V), head over to the main GSOC website.

To view my early notes while working on this project, see the [notes](./notes/README.md) subdirectory