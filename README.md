# sales-dashbord
Week 3: Sales Data Analysis in Power BI



Download Power BI here
After installing on your local computer, open Power BI. 


Now it is time to begin our Analysis.

Under the Home tab, click on Get Data
Go to Excel Workbook. A new window will pop out for you to select your data.


Upload the data provided you and check locations, people, products and sales as shown in the picture below.


Since our data is cleaned and is in the format that we want, there is no need to transform data. Click on Load at the bottom of the window.
We return back to our Canvas. Next, we want to create a data model between the tables.
Go to the left side and click on the third icon as shown in the picture below.


The data model view opens. You see that Power BI automatically connects people and products table to your sales table.
In your locations table, drag Geo onto Geography in the sales table to create a relationship between the two table.


We have created a star schema where our sales is the fact table and the other tables are the dimension tables.
Go back to the report view i.e. The first icon on top of the model view icon.


1.Visualize Sales by location

Click on Stacked- Bar Chart
Drag Geo under location table to the X-axis
Drag Amount under the sales table to the Y-axis




2.What is the company’s Total Sales?

Go to the sales table on the left side of the canvas
Right click on Amount and select New measure
Type the formula Total Sales = sum(sales [Amount]) and hit enter


A new measure with name Total sales is created.




3.What is our Total Cost as a company?

We don’t have the cost column in our tables, so we have to create a new column for our cost.
Go to the data view. The second icon under the report view at the far right of the canvas.
Go to Table tools at the top and click on New Column.


Type the formula Cost = sales[Boxes] * RELATED(products [Cost per box])


Hit Enter and return to the report view.
Now repeat the steps you used to create the Total Sales measure and create Total Cost. The formula for this is Total Cost = sum(sales[Cost]).
4.What is the company’s Total Profit?

Again, create a New measure and name it Total Profit
Type the formula Total Profit = [Total Sales] – [Total Cost] 
Create a New measure and name it Profit%. To calculate our Profit%, we divide Total Profit over Total Sales.
Type Profit% = divide ([Total Profit], [Total Sales])


5.Has the Company met its Profit target?

Create a New measure and label it Profit Target
Type the formula Profit Target Achieved? = if([Profit%] > 0.5, “Yes”, “No”)


Time to start putting them all together on our canvas 😊

Go under Visualizations and select cards
Drag Total Cost and place in the fields box


Go to Format Visual, the icon beside Build Visual under the Visualization pane.
Click on General and change the Background color. (Choose any color of your choice).
Turn on Shadow to give shadow effect to our card.
Click on the Total Cost card and press CTRL + C. Paste the visual by pressing CTRL + V in the canvas. Do those four times and align the cards as shown in the picture below.


In the second card, change the field value from Total Cost to Total Sales.
For the third, change to Total Profit and the fourth to Profit%




Now, we want to add currency sign to our values.

Click on the Total Cost measure on the right pane 
Go to Format and change General to Currency


Do same for the Total Sales and Total Profit Cards
Go to the Callout value and change the Font size to 50. Make it bold.
Do same for the remainder of the cards.




We want to see the trends of each metric over the months.

Click on an Area Chart under the Visualization pane.
Drag the Month column under the Date Hierarchy to the X-axis and drag the Total Cost to the Y-axis.


Do same for the rest of the cards. (Tip: You can use the copy and paste trick)










We want to see the performance of the Salespersons 

Click on Table under the Visualization pane
Add Salesperson, Total Profit, Profit% and Profit Target Acchieved? To the Values column
Add a conditional bar to the Total Profit column.
Go to Total Profit under the Values pane and click on the drop down.
Click on Conditional formatting and then Data bars.


We want to see performance of our products.

Repeat same steps for that of Salespersons




Now bring back Sales per Country



Change the Geo to Country. To change the name, right click on the X-axis where you dropped the Geo data and select Rename Visual.
Change the title of the chart to Total Sales by Country
Add on more card and display the total number of Customers


Now we want to add title to our dashboard

Type a title of your choice. I am going for Sales Dashboard Analysis


Format the background color and style the font. Be creative😉






Now we want to slice or filter our visuals 

Add a slicer visual to the canvas and drag Teams under the people table to its values.


Highlight the slicer chart and go to Format Visual, Visual and change the orientation from vertical to horizontal.
Change the background to suit that of title background i.e. Dark Blue
Press CTRL and left click on cards and area charts.
Right-click and group
Go to the insert bar and add a shape. Select rectangle and extend the shape to cover the cards and area charts.
Change the background color of the rectangle to white and go to format and send backwards



You should end up with an output like this or even better. Be creative with your formatting.










Share your Dashboard

Log in with your azubi email by clicking on sign in at the top right corner


On the Home tab, click on publish and publish to your workspace.


Go to Power BI service and log in with your azubi email to view your dashboard and share to people as well.
