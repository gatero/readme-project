# Project Name

Description for your project. No need to go into extensive detail here really.

If using a CI badge, add it next to the project name

## Quick Start

This is a list of steps to take to quickly scaffold and/or set up the project from a freshly cloned copy. It should consist of a list of commands or actions to run in order.

1. List of commands
2. to run
3. e.g. `npm install`
4. or `git clone --recursive`

Additional info such as live servers or tasks relevant to development can also go here:

* Additional commands available
* e.g. `gulp serve`
* or `npm link`

## Requirements

Requirements go here. Include minimum version (and maximum, if relevant), links, and alternate/preferred installation methods.

* [example 1](http://example.org) v1.2.3+
* [example 2](http://example.com) v3.2.1+ (install with `curl -s http://install.example.com | sh`)
* [libexample](http://example.net) v4.1.1+ or [libnewexample](http://example.net) v1.0.3+
* [These assets](http://example.org/assets.zip) unzipped into `app/assets` (overwrite everything)

## Tasks (for web apps with e.g. grunt or gulp)

List of common tasks goes here. Preferably in order of how much use it gets; i.e. more commonly used tasks at the top. This is usually for projects that consist of a website or product being developed.

### Live server

~~~sh
$ # Commands to execute the task
$ # Multiple commands if necessary
~~~

This describes the current task. Also describe any useful and relevant parameters and options. Include also any caveats and warnings.

### Build

~~~sh
$ # Commands to execute the task
$ # Multiple commands if necessary
~~~

This is another task.

## Development (for web apps; feel free to rename this section)

This section is meant to guide a new developer and help them start working as soon as possible. Use this section to describe, in rough terms, how the app works and how to add new functionality (or whatever) to it. Link to other documentation as necessary.

### Styles

All styles live in `app/public/styles`. To add new components, add them to `app/public/styles/components` and `@include` them in `app/public/styles/main.scss`.

### Templates

Templates are located in `app/framework/blah/templates`. Every template must include an ID as part of the [header](http://example.org), and must also inherit from `app/framework/blah/layouts/main.php`.

## Usage (for tools)

For projects that are meant to be used as a _tool_ instead of a product, use the How to Use section. Describe it in general terms here.

~~~sh
$ super-tool [options] -i infile -o outfile
~~~

Options:

    -p <file>  Prints file before processing
    -l <num>   Processes the first <num> lines
    -n         Add newlines
    -N         Add CRLF newlines
    -d <dir>   Output into <dir>

### Examples (Optional)

**Process and output into two directories at once:**
~~~sh
$ super-tool -d app/out -i file.txt -o - | tee app/processed.txt
~~~

**Sort and then process, with CRLF (Windows-style) newlines**
~~~sh
$ cat file.txt | sort | super-tool -N
~~~

**Add crazy new lines to everything**
~~~sh
$ find . -name "*.txt" | xargs -nN -d app/out
~~~

## Special cases (Optional)

If you consider that a certain part of your app/tool/whatever deserves special consideration (whether it's because it behaves oddly, or any important gotchas somewhere), feel free to add its own section.

## Contributing (Optional, recommended)

This is where you describe any requirements you have for PRs or any sort of contribution. This includes any coding standards to adhere to, tests to run, etc.

## Troubleshooting

Describe how to troubleshoot your app here. Ideally, make a list of steps that will at least help get useful information to troubleshoot.

1. Run `gulp lint`
2. Read the file
3. See if you can find what exploded
