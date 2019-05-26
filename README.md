# clime (v1.0.0)
```clime``` is a simple script that will fetch weather information and display it on your terminal.

---
## Usage

```shell
clime [where] [unit] [type]

[where] arguments:
-o, --origin			            : Current location
City,2-digit Country Code	    : Example - Boston,US (notice no spaces)

[unit] arguments:
-c, --celsius			        : Degrees Celsius (Metric)
-f, --fahrenheit		        : Degrees Fahrenheit (Imperial)
-k, --kelvin			        : Kelvin (SI)

[type] arguments:
-n, --now			                : Current weather
-m, --multiple			        : Weather forecast in 3-hour intervals for 5-days
```

**Note:** All 3 arguments must be filled in for a successful result.

###Examples:
```shell
clime -o -c -n
```
_Output_:
```shell
Currently in Cornelius, US
29.7°C | clear sky
```
----
```shell
clime Delhi,IN -c -n 
```
_Output_:
```shell
Currently in Delhi,IN
37.1°C | haze
```
---
```shell
clime -o -f -m
```
_Output_:
```shell
Forecast in Cornelius, US
----------2019-05-26----------

15:00:00 | 95.14°F | clear sky

18:00:00 | 98.69°F | clear sky

21:00:00 | 97.14°F | overcast clouds

----------2019-05-27----------

00:00:00 | 85.51°F | overcast clouds

03:00:00 | 76.01°F | overcast clouds

06:00:00 | 71.42°F | broken clouds

09:00:00 | 70.43°F | clear sky

12:00:00 | 74.39°F | clear sky

15:00:00 | 84.65°F | overcast clouds

18:00:00 | 90.34°F | overcast clouds

21:00:00 | 89.58°F | overcast clouds

----------2019-05-28----------

00:00:00 | 80.79°F | overcast clouds

03:00:00 | 74.59°F | overcast clouds

06:00:00 | 71.71°F | overcast clouds

09:00:00 | 69.53°F | broken clouds

12:00:00 | 74.62°F | broken clouds

15:00:00 | 87.08°F | overcast clouds

18:00:00 | 92.98°F | overcast clouds

21:00:00 | 93.34°F | scattered clouds

... and so on.
```
---
```shell
clime Boston,US -k -m 
```
_Output_:
```shell
Forecast in Boston,US
----------2019-05-26----------

15:00:00 | 303.38 K | scattered clouds

18:00:00 | 305.76 K | scattered clouds

21:00:00 | 302.82 K | broken clouds

----------2019-05-27----------

00:00:00 | 295.36 K | broken clouds

03:00:00 | 290.6 K | overcast clouds

06:00:00 | 288.851 K | overcast clouds

09:00:00 | 286 K | broken clouds

12:00:00 | 289.9 K | scattered clouds

15:00:00 | 295.1 K | broken clouds

18:00:00 | 297.463 K | broken clouds

21:00:00 | 297.437 K | broken clouds

----------2019-05-28----------

00:00:00 | 292.756 K | broken clouds

03:00:00 | 285.913 K | scattered clouds

06:00:00 | 282.513 K | scattered clouds

09:00:00 | 281.2 K | broken clouds

12:00:00 | 286.63 K | broken clouds

15:00:00 | 291.048 K | overcast clouds

18:00:00 | 287.83 K | light rain

21:00:00 | 285.83 K | light rain

... and so on.
```

---
## Installation

**Note:** _This has only been tried and tested on Debian and MacOS. This installation guide may not work on other operating systems._

### Prerequisites
* Install [jq](https://stedolan.github.io/jq/download/)

1. Clone this repository.
2. Unless you have one already, create a folder in your root directory called ```bin/```.
```script
cd ~
mkdir bin/ 
```
3. Add the absolute path of the ```bin/``` directory to the ```.bashrc``` or ```.bash_profile```.
    * In your ```bin/```, do a ```pwd``` command. The output of that command will be your absolute path to ```bin/```.
    * Open your ```.bashrc```. On the top of the file, add this line
    ```script
    export PATH=$PATH:<OUTPUT-OF-pwd>
    ```
4. Copy the ```clime``` script from the repository to the ```~/bin/``` folder.
```script
cp clime ~/bin/
```
5. Set ```clime``` as an executable in the ```~/bin/``` directory.
```script
cd ~/bin/
chmod +x clime
```
6. Type ```clime``` and hit the ```Return``` key to see the result.
```script
clime
```
```script
Get simple weather details using the command-line and on your command-line.

clime [where] [unit] [type]

[where] arguments:
-o, --origin			            : Current location
City,2-digit Country Code	    : Example - Boston,US (notice no spaces)

[unit] arguments:
-c, --celsius			        : Degrees Celsius (Metric)
-f, --fahrenheit		        : Degrees Fahrenheit (Imperial)
-k, --kelvin			        : Kelvin (SI)

[type] arguments:
-n, --now			                : Current weather
-m, --multiple			        : Weather forecast in 3-hour intervals for 5-days
```
If the above output is your result, then ```clime``` is setup properly

---
## Acknowledgements

* ```clime``` is powered by [OpenWeatherMap](https://openweathermap.org).

---
## Contributors
- Andrei Biswas <axb6972@rit.edu>

---
## License
clime is under the [MIT License](https://github.com/codeabiswas/clime_cli/blob/develop/LICENSE).