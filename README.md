# Phantom JS / JsTestDriver Automation

A simple set of scripts to help glue together [JsTestDriver](http://code.google.com/p/js-test-driver/)
and [Phantom JS](http://www.phantomjs.org/) for an automated, headless environment for javascript
tests.

## Setup

1. Download v1.5 (or greater) of Phantom JS and make sure the _phantomjs_ binary is on your PATH.
   (On a Mac homebrew has an updated forumla for the 1.5 static build: brew install phantomjs)

2. Run _./server start_ to fire up the JsTestDriver server and Phantom JS.

(Run _./server stop_ to kill the daemonized JSTD server and PhantomJS processes.)

## Running Tests

The _runtests.sh_ script will run all js unit tests against JsTestDriver, using Phantom JS
as the captured browser. Any args passed to this script will be appended to the JsTestDriver invocation.

Example:

    ./runtests.sh --config examples/helloworld/jsTestDriver.conf --tests all --testOutput examples/helloworld/reports

