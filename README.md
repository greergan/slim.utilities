# slim.utilities
A set of reusable Typescript functions for the Slim platform

## slim.comingle

A synchronized version of comingle. Takes in multiple JSON objects and outputs a new object which contains comingled properties.

```
import { comingleSync } from "./comingleSync.js"

const json1 = {
    first_name: "Arthur"
};
const json2 = {
    middle_name: "Conan"
};
const json3 = {
    last_name: "Doyle"
};

const json4 = {
    first_name: "George"
}

const merged_object = comingleSync([json1, json2, json3, json4]);
console.log(merged_object);

const without_middle_name = comingleSync([json1, json2, json3, json4], {skip:['middle_name']});
console.log(without_middle_name);
```
Run the test.js file using Deno
```
deno run -r https://greergan.github.io/slim.comingle/test.js
```
