# Building Course Repositories in SharePoint using Power Automate

## Overview
This repository contains guidelines and files needed to create SharePoint lists corresponding to individual courses that will sync on a scheduled basis with Excel sheets that are updated with new or changed course items. The purpose of the Power Automate flow is to establish collaborative coure repositories for instructors within a group or organization. A professional or organizational SharePoint account is required to upload the zip file to Power Automate.

We suggest watching the [accompanying instructional videos](http://www.google.com) for guidance in setting up your course repositories.

## GitHub Contents
1. An Excel sheet template
2. A zip file containing the Power Automate flow to synce the Excel sheet to a SharePoint list

___

## I.	Creating a List in SharePoint

*Insert instructions for creating Course Repository Drop-off*

This is the most basic and straightforward part of building a repository. Each course will have its own designated List in SharePoint. To create a list, go to **Course Repository Drop-off** in your organization's SharePoint home page.

[Figure 1](https://www.image.com)

If an Excel sheet for the course you are looking for does not exist yet, click **+ New** in the top navigation bar. Next, click Course Template and save it as **Course Name Repository.xlsx**. If the course spreadsheet already exists, skip to Section III.
 
___

## II. Creating a Workflow in Power Automate

*This step only applies to admins. If you are amending or adding new data to a course repository, you can skip to Section III.*

Power Automate is a SharePoint app that allows you to create a workflow that automates processes within SharePoint. For example, Power Automate can be used to create a workflow that updates a **List** item automatically from an Excel spreadsheet. You can access Power Automate from the grid icon on the top-left-hand side of SharePoint. If you cannot find it in the first 10 apps, click **All apps →** to view the entire list of apps.

To create a workflow, navigate to **My flows** on the left-hand side of the screen. Once there, click **+ New** flow in the top navigation bar.

Here is a preview of what the workflow looks like when complete.

![Power Automate flow overview](https://user-images.githubusercontent.com/96262719/209042474-3955b1d2-58ce-4f47-b87b-60a10d6a6e7f.png)

***

## III.	Adding New Files to the SharePoint List
This is the section that you are most likely to reference when updating course materials. First, navigate to the repository Excel sheet for the course you are interested in adding resources to.

***

## IV.	Searching the Course Repository List
The course repository list can be found in the same navigation list as the Course Repository Drop-off. There will be a separate list for every course. Once there, you can browse the entire list, use the search bar to find specific items, or filter items by column. 