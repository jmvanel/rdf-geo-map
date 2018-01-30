# rdf-geo-map

Widget HTML page for geographical maps from RDF data.

The static page source is geo-map.html in doc/ directory .
It is a reusable web page getting its RDF data URL from the query part of the URL, namely an `url=` pseudo HTTP parameter .

NOTE: I call this a pseudo HTTP parameter, because it looks like an HTTP parameter in the URL, but since it's a static page, the parameters are analyzed by a JavaScript function.

For using it in your application, the page geo-map.html is served by github.io at the HTTPS URL:

https://jmvanel.github.io/rdf-geo-map/geo-map.html

If you need an HTTP URL, use instead the rawgit server:

http://rawgit.com/jmvanel/rdf-geo-map/master/docs/geo-map.html

## Examples

An example of using the Widget with a static RDF data URL:

http://rawgit.com/jmvanel/rdf-geo-map/master/docs/geo-map.html?url=http://dbpedia.org/resource/%C3%8Ele-de-France

An example of using the Widget in semantic\_forms :
 
http://semantic-forms.cc:9112/assets/geo-map/geo-map.html?view=points&enrich=yes&url=http://semantic-forms.cc:9112/sparql?query=PREFIX%20rdfs%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0APrefix%20geo%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2003%2F01%2Fgeo%2Fwgs84_pos%23%3E%0A%23CONSTRUCT%20%7B%20%3FS%20%3FP%20%3FO%20.%20%7D%20WHERE%20%7B%20GRAPH%20%3FG%20%7B%20%3FS%20%3FP%20%3FO%20.%20%7D%20%7D%20LIMIT%2010%0A%0ACONSTRUCT%20%7B%20%3Fsub%20geo%3Along%20%3FLON%20.%3Fsub%20geo%3Alat%20%3FLAT%20.%20%3Fsub%20rdfs%3Alabel%20%3FLAB.%7D%0AWHERE%20%7BGRAPH%20%3FGRAPH%20%7B%20%3Fsub%20geo%3Along%20%3FLON%20.%3Fsub%20geo%3Alat%20%3FLAT%20.%20%3Fsub%20rdfs%3Alabel%20%3FLAB.%20%20%7D%20%7D%0ALIMIT%201000


