# Holster
Easy placeholder templates in MeteorJS for Blaze inspired by facebooks loading pattern

While your templates fetching data, use this package to add a low-fi placeholder, or as a drop-in for prototype layouts.  

![holster placeholder text screen shot](https://raw.githubusercontent.com/Pushplaybang/holster/master/assets/screenshot.png)



## Install
Simple install the package via atmosphere

```sh
meteor add pushplaybang:holster
```




## Templates
There are a few templates to choose from, with relatively simple options,  Each determines the number of lines the placeholder text blocks contains.

 * holsterSingle
 * holsterDouble
 * holsterTriple
 * holsterQuad

each takes three parameters, heres an example:

```html
{{> holsterSingle type="title" mod="none" color="grey" }}
```

* **type**  - title, h-1, h-2, h-3, paragraph, small
* **mod** - none, half, end
* **color** - light, grey, dark

## Example
I usually return the ready state of the template level subscription through my helpers, and then use it in the template to show these while I'm fetching data.

````html
<h2>
  {{#unless ready}}
    {{> holsterDouble type="h-2" mod="none" color="light" }}
  {{else}}
    {{ title }}
  {{/unless}}
</h2>
````


### TODO
* image holster
* Form holster
* list holster
* possibly convert to svg



### Contributions and Suggestions Welcome!
Have something you think this needs or could use as an improvement, let me know.  add [an issue on github]() or fork and create a pull request.



____


### License [MIT](https://opensource.org/licenses/MIT)
Copyright (c) 2016 Paul van Zyl

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.  IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

