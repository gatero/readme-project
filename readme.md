# The Readme Project

This is the Readme Project. It aims to standardize and establish a set of minimum documentation for our future projects to speed up development (and also to not have to stand up and walk over to ask the leader for questions and troubleshooting).

## Quick start

There is no quick start for this one. C'mon, just read the whole thing.

Okay fine, you can have this [sample Readme](sample-readme.md).

## Motivation

This mini-project is born out of frustration when dealing with multiple, often rushed projects, where there's usually a pressing need to deliver results and documentation suffers due to that.

This is meant to provide a semi-reasonable standard for documenting our projects from the moment they begin. The aim is to have a concise, but useful resource for new (and old) developers to quickly get up to speed and start developing.

Another aim of this project is to document the minimum steps necessary to have a fully functional development environment, with no issues. This is really important to avoid having to spend time fixing bugs or chasing down whichever developer started the project.

The above means that, basically, if the Readme is followed and the dev environment is not in a usable state, the Readme **must** be updated.

## The sections

With all that said and done, this project attempts to define a standard Readme.md with several mandatory and optional sections. It also defines a certain formatting, but this is not required, as long as the meaning is obvious and clear.

### Project Title

**Mandatory** (I mean, come on…)

Obviously, this is the name of the project. It can be the same as the actual repository name, or the name of the parent fork, or pretty much anything. It's up to you.

CI badges, if used, go here on the same line. This is so we can quickly determine whether the last commit is good or not.

[Jenkins CI badges](https://wiki.jenkins-ci.org/display/JENKINS/Embeddable+Build+Status+Plugin)
[Travis CI badges](http://docs.travis-ci.com/user/status-images/)

Example:

~~~markdown
# generator-potato-salad ![badge](http://url-to-your-badge.png)
~~~

### Quick Start

**Mandatory**

This is a list of steps to take to quickly scaffold and/or set up the project from a freshly cloned copy, along with a quick explanation if needed.

It should consist of a list of commands or actions to run in order. For example:

~~~markdown
1. `command one`
2. `command two`
3. `command three`
~~~

This list may include commands to install requirements or dependencies outside of the scope of the project, but it isn't necessary. On the other hand, any steps that need to be done _anyway_ after the requirements are satisfied **must** be included here.

For example, this yeoman webapp project should have the following:

~~~markdown
## Quick Start

1. `gem install sass`            ← These two steps are optional, as long as
2. `npm install -g bower grunt`  ← these packages are listed in Requirements
3. `npm install`    ← Not optional, since these two commands set the
4. `bower install`  ← working directory up
~~~

If there are any more useful commands to use while actively developing, you may also list them here. For example:

~~~markdown
* `gulp serve` to create a web server and watch your files
* `npm test` to run the headless test suite
* `gulp build` to create a minified, optimized version of the web app
* `sass watch` to watch your scss files and recompile on the fly
~~~

### Requirements

**Mandatory**

Here is where you specify the absolute requirements of your app/tool/project; i.e. without these, you won't even be able to continue developing.

Include a list of required packages, tools, software stack, etc. with the minimum version (and maximum, if relevant), along with a link to their website. Any preferred or required installation method should also be included.

For example:

~~~markdown
## Requirements

* [Vagrant](http://vagrantup.com) v1.7.0+
* [node.js](http://nodejs.org) v0.12.0+ or [io.js](http://iojs.org) v2.0.0+ (install with [nvm](https://github.com/creationix/nvm))
* [Ruby](http://ruby-lang.org) v2.0+ with the [sass](http://sass-lang.com) gem installed (`gem install sass`)
* [These assets](http://example.org/assets.zip) unzipped into `app/assets`
~~~

### Tasks

**Mandatory for web apps using grunt/gulp**

This should be a list of tasks available. You can go into as much detail as you want, but be sure to provide a full list. For common tasks, try to include a description of how they (are supposed to) work.

Example:

~~~markdown
## Tasks

### `gulp serve`

This creates a temporary directory, compiles scss and coffeescript, creates a web server running on port 9000 and opens your browser pointing to [localhost:9000](http://localhost:9000).

### `gulp build`

This compiles scss and coffeescript, minifies and concatenates CSS and javascript, and optimizes images and HTML and outputs the result into `dist`, ready to be uploaded and served.

### Other tasks

* `gulp deploy` builds and uploads the result to S3/Github/whatever server
* `gulp test` runs headless test suites using PhantomJS
* `gulp lint` checks scripts and styles for code consistency
~~~

### Development

**Mandatory for web apps**

(Feel free to change the name of this section. I have no idea what it should be.)

The aim of this section is to guide new developers and help them identify and locate the resources they need to start developing as quickly as possible. Go into as much detail as necessary, and feel free to add subsections for each part of the application as required.

Example:

~~~markdown
## Development

### Styles

All styles live in `app/public/styles`. To add new components, add them to `app/public/styles/components` and `@include` them in `app/public/styles/main.scss`.

### Adding new templates

Templates are located in `app/framework/blah/templates`. Every template must include an ID as part of the [header](http://example.org), and must also inherit from `app/framework/blah/layouts/main.php`.
~~~

### Usage

**Mandatory for tools and frameworks**

Anything that is meant to assist the development of another product or web app should have this section.

If it's a CLI tool, add something like this:

    ## Usage
    ~~~sh
    $ super-tool [options] -i infile -o outfile
    ~~~

    Options:

        -p <file>  Prints file before processing
        -l <num>   Processes the first <num> lines
        -n         Add newlines
        -N         Add CRLF newlines
        -d <dir>   Output into <dir>

If it's a GUI tool, add screenshots demonstrating common usage.

### Examples

**Optional**

This section, if included, should be a subsection of Usage above. It's recommended for CLI tools, and should include more varied examples than in the Quick Start section. For example:

    ### Examples

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

### Other considerations

**Optional**

For additional considerations, gotchas, caveats, or anything else that developers should know. This can either be separate sections, or a single section with subsections.

Example:

~~~markdown
## Other considerations

### Gulpfile

The gulpfile contains code that manipulates the working directory. Before staging changes, make sure to use `gulp clean` so that you don't check in unwanted files.

### Deployment

`gulp deploy` should be used with care. It will discard the remote `gh-pages` branch and submit the build artifacts as a single commit. Do _not_ use with master or with any branch you care about
~~~

This could also be presented like this (note the headings):

~~~markdown
## Gulpfile

The gulpfile contains code that manipulates the working directory. Before staging changes, make sure to use `gulp clean` so that you don't check in unwanted files.

## Deployment

`gulp deploy` should be used with care. It will discard the remote `gh-pages` branch and submit the build artifacts as a single commit. Do _not_ use with master or with any branch you care about
~~~

### Contributing

**Optional, but recommended**

This section should detail any requirements you have (as a repository owner/admin) in order to merge PRs and accept code contributions. This should also ideally include any code style guidelines, and may also include things like tests that are required to pass.

For example:

~~~markdown
## Contributing

Follow these steps:

1. Fork the repo
2. Make your changes in a new branch
3. Add test cases as necessary
4. Submit your PR

Make sure lint tests pass: `gulp lint`

Do not mix actual code changes with coding style changes in a single PR. Instead, make those changes in a separate branch, and submit in a new PR.
~~~

### Troubleshooting

This section should describe a list of steps to take when the app fails (that is, when the dev environment can't be set up properly) in order to obtain enough information to fix the issue. It is not actually meant for app-specific errors (e.g. the app itself doesn't behave as it should), but if added they should be in a subsection.

Optionally, and in the case of common errors, workarounds can also be added here.

Example:

~~~markdown
## Troubleshooting

**Mandatory**

If an error occurs when attempting `vagrant up`, verify the following:

1. `$ vagrant --version` should be v1.7+
2. `$ fab --version` should be v1.10+
3. `$ super-tool --version` should be v0.3+

To fix this, run `super-tool --fix-everything`

If errors persist, make sure you have a `super-tool-error.log` file.
~~~
