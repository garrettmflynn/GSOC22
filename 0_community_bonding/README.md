# Community Bonding Period
**May 20 - June 12**

## May 29th, 2022
1. Shared the project with EEGLab and HED people that Pedro connected me with via email
2. Allow for free text specification on loaded HED schemas
3. Fixed service worker registration to check the network for new updates
4. Completed the first draft of a *bids2bids* conversion for adding expected files and reformatting directories / filenames to conform with the BIDS standard.
    - One known issue is that it doesn't change metadata within files (e.g. scan files, where there may be a reference to a file that has now been renamed)
5. Listened to the EEGLab presentation shared by Pedro
5. Renamed the project from `artifact` to `ged` to reflect the broader goals of the Global EEG Norms project.


## May 28th, 2022
*Welp, I finally caught COVID...*
1. Styled the timeseries graph embedded in the dataset inspector
2. Loaded the SCORE schema

## May 27th, 2022
1. Visually annotate the first channel of an EDF file on Plotly
2. Reformatted the demo with the [visualscript](https://github.com/brainsatplay/brainsatplay/tree/main/src/visualscript), one of my other OS projects. Fixed several problems with how `visualscript` formats nested dashboards.

## May 26th, 2022
1. Loaded EDF and NWB files into the browser
2. Implented granular read on the EDF decoder since many files are very large and immediate buffer-parsing stalls the browser. It couldn't even handle more than two of my test files in memory!
3. Fixed WebNWB's ingestion of h5wasm (as the API surface has changed...)
4. Created a dummy .xml file for the artifacts ontology
5. Cloned [hed-examples](https://github.com/hed-standard/hed-examples) to have access to BIDS files with valid HED tags

## May 25rd, 2022
1. Loading all files as their filenames to avoid confusion about interpretation.
    - Having issues with compressed NiFTI images—though [bids-validator](https://github.com/bids-standard/bids-validator) also has an issue. Get a good (uncorrupted) dataset!
2. Can re-export the BIDS dataset as a .zip folder. You can optionally check using the [bids-validator](https://github.com/bids-standard/bids-validator) before allowing!
    - Issues with NiFTI headers when imported again...

### Meeting with Mentors (#1)
#### What I Need
[x] Nice EEG dataset—ideally with HED tags

#### Next Steps
[ ] Arbitrarily add an HED tag to an existing dataset

[ ] Lobby bids-validator to expose more of their API at the JavaScript object level (i.e. with objects as inputs)

[x] Check out [hed-schema-library](https://github.com/hed-standard/hed-schema-library) for how to register a new HED schema that we create for artifacts

#### What They Will Do
[ ] Add me to their neuroimaging Mendeley group

[x] Introduce me to the EEG BIDS and EEGLab groups and make them aware of our project

#### Clarifications
Our project is about *standards* in EEG data. We are only beginning with artifacts in resting-state EEG...but that is not the end.

The outcome is a dashboard that is useful for neurophysiology specialists who don't know anything about BIDS—and probably don't care.

## May 24rd, 2022
1. Commented on an [Issue](https://github.com/hed-standard/hed-javascript/issues/11) about the current hed-validator documentation
    - It turns out that the documentation has not been updated for quite a while—and they have developed an entirely new interface to work inside [bids-validator](https://github.com/bids-standard/bids-validator) that relies on an events file and merged JSON sidecars. So the last day was not very useful...
2. Loading .tsv, .json, and .gzip files into a JavaScript object, influenced by the [bids-validator](https://github.com/bids-standard/bids-validator) (which doesn't natively expose any methods to load objects...)
3. Created a rough frontend that allows for viewing and validating a BIDS dataset as a JavaScript object!


![Screenshot of chrome developer console with BIDSDataset object](./BIDSDatasetObject.png)

## May 23rd, 2022
1. Loaded HED schema files from the browser and used them to validate strings provided by the user with an `<input>` tag!

## May 22nd, 2022
1. Forked [bids-validator](https://github.com/bids-standard/bids-validator) and  [hed-javascript](https://github.com/hed-standard/hed-javascript) to begin dissecting how they handle BIDS files.
2. Rewrote the [hed-javascript](https://github.com/hed-standard/hed-javascript) repo for ES6 import/export support (so that it can be browser-native...)