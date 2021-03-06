![Flare](./flare.png)

# Flare

Flare is a design system for agile front-end software engineering. 

Flare's paradigm helps to understand the user interface from a simple and structured standpoint, introducing an abstraction layer that shapes a common language between analysts, designers, coders and testers.

The design system implementation is focused in the separation of content, design and code; specially when combined with a static-site generator. Making it ideal for front-end agile software projects where the three aspects evolve at different pace.

Currently Flare is in an early version 0.3.0 and it provides with a [VueJS](https://vuejs.org/) implementation mounted in [Gridsome](https://gridsome.org/).

## Getting started

Getting started is easy with [degit](https://github.com/Rich-Harris/degit), install it with:

````bash
yarn global add degit
````

Use it to create an empty project.

````bash
degit github:lkmx/flare-starter-gridsome#main project-name
````

Install the dependencies and run a development server

````bash
cd project-name
yarn
yarn run develop
````

Your new app should be running now in [http://localhost:8080](http://localhost:8080).

Build the app for production

````bash
yarn run build
````

Find the files in `dist`