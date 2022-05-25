# Community Bonding Period
May 20 - June 12

## Activities 
### May 22nd, 2022
1. Forked [bids-validator](https://github.com/bids-standard/bids-validator) and  [hed-javascript](https://github.com/hed-standard/hed-javascript) to begin dissecting how they handle BIDS files.
2. Rewrote the [hed-javascript](https://github.com/hed-standard/hed-javascript) repo for ES6 import/export support (so that it can be browser-native...)

### May 23rd, 2022
1. Loaded HED schema files from the browser and used them to validate strings provided by the user with an `<input>` tag!

### May 24rd, 2022
1. Commented on an [Issue](https://github.com/hed-standard/hed-javascript/issues/11) about the current hed-validator documentation
    - It turns out that the documentation has not been updated for quite a while—and they have developed an entirely new interface to work inside [bids-validator](https://github.com/bids-standard/bids-validator) that relies on an events file and merged JSON sidecars. So the last day was not very useful...
2. Loading .tsv, .json, and .gzip files into a JavaScript object, influenced by the [bids-validator](https://github.com/bids-standard/bids-validator) (which doesn't natively expose any methods to load objects...)
3. Created a rough frontend that allows for viewing and validating a BIDS dataset as a JavaScript object!


![Screenshot of chrome developer console with BIDSDataset object](./BIDSDatasetObject.png)

### May 25rd, 2022
[coming soon] Meet with Pedro and Jorge
