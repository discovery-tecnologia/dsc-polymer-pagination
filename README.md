# &#60;dsc-polymer-pagination&#62;

[![Build Status](https://travis-ci.org/discovery-tecnologia/dsc-polymer-pagination.svg?branch=master)](http://travis-ci.org/#!/discovery-tecnologia/dsc-polymer-pagination)
![Bower version](https://img.shields.io/bower/v/dsc-polymer-pagination.svg)
![](https://img.shields.io/pypi/l/Django.svg)

A material design implementation of a data table. Easy API integration.

Differential:

 * Easy to use
 * Customizable style
 * API integration

## Demo

```
$ git clone https://github.com/discovery-tecnologia/dsc-polymer-pagination.git
$ cd dsc-polymer-pagination
$ npm install
$ npm install -g polymer-cli
$ polymer serve
```
Open browser: http://localhost:8080/components/dsc-polymer-pagination/demo/

## Usage

Install with:

```
$ bower i dsc-polymer-pagination --save
```

Example usage:

```html
<dsc-polymer-pagination
        page="[[page]]"
        pages="[[pages]]"
        limit="[[limit]]"
        total="[[total]]"
        loading="[[loading]]"
        on-pagination-change="_handlerChange">
    </dsc-polymer-pagination>
```

## API Reference

### Properties

| Property       | Description                                                      | Default |
|:---------------|------------------------------------------------------------------|---------|
| loading        | Block all buttons.                                               | null    |
| limit          | Quantity per page.                                               | null    |
| pages          | Total number of pages.                                           | null    |
| page           | Current page number.                                             | null    |
| total          | Total items in all pages                                         | null    |

### Events

| Event             | Description                                                    |
|:------------------|----------------------------------------------------------------|
| pagination-change | Event of one or more of the following states: page and limit.  |

## Test

Check sintax and execute selenium tests.

```
$ npm test
```

## TODO

 * internationalization
