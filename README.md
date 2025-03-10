 REPORTS USING SET INTERACTIONS BETWEEN VISUALS, HIERARCHIES AND 
DRILLDOWN



Dashboard Link :https://app.powerbi.com/groups/me/reports/867f607a-5158-4fdf-ab31-b78311f18920/2b5b83ed2cda7d8cba6f?experience=power-bi



Procedure:
1.	Importing the Dataset:
	Launch Power BI Desktop.
	Click on "Get Data" in the Home tab of the ribbon.
	Select the appropriate data source option "Excel” and follow the prompts to import your sample dataset into Power BI.


2.	Insert Rectangle Shape:





	Click on “Format tab” on right side and perform changes on visual.
	Shape > Style > #E66C37
	Shape > Text >Text = “Sales report” , Font Size = 46, Horizontal Alignment = “Center”.



3.	Create a Slicer:
	Visualizations > Build Visual > Slicer
	Visualizations > Build Visual > Field = “Location”
	Visualizations >Format Visuals> Title> Font Size =14
	Visualizations >Format Visuals> Effects> Background Color = #9B0065
	Visualizations >Format Visuals> Effects> Height= 79
	Visualizations >Format Visuals> Effects> Width = 582


4.	Add Card with Current Date:
	With the card visualization selected, locate the "Fields" pane on the right-hand side.
	Right-click anywhere in the "Fields" pane and select "New Measure" from the contextmenu. This will open the formula bar at the top.
	In the formula bar, enter the following DAX formula to create a measure that calculatesthe current date:
	CurrentDate = Now()
	Press Enter to apply the formula.
	Visualization >Format Visual > General > Effects > Background Color : #F18F49
	Visualization > Format Visual >Visual > Category Label > Font Size = 12


5.	Create Stacked Bar Chart:
	Visualizations >Build Visuals >Fields > Y –Axis =”Category Name Hierarchy”
	Visualizations >Build Visuals >Fields > X-Axis =”Sum of Selling Price”
	Visualizations >Format Visuals> Y-axis> Values >Color = #5F6B6D
	Visualizations >Format Visuals> Y-axis> Values >Title >Color = #374649
	Visualizations >Format Visuals> X-axis> Values >Color = #5F6B6D
	Visualizations >Format Visuals> X-axis> Values >Title >Color = #374649
	Visualizations >Format Visuals> Bar> Show All
	Visualizations >Format Visuals> Bar> Accessories> Color = #374649
	Visualizations >Format Visuals> Bar>Formal>color = #D2B04C
	Visualizations >Format Visuals> Bar> SemiFormal> Color = #00ACFC
	Visualizations >Format Visuals> Bar> Casual Wear> Color = #C83D95
	Visualizations >Format Visuals> Data Labels > Options> Inside Center
	Visualizations >Format Visuals> Data Labels> Values > Font Size = 18
	Visualizations >Format Visuals> Title> Text =”Sum of selling Price By Category Name”
	Visualizations >Format Visuals> Title> Font Size =24
	Visualizations >Format Visuals> Effects> Background Color = #F1792


6.	Create Stacked Column Chart:

	Visualizations >Build Visuals >Fields > Y –Axis =”selling price”
	Visualizations >Build Visuals >Fields > X-Axis =”Month”
	Visualizations >Format Visuals> Y-axis> Values >Color = #374649
	Visualizations >Format Visuals> Y-axis> Values >Title >Color = #5F6B6D
 

	Visualizations >Format Visuals> X-axis> Values >Color = #374649
	Visualizations >Format Visuals> X-axis> Values >Title >Color = #5F6B6D
	Visualizations >Format Visuals> Bar> Show All
	Visualizations >Format Visuals> Data Labels > Options> Inside Center
	Visualizations >Format Visuals> Data Labels> Values > Font Size = 14
	Visualizations >Format Visuals> Title> Text =”total selling price by month”
	Visualizations >Format Visuals> Title> Font Size =20
	Visualizations >Format Visuals> Effects> Background Color = #5C2D91


7.	Create a Card to display Selling Price:

	With the card visualization selected, locate the "Fields" pane on the right-hand side.
	Right-click anywhere in the "Fields" pane and select "New Measure" from the contextmenu. This will open the formula bar at the top.
	In the formula bar, enter the following DAX formula to create a measure that calculatesthe total selling price:
o total selling price = SUMX(Data,Data[Selling price]*Data[Item quantity])
	Drag “Total Selling Price” to “Fields”.
	Visualization >Format Visual > General > Effects > Background Color : #5B2D71
	Visualization > Format Visual >Visual > Category Label > Font Size = 20


8.	Create a Card to display Total Item Count:

	With the card visualization selected, locate the "Fields" pane on the right-hand side.
	Right-click anywhere in the "Fields" pane and select "New Measure" from the
 

contextmenu. This will open the formula bar at the top.
	Drag “Total Item Count” to “Fields”.
	In the formula bar, enter the following formula to create a measure that calculates the total item count:
o total item count = countx(data,Data[Item quantity])
	Visualization >Format Visual > General > Effects > Background Color : #AF916D
	Visualization > Format Visual >Visual > Category Label > Font Size = 20


9.	Create a Card to display Profit:

	With the card visualization selected, locate the "Fields" pane on the right-hand side.
	Right-click anywhere in the "Fields" pane and select "New Measure" from the contextmenu. This will open the formula bar at the top.
	Drag “profit” to “Fields”.
	In the formula bar, enter the following formula to create a measure that calculates the profit:
o profit = Data[total selling price]-[total cost price]
	Visualization >Format Visual > General > Effects > Background Color :#5C0001
	Visualization > Format Visual >Visual > Category Label > Font Size = 20


10.	Create a Card to display Profit %:

	With the card visualization selected, locate the "Fields" pane on the right-hand side.
	Right-click anywhere in the "Fields" pane and select "New Measure" from the contextmenu. This will open the formula bar at the top.
	Drag “profit %” to “Fields”.
	In the formula bar, enter the following formula to create a measure that calculates the profit%:
o %Profit = (Data[profit]/Data[total cost price])*100
	Visualization >Format Visual > General > Effects > Background Color : #F8BCBD
 

	Visualization > Format Visual >Visual > Category Label > Font Size = 20



11.	Create Stacked Bar Chart:

	Visualizations >Build Visuals >Fields > Y –Axis =”Category Name”
	Visualizations >Build Visuals >Fields > X-Axis =”Profit”
	Visualizations >Format Visuals> Y-axis> Values >Color = #5F6B6D
	Visualizations >Format Visuals> Y-axis> Values >Title >Color = #374649
	Visualizations >Format Visuals> X-axis> Values >Color = #5F6B6D
	Visualizations >Format Visuals> X-axis> Values >Title >Color = #374649
	Visualizations >Format Visuals> Bar> Show All
	Visualizations >Format Visuals> Bar> Accessories> Color = # F18F49
	Visualizations >Format Visuals> Bar>Formal>color = # F18F49
	Visualizations >Format Visuals> Bar> SemiFormal> Color = # F18F49
	Visualizations >Format Visuals> Bar> Casual Wear> Color = # F18F49
	Visualizations >Format Visuals> Data Labels > Options> Inside Center
	Visualizations >Format Visuals> Data Labels> Values > Font Size = 18
	Visualizations >Format Visuals> Title> Text =”Profit By Category Name”
	Visualizations >Format Visuals> Title> Font Size =18
	Visualizations >Format Visuals> Effects> Background Color = #008cEEE

12.	Create Donut Chart:

	Visualizations >Build Visuals >Fields > Legend=”Location”
	Visualizations >Build Visuals >Fields > Values=”Sum of Item Count”
	Visualizations >Format Visuals> Legend> slices >Color =”374649”
	Visualizations >Format Visuals> Values >Color = #5F6B6D
	Visualizations >Format Visuals> Legend> slices>Chennai >Color = #1DD5EE
	Visualizations >Format Visuals> Legend> slices>Banglore >Color = #5C2D91
	Visualizations >Format Visuals> Legend> slices >Hyderabad>Color = #F18F49
	Visualizations >Format Visuals> Bar> Show All
	Visualizations >Format Visuals> Data Labels > Options> Inside Center
	Visualizations >Format Visuals> Data Labels> Values > Font Size = 14
	Visualizations >Format Visuals> Title> Text =”Sum of Item amount by Location”
	Visualizations >Format Visuals> Title> Font Size =18
	Visualizations >Format Visuals> Effects> Background Color = #EF008C


13.	Create Pie-Chart:

	Visualizations >Build Visuals >Fields > Legend=”Ordertype Name”
	Visualizations >Build Visuals >Fields > Values=”Sum of Item quantity”
	Visualizations >Format Visuals> Legend> slices >Color = #374649
	Visualizations >Format Visuals> Values >Color = #374649
	Visualizations >Format Visuals> Legend> slices>on line>Color = #FE6D86
	Visualizations >Format Visuals> Legend> slices>On Shop >Color = #F18F49
	Visualizations >Format Visuals> Bar> Show All
	Visualizations >Format Visuals> Data Labels > Options> Inside Center
 

	Visualizations >Format Visuals> Data Labels> Values > Font Size = 14
	Visualizations >Format Visuals> Title> Text =”Sum of Item quantiy by ordertype name”
	Visualizations >Format Visuals> Title> Font Size =16
	Visualizations >Format Visuals> Effects> Background Color = #FFD86C


14.	Create a Filter to clear Button:
	Insert > Shapes > Select “Rectangle Shape”
	Visualizations > Format > Shape > Text > “ON” > Text = “Clear”
	Visualizations > Format > Shape > Action > “ON”
	Now make all visuals to initial state the follow next step
	View > BookMark > Add BookMark =”Clear”
	Visualizations > Format > Shape > Action > Select = “BookMark”
	Visualizations > Format> Shape > Action > BookMark =”Clear”

15.	Creating Hierarchy for drill down and drill up operations:
	Data > Category Name > Create hierarchy
	Data > Item Name > Add to hierarchy
 

	Place cursor on visual > Click “  “ to drill down
	Place cursor on visual > Click “  “ to drill next level of hierarachy


 
16. Final Output


![Image](https://github.com/user-attachments/assets/96fa2f5a-6339-4e07-88c3-bd64d12ca535)
