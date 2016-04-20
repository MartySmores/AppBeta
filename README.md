# Beginner's Guide to Webpack Repo

> This tutorial uses Babel 6

#### This goes along with the medium post [Beginner's Guide to Webpack](https://medium.com/@dabit3/beginner-s-guide-to-webpack-b1f1a3638460)

##### To get started with this project, do the following:

1. Git clone the project
2. cd into the project
3. run 'npm install' from the terminal
4. install webpack and webpack-dev-server globally:
```
npm install webpack-dev-server -g
npm install webpack -g

```




d3.selectAll("circle").remove()
d3.json("circle3.json", function(collection) {
	/* Add a LatLng object to each item in the dataset */
	collection.objects.forEach(function(d) {
		d.LatLng = new L.LatLng(d.circle.coordinates[0],
								d.circle.coordinates[1])
	})

	var feature = g.selectAll("circle")
		.data(collection.objects)
		.enter().append("circle")
		.style("stroke", "black")
		.style("opacity", .6)
		.style("fill", function(d) {
			return d.circle.colour[0];
	})
		.attr("r", function(d) { return d.circle.scale[0]; });

	map.on("viewreset", update);
	update();

	function update() {
		feature.attr("transform",
		function(d) {
			return "translate("+
				map.latLngToLayerPoint(d.LatLng).x +","+
				map.latLngToLayerPoint(d.LatLng).y +")";
			}
		)
	}
})
# AppBeta
