# Thinking in Stripes

## Introduction

[The Stripes toolkit](https://github.com/folio-org/stripes-core) aims to make it as easy as possible to write UI modules that commuicate with RESTful Web services. Most importantly, it is the toolkit used to write UI modules for [the FOLIO library services platform](https://www.folio.org/).

## Overview

Stripes consists of several separate JavaScript libraries that work together. The good news is that you don't need to think about most of them in order to create Stripes-based UI modules. They are:

* **stripes-connect** -- provides the connection to FOLIO's services.
* **stripes-components** -- provides re-usable UI components such as checkboxes, search forms and multi-pane layouts.
* **stripes-loader** -- low-level machinery that pulls a set of Stripes Modules into a web application
* **stripes-core** -- a web application that controls a set of UI modules and helps them to work together.

In general, Stripes Core is configured by a list of UI modules to include, and it uses stripes-loader to pull them all into a bundle of HTML/CSS/JS resources. Each of those modules composes UI elements from stripes-components (and other sources as needed) to search, view, edit and manage data maintained by the FOLIO web-services.

As a module author, you need to know JavaScript, be familiar with UI components (including those available from stripes-components) and understand how to connect to FOLIO web-services.

## Underlying technology

Stripes UI modules are written in **JavaScript** -- specifically, in [EcmaScript 6 (ES6)](http://es6-features.org/), a modern version of JavaScript that fixes many of the problems that made earlier version of the language difficult to work with.

The Stripes UI is built using [**React**](https://facebook.github.io/react/), a library that provides an elegant component-based approach that can provide a very responsive user experience. The promise of React is that it "will efficiently update and render just the right components when your data changes." And that is also the goal of stripes-connect.

React works best when used with [**JSX**](https://jsx.github.io/), a simple syntax for embedding XML (including HTML) into JavaScript. You don't need to use JSX,  but it's easy to learn and very expressive.

So you should consider ES6, React and JSX the prerequisites for writing Stripes UI components.

(Under the hood, stripes-connect uses [Redux](https://github.com/reactjs/redux) to manage its state. But UI module authors do not need to use Redux directly.)

## Principles of stripes-connect

XXX to do