# Hue

![Hue Logo](https://i.imgur.com/Pxe9la8.png)

Hue provides a minimal and powerful interface to print colored text and labels in the terminal.\
It works with Python 2 as well as Python 3.

What makes hue better than other coloring libraries? [Here's a comparison.](#why-hue)

## Supported Stuff

Following styles are supported

![Hue Styles](https://i.imgur.com/899ZtQy.png)

Following colors are supported

![Hue Colors](https://i.imgur.com/9tWvPkD.png)

Following labels are supported

![Hue Labels](https://i.imgur.com/dpJxqT2.png)


### Installation
You can install Hue with **pip** as follows:
```
pip install huepy
```
or with **easy_install**:
```
easy_install huepy
```

### Usage
First of all, import everything that Hue has to offer as follows:

```python
from huepy import *
```

To print text in a different color

```python
print red('This string is red')
```

For a different style of text

```python
print italic('This string is in italic')
```

Nest color and style to combine styles and colors

```python
print bold(red('This string is bold and red'))
```

Output:
![Output Examples](https://i.imgur.com/Lo7ZyHq.png)

And what is the use of those labels?\
I have been using these labels in projects as a minimal output schema.\
If some error occured in your program or something else bad happened you don't need to print the whole line in red. With hue, you can simply do this

```python
print bad('An error occured.')
```

Example outputs of the labels
![Label Examples](https://i.imgur.com/zJ7ZgUi.png)

#### List of all colors

```python
white, grey, black, green, lightgreen, cyan, lightcyan, red, lightred,
blue, lightblue, purple, light purple, orange, yellow
```

#### List of all styles

```python
bold, bg, under, strike, italic
```

#### List of all labels

```python
info, que, run, bad, good
```

**Note:** Currently Hue rely on ANSI escape sequences to output colors, so only Windows 10 will output colors.

### Why hue

Because its awesome!
Lets print a red colored string in popular coloring libraries:

- Colorama
```python
from colorama import Fore
print Fore.RED + 'This string is red'
```
- Termcolor
```python
import sys
from termcolor import colored, cprint
print colored('This string is red', 'red')
```
- Hue
```python
from hue import *
print red('This string is red')
```
Here's comparison table:

||Hue|Colorama|Termcolor|
|---|---|--------|---------|
|Compatibility|Unix & Windows 10|Unix & Windows|Unix|
|Ease of use|10/10|4/10|5/10|
|Bright Colors|Yes|No|No|

**Note:** Colorama and Termcolor print bold styled strings when asked for bright colored strings. On the other hand, Hue supports both bright and bold strings. Also the *Ease to use* ratings are a result of my own experience and may differ for others.

### Contribution

Further developement of Hue will be focused on Windows compatibility. Everyone is welcome to start a pull request for windows support. Additional colors and labels will be appreciated too.
