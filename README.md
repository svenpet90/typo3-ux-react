TYPO3 Extension "typo3-ux-react"
=================================

## What does it do?
Render React components directly in Fluid template

This Extensions enables you to render React Components directly in Fluid templates.
It acts as an integration for [symfony/ux-react](https://github.com/symfony/ux-react) into TYPO3.

## Prerequsites


## Installation

The recommended way to install the extension is by
using [Composer](https://getcomposer.org/). In your Composer based TYPO3 project
root, just run:
<pre>composer require svenpetersen/typo3-ux-react</pre>

## Setup
Before you start, make sure you have [EXT:typo3_encore](https://github.com/sabbelasichon/typo3_encore).
This extensions integrates [Webpack Encore](https://symfony.com/doc/current/frontend.html) into TYPO3.

Follow the [Symfony UX React official documentation](https://symfony.com/bundles/ux-react/current/index.html)

Additionally:

    # Add this line to your package.json dependencies:
    "@symfony/ux-react": "file:vendor/symfony/ux-react/assets"

    # Install react
    $ npm i react react-dom

    # or
    $ yarn add react react-dom

    # Add these lines to your controllers.json:
    "@symfony/ux-react": {
        "react": {
            "enabled": true,
            "fetch": "eager"
        }
    }

    # run
    $ npm install --force
    $ npm run watch

    # or
    $ yarn install --force
    $ yarn watch

## Usages
In any fluid template: Just register the Namespace and use the provided ViewHelper to render your component:

    <html xmlns:ux="http://typo3.org/ns/SvenPetersen/UX/React/ViewHelpers">
        <div {ux:reactComponent(name:'MyComponent',props:"{'name':'John Doe'}")}></div>
    </html>

## Contributing

Please refer to the [contributing](CONTRIBUTING.md) document included in this
repository.
