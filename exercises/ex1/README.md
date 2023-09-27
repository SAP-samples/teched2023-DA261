# Exercise 1 - Plan Story Navigation and Enrichment

**Objective:** You should develop an understanding of basic story
navigation, and how to modify a story to include new visualiziations,
change existing widget settings, and leverage custom widgets and script
to improve our planning template.

**Estimated Time:** 25 min

**Exercise Description:**  CycleBros is a Germany headquartered
recreational bike manufacturer and distributor. You are an FP&A analyst
for CycleBros, and you are looking to make changes to existing dashboard
to support the upcoming planning cycle, including some customization for
specific changes occurring in the US region and end-user requested
enhancements.

**Key Features:**

- Basic navigation of the dashboard
- Inclusion of new widgets and minor changes to existing widget
  settings
- Introduction of a custom widget and script to support direct
  end-user upload of planning data

⚠️**Disclaimer** When completing exercises, it is expected that data
values or screenshots should match what you see on your screen. If you
see inconsistencies as you work through the exercise, please refer to
the appropriate section in **Getting Started** Readme. For any
inconsistencies which are not addressed therein, please check with your
instructor.

🚩As a FP&A Analyst for CycleBros, we are interested in extending the
existing dashboard that incorporates Business Intelligence and Planning.
Start by reviewing the initial dashboard. You will notice that we have 2
tabs. The tab first is tracking financial performance for the current
year (currently filtered to All Regions and the current close period --
Oct 2023). In the second tab, we have a sales plan entry template which
is meant to capture sales quantity forecasts by period for each of
products. Note that we have included a couple of input controls (i.e.,
plan version and user) which are already selected and are not meant to
be modified during the exercise (this is to simplify data capture and
data segregation for TechEd). Additionally, for the purposes simplicity
we have narrowed the exercises to primarily focus on the US region. We
will make a couple of minor changes to dashboard filters, while also
making some additional enhancements to improve end-user plan entry
flexibility.

Let's start by editing the dashboard!

1. First ensure you are on the Financial Overview tab. Then
   click **Edit** to change the dashboard to authoring mode.

<img src="./images/image1.png" style="width:456px;height:275px;"/>

🚩 The first thing we want to do is make some end-user requested changes
to the Financial Overview page. This include updating the dashboard
title to dynamic reflect our region filter selection, changing the
default filter for region to focus on the US, and modifying the default
drill level for our P&L in the table widget.

2. In the dashboard title text box, highlight the **DA261** and click
   the delete key

<img src="./images/image2.png"/>

3. With your cursor between the brackets () right-click. Select **Add**
   \> **Dynamic Text**

<img src="./images/image3.png"/>

4. From the Insert Dynamic Text popup, select **Story Filters** and
   check the box for **SAP_XPA_REGION** and click the **Create** button

<img src="./images/image4.png" style="width:461px;height:279px;"/>

5. Now let's change the default filter selection for the region by
   clicking on the **SAP_XPA_REGION** filter at the top of the
   dashboard and deselecting the **All** filter 

<img src="./images/image5.png" style="width:414.96096px;height:282.53664000000003px;"/>

6. Select **United States** and click **Apply Selections**

<img src="./images/image6.png" style="width:416.41824px;height:288.33408000000003px;"/>

6. Finally, let's change the default drill depth in our table by first
   right-clicking on the **SAP_XPA_ACCOUNT** dimension header within
   the table. Select **Drill** \> **Level 4**

<img src="./images/image7.png" style="width:480.62784px;height:287.14464px;"/>

7. Click **File/Save** to save your dashboard updates

<img src="./images/image8.png" style="width:472.29984px;height:266.22335999999996px;"/>

⚠️**Quality Check!** Does your dashboard look like this?

<img src="./images/image9.png" style="width:562.1337599999999px;height:407.36735999999996px;"/>

🚩 Now that we have updated the Financial Overview, we are next going to
make some preliminary changes to the Sales Plan Entry tab to prepare for
the upcoming planning cycle. We are going to add two new widgets. The
first will simplify review of total units planned, while the second will
introduce a custom widget to provide a mechanism for end-users to
directly upload their sales plan numbers from csv or xls.

8. Navigate to the **Sales Plan Entry** tab, and review the template

<img src="./images/image10.png" style="width:415.0032px;height:180.82752px;"/>

🚩 We want to add a a numeric point chart to track full year total
quantity planned. This number will ultimately be visible in the table as
well, but we want to make it more prominent the end-user. Rather than
inserting a net-new chart, we are going to duplicate an existing object
and repoint it.

9. Navigate back to the **Financial Overview** tab, and select the Unit
   Sales numeric point chart

<img src="./images/image11.png" style="width:549.6432px;height:236.65152px;"/>

10. From the widget menu select **Copy \> Copy To \> Sales Plan Entry**

<img src="./images/image12.png" style="width:417.85632px;height:232.84416000000002px;"/>

11. Navigate to the **Sales Plan Entry** tab

<img src="./images/image13.png" style="width:519.1699199999999px;height:307.85375999999997px;"/>

12. Move (click and drag) and resize the widget (select corner or edge
    and click-drag) so the right side aligns with the right side of the
    table widget so it appears similar to the screenshot below

<img src="./images/image14.png" style="width:463.08480000000003px;height:287.69664px;"/>

13. Highlight the **YTD -- Oct, 2023** in the widget title and click the
    delete key (note that the Oct, 2023 is dynamic text referencing the
    Current Date story filter)

<img src="./images/image15.png" style="width:405.15744px;height:228.79488px;"/>

14. With your cursor between the brackets () right-click. Select **Add
    \> Dynamic Text**

<img src="./images/image16.png" style="width:422.13024px;height:232.74239999999998px;"/>

15. Select Input Controls, and check **Version.** The click the
    **Create** button.

<img src="./images/image17.png" style="width:422.45472px;height:262.13184px;"/>

16. Click on the chart (to ensure it is selected) and open the **Right
    Side Panel.** If not already active, toggle the **Builder** panel

<img src="./images/image18.png" style="width:558.12864px;height:267.85344px;"/>

17. Click on the **Select Model** button in the Builder panel

<img src="./images/image19.png" style="width:427.03584px;height:244.97376000000003px;"/>

18. Select **OK** on the resulting warning message

<img src="./images/image20.png" style="width:385.97952px;height:107.928px;"/>

19. Click on the Select Model dropdown and choose the
    **SAP_XPA_SALESPLAN_TE2023**

<img src="./images/image21.png" style="width:390.86303999999996px;height:221.14656px;"/>

20. Click the **OK** button

<img src="./images/image22.png" style="width:304.00032px;height:109.33344px;"/>

21. Configure the builder panel as displayed in the image below

<img src="./images/image23.png" style="width:227.05152px;height:324.05568px;"/>

22. Navigate to the styling panel. Change the ID of the chart to
    "SP_US_FY_CHT". Hit the Enter key to commit the ID change

<img src="./images/image24.png" style="width:242.89056px;height:371.81759999999997px;"/>

23. Click the widget menu for the numeric point chart. Then choose
    **More Options \> Show/Hide \> Primary Value Labels** to toggle off
    the Gross Sales label

<img src="./images/image25.png" style="width:380.2848px;height:195.87072px;"/>

24. Click the **File \> Save** menu to save your dashboard

<img src="./images/image26.png" style="width:385.22303999999997px;height:231.46368px;"/>

⚠️**Quality Check!** Does your Sales Plan Entry tab look as follows?
Note: the Plan_Contributor input control will reflect your user ID

<img src="./images/image27.png" style="width:624.0px;height:347.59968000000003px;"/>

🚩 Now that we have made basic updates to the input template, we are
going to introduce some scripting components to leverage a custom widget
allowing end-users to directly upload a csv or xls from their local
computer.

25. Open the left side panel

<img src="./images/image28.png" style="width:511.608px;height:335.3328px;"/>

26. Under the **Assets** menu, expand **Custom Widgets**

<img src="./images/image29.png" style="width:126.91968px;height:148.28832px;"/>

27. Select the **Upload XLS v2.0.1** and drag it into an open space on
    the canvass near the top of the tab (note that the widget label will
    disappear once you have finished positioning the widget)

<img src="./images/image30.png" style="width:363.35519999999997px;height:293.856px;"/>

28. From the insert menu let's add a new **Button** (we'll use this to
    call our custom widget)

<img src="./images/image31.png" style="width:423.20543999999995px;height:240.1776px;"/>

29. Open up the styling menu of the button and change the settings to
    the following

<img src="./images/image32.png" style="width:232.00032px;height:629.33376px;"/>

🚩 Finally, we need to add JavaScript to trigger events in both the
custom widget and the button to call the custom widget. The custom
widget includes multiple custom events (part of the widget code itself),
but in the interest of time we will only populate two of these with
script. Upon click, the button we inserted in the previous step will
define a series of mappings (based on a predefined structure of the
upload file to the model we are uploading the data into), and then call
the custom widget. The custom widget has events to 1) display status
information during the file upload process, and 2) process the data into
the model once the file upload is complete including reporting any
errors and a reject file if some records are not loaded.

30. If it is not already visible, then open the left side panel. Select
    the **UploadXLS_1** which should appear within the
    **SalesPlanEntry** page in the **Outline** menu

<img src="./images/image33.png" style="width:397.88256px;height:302.7744px;"/>

31. Click on the **Edit Scripts** button and select the **onFileUpload**
    event

<img src="./images/image34.png" style="width:176.18304px;height:243.1968px;"/>

32. Paste the following Javascript into the function dialog:

> *var sheets = UploadXLS_1.getSheetNames();*
>
> *var records = UploadXLS_1.getTotalRows(sheets\[0\]);*
>
> *var chunkSize = UploadXLS_1.getChunkSize();*
>
> *if(records \<= chunkSize){*
>
> *Application.showBusyIndicator(\'Uploading \'+records.toString() + \'
> rows from the Excel file\');*
>
> *}else{*
>
> *Application.showBusyIndicator(\'Uploading first
> \'+chunkSize.toString() + \' rows from the total \'+records.toString()
> +\' in the Excel file\');*
>
> *}*

<img src="./images/image35.png" style="width:624.0px;height:256.46688px;"/>

33. Click on the **Edit Scripts** button and select the **onDataUpload**
    event

<img src="./images/image36.png" style="width:243.06432px;height:158.8992px;"/>

34. Paste the following Javascript into the function dialog:

*SP_SALESPLAN_TBLE.getDataSource().refreshData();*

*Application.hideBusyIndicator();*

*var status = this.getUploadResult().jobStatus;*

*if (status ===
sdk_com_sap_sample_uploadxls\_\_2_JobStatus.COMPLETED_WITH_FAILURES){*

*console.log(this.getUploadResult().failedRows);*

*this.downloadFailedRecords();*

*}*

*SP_US_FY_CHT.getDataSource().refreshData();*

*console.log(this.getUploadResult().jobStatus);*

<img src="./images/image37.png" style="width:624.0px;height:275.59968000000003px;"/>

35. Click on the **Edit Scripts** button and select the
    **onFailedUpload** event

<img src="./images/image38.png" style="width:234.16992px;height:169.20672px;"/>

36. Paste the following Javascript into the function dialog:

*Application.showMessage(ApplicationMessageType.Error,\'There was an
error uploading the Excel data\');*

*Application.hideBusyIndicator();*

*console.log(this.getUploadResult());*

37. Select the **BTN_UPLOAD** which should also appear within the
    SalesPlanEntry page in the **Outline** menu

<img src="./images/image39.png" style="width:152.11488px;height:248.91456px;"/>

38. Click on the **Edit Scripts** button and select the **onClick**
    event

<img src="./images/image40.png" style="width:272.85984px;height:184.29216px;"/>

39. Paste the following JavaScript in the function dialog:

*var modelId = SP_SALESPLAN_TBLE.getDataSource().getInfo().modelId;*

*UploadXLS_1.setModelId(modelId);*

*var mappings = {*

*\"SAP_XPA_ACCOUNT\":\"Account\",*

*\"Version\":\"Version\",*

*\"SAP_XPA_PRODUCT\":\"Product\",*

*\"SAP_XPA_BUSUNIT\":\"Org\",*

*\"SAP_LOB_REGION\":\"Sales Region\"*

*};*

*var defaultValues = {*

*\"SAP_XPA_MGR\":IC_MANAGER.getInputControlDataSource().getActiveSelectedMembers()\[0\].displayId*

*};*

*UploadXLS_1.uploadData(mappings,defaultValues,true,\"\",false);*

*Application.showBusyIndicator(\'Uploading File\...\');*

<img src="./images/image41.png" style="width:589.89888px;height:252.28224px;"/>

40. Click the **File \> Save** menu to save your dashboard

<img src="./images/image42.png" style="width:338.13120000000004px;height:171.04512px;"/>

🚩 In the final step of exercise 1, we will test our template changes,
including our upload widget. Recall where you saved the
SalesPlan_Quantity.xls file in the getting started section as we will
use that file for our testing. Also note that we have not fully coded
the upload button as we would in a production scenario (e.g., process
cancellation, error trapping) due to time considerations, so proceed
through these steps slowly. If you experience any issues, consider
reloading your story (**View** \> **Reload this Page** in Chrome)

41. Click the View mode button to change from edit mode to view mode

<img src="./images/image43.png" style="width:327.20448px;height:173.77248px;"/>

42. Navigate to the **Sales Plan Entry** tab

<img src="./images/image44.png" style="width:493.34975999999995px;height:258.05952px;"/>

43. Ensure the page has fully loaded, and then click on the **User
    Upload** button 

<img src="./images/image45.png" style="width:414.31008px;height:262.44096px;"/>

44. From the file system dialog, locate the **SalesPlan_Quantity.xls**
    file and click **OK**

🚩 At this point you should see a popup dialog indicating that 1008 rows
are being uploaded from the Excel file. This upload may take a few
moments after which you should see the dashboard refresh with the upload
quantities.

⚠️**Quality Check!** Does your refreshed dashboard (including upload
results) look like this? Note: the Plan_Contributor input control will
reflect your user ID

<img src="./images/image46.png" style="width:624.0px;height:372.73344px;"/>

## Summary

**Congratulations, you have completed Exercise 1!**

**You are now able to:**

* Make simple changes to an existing dashboard
* Introduce additional charts and widgets into your dashboard
* Leverage JavaScript script to further tailor your planning template

Please continue to [Exercise 2 - Advanced Planning with Data Actions and Multi Actions](https://github.com/SAP-samples/teched2023-DA261/tree/main/exercises/ex2)
