# Building Course Repositories in SharePoint using Power Automate

## Overview
This repository contains guidelines and files to help you build a collaborative course repository using Power Automate flows. Each flow will link to a SharePoint list corresponding to individual courses that will sync on a scheduled basis with Excel sheets you can update as needed. You can share these lists with anyone you like within the same group or organization. A professional or organizational SharePoint account is required to upload the zip file to Power Automate.

We suggest watching the [accompanying instructional videos](http://www.website.com) (*coming soon*) for guidance in setting up your course repositories.

### GitHub Contents
1. An Excel sheet course template
2. A zip file containing the Power Automate flow to sync the Excel sheet to a SharePoint list

___

# SharePoint
## I. Creating a Course Repository Drop-off List in SharePoint

To begin building a repository, you should first navigate to the homepage for your group's SharePoint. The purpose of this section is to build a SharePoint list in which all of the Excel sheets are stored. Whether you make individual spreadsheets per course or combine all materials in one spreadsheet, perhaps differentiating course using a column, is up to you. The spreadsheets contained within the **Course Repository Drop-off** are where you can make edit, add, or delete course materials. These changes will be updated automatically to the SharePoint list for each course repository using the Power Automate flow built in this vignette.

1. Directly under the SharePoint group name, select **+ New** and then select **List**.
2. Next, select the button in the top left corner labeled **Blank list**.
3. Type **Course Repository Drop-off** in the **Name** field. Add a description if helpful.
4. Select **Create**, and now you have a list where you can add Excel sheets that correspond to different courses.

<p align="center">
    <img img width="412" alt="Figure 1. Find List under + New menu" src="https://user-images.githubusercontent.com/96262719/209174838-4239c1da-4863-4ec5-9e90-8f2fb00a380d.png">
</p>

***

## II.	Uploading a Course Template Excel Sheet to SharePoint

1. Download and save the [**Course Template.xlsx**](https://github.com/prosodactyl/course-repository-power-automate/blob/main/Course%20Template.xlsx/) Excel sheet from GitHub.
2. Navigate to the **Course Repository Drop-off** list in SharePoint that you created in Section I.
3. Click **+ New** and then **+ Add template** in the drop-down menu.
4. Select **Course Template.xlsx** from your saved documents folder and then click **Open**.

To determine whether you've uploaded the template successfully, click the **+ New** drop-down menu again. You should see the **Course Template** Excel document as an option.

***

<ins>Tip:</ins> To edit the templates visible in the drop-down list, click **+ New** and select **Edit New menu**. From here, you can select which templates are visible in the drop-down menu. Select or unselect templates to customize your menu and then click **Save** at the top of the menu.

***
## III.	Creating Course Repositories in SharePoint

*If the course spreadsheet already exists in the **Course Repository Drop-off** SharePoint list, skip to Section IV.*

1. If an Excel sheet for the course you are looking for does not exist yet, click **+ New** in the top navigation bar. 
2. Next, click **Course Template**. An Excel spreadsheet will open. 
3. Navigate to the top bar, next to **Excel**, and click **Book - Saved** to rename the repository spreadsheet. Name the spreadsheet so that it pertains to a certain course. For example, for the fall semester of an Academic Speaking course, you may name the spreadsheet **AS Fall Repository.xlsx**.

<p align="center">
    <img img width="412" alt="Figure 2. New course repository" src="https://user-images.githubusercontent.com/96262719/218803049-d4f13a87-6ddd-47ae-8c75-f513e87293a5.png">
</p>

***

## IV. Creating a Course Repository SharePoint List

In this section, you will create a SharePoint list that corresponds to the Excel spreadsheet you created in Section III.

1. On your organization's SharePoint home page, select **+ New** and then select **List**, as you did in Section I.

<p align="center">
    <img img width="412" alt="Figure 3. Find List under + New menu" src="https://user-images.githubusercontent.com/96262719/209174838-4239c1da-4863-4ec5-9e90-8f2fb00a380d.png">
</p>

2. Next, select the button in the top left corner labeled **Blank list**.

<u>Tip</u>: If you have created a course SharePoint list in the past, you can select **From existing list** to create columns in your new SharePoint list.

3. Type the name of your course repository in the **Name** field. Add a description if helpful.
4. Select **Create**.
5. To add columns, in the SharePoint list, click **+ Add column**.
6. Select the column type. For the purposes of these course repositories, you can select **Text** for column type. The only caveat is you must choose **Hyperlink** for the **Link** and **Connected Files** columns so that the links are clickable.

<p align="center">
    <img img width="412" alt="Figure 4. Creating columns" src="https://user-images.githubusercontent.com/96262719/218814934-4ddaf8b8-85c4-4037-8e06-452039d80aba.png">
</p>

7. Submit the column name, being sure to use the same columns names as those that exist in the corresponding Excel spreadsheet.
 
<u>Note</u>: Even though you could create a list from an Excel spreadsheet, you will likely not be able to amend the column type. What that means is that the **Hyperlink** columns will not be clickable, which may create issues for the Power Automate flow and for navigating the SharePoint contents.

***

Now that you have set everything up in SharePoint, it's time to move over to Power Automate. You may ask why there is a need to create a Power Automate flow if you are able to create a SharePoint list directly from an Excel spreadsheet. The limitation with this method is that the SharePoint list will not update based on changes made in the source Excel spreadsheet. The Power Automate flow created with this vignette updates the contents of the SharePoint list based on any changes that are made to the source Excel spreadsheet automatically.

***

# Power Automate

[Power Automate](https://powerautomate.microsoft.com/) is a SharePoint app that allows you to create a workflow that automates processes within SharePoint. For example, Power Automate can be used to create a workflow that updates a **List** item automatically from an Excel spreadsheet. 

You can access Power Automate from the grid icon on the top-left-hand side of SharePoint. If you cannot find it in the first 10 apps, click **All apps →** to view the entire list of apps.

## I. Establish Power Automate Connections

To successfully import the zip file containing the Power Automate flow, you must establish connections between Power Automate and both (a) Excel Online (Business) and (b) SharePoint. To do this, follow the steps below.

1. On the Power Automate home screen, click **Data** and then **Connections** in the lefthand bar.

<p align="center">
    <img img width="412" alt="Figure 5. Power Automate Connections" src="https://user-images.githubusercontent.com/96262719/218875731-211ecb90-234d-4c52-b7eb-7e9121204ad4.png">
</p>

2. Next, click **+ New connection** at the top of the window.
3. From this screen, you can browse the list for both Excel Online (Business) and SharePoint, or you can use the search function at the top righthand side of the window.
4. After clicking Excel Online (Business), click **Create** and you will be prompted to connect your Excel Online account to Power Automate. Make sure that you are connecting the account associated with your organization.
5. Follow the same steps to connect to the SharePoint account associated with your organization.

## II. Creating a Workflow in Power Automate

*If you are amending, deleting, or adding new data to a course repository, you can skip to Section V.*

1. Download the latest version of the [<b>CourseRepository WorkflowTemplate.zip</b>](https://github.com/prosodactyl/course-repository-power-automate/blob/main/CourseRepositoryWorkflowTemplate_v1.zip) in GitHub.
2. In Power Automate, navigate to **My flows** on the left-hand side of the screen. Once there, click **← Import** in the top navigation bar and then **← Import Package (Legacy)**. 

<p align="center">
    <img img width="412" alt="Figure 6. Upload flow" src="https://user-images.githubusercontent.com/96262719/210643640-cab3be56-11d8-4ba2-8e60-920fd77573bb.png">
</p>

3. Click the blue button labeled **Upload** and find the zip file in your folder. It will take a few moments for the zip file to upload in Power Automate.
4. Once uploaded, you will have to select import settings. In the **Import Setup** column for the **Course Repository Template**, click **Update**, navigate to the drop-down menu and select **Create as new**. Here you can name the flow whatever you would like. Click **Save** to update the name.
5. In the **Related resources** section, click **Select during import** for any items listed and select your account email.

<p align="center">
    <img img width="700" alt="Figure 7. Import flow" src="https://user-images.githubusercontent.com/96262719/210643720-a4061591-36c5-4f2a-9192-02309aee902d.png">
</p>

6. Once all fields are filled, you may click the **Import** button. The flow will take a few moments to import.
7. To find the imported flow, click **My flows** in the left-hand bar.

## III. Customizing the Power Automate Flow

1. Click on the imported flow. The page you see is the landing page for the flow, which will show the status (on/off), creation date, the last time it was modified, and any successful or failed runs.

<p align="center">
    <img img width="600" alt="Figure 8. Flow landing page" src="https://user-images.githubusercontent.com/96262719/210643784-a21461e8-e36c-464c-b957-5349dfe0a936.png">
</p>

2. Click on **Edit** in the top bar.
Here is a preview of the complete workflow in Power Automate. Each bar (e.g., *Recurrence*, *List rows present in a table*, etc.) is subsequently referred to as a node.

<p align="center">
    <img img width="500" alt="Figure 9. Power Automate flow overview" src="https://user-images.githubusercontent.com/96262719/210643857-c23819fc-87e3-4045-954c-48650d3bca78.png">
</p>

3. You will have to open each node to link your Excel spreadsheet and SharePoint list to the Power Automate flow. This can be done by clicking on each node to expand the contents within. 
3. Directly underneath the title, you will find a word bubble icon next to a comment. The comment within each node will explicitly state whether there is any content in the node that needs to be updated to reference either your Excel spreadsheet or SharePoint list.

<p align="center">
    <img img width="600" alt="Figure 10. Power Automate comments" src="https://user-images.githubusercontent.com/96262719/218887480-898cc2a5-07b9-435e-b74e-86535bfbe62b.png">
</p>

4. The following table provides an explanation for each of the nodes.

<i>Insert table here.</i>
5. After you have checked every node and customized each one accordingly, save the flow by clicking the **Save** icon at the top left of the browser or at the bottom of the flow.

<p align="center">
    <img img width="600" alt="Figure 11. Save flow" src="https://user-images.githubusercontent.com/96262719/218862385-888a3033-63cc-4ba5-8a3d-8e203695a0f4.png">
</p>

6. Before you test out the flow, you must turn it on. To do so, click the left arrow next to your flow name to return to the landing page for that flow. 
7. Navigate to the top bar and click on **Turn on**.

<p align="center">
    <img img width="600" alt="Figure 12. Turn flow on" src="https://user-images.githubusercontent.com/96262719/218862939-4b1dece3-fade-4055-8c92-36d732bae450.png">
</p>

8. After ensuring the flow is on, click **Run** in the same bar to test the flow.

*Add more info about running flow here (2/14/2023)*

9. To share the flow with others in your organization, go to **My flows**. Find the repository flow you would like to share, hover over it, and you will see a circle outline containing three smaller circles. Click this symbol and search for other users in your organization.

10. If you have shared a flow with someone or someone has shared one with you, your flow has now moved over to **My flows** → **Shared with me**.

***

# How to Use the Course Repository

## I.	Adding New Files to the SharePoint List
This is the section that you are most likely to reference when updating course materials. 

1. First, navigate to the **Course Repository Drop-off** SharePoint list.
2. Find the repository Excel sheet for the course you are interested in adding resources to.
3. Make a new line in the Excel sheet with new materials.

<u>Tip</u>: You may also make changes to any of the cells with updated information or delete a row if a material is no longer associated or necessary for a course.

***

## II.	Searching the Course Repository
The course repository list can be found in the same navigation list as the Course Repository Drop-off. There will be a separate list for every course. Once there, you can browse the entire list, use the search bar to find specific items, or filter items by column. 
