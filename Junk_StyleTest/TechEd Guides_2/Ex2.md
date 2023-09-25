<link rel="stylesheet" href="styles.css" />
<h1
id="exercise-2-advanced-planning-with-data-actions-and-multi-actions">Exercise
2 – Advanced Planning with Data Actions and Multi Actions </h1>
<p><strong>Objective:</strong> You will develop a basic understanding
how to create and execute data action and multi actions. You will
explore data action tracing, which is useful for debugging data actions
and will create parameters to streamline the execution of data/multi
actions</p>
<p><strong>Estimated Time:</strong> 45 mins</p>
<p><strong>Exercise Description:</strong>  Now that the sales quantity
has been uploaded to the sales model, we are going to create a data
action to calculate sales revenue and an allocation to distribute retail
returns to the product level based on our expected sales revenue. In the
last step of the exercise, we will transfer our sales plan to our
financial plan.</p>
<p><strong>Key Features:</strong></p>
<ul>
<li><p>Creation of data action to streamline calculations.</p>
<ul>
<li><p>Create data action parameters to streamline execution.</p></li>
<li><p>Create a simple advanced formula for sales revenue
calculation.</p></li>
<li><p>Create an allocation rule to allocate retail expenses.</p></li>
<li><p>Creating a cross model copy rule, which aggregates data based on
region.</p></li>
</ul></li>
<li><p>Executing a trace on a data action and reviewing
results.</p></li>
<li><p>Creating a multi-action to orchestrate data actions.</p></li>
<li><p>Format trigger within the story and map parameters.</p></li>
</ul>
<p>⚠️<strong>Disclaimer</strong> When completing exercises, it is
expected that data values or screenshots should match what you see on
your screen. If you see inconsistencies as you work through the
exercise, please refer to the appropriate section in <strong>Getting
Started</strong> Readme. For any inconsistencies which are not addressed
therein, please check with your instructor.</p>
<p>🚩As a FP&amp;A Analyst for CycleBros, we are interested in
automating the calculation framework for our planning scenario. We will
automate the calculation via data and multi actions, which we will
create as part of this exercise. We will learn how to execute traces on
data actions and then how to include all this logic into a story.</p>
<p>Let’s start by editing the dashboard to show the finance plan. This
will make it easy to eventually see how our sales planning activities
transfer to the finance plan near the end of the exercise.</p>
<ol start="6" type="1">
<li><p>We are now going to adjust the layout of the sales planning
table. Our first step will be select the table object, select edit mode
for the story, the right design panel and then the builder panel. This
will allow us to redefine the definition of the table object.</p></li>
</ol>
<p><img src="./images/ex2/image1.png"
style="width:6.5in;height:3.33611in" /></p>
<ol start="7" type="1">
<li><p>Adjust the table definition to match the definition provided
below. For <strong>Account</strong>, we will filter on Gross Revenue and
for <strong>Measures</strong> we will filter on Quantity and
Amount.</p></li>
</ol>
<p><img src="./images/ex2/image2.png"
style="width:3.29225in;height:6.23795in" /></p>
<ol start="8" type="1">
<li><p>We will enable null suppression to remove the null rows from the
report.</p></li>
</ol>
<p><img src="./images/ex2/image3.png"
style="width:2.83297in;height:1.92378in" /></p>
<ol start="9" type="1">
<li><p>We will now collapse the hierarchy of the report so that we are
only looking at an overview of our sales plan.</p></li>
</ol>
<p><img src="./images/ex2/image4.png"
style="width:4.33381in;height:1.60249in" /></p>
<ol start="10" type="1">
<li><p>Once we close the right builder pane and resize the table, your
results should look like this:</p></li>
</ol>
<p><img src="./images/ex2/image5.png"
style="width:6.5in;height:2.47569in" /></p>
<ol start="11" type="1">
<li><p>We are now going to create a table that shows our Finance data.
As part of this exercise, we are going to integrate our sales plan into
the finance plan so we will add a table showing finance data so we can
showcase this integration. To begin, we will duplicate the Sales
Quantity table, reposition it and then open up the builder panel so we
can select our finance model.</p></li>
</ol>
<p><img src="./images/ex2/image6.png"
style="width:6.5in;height:3.55278in" /></p>
<ol start="12" type="1">
<li><p>Acknowledge the warning and then select the finance
model.</p></li>
</ol>
<p><img src="./images/ex2/image7.png"
style="width:3.2991in;height:0.5576in" /></p>
<p><img src="./images/ex2/image8.png"
style="width:3.1975in;height:2.34244in" /></p>
<ol start="13" type="1">
<li><p>Set the table layout and filters as shown</p></li>
</ol>
<blockquote>
<p><img src="./images/ex2/image9.png"
style="width:4.93681in;height:9in" /></p>
</blockquote>
<ol start="14" type="1">
<li><p>Rename the table to Finance () and then add dynamic text between
the “()” for the version.</p></li>
</ol>
<blockquote>
<p><img src="./images/ex2/image10.png"
style="width:2.756in;height:1.62824in" /></p>
</blockquote>
<ol start="15" type="1">
<li><p>Select the Version item from the Input Controls
selections.</p></li>
</ol>
<blockquote>
<p><img src="./images/ex2/image11.png"
style="width:3.97982in;height:2.50312in" /></p>
</blockquote>
<p>⚠️ <strong>Quality Check!</strong> Does your refreshed dashboard
(including upload results) look like this? Note: The right planning
panel may need to be de-selected from the meu to replicate this
view.</p>
<p><img src="./images/ex2/image12.png"
style="width:6.5in;height:3.75833in" /></p>
<ol start="16" type="1">
<li><p>Save your story.</p></li>
</ol>
<blockquote>
<p><img src="./images/ex2/image13.png"
style="width:3.64713in;height:1.90773in" /></p>
</blockquote>
<ol start="17" type="1">
<li><p>From the main menu, select <strong>Files</strong>, our
<strong>Workspace</strong>, then DA261-User Content and then your user
folder. We can now select the “+” button to add a Data Action. This data
action will be used to calculate gross sales based on quantity and
price. We will then extend this data action to allocate Retail Returns
to the subregions of the United States based on our calculated Gross
Sales values.</p></li>
</ol>
<p><img src="./images/ex2/image14.png"
style="width:6.5in;height:3.00556in" /></p>
<ol start="18" type="1">
<li><p>Enter a name like “Calculate_Sales_&amp;_Returns” and select the
Sales Model from the model folder within our workspace. This is the same
sales model we were using when we were creating our story. When
complete, save the data action to your folder.</p></li>
</ol>
<p><img src="./images/ex2/image15.png"
style="width:6.5in;height:3.15903in" /></p>
<ol start="19" type="1">
<li><p>Validate that you are saving the data action to your user
folder.</p></li>
</ol>
<p><img src="./images/ex2/image16.png"
style="width:6.5in;height:4.60486in" /></p>
<ol start="20" type="1">
<li><p>We are going to add an advanced formulae to calculate gross sales
from quantity and price. We are going to open the content menu so we can
restrict the scope of the calculation.</p></li>
</ol>
<p><img src="./images/ex2/image17.png"
style="width:6.5in;height:4.74722in" /></p>
<ol start="21" type="1">
<li><p>However, before we restrict the context, we are going to create a
parameter to restrict the calculation to our user id.</p></li>
</ol>
<p><img src="./images/ex2/image18.png"
style="width:6.5in;height:2.43542in" /></p>
<ol start="22" type="1">
<li><p>Give your parameter a name like “User” and then make the
appropriate settings as shown. When complete save your Data Action.
Select the advanced formula item that we were starting to configure
before we created our parameter.</p></li>
</ol>
<p><img src="./images/ex2/image19.png"
style="width:6.5in;height:4.3in" /></p>
<ol start="23" type="1">
<li><p>Give the step a name like “Calculate Sales”. Next configure the
context as shown. Note that for the PLAN_CONTRIBUTOR. You will need to
select the USER parameter you have just created from the parameter list
within the selection popup. Once the context is set, we will start the
process of building a graphical calculation to calculate gross
sales.</p></li>
</ol>
<p><img src="./images/ex2/image20.png"
style="width:6.5in;height:3.34792in" /></p>
<ol start="24" type="1">
<li><p>We are going to calculate the Gross Sales Amount by taking the
price, which is stored at the Unassigned region multiplied by the sales
quantity we uploaded from our excel file.</p></li>
</ol>
<p><img src="./images/ex2/image21.png"
style="width:4.14216in;height:2.69772in" /></p>
<p>⚠️<strong>Quality Check!</strong> Please check that your advanced
formula is identical to what is shown below.</p>
<p><img src="./images/ex2/image22.png"
style="width:6.5in;height:3.17431in" /></p>
<ol start="25" type="1">
<li><p>We are now going to add an allocation step so that we can
allocate retail returns to our sub-regions (i.e. North, East, South and
West).</p></li>
</ol>
<p><img src="./images/ex2/image23.png"
style="width:4.73003in;height:1.89605in" /></p>
<ol start="26" type="1">
<li><p>Configure the allocation rules as shown and then save your rule.
In this case, we have already planned retail return values for 2024 for
the entire region, which is stored in the Unassigned region. We are
going to allocate these values by the gross sales we previously
calculated for each subregion.</p></li>
</ol>
<p><img src="./images/ex2/image24.png"
style="width:6.5in;height:4.28403in" /></p>
<ol start="27" type="1">
<li><p>We are now going to set the trace points on the data
actions.</p></li>
</ol>
<p><img src="./images/ex2/image25.png"
style="width:6.5in;height:2.68819in" /></p>
<ol start="28" type="1">
<li><p>Set the trace points as shown by selecting these areas on the
data action flow. This will allow us to see data action changes between
steps.</p></li>
</ol>
<p><img src="./images/ex2/image26.png"
style="width:6.5in;height:2.51806in" /></p>
<ol start="29" type="1">
<li><p>We can also select trace points within advanced formulas. Here we
are going to set a trace point where we are calculating gross sales.
Notice that we also see a new tracing point added on the Tracing pane on
the right side of the screen.</p></li>
</ol>
<p><img src="./images/ex2/image27.png"
style="width:6.5in;height:1.85625in" /></p>
<ol start="30" type="1">
<li><p>Please select the 2024 Plan and your User ID for the data input
parameters.</p></li>
</ol>
<p><img src="./images/ex2/image28.png"
style="width:2.50683in;height:1.39333in" /></p>
<ol start="31" type="1">
<li><p>We are now going to select the Show Table to Review the results
of the first step. Notice that our selection parameters will be shown in
the right pane for transparency.</p></li>
</ol>
<p><img src="./images/ex2/image29.png"
style="width:6.5in;height:2.96181in" /></p>
<p>⚠️<strong>Quality Check!</strong> Please check that your trace window
should be identical to what is shown below.</p>
<p><img src="./images/ex2/image30.png"
style="width:6.5in;height:2.88542in" /></p>
<ol start="32" type="1">
<li><p>As we configure the table, you may need to change the
<strong>Display Options</strong> to
<strong>Description</strong>.</p></li>
</ol>
<p><img src="./images/ex2/image31.png"
style="width:6.5in;height:2.0875in" /></p>
<ol start="33" type="1">
<li><p>Configure the table as shown. Notice that price is stored at the
unassigned region and that the Amount has not been calculated.</p></li>
</ol>
<p><img src="./images/ex2/image32.png"
style="width:6.5in;height:3.93819in" /></p>
<ol start="34" type="1">
<li><p>Select the tracing point for Calculate_Sales. Here we will see
the results tracepoint for the calculation we created in our advanced
formula. If we had multiple calculation lines in our advanced formula,
we could have set multiple trace points. Also note that we can also
explore the calculation scope for our advanced formula on the right
pane.</p></li>
</ol>
<p><img src="./images/ex2/image33.png"
style="width:6.5in;height:4.07292in" /></p>
<ol start="35" type="1">
<li><p>If you would like, you can also select values from the Watch Area
table and use the copy button to copy them to the clipboard. These
values can be then pasted into a document like Excel for further
analysis. While we are showing this capability, we have not included
exercise steps to paste these values into other documents.</p></li>
</ol>
<p><img src="./images/ex2/image34.png"
style="width:6.5in;height:3.81042in" /></p>
<ol start="36" type="1">
<li><p>Next, we are going to select the tracing steps after our
Calculate_Sales advanced formulas has executed. As we only have one
calculation in our advanced formula, the results of this table should
match the previous trace point. Notice that we do not see any values for
Retail Returns as this will be addressed in our allocation
step.</p></li>
</ol>
<p><img src="./images/ex2/image35.png"
style="width:6.5in;height:2.78333in" /></p>
<ol start="37" type="1">
<li><p>Selectin the AFTER Allocate Expected Returns, we can see that the
Retail Returns from the unassigned region (i.e. ‘#’), to each of the
subregions based on Gross Sales.</p></li>
</ol>
<p><img src="./images/ex2/image36.png"
style="width:6.5in;height:2.73681in" /></p>
<ol start="38" type="1">
<li><p>The Trace creates a private version, which can be viewed in the
story we created. Since we will not be doing anything with this this
trace version we will delete the information.</p></li>
</ol>
<p><img src="./images/ex2/image37.png"
style="width:6.5in;height:2.775in" /></p>
<p><img src="./images/ex2/image38.png"
style="width:2.76499in;height:0.51725in" /></p>
<ol start="39" type="1">
<li><p>In case you have not done so before, please <strong>Save</strong>
your data action. When we created the data action, we did it from our
personal folder we created in our workspace. As the next step, we are
going to create another <strong>Data Action</strong> to load the sales
plan into the finance plan. We will perform this step from the main menu
to initiate the build activity and then save it to our personal
folder.</p></li>
</ol>
<p><img src="./images/ex2/image39.png"
style="width:4.09386in;height:1.71627in" /></p>
<ol start="40" type="1">
<li><p>Xxxx</p></li>
</ol>
<p><img src="./images/ex2/image40.png"
style="width:2.77974in;height:2.77379in" /></p>
<ol start="41" type="1">
<li><p>Please give the data action a name like “ Cross-Model Copy Step”
and then select our Finance model from the exercise.</p></li>
</ol>
<p><img src="./images/ex2/image41.png"
style="width:4.37381in;height:1.70326in" /></p>
<ol start="42" type="1">
<li><p>We are going to save this data action to our personal folder.
Note that when creating models, stories and data/multi-actions, that
these objects can be stored within a file structure for easy
organization.</p></li>
</ol>
<p><img src="./images/ex2/image42.png"
style="width:4.06581in;height:2.86475in" /></p>
<ol start="43" type="1">
<li><p>We are going to create some parameters for the data action. This
will allow us to better control the scope of the data action.</p></li>
</ol>
<p><img src="./images/ex2/image43.png"
style="width:6.5in;height:3.10833in" /></p>
<ol start="44" type="1">
<li><p>To create a parmeter, we will give it a name, set the model to
our sales planning model (i.e. SAP_XPA_SALESPLAN_TE2023). We will then
select our dimension (i.e. PLAN_CONTRIBUTOR) and set the cardinality to
single (vs. multiple values) and the level being a leaf member. As the
sales plan for the purpose of this exercise is organized by user, this
will allow us to pass our user to the data action to restrict its
scope.</p></li>
</ol>
<p><img src="./images/ex2/image44.png"
style="width:6.5in;height:4.17292in" /></p>
<ol start="45" type="1">
<li><p>We are going to create another parameter for source version. As
we are creating a data action to copy data between models, this
parameter will be used to indicate which version we would like to copy
from the sales plan.</p></li>
</ol>
<p><img src="./images/ex2/image45.png"
style="width:6.5in;height:2.48889in" /></p>
<ol start="46" type="1">
<li><p>Please give the parameter a name, such as “SVersion” and set the
model to SAP_XPA_SALESPLAN_TE2023. We are going to assign the dimension
to Version and the cardinality to single, which means we only want to
pass a single value via this parameter. We will then enter the default
value of “2024 Plan.” Although we have set a default value, the user can
override this value when the data action is executed.</p></li>
</ol>
<p><img src="./images/ex2/image46.png"
style="width:6.5in;height:4.15903in" /></p>
<ol start="47" type="1">
<li><p>We are now going to create our <strong>cross-model copy</strong>
step to copy data from our sales plan to our finance plan.</p></li>
</ol>
<p><img src="./images/ex2/image47.png"
style="width:6.5in;height:3.07361in" /></p>
<ol start="48" type="1">
<li><p>Please give the parameter a name, such as “<strong>Sales 2
Finance</strong>” and set the model to SAP_XPA_SALESPLAN_TE2023. We are
going to assign set the filters for <strong>Version</strong> and Plan
<strong>Contributor</strong> as shown. When selecting the filter value,
you will need to select <strong>Parameters</strong> on the pane on the
left side of the popup window to select the parameters you have
previously created.</p></li>
</ol>
<p><img src="./images/ex2/image48.png"
style="width:6.5in;height:3.04375in" /></p>
<ol start="49" type="1">
<li><p>Using drag and drop, map the source dimension to the target
dimensions. Note that you will not be able to map SAP_XPA_COSTCENTER as
this dimension is not included in the finance model. We will want to
select this dimension and manually map it to the <strong>Sales &amp;
Marketing</strong> cost center.</p></li>
</ol>
<p><img src="./images/ex2/image49.png"
style="width:6.5in;height:2.91875in" /></p>
<ol start="50" type="1">
<li><p>Select the measures mapping so we can edit the mapping
rules.</p></li>
</ol>
<p><img src="./images/ex2/image50.png"
style="width:3.68427in;height:2.84547in" /></p>
<ol start="51" type="1">
<li><p>We are going to create a user defined rule to map the Amount from
the sales plan to Local Currency in our finance plan. We are also going
to set the auto-generation strategy to “<strong>Identical Names and
Compatible Types.</strong>” We could have also filtered on measures when
creating the rule to just include Quantity and Amount as well.</p></li>
</ol>
<p><img src="./images/ex2/image51.png"
style="width:6.5in;height:3.38958in" /></p>
<ol start="52" type="1">
<li><p>Now select the SAP_LOB_REGION. Here we have the issue that we
have sub-regions assigned to the United States in our sales plan that
have been aggregated to just the United States in our finance
plan.</p></li>
</ol>
<p><img src="./images/ex2/image52.png"
style="width:3.83844in;height:3.02441in" /></p>
<ol start="53" type="1">
<li><p>For the region, select “Identical names (including Ancestors)” to
map the subregions from the sales plan to the region in the finance
plan. Using this strategy, we can plan at a different level in our sales
plan than our finance plan.</p></li>
</ol>
<p><img src="./images/ex2/image53.png"
style="width:6.5in;height:4.22292in" /></p>
<ol start="54" type="1">
<li><p>If you have not already done so, please save your plan and then
select the <strong>Multi Actions</strong> from the main menu as shown.
With the multi-action, we can bind data actions that we created for our
sales and finance model into a single action we can trigger in a
story.</p></li>
</ol>
<p><img src="./images/ex2/image54.png"
style="width:6.5in;height:4.18056in" /></p>
<ol start="55" type="1">
<li><p>We are going to create a new Multi Action.</p></li>
</ol>
<p><img src="./images/ex2/image55.png"
style="width:2.23056in;height:2.0473in" /></p>
<ol start="56" type="1">
<li><p>Before we add the data actions we previously created to our
multi-action, we are going to create some parameters to orchestrate the
execution.</p></li>
</ol>
<p><img src="./images/ex2/image56.png"
style="width:4.39657in;height:1.44439in" /></p>
<ol start="57" type="1">
<li><p>We are going to create parameter called “SVersion” that will be
used transfer what source version we would like to use from our sales
plan. Please enter the values as shown below.</p></li>
</ol>
<p><img src="./images/ex2/image57.png"
style="width:3.01362in;height:6.20338in" /></p>
<ol start="58" type="1">
<li><p>We are now going to add another parameter for our userID. While
we would not normally run a data action by user id, we have added this
parameter as we have many participants running data actions for this
exercise and want to carefully limit our scope.</p></li>
</ol>
<p><img src="./images/ex2/image58.png"
style="width:5.58333in;height:3.26389in" /></p>
<ol start="59" type="1">
<li><p>Please create the parameter as shown below.</p></li>
</ol>
<p><img src="./images/ex2/image59.png"
style="width:4.33819in;height:9in" /></p>
<ol start="60" type="1">
<li><p>We are now going to create another parameter for the target
version. Note that for this exercise we could have just hard-coded these
values, but have chosen to include them as parameters to make them more
dynamic.</p></li>
</ol>
<p><img src="./images/ex2/image60.png"
style="width:5.59722in;height:5.44444in" /></p>
<ol start="61" type="1">
<li><p>Please create the version as shown below.</p></li>
</ol>
<blockquote>
<p><img src="./images/ex2/image61.png"
style="width:4.41944in;height:9in" /></p>
</blockquote>
<ol start="62" type="1">
<li><p>Select the + button and then add a <strong>Data Action
Step</strong>. This is where we will start to attach the data actions we
previously created to the multi-action.</p></li>
</ol>
<p><img src="./images/ex2/image62.png"
style="width:4.37104in;height:3.05413in" /></p>
<ol start="63" type="1">
<li><p>Select the data action that you have previously created, which
should be stored in your user folder. Please configure the parameters as
well.</p></li>
</ol>
<p><img src="./images/ex2/image63.png"
style="width:2.21849in;height:3.44914in" /></p>
<ol start="64" type="1">
<li><p>We will now add another data action to our multi action. Note
that when we create a data action, we can only assign a single model to
it. When using a multi action, we can include many data action steps to
it, which may be bound to different models. Our first data action is
bound to the sales plan, whereas our second data action will be bound to
the finance plan model.</p></li>
</ol>
<blockquote>
<p><img src="./images/ex2/image64.png"
style="width:6.5in;height:4.36667in" /></p>
</blockquote>
<ol start="65" type="1">
<li><p>Configure the data action as shown and then save the
multi-action. you will need to save the Multi Action to your personal
folder, which will be shown in the following step.</p></li>
</ol>
<p><img src="./images/ex2/image65.png"
style="width:6.5in;height:4.05764in" /></p>
<ol start="66" type="1">
<li><p>Save the Multi Action to your personal folder. Please give it a
name like “Calc_Sales_and_Aggregate”</p></li>
</ol>
<p><img src="./images/ex2/image66.png"
style="width:6.5in;height:4.59653in" /></p>
<ol start="67" type="1">
<li><p>Open your main user story that we created in the first part of
the exercise.</p></li>
</ol>
<p><img src="./images/ex2/image67.png"
style="width:6.5in;height:3.61667in" /></p>
<ol start="68" type="1">
<li><p>Navigate to the second page of the worksheet related to
<strong>Sales Plan Entry</strong> and then select the
<strong>Edit</strong> button. We need to be in edit mode to add our
newly created multi-action into our story.</p></li>
</ol>
<p><img src="./images/ex2/image68.png"
style="width:6.5in;height:3.67083in" /></p>
<ol start="69" type="1">
<li><p>Add a <strong>Multi Action Trigger</strong> as shown
below.</p></li>
</ol>
<blockquote>
<p><img src="./images/ex2/image69.png"
style="width:6.5in;height:2.25208in" /></p>
</blockquote>
<ol start="70" type="1">
<li><p>Open up the right editing pane and then select your multi action
that you have just created form your personal folder. Assign the
parameters as shown below. Press the formatting button so we can format
the trigger in the next step.</p></li>
</ol>
<p><img src="./images/ex2/image70.png"
style="width:4.69792in;height:6.03853in" /></p>
<ol start="71" type="1">
<li><p>We are now going to format the trigger. While you are free to
select any color, we have provided a hex number as well for a particular
shade of blue.</p></li>
</ol>
<p><img src="./images/ex2/image71.png"
style="width:2.69577in;height:0.95305in" /></p>
<p><img src="./images/ex2/image72.png"
style="width:1.7797in;height:4.81366in" /></p>
<ol start="72" type="1">
<li><p>Please reposition the Multi Action and then <strong>Save</strong>
your story. We will then select the <strong>View</strong> mode as we get
ready to execute the Multi Action.</p></li>
</ol>
<p><img src="./images/ex2/image73.png"
style="width:6.5in;height:2.15208in" /></p>
<p>Navigate to the Sales Plan Entry Page.</p>
<p>⚠️<strong>Quality Check!</strong> Please check that your sales story
page should be identical to what is shown below.</p>
<p><img src="./images/ex2/image74.png"
style="width:6.5in;height:3.51389in" /></p>
<ol start="73" type="1">
<li><p>Press the <strong>Multi Action</strong> button to execute it. The
prompts in this case should be 2024 Plan for both the source and target
version.</p></li>
</ol>
<p><img src="./images/ex2/image75.png"
style="width:6.5in;height:3.51389in" /></p>
<ol start="74" type="1">
<li><p>We should now see the sales plan values transferred to the
finance plan. We can expand the hierarchies to get a better sense of the
plan transfer.</p></li>
</ol>
<p><img src="./images/ex2/image76.png"
style="width:6.5in;height:3.44375in" /></p>
<h2 id="summary">Summary</h2>
<p><strong>Congratulations, you have completed Exercise 2!</strong></p>
<p><strong>You are now able to:</strong></p>
<ul>
<li><p>Create and execute data and multi-actions.</p></li>
<li><p>Perform tracking on data action steps.</p></li>
</ul>
<p>Continue to Exercise 3 - XXXXXXXXXXXX</p>