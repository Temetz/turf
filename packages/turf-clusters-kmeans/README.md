# @turf/clusters-kmeans

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## clustersKmeans

Takes a set of [points](https://tools.ietf.org/html/rfc7946#section-3.1.2) and partition them into clusters using the k-mean .
It uses the [k-means algorithm](https://en.wikipedia.org/wiki/K-means_clustering)

**Parameters**

-   `points` **[FeatureCollection](https://tools.ietf.org/html/rfc7946#section-3.3)&lt;[Point](https://tools.ietf.org/html/rfc7946#section-3.1.2)>** to be clustered
-   `options` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** Optional parameters (optional, default `{}`)
    -   `options.numberOfClusters` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** numberOfClusters that will be generated (optional, default `Math.sqrt(numberOfPoints/2)`)
    -   `options.mutate` **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** allows GeoJSON input to be mutated (significant performance increase if true) (optional, default `false`)

**Examples**

```javascript
// create random points with random z-values in their properties
var points = turf.randomPoint(100, {bbox: [0, 30, 20, 50]});
var options = {numberOfClusters: 7};
var clustered = turf.clustersKmeans(points, options);

//addToMap
var addToMap = [clustered];
```

Returns **[FeatureCollection](https://tools.ietf.org/html/rfc7946#section-3.3)&lt;[Point](https://tools.ietf.org/html/rfc7946#section-3.1.2)>** Clustered Points with an additional two properties associated to each Feature:-   {number} cluster - the associated clusterId
-   {[number, number]} centroid - Centroid of the cluster [Longitude, Latitude]

<!-- This file is automatically generated. Please don't edit it directly:
if you find an error, edit the source file (likely index.js), and re-run
./scripts/generate-readmes in the turf project. -->

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/clusters-kmeans
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
