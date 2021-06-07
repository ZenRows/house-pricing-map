# House Pricing Map

Demo for a House Pricing distribution plotted on OpenStreetMap and Google Maps using heatmaps.

## Installation

There is **no need for installation**. Instead, take the files and open them in your favorite browser. We use JSONP to provide data inside the script; some browsers might block those requests. If there is any error, check the console.

## Dataset

All the housing data is in the `data.jsonp` file. The data comes directly from a [ZenRows](https://www.zenrows.com/) Task. We removed some fields to make it smaller. The script supports datasets with all the fields, so do not worry about directly pasting a new task output.


In the HTML files is a **minimum configuration** in case you want to plot different content. After setting the new data, modify the values `latitudeField`, `longitudeField`, and `valueField` (if changed) and refresh the page. Those should tell the script what data fields to get for creating the locations and heatmap.

We provide **two different HTMLs files with maps**, one using OpenStreetMap and the other one Google Maps. So there is no need to modify any of these (apart from the previous case), even if you use your own dataset.

### OpenStreetMap and Leaflet

Here we use some open-source projects for drawing maps and heatmaps: [OpenStreetMap](https://www.openstreetmap.org), [Leaflet](https://leafletjs.com), and [heatmap.js](https://www.patrick-wied.at/static/heatmapjs). Thanks once again to all of them. There is more info about how it works in the [HTML file](./leaflet.html).

### Google Maps

For this one, you will **need API Keys**. We provide them for the demo. Please do not abuse. There is a comment in the HTML showing that line that needs changing. There is more info about how it works in the [HTML file](./google-maps.html).

## How to get your own data

We need a **simple structure**: an object array containing latitude, longitude, and a numeric value. That's all.

You can gather that information manually for small datasets, but that will get complicated for large sets. However, there are great ones published online and free-to-use. Feel free to check them out and test them.

For **people with data or content**, export or transform them as JSON. [MySQL](https://dev.mysql.com/doc/mysql-shell/8.0/en/mysql-shell-json-output.html) supports exporting to JSON/array, and the same goes for  [MongoDB](https://docs.mongodb.com/database-tools/mongoexport/). You can also get excel or CSV files and convert them. But, again, there are online tools for that.

### How to collect online data

We implement a **no-code solution** for those of you that have great ideas but no data. You can several URLs to get content from, and we will extract structured data and store it in any format, like JSON, for you. So give it a try in [ZenRows](https://app.zenrows.com/register).

We generated data for this with a simple task that extracted almost **3000 houses in Bilbao, Spain**. t runs in less than a minute.

If you like the results, get in [contact](https://www.zenrows.com/contact) to show us what you've done ;)

## Contributing
Pull requests are welcome. For significant changes, please open an issue first to discuss what you would like to change.

## License
[MIT](./LICENSE)
