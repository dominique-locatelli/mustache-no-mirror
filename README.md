# Mustache no mirror
This is a fork of the Dart library ['mustache'] (https://github.com/xxgreg/mustache) modified to remove calls to mirror API.


## Why removing calls to mirror API ?
Because when using the mirror API with *dart2js*, the generated code is very large ( 800kb -> 6Mb )


## What are the implications of this modification ?
Without the mirror API, the only way to retrieve named properties is the *[ ]* operator, 
so the values objects passed to *render* methods must implement this operator.
