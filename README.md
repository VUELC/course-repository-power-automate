# Building Course Repositories in SharePoint using Power Automate

## Overview
This repository contains guidelines and files needed to create SharePoint lists corresponding to individual courses that will sync on a scheduled basis with Excel sheets that are updated with new or changed course items. The purpose of the Power Automate flow is to establish collaborative course repositories for instructors within a group or organization. A professional or organizational SharePoint account is required to upload the zip file to Power Automate.

We suggest watching the [accompanying instructional videos](http://www.google.com) for guidance in setting up your course repositories.

## GitHub Contents
1. An Excel sheet course template
2. A zip file containing the Power Automate flow to sync the Excel sheet to a SharePoint list

___

## I. Creating a Course Repository Drop-off List in SharePoint

To establish a simple system to building a repository, you should first navigate to the homepage for your group's SharePoint. 

1. Directly under the SharePoint group name, select **+ New** and then select **List**.
2. Next, select the button in the top left corner labeled **Blank list**.
3. Type **Course Repository Drop-off** in the **Name** field. Add a description if helpful.
4. Select **Create**, and now you have a list where you can add Excel sheets that correspond to different courses.

<img img width="412" alt="Figure 1. Find List under + New menu" src="https://user-images.githubusercontent.com/96262719/209174838-4239c1da-4863-4ec5-9e90-8f2fb00a380d.png">

***

## II.	Uploading a Course Template Excel Sheet to SharePoint

1. Download and save the [**Course Template.xlsx**](https://github.com/prosodactyl/course-repository-power-automate/blob/main/Course%20Template.xlsx) Excel sheet from GitHub.
2. Navigate to the **Course Repository Drop-off** list in SharePoint that you created in Section I.
3. Click **+ New** and then **+ Add template** in the drop-down menu.
4. Select **Course Template.xlsx** from your saved documents folder and then click **Open**.

To determine whether you've uploaded the template successfully, click the **+ New** drop-down menu again. You should see the **Course Template** Excel document as an option.

***

<ins>Tip:</ins> To edit the templates visible in the drop-down list, click **+ New** and select **Edit New menu**. From here, you can select which templates are visible in the drop-down menu. Select or unselect templates to customize your menu and then click **Save** at the top of the menu.

***

## III.	Creating Course Repositories in SharePoint

If an Excel sheet for the course you are looking for does not exist yet, click **+ New** in the top navigation bar. Next, click Course Template and save it as **Course Name Repository.xlsx**. If the course spreadsheet already exists, skip to Section IV.
 
***

## IV. Creating a Workflow in Power Automate

*If you are amending or adding new data to a course repository, you can skip to Section V.*

[Power Automate](https://powerautomate.microsoft.com/) is a SharePoint app that allows you to create a workflow that automates processes within SharePoint. For example, Power Automate can be used to create a workflow that updates a **List** item automatically from an Excel spreadsheet. 

You can access Power Automate from the grid icon on the top-left-hand side of SharePoint. If you cannot find it in the first 10 apps, click **All apps →** to view the entire list of apps.

1. Download the latest version of the [<b>CourseRepository WorkflowTemplate.zip</b>](https://github.com/prosodactyl/course-repository-power-automate/blob/main/CourseRepositoryWorkflowTemplate_v1.zip) in GitHub.
2. In Power Automate, navigate to **My flows** on the left-hand side of the screen. Once there, click **← Import** in the top navigation bar and then **← Import Package (Legacy)**. 

![Figure 2. Upload flow](https://user-images.githubusercontent.com/96262719/210643640-cab3be56-11d8-4ba2-8e60-920fd77573bb.png)

3. Click the blue button labeled **Upload** and find the zip file in your folder. It will take a few moments for the zip file to upload in Power Automate.
4. Once uploaded, you will have to select import settings. In the **Import Setup** column for the **Course Repository Template**, click **Update**, navigate to the drop-down menu and select **Create as new**. Here you can name the flow whatever you'd like.
5. In the **Related resources** section, click **Select during import** for any items listed and selected your account email.

![Figure 3. Import flow](https://user-images.githubusercontent.com/96262719/210643720-a4061591-36c5-4f2a-9192-02309aee902d.png)

6. Once all fields are filled, you may click the **Import** button. The flow will take a few moments to import.
7. To find the imported flow, click **My flows** in the left-hand bar.

## V. Customizing the Power Automate Flow


1. Click on the imported flow. The page you see is the landing page for the flow, which will show the status (on/off), creation date, the last time it was modified, and any successful or failed runs.

![Figure 4. Flow landing page](https://user-images.githubusercontent.com/96262719/210643784-a21461e8-e36c-464c-b957-5349dfe0a936.png)

2. Click on **Edit** in the top bar.
Here is a preview of the complete workflow in Power Automate.

![Figure 4. Power Automate flow overview](https://user-images.githubusercontent.com/96262719/210643857-c23819fc-87e3-4045-954c-48650d3bca78.png)

3. Each node contains notes giving some information about the content therein. 
4. The following table provides an explanation for each of the nodes.

<i>Insert table here.</i>

***

## VI.	Adding New Files to the SharePoint List
This is the section that you are most likely to reference when updating course materials. First, navigate to the repository Excel sheet for the course you are interested in adding resources to.

***

## VII.	Searching the Course Repository List
The course repository list can be found in the same navigation list as the Course Repository Drop-off. There will be a separate list for every course. Once there, you can browse the entire list, use the search bar to find specific items, or filter items by column. 