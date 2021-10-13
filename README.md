# Departmental Request App Tutorial

In this tutorial, you will learn how to use App Engine Studio to build a departmental request app in your [Personal Developer Instance (PDI)](https://developer.servicenow.com/dev.do#!/guides/rome/developer-program/pdi-guide/personal-developer-instance-guide-introduction) through step by step instructions and video.

You can find a completed version of this app on GitHub: [departmental-request-app](https://github.com/ServiceNowDevProgram/departmental-request-app)

## Prerequisites

You will need a Rome PDI with the latest version of App Engine Studio installed. You can follow the instructions at the bottom of the [Rome AES blog post](https://devlink.sn/rome-aes?utm_source=app-tutorial) to upgrade AES to version 20.0.1 or to check the version.

## Use Case

![app icon](images/deptreqicon.png)

The use case that you will work through in this app tutorial is a generic departmental request app. Many departments in an organization need a way to handle requests for something from outside of their department. This usually starts with a shared mailbox and a spreadsheet to track these requests, but that type of solution doesn't scale and can't be automated very well. In this use case, you will be building an app that transitions from the old email/spreadsheet to a catalog form on the portal, a dedicated experience for fulfillers, approval and email automation, and data security.

## Objectives

In this tutorial, you will use App Engine Studio to build:

1. A data model with request and request type tables.
1. A catalog experience for requesters.
1. A workspace experience for approvers.
1. An approval flow.
1. A completed email flow.
1. A security model with fulfiller and admin roles.

[Proceed to Exercise 1 - Create the App](Exercise1-CreateApp.md)