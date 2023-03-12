## Bashutils
`Bashutils` is a collection of bash scripts designed to speed up interaction with the console and improve productivity. Main focus of `Bashutils` is text processing. 

For example, if you want to convert all the letters in your message to lowercase and replace all spaces with underscore, you can write:
```bash
$ echo "TEXT OF A MESSAGE" | awk '{print tolower($0)}' | sed 's/ /_/g' 
```
with `Bashutils`
```bash
$ echo "TEXT OF A MESSAGE" | lowercase | underscore
```
or simply 
```bash
$ lowercase "TEXT OF A MESSAGE" | underscore
text_of_a_message
```

### Features

<video width="100%" height="auto" controls><source src="sample-usage.mp4" type="video/mp4">
    Your video does not support the video tag.
</video>

![](sample-usage.gif?raw=true "Sample usage")


- camelcase - Converts snakecase notation to camelcase
```bash
$ camelcase "foo_bar"
fooBar
```

- pascalcase - Converts snakecase notation to pascalcase 
```bash
$ pascalcase "foo_bar"
FooBar
```

- snakecase - Converts camelcase notation to snakecase
```bash
$ camelcase "fooBar"
foo_bar
```

- lowercase - Converts uppercase text to lowercase
```bash
$ lowercase "FOO BAR BAZ"
foo bar baz
```

- uppercase - Converts lowercase text to uppercase
```bash
$ uppercase "foo bar baz"
FOO BAR BAZ
```

- dash - Replaces space or underscore occurrences with dash
```bash
$ dash "foo bar_baz"
foo-bar-baz
```

- space - Replaces dash or underscore occurrences with space
```bash
$ space "foo-bar_baz"
foo bar baz
```

- underscore - Replaces dash or space occurrences with underscore
```bash
$ underscore "foo-bar baz"
foo_bar_baz
```

- dec2hex - Converts decimal number to hexadecimal
```bash
$ dec2hex 254
FE
```

- hex2dec  - Converts hexadecimal number to decimal
```bash
$ hex2dec FFFF
65535
```

### Installation
- Clone/download `bashutils` to a directory. 
- Update system PATH variable to point to the `bashutils` directory.

	Edit bash startup configuration script file and add following change to the end of the file:
	```console
	export PATH="/path/to/download/dir/bashutils:$PATH"
	```
	Usually path to the startup script file is:
	- ~/.bash_profile on MacOS,
	- ~/.bashrc on Debian/Ubuntu based systems,
	- For other system refers to its manuals.

- Reopen terminal or reload configuration

The `bashutils` scripts should be ready for use.

### License
MIT © [Robert Andrzejczyk](https://github.com/rojarand)

### Contribute
Contributions are always welcome!

