
# <img src="src/docs/asciidoc/images/icon.png" width="80" height="80"> Memmas Project

This project intends to be a micro service running on the Lagom framework. This project contains the microservice implementation neceseary to send messages between two actors with in the system. Currently this is in a proof-of-concept state.

## Table of Contents
1. [Context](#context)
2. [Getting Started](#getting-started)
3. [API Reference](#api-reference)
4. [Notes](#notes)


## Context
1. A consumer can submit a date and time to schedule a massage with a provider
2. A provider can list all schedukle appointments

## Getting Started

The microservice was built entirely using lagom framework. Following the lagom documentation to the best of my understanding. For more information read the [try lagom](https://www.lagomframework.com/get-started-scala.html)

## API Reference
There are currently two enpoints as describe below:

1. schedule an appoitment: 
	```POST /api/appointment/:provide```
	
	body: 
	
      ```{ "date":"201903031000", "duration":"15", "consumer":"Martin"}```
2. check all appointments:
	```GET /api/appointment/:provide```

## Notes

The data base is a cassandra and is wiped on every run, so there is no long term persistence. This still should be enouh for a proof-of-concept.