# clime
```clime``` is a simple script that will fetch weather information and display it to your terminal.

**version 1.0.0**

---
## Usage

```shell
clime [where] [unit] [type]

[where] arguments:
-o, --origin			        : Current location
City,2-digit Country Code	: Example - Boston,US (notice no spaces)

[unit] arguments:
-c, --celsius			        : Degrees Celsius (Metric)
-f, --fahrenheit		        : Degrees Fahrenheit (Imperial)
-k, --kelvin			        : Degrees Kelvin (SI)

[type] arguments:
-n, --now			            : Current weather
-m, --multiple			    : Weather forecast \\in 3-hour intervals \\for 5-days
```

**Note:** All 3 arguments must be completed for a successful result.

---
## Installation

**Note:** _This has only been tried and tested on Debian and MacOS. This installation guide may not work on a different operating system._

### Prerequisites
* Install [jq](https://stedolan.github.io/jq/download/)

1. Clone this repository
2. Unless you have one already, create a folder in your root directory called ```bin/```
```script
cd ~
mkdir bin/
```
3. Copy the ```clime``` script from the repository to the ```~/bin/``` folder.
```script
cp clime ~/bin/
```
4. Set ```clime``` as an executable in the ```~/bin/``` directory
```script
cd ~/bin/
chmod +x clime
```
5. It should work now! Type ```clime``` and hit the Return key to see the result.
```script
clime

clime [where] [unit] [type]

[where] arguments:
-o, --origin			    : Current location
City,2-digit Country Code	: Example - Boston,US (notice no spaces)

[unit] arguments:
-c, --celsius			    : Degrees Celsius (Metric)
-f, --fahrenheit		    : Degrees Fahrenheit (Imperial)
-k, --kelvin			    : Degrees Kelvin (SI)

[type] arguments:
-n, --now			        : Current weather
-m, --multiple			    : Weather forecast \\in 3-hour intervals \\for 5-days
```

---
## Contributors
- Andrei Biswas <axb6972@rit.edu>

---
## License
clime is under the [MIT License](https://github.com/codeabiswas/clime_cli/blob/develop/LICENSE).