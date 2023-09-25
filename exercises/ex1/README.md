<link rel="stylesheet" href="styles.css" />
<h1 id="exercise-1-plan-story-navigation-and-enrichment">Exercise 1 –
Plan Story Navigation and Enrichment</h1>
<p><strong>Objective:</strong> You should develop an understanding of
basic story navigation, and how to modify a story to include new
visualiziations, change existing widget settings, and leverage custom
widgets and script to improve our planning template.</p>
<p><strong>Estimated Time:</strong> 25 mins</p>
<p><strong>Exercise Description:</strong>  CycleBros is a Germany
headquartered recreational bike manufacturer and distributor. You are an
FP&amp;A analyst for CycleBros, and you are looking to make changes to
existing dashboard to support the upcoming planning cycle, including
some customization for specific changes occurring in the US region and
end-user requested enhancements.</p>
<p><strong>Key Features:</strong></p>
<ul>
<li><p>Basic navigation of the dashboard</p></li>
<li><p>Inclusion of new widgets and minor changes to existing widget
settings</p></li>
<li><p>Introduction of a custom widget and script to support direct
end-user upload of planning data</p></li>
</ul>
<p>⚠️<strong>Disclaimer</strong> When completing exercises, it is
expected that data values or screenshots should match what you see on
your screen. If you see inconsistencies as you work through the
exercise, please refer to the appropriate section in <strong>Getting
Started</strong> Readme. For any inconsistencies which are not addressed
therein, please check with your instructor.</p>
<p>🚩As a FP&amp;A Analyst for CycleBros, we are interested in extending
the existing dashboard that incorporates Business Intelligence and
Planning. Start by reviewing the initial dashboard. You will notice that
we have 2 tabs. The tab first is tracking financial performance for the
current year (currently filtered to All Regions and the current close
period – Oct 2023). In the second tab, we have a sales plan entry
template which is meant to capture sales quantity forecasts by period
for each of products. Note that we have included a couple of input
controls (i.e., plan version and user) which are already selected and
are not meant to be modified during the exercise (this is to simplify
data capture and data segregation for TechEd). Additionally, for the
purposes simplicity we have narrowed the exercises to primarily focus on
the US region. We will make a couple of minor changes to dashboard
filters, while also making some additional enhancements to improve
end-user plan entry flexibility.</p>
<p>Let’s start by editing the dashboard!</p>
<ol type="1">
<li><p>First ensure you are on the Financial Overview tab. Then
click <strong>Edit</strong> to change the dashboard to authoring
mode.</p></li>
</ol>
<p><img src="./images/image1.png"
style="width:3.70921in;height:2.35075in" /></p>
<p>🚩 The first thing we want to do is make some end-user requested
changes to the Financial Overview page. This include updating the
dashboard title to dynamic reflect our region filter selection, changing
the default filter for region to focus on the US, and modifying the
default drill level for our P&amp;L in the table widget.</p>
<ol start="2" type="1">
<li><p>In the dashboard title text box, highlight the
<strong>DA261</strong> and click the delete key</p></li>
</ol>
<p><img src="./images/image2.png"
style="width:5.30306in;height:2.68382in" /></p>
<ol start="3" type="1">
<li><p>With your cursor between the brackets () right-click. Select
<strong>Add</strong> &gt; <strong>Dynamic Text</strong></p></li>
</ol>
<p><img src="./images/image3.png"
style="width:5.37249in;height:2.86475in" /></p>
<ol start="4" type="1">
<li><p>From the Insert Dynamic Text popup, select <strong>Story
Filters</strong> and check the box for <strong>SAP_XPA_REGION</strong>
and click the <strong>Create</strong> button</p></li>
</ol>
<p><img src="./images/image4.png"
style="width:4.80436in;height:2.90725in" /></p>
<ol start="5" type="1">
<li><p>Now let’s change the default filter selection for the region by
clicking on the <strong>SAP_XPA_REGION</strong> filter at the top of the
dashboard and deselecting the <strong>All</strong> filter </p></li>
</ol>
<p><img src="./images/image5.png"
style="width:4.32251in;height:2.94309in" /></p>
<ol start="6" type="1">
<li><p>Select <strong>United States</strong> and click <strong>Apply
Selections</strong></p></li>
</ol>
<p><img src="./images/image6.png"
style="width:4.33769in;height:3.00348in" /></p>
<ol start="6" type="1">
<li><p>Finally, let’s change the default drill depth in our table by
first right-clicking on the <strong>SAP_XPA_ACCOUNT</strong> dimension
header within the table. Select <strong>Drill</strong> &gt;
<strong>Level 4</strong></p></li>
</ol>
<p><img src="./images/image7.png"
style="width:5.00654in;height:2.99109in" /></p>
<ol start="7" type="1">
<li><p>Click <strong>File/Save</strong> to save your dashboard
updates</p></li>
</ol>
<p><img src="./images/image8.png"
style="width:4.91979in;height:2.77316in" /></p>
<p>⚠️<strong>Quality Check!</strong> Does your dashboard look like
this?</p>
<p><img src="./images/image9.png"
style="width:5.85556in;height:4.24341in" /></p>
<p>🚩 Now that we have updated the Financial Overview, we are next going
to make some preliminary changes to the Sales Plan Entry tab to prepare
for the upcoming planning cycle. We are going to add two new widgets.
The first will simplify review of total units planned, while the second
will introduce a custom widget to provide a mechanism for end-users to
directly upload their sales plan numbers from csv or xls.</p>
<ol start="8" type="1">
<li><p>Navigate to the <strong>Sales Plan Entry</strong> tab, and review
the template</p></li>
</ol>
<p><img src="./images/image10.png"
style="width:6.32295in;height:3.88362in" /></p>
<p>🚩 We want to add a a numeric point chart to track full year total
quantity planned. This number will ultimately be visible in the table as
well, but we want to make it more prominent the end-user. Rather than
inserting a net-new chart, we are going to duplicate an existing object
and repoint it.</p>
<ol start="9" type="1">
<li><p>Navigate back to the <strong>Financial Overview</strong> tab, and
select the Unit Sales numeric point chart</p></li>
</ol>
<p><img src="./images/image11.png"
style="width:5.72545in;height:2.46512in" /></p>
<ol start="10" type="1">
<li><p>From the widget menu select <strong>Copy &gt; Copy To &gt; Sales
Plan Entry</strong></p></li>
</ol>
<p><img src="./images/image12.png"
style="width:4.35267in;height:2.42546in" /></p>
<ol start="11" type="1">
<li><p>Navigate to the <strong>Sales Plan Entry</strong> tab</p></li>
</ol>
<p><img src="./images/image13.png"
style="width:5.40802in;height:3.20681in" /></p>
<ol start="12" type="1">
<li><p>Move (click and drag) and resize the widget (select corner or
edge and click-drag) so the right side aligns with the right side of the
table widget so it appears similar to the screenshot below</p></li>
</ol>
<p><img src="./images/image14.png"
style="width:4.8238in;height:2.99684in" /></p>
<ol start="13" type="1">
<li><p>Highlight the <strong>YTD – Oct, 2023</strong> in the widget
title and click the delete key (note that the Oct, 2023 is dynamic text
referencing the Current Date story filter)</p></li>
</ol>
<p><img src="./images/image15.png"
style="width:4.22039in;height:2.38328in" /></p>
<ol start="14" type="1">
<li><p>With your cursor between the brackets () right-click. Select
<strong>Add &gt; Dynamic Text</strong></p></li>
</ol>
<p><img src="./images/image16.png"
style="width:4.39719in;height:2.4244in" /></p>
<ol start="15" type="1">
<li><p>Select Input Controls, and check <strong>Version.</strong> The
click the <strong>Create</strong> button.</p></li>
</ol>
<p><img src="./images/image17.png"
style="width:4.40057in;height:2.73054in" /></p>
<ol start="16" type="1">
<li><p>Click on the chart (to ensure it is selected) and open the
<strong>Right Side Panel.</strong> If not already active, toggle the
<strong>Builder</strong> panel</p></li>
</ol>
<p><img src="./images/image18.png"
style="width:5.81384in;height:2.79014in" /></p>
<ol start="17" type="1">
<li><p>Click on the <strong>Select Model</strong> button in the Builder
panel</p></li>
</ol>
<p><img src="./images/image19.png"
style="width:4.44829in;height:2.55181in" /></p>
<ol start="18" type="1">
<li><p>Select <strong>OK</strong> on the resulting warning
message</p></li>
</ol>
<p><img src="./images/image20.png"
style="width:4.02062in;height:1.12425in" /></p>
<ol start="19" type="1">
<li><p>Click on the Select Model dropdown and choose the
<strong>SAP_XPA_SALESPLAN_TE2023</strong></p></li>
</ol>
<p><img src="./images/image21.png"
style="width:4.07149in;height:2.30361in" /></p>
<ol start="20" type="1">
<li><p>Click the <strong>OK</strong> button</p></li>
</ol>
<p><img src="./images/image22.png"
style="width:3.16667in;height:1.13889in" /></p>
<ol start="21" type="1">
<li><p>Configure the builder panel as displayed in the image
below</p></li>
</ol>
<p><img src="./images/image23.png"
style="width:2.36512in;height:3.37558in" /></p>
<ol start="22" type="1">
<li><p>Navigate to the styling panel. Change the ID of the chart to
<strong>SP_US_FY_CHT</strong>. Hit the Enter key to commit the ID
change</p></li>
</ol>
<p><img src="./images/image24.png"
style="width:2.53011in;height:3.8731in" /></p>
<ol start="23" type="1">
<li><p>Click the widget menu for the numeric point chart. Then choose
<strong>More Options &gt; Show/Hide &gt; Primary Value Labels</strong>
to toggle off the Gross Sales label</p></li>
</ol>
<p><img src="./images/image25.png"
style="width:3.9613in;height:2.04032in" /></p>
<ol start="24" type="1">
<li><p>Click the <strong>File &gt; Save</strong> menu to save your
dashboard</p></li>
</ol>
<p><img src="./images/image26.png"
style="width:4.01274in;height:2.41108in" /></p>
<p>⚠️<strong>Quality Check!</strong> Does your Sales Plan Entry tab look
as follows? Note: the Plan_Contributor input control will reflect your
user ID</p>
<p><img src="./images/image27.png"
style="width:6.5in;height:3.62083in" /></p>
<p>🚩 Now that we have made basic updates to the input template, we are
going to introduce some scripting components to leverage a custom widget
allowing end-users to directly upload a csv or xls from their local
computer.</p>
<ol start="25" type="1">
<li><p>Open the <strong>Left Side Panel</strong></p></li>
</ol>
<p><img src="./images/image28.png"
style="width:5.32925in;height:3.49305in" /></p>
<ol start="26" type="1">
<li><p>Under the <strong>Assets</strong> menu, expand <strong>Custom
Widgets</strong></p></li>
</ol>
<p><img src="./images/image29.png"
style="width:1.32208in;height:1.54467in" /></p>
<ol start="27" type="1">
<li><p>Select the <strong>Upload XLS v2.0.1</strong> and drag it into an
open space on the canvass near the top of the tab (note that the widget
label will disappear once you have finished positioning the
widget)</p></li>
</ol>
<p><img src="./images/image30.png"
style="width:3.78495in;height:3.061in" /></p>
<ol start="28" type="1">
<li><p>From the insert menu let’s add a new <strong>Button</strong>
(we’ll use this to call our custom widget)</p></li>
</ol>
<p><img src="./images/image31.png"
style="width:4.40839in;height:2.50185in" /></p>
<ol start="29" type="1">
<li><p>Open up the styling menu of the button and change the settings to
the following</p></li>
</ol>
<p><img src="./images/image32.png"
style="width:2.41667in;height:6.55556in" /></p>
<p>🚩 Finally, we need to add JavaScript to trigger events in both the
custom widget and the button to call the custom widget. The custom
widget includes multiple custom events (part of the widget code itself),
but in the interest of time we will only populate two of these with
script. Upon click, the button we inserted in the previous step will
define a series of mappings (based on a predefined structure of the
upload file to the model we are uploading the data into), and then call
the custom widget. The custom widget has events to 1) display status
information during the file upload process, and 2) process the data into
the model once the file upload is complete including reporting any
errors and a reject file if some records are not loaded.</p>
<ol start="30" type="1">
<li><p>If it is not already visible, then open the Left Side Panel.
Select the <strong>UploadXLS_1</strong> which should appear within the
<strong>SalesPlanEntry</strong> page in the Outline menu</p></li>
</ol>
<p><img src="./images/image33.png"
style="width:4.14461in;height:3.1539in" /></p>
<ol start="31" type="1">
<li><p>Click on the <strong>Edit Scripts</strong> button and select the
<strong>onFileUpload</strong> event</p></li>
</ol>
<p><img src="./images/image34.png"
style="width:1.83524in;height:2.5333in" /></p>
<ol start="32" type="1">
<li><p>Paste the following Javascript into the function dialog:</p></li>
</ol>
<blockquote>
<p><em>var sheets = UploadXLS_1.getSheetNames();</em></p>
<p><em>var records = UploadXLS_1.getTotalRows(sheets[0]);</em></p>
<p><em>var chunkSize = UploadXLS_1.getChunkSize();</em></p>
<p><em>if(records &lt;= chunkSize){</em></p>
<p><em>Application.showBusyIndicator('Uploading '+records.toString() + '
rows from the Excel file');</em></p>
<p><em>}else{</em></p>
<p><em>Application.showBusyIndicator('Uploading first
'+chunkSize.toString() + ' rows from the total '+records.toString() +'
in the Excel file');</em></p>
<p><em>}</em></p>
</blockquote>
<p><img src="./images/image35.png"
style="width:6.5in;height:2.67153in" /></p>
<ol start="33" type="1">
<li><p>Click on the <strong>Edit Scripts</strong> button and select the
<strong>onDataUpload</strong> event</p></li>
</ol>
<p><img src="./images/image36.png"
style="width:2.53192in;height:1.6552in" /></p>
<ol start="34" type="1">
<li><p>Paste the following Javascript into the function dialog:</p></li>
</ol>
<p><em>SP_SALESPLAN_TBLE.getDataSource().refreshData();</em></p>
<p><em>Application.hideBusyIndicator();</em></p>
<p><em>var status = this.getUploadResult().jobStatus;</em></p>
<p><em>if (status ===
sdk_com_sap_sample_uploadxls__2_JobStatus.COMPLETED_WITH_FAILURES){</em></p>
<p><em>console.log(this.getUploadResult().failedRows);</em></p>
<p><em>this.downloadFailedRecords();</em></p>
<p><em>}</em></p>
<p><em>SP_US_FY_CHT.getDataSource().refreshData();</em></p>
<p><em>console.log(this.getUploadResult().jobStatus);</em></p>
<p><img src="./images/image37.png"
style="width:6.5in;height:2.87083in" /></p>
<ol start="35" type="1">
<li><p>Click on the <strong>Edit Scripts</strong> button and select the
<strong>onFailedUpload</strong> event</p></li>
</ol>
<p><img src="./images/image38.png"
style="width:2.43927in;height:1.76257in" /></p>
<ol start="36" type="1">
<li><p>Paste the following Javascript into the function dialog:</p></li>
</ol>
<p><em>Application.showMessage(ApplicationMessageType.Error,'There was
an error uploading the Excel data');</em></p>
<p><em>Application.hideBusyIndicator();</em></p>
<p><em>console.log(this.getUploadResult());</em></p>
<ol start="37" type="1">
<li><p>Select the <strong>BTN_UPLOAD</strong> which should also appear
within the SalesPlanEntry page in the Outline menu</p></li>
</ol>
<p><img src="./images/image39.png"
style="width:1.58453in;height:2.59286in" /></p>
<ol start="38" type="1">
<li><p>Click on the <strong>Edit Scripts</strong> button and select the
<strong>onClick</strong> event</p></li>
</ol>
<p><img src="./images/image40.png"
style="width:2.84229in;height:1.91971in" /></p>
<ol start="39" type="1">
<li><p>Paste the following JavaScript in the function dialog:</p></li>
</ol>
<p><em>var modelId =
SP_SALESPLAN_TBLE.getDataSource().getInfo().modelId;</em></p>
<p><em>UploadXLS_1.setModelId(modelId);</em></p>
<p><em>var mappings = {</em></p>
<p><em>"SAP_XPA_ACCOUNT":"Account",</em></p>
<p><em>"Version":"Version",</em></p>
<p><em>"SAP_XPA_PRODUCT":"Product",</em></p>
<p><em>"SAP_XPA_BUSUNIT":"Org",</em></p>
<p><em>"SAP_LOB_REGION":"Sales Region"</em></p>
<p><em>};</em></p>
<p><em>var defaultValues = {</em></p>
<p><em>"SAP_XPA_MGR":IC_MANAGER.getInputControlDataSource().getActiveSelectedMembers()[0].displayId</em></p>
<p><em>};</em></p>
<p><em>UploadXLS_1.uploadData(mappings,defaultValues,true,"",false);</em></p>
<p><em>Application.showBusyIndicator('Uploading File...');</em></p>
<p><img src="./images/image41.png"
style="width:6.14478in;height:2.62794in" /></p>
<ol start="40" type="1">
<li><p>Click the <strong>File &gt; Save</strong> menu to save your
dashboard</p></li>
</ol>
<p><img src="./images/image42.png"
style="width:3.5222in;height:1.78172in" /></p>
<p>🚩 In the final step of exercise 1, we will test our template
changes, including our upload widget. Recall where you saved the
SalesPlan_Quantity.xls file in the getting started section as we will
use that file for our testing. Also note that we have not fully coded
the upload button as we would in a production scenario (e.g., process
cancellation, error trapping) due to time considerations, so proceed
through these steps slowly. If you experience any issues, consider
reloading your story (<strong>View</strong> &gt; <strong>Reload this
Page</strong> in Chrome)</p>
<ol start="41" type="1">
<li><p>Click the View mode button to change from edit mode to view
mode</p></li>
</ol>
<p><img src="./images/image43.png"
style="width:3.40838in;height:1.81013in" /></p>
<ol start="42" type="1">
<li><p>Navigate to the <strong>Sales Plan Entry</strong> tab</p></li>
</ol>
<p><img src="./images/image44.png"
style="width:5.13906in;height:2.68812in" /></p>
<ol start="43" type="1">
<li><p>Ensure the page has fully loaded, and then click on the
<strong>User Upload</strong> button </p></li>
</ol>
<p><img src="./images/image45.png"
style="width:4.31573in;height:2.73376in" /></p>
<ol start="44" type="1">
<li><p>From the file system dialog, locate the
<strong>SalesPlan_Quantity.xls</strong> file and click
<strong>OK</strong></p></li>
</ol>
<p>🚩 At this point you should see a popup dialog indicating that 1008
rows are being uploaded from the Excel file. This upload may take a few
moments after which you should see the dashboard refresh with the upload
quantities.</p>
<p>⚠️<strong>Quality Check!</strong> Does your refreshed dashboard
(including upload results) look like this? Note: the Plan_Contributor
input control will reflect your user ID</p>
<p><img src="./images/image46.png"
style="width:6.5in;height:3.88264in" /></p>
<h2 id="summary">Summary</h2>
<p><strong>Congratulations, you have completed Exercise 1!</strong></p>
<p><strong>You are now able to:</strong></p>
<ul>
<li><p>Make simple changes to an existing dashboard</p></li>
<li><p>Introduce additional charts and widgets into your
dashboard</p></li>
<li><p>Leverage JavaScript script to further tailor your planning
template</p></li>
</ul>