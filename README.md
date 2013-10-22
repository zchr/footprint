footprint
=========

Using Google Takeout, users can download their location history as a .json file. I wanted to map this data to see where I've been in Google's mind. The results are fascinating.

The code is heavily sculpted around Leaflet.js's outstanding tutorial here: http://leafletjs.com/examples/quick-start.html

The only requirement is a free CloudMade (http://cloudmade.com/) API key to insert in the url where specified.

As commented, the latitude and longitude pulled from the json file for each point assumes the same structure as Google's LocationHistory.json file, though it will work for any json file with coordiantes so long as the variable "lat" points to the correct latitude point and the varialbe "longi" points to the correct longitude point within each json object. Also, Google's format gave coordinates without decimals (such as "337880428" instead of "33.7880428"). If you're json file gives the decimal version, then there is no need to divide by 10,000,000.
