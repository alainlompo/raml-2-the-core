<h3> What's new in RAML 1.0</h3>
<h4>Overlays</h4>

Overlays allow you to include new informations into your .raml api design file: you may include new infos such as annotations, descriptions, example, ...
It allows you to extend your main .raml file for different API use cases.

<pre>
 #%RAML 1.0 
 types: !include common-services.raml
</pre>