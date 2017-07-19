# &#60;dsc-polymer-datatable&#62;

[![Build Status](https://travis-ci.org/discovery-tecnologia/dsc-polymer-datatable.svg?branch=master)](http://travis-ci.org/#!/discovery-tecnologia/dsc-polymer-datatable)
![Bower version](https://img.shields.io/bower/v/dsc-polymer-datatable.svg)
![](https://img.shields.io/pypi/l/Django.svg)

A material design implementation of a data table. Easy API integration.

Differential:

 * Easy to use
 * Customizable header buttons
 * Sort columns
 * Pagination
 * Customizable style
 * API integration

## Demo

```
$ git clone https://github.com/discovery-tecnologia/dsc-polymer-datatable.git
$ cd dsc-polymer-datatable
$ npm install
$ npm install -g polymer-cli
$ polymer serve
```
Open browser: http://localhost:8080/components/dsc-polymer-datatable/demo/

## Usage

Install with:

```
$ bower i dsc-polymer-datatable --save
```

Example usage:

```html
<dsc-polymer-datatable
    id="my-component"
    selectable
    title="Albums"
    on-change="_handlerChange"
    on-select="_handlerSelect">
  <dsc-columns>
    <dsc-column type="number" label="ID" name="_id" hidden></dsc-column>
    <dsc-column type="string" label="Title" name="title" sortable></dsc-column>
    <dsc-column type="string" label="Category" name="category"></dsc-column>
    <dsc-column type="string" label="Created at" name="createdAt" sortable></dsc-column>
  </dsc-columns>
  <div id="toolBar">
    <paper-icon-button icon="add" on-click="_handlerNew" title="Add"></paper-icon-button>
  </div>
  <div id="toolBarOnOneSelect">
    <paper-icon-button icon="create" on-click="_handlerEdit" title="Edit"></paper-icon-button>
  </div>
  <div id="toolBarOnSelect">
    <paper-icon-button icon="delete" on-click="_handlerDelete" title="Remove"></paper-icon-button>
  </div>
</dsc-polymer-datatable>
```

## API Reference

It is possible to include elements to be displayed in the header by means of ID **toolBar**.

If the elements need to be displayed only when there is a selected row or more, use their IDs **toolBarOnOneSelect** or **toolBarOnSelect**


### Properties

| Property       | Description                                                      | Default |
|:---------------|------------------------------------------------------------------|---------|
| limit          | Quantity per page.                                               | null    |
| orderBy        | Current field of the document by which records are to be sorted. | null    |
| orderDirection | Sense of ordination. Ascending or descending. 'asc' or 'desc'.   | null    |
| pages          | Total number of pages.                                           | null    |
| page           | Current page number.                                             | null    |
| total          | Total items in all pages                                         | null    |
| search         | String to search on API                                          | null    |

### Methods

| Method                 | Description                                      | param |
|:-----------------------|--------------------------------------------------|-------|
| **setLoading**(bool)   | Allows you to externally manipulate the loading status. For internal states the component already has the loading | Boolean |
| **setData**(data)      | Set array of objects by exitent items.           | Object |
| **refresh**()          | Refresh data by current state(page, order, etc) by trigger 'datatable-change' event. | - |
| **getSelectedItems**() | Return array of selected objects. Equivalent to event 'datatable-select'             | - |

### Events

| Event            | Description                                      |
|:-----------------|--------------------------------------------------|
| datatable-change | Event of one or more of the following states: orderBy, orderDirection, page, limit or search. |
| datatable-select | On table selection change. Return all selecteds items data.                                   |

## Test

Check sintax and execute selenium tests.

```
$ npm test
```

## TODO

 * internationalization
