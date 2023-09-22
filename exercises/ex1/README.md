## Exercise 1 – Plan Story Navigation and Enrichment

**Objective:** You should develop an understanding of basic story
navigation, and how to modify a story to include new visualiziations, change
existing widget settings, and leverage custom widgets and script to improve our
planning template.

**Estimated Time:** 25 mins

**Exercise Description:**  CycleBros is a Germany headquartered recreational
bike manufacturer and distributor.  You
are an FP&A analyst for CycleBros, and you are looking to make changes to
existing dashboard to support the upcoming planning cycle, including some
customization for specific changes occurring in the US region and end-user requested
enhancements.

**Key Features:**

* Basic navigation of the dashboard
* Inclusion of new widgets and minor changes to
  existing widget settings

* Introduction of a custom widget and script to
  support direct end-user upload of planning data

⚠️**Disclaimer** When
completing exercises, it is expected that data values or screenshots should
match what you see on your screen.  If
you see inconsistencies as you work through the exercise, please refer to the
appropriate section in **Getting Started** Readme.  For any inconsistencies which are not addressed
therein, please check with your instructor.

---

🚩As a FP&A Analyst for CycleBros, we are interested in
extending the existing dashboard that incorporates Business Intelligence and
Planning.   Start by reviewing the
initial dashboard.  You will notice that
we have 2 tabs.  The tab first is
tracking financial performance for the current year (currently filtered to All
Regions and the current close period – Oct 2023).   In the second tab, we have a sales plan
entry template which is meant to capture sales quantity forecasts by period for
each of products.  Note that we have
included a couple of input controls (i.e., plan version and user) which are
already selected and are not meant to be modified during the exercise (this is
to simplify data capture and data segregation for TechEd).  Additionally, for the purposes simplicity we
have narrowed the exercises to primarily focus on the US region.  We will make a couple of minor changes to dashboard
filters, while also making some additional enhancements to improve end-user
plan entry flexibility.

Let’s start by editing the dashboard!

1. First ensure you are on the Financial Overview tab.  Then click **Edit to change the dashboard to authoring
   mode.**

🚩 The first thing we want to do is make some end-user
requested changes to the Financial Overview page.   This include updating the dashboard title to
dynamic reflect our region filter selection, changing the default filter for
region to focus on the US, and modifying the default drill level for our
P&L in the table widget.

2. In the dashboard title text box, highlight the **DA261**
   and click the delete key

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image001.png)

3. With your cursor between the brackets () right-click.  Select  **Add** > **Dynamic Text**

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image002.png)

4. From the Insert Dynamic Text popup, select **Story
   Filters** and check the box for **SAP_XPA_REGION **and click the **Create**
   button

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image003.png)

5. Now let’s change the default filter selection for the
   region by clicking on the **SAP_XPA_REGION** filter at the top of the dashboard
   and deselecting the **All** filter

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image004.png)

6. Select **United States** and click **Apply Selections**

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image005.png)

6. Finally, let’s change the default drill depth in our
   table by first right-clicking on the **SAP_XPA_ACCOUNT** dimension header within
   the table.  Select  **Drill ** >**
   Level 4**

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image006.png)

7. Click **File/Save** to save your dashboard updates

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image007.png)

⚠️**Quality Check!** Does
your dashboard look like this?

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image008.png)

🚩 Now that we have updated the Financial Overview, we are
next going to make some preliminary changes to the Sales Plan Entry tab to
prepare for the upcoming planning cycle.We are going to add two new widgets.
The first will simplify review of total units planned, while the second
will introduce a custom widget to provide a mechanism for end-users to directly
upload their sales plan numbers from csv or xls.

8. Navigate to the **Sales Plan Entry** tab, and review
   the template

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image009.png)

🚩 We want to add a a numeric point chart to track full
year total quantity planned.  This number
will ultimately be visible in the table as well, but we want to make it more
prominent the end-user.  Rather than
inserting a net-new chart, we are going to duplicate an existing object and
repoint it.

9. Navigate back to the **Financial Overview** tab, and select
   the Unit Sales numeric point chart

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image010.png)

10. From the widget menu select **Copy > Copy To > Sales
    Plan Entry**

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image011.png)

11. Navigate to the **Sales Plan Entry** tab

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image013.png)

12. Move (click and drag) and resize the widget (select
    corner or edge and click-drag) so the right side aligns with the right side of
    the table widget so it appears similar to the screenshot below

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image015.png)

13.
Highlight the  **YTD – Oct, 2023** in the widget title and
click the delete key (note that the Oct, 2023 is dynamic text referencing the
Current Date story filter)

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image017.png)

14. With your cursor between the brackets () right-click.  Select **Add > Dynamic Text**

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image018.png)

15. Select Input Controls, and check **Version.  **The click the **Create** button.

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image019.png)

16. Click on the chart (to ensure it is selected) and open
    the **Right Side Panel.  **If not
    already active, toggle the **Builder** panel

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image020.png)

17. Click on the **Select Model** button in the Builder
    panel

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image022.png)

18. Select **OK** on the resulting warning message

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image024.png)

19. Click on the Select Model dropdown and choose the **SAP_XPA_SALESPLAN_TE2023**

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image025.png)

20. Click the **OK** button

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image026.png)

21. Configure the builder panel as displayed in the []()[i]()mage below

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image028.png)

22. Navigate to the styling panel.  Change the ID of the chart to  **SP_US_FY_CHT** .  Hit the Enter key to commit the ID change

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image030.png)

23. Click the widget menu for the numeric point chart. Then
    choose **More Options > Show/Hide > Primary Value Labels** to toggle
    off the Gross Sales label

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image032.png)

24. Click the **File > Save** menu to save your
    dashboard

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image033.png)

⚠️[**Quality Check!**]() Does your Sales Plan
Entry tab look as follows? Note: the Plan_Contributor input control will
reflect your user ID

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image034.png)

🚩 Now that we have made basic updates to the input
template, we are going to introduce some scripting components to leverage a
custom widget allowing end-users to directly upload a csv or xls from their
local computer.

25. Open the **Left Side Panel**

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image036.png)

26. Under the **Assets** menu, expand **Custom Widgets**

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image038.png)

27. Select the **Upload XLS v2.0.1** and drag it into an
    open space on the canvass near the top of the tab (note that the widget label
    will disappear once you have finished positioning the widget)

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image040.png)

28. From the insert menu let’s add a new  **Button ** (we’ll
    use this to call our custom widget)

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image041.png)

29. Open up the styling menu of the button and change the settings to the following

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image043.png)

 🚩 Finally, we need to add JavaScript to trigger events in
both the custom widget and the button to call the custom widget.  The custom widget includes multiple custom
events (part of the widget code itself), but in the interest of time we will
only populate two of these with script.  Upon click, the button we inserted in the
previous step will define a series of mappings (based on a predefined structure
of the upload file to the model we are uploading the data into), and then call
the custom widget.    The custom widget has events to 1) display status
information during the file upload process, and 2) process the data into the
model once the file upload is complete including reporting any errors and a
reject file if some records are not loaded.

30. If it is not already visible, then open the Left Side Panel.  Select the **UploadXLS_1** which should
    appear within the **SalesPlanEntry** page in the Outline menu

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image044.png)

31. Click on the **Edit Scripts** button and select the **onFileUpload**
    event

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image045.png)

32. Paste the following Javascript into the function dialog:

*var sheets = UploadXLS_1.getSheetNames();*

*var records =
UploadXLS_1.getTotalRows(sheets[0]);*

*var chunkSize = UploadXLS_1.getChunkSize();*

*if(records <= chunkSize){*

* Application.showBusyIndicator('Uploading
  '+records.toString() + ' rows from the Excel file');*

*}else{*

* Application.showBusyIndicator('Uploading
  first '+chunkSize.toString() + ' rows from the total '+records.toString() +' in
  the Excel file');*

*}*

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image047.png)

33. Click on the [**Edit Scripts** ]()button and select the **onDataUpload**
    event

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image048.png)

34. Paste the following Javascript into the function dialog:

*SP_SALESPLAN_TBLE.getDataSource().refreshData();*

*Application.hideBusyIndicator();*

*var status = this.getUploadResult().jobStatus;*

*if (status === sdk_com_sap_sample_uploadxls__2_JobStatus.COMPLETED_WITH_FAILURES){*

* console.log(this.getUploadResult().failedRows);*
* this.downloadFailedRecords();*

*}*

*SP_US_FY_CHT.getDataSource().refreshData();*

*console.log(this.getUploadResult().jobStatus);*

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image050.png)

35. Click on the **Edit Scripts** button and select the **onFailedUpload**
    event

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image051.png)

36. Paste the following Javascript into the function dialog:

*Application.showMessage(ApplicationMessageType.Error,'There
was an error uploading the Excel data');*

*Application.hideBusyIndicator();*

*console.log(this.getUploadResult());*

37. Select the **BTN_UPLOAD** which should also appear
    within the SalesPlanEntry page in the Outline menu

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image052.png)

38. Click on the **Edit Scripts** button and select the **onClick**
    event

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image054.png)

39. Paste the following JavaScript in the function dialog:

*var modelId =
SP_SALESPLAN_TBLE.getDataSource().getInfo().modelId;*

*UploadXLS_1.setModelId(modelId);*

*var mappings = {*

* "SAP_XPA_ACCOUNT":"Account",*
* "Version":"Version",*
* "SAP_XPA_PRODUCT":"Product",*
* "SAP_XPA_BUSUNIT":"Org",*
* "SAP_LOB_REGION":"Sales
  Region"*

*};*

*var defaultValues = { *

* "SAP_XPA_MGR":IC_MANAGER.getInputControlDataSource().getActiveSelectedMembers()[0].displayId*
* };*

*UploadXLS_1.uploadData(mappings,defaultValues,true,"",false);*

*Application.showBusyIndicator('Uploading File...');*

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image055.png)

40. Click the **File > Save** menu to save your
    dashboard

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image057.png)

🚩 In the final step of exercise 1, we will test our template
changes, including our upload widget.  Recall
where you saved the SalesPlan_Quantity.xls file in the getting started section
as we will use that file for our testing.
Also note that we have not fully coded the upload button as we would in
a production scenario (e.g., process cancellation, error trapping) due to time
considerations, so proceed through these steps slowly.   If you experience any issues, consider
reloading your story ( **View ** > **Reload this Page** in Chrome)

41. Click the View mode button to change from edit mode to
    view mode

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image059.png)

42. Navigate to the **Sales Plan Entry** tab

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image060.png)

**43.  **Ensure the page has fully loaded, and then click on the **User
Upload** button

![](file:////Users/I818705/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image062.png)

44. From the file system dialog, locate the **SalesPlan_Quantity.xls**
    file and click **OK**

🚩 At this point you should see a popup dialog indicating
that 1008 rows are being uploaded from the Excel file.   This upload may take a few moments after
which you should see the dashboard refresh with the upload quantities.

⚠️[**Quality Check!**]() Does your refreshed dashboard (including upload
results) look like this? Note: the Plan_Contributor input control will reflect
your user ID 


## **Summary**



**Congratulations, you have completed Exercise
1!**

**You are now able to:**

* Make simple changes to an existing dashboard
* Introduce additional charts and widgets into
  your dashboard

* Leverage JavaScript script to further tailor
  your planning template
