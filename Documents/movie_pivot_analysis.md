# **🎬 Movie Data Analysis: Advanced Pivot Table Scenarios**
Live Project Data: [Click here to view the interactive Google Sheet with live Pivot Tables]([https://docs.google.com/spreadsheets/d/1uBqGbriOBlDUUKthA4EML3s1cHAwzyp8_KDC9CCQMDk/edit?usp=sharing])

**The Scenario:** You are an analyst for a movie studio. The executives have handed you a raw dataset of 1,000 movies. The columns are: Movie Title, Genre, Release Year, Budget, and Box Office Revenue.

They have three specific business questions they want answered before their next board meeting.

## Question 1:  "Which genre is the most reliably profitable? Don't just show us total revenue; we want to see the AVERAGE revenue per movie for each genre."

*The Challenge:* By default, pivot tables want to SUM (add up) all the numbers. Action movies might have the highest total revenue just because there are so many of them, but we need the average.
_______________________
### **The Pivot Table Solution:**

**Rows:** Drag Genre here.

**Values:** Drag Box Office Revenue here.

**The "Continued" Trick:** Click on the Revenue value in that bucket and select Value Field Settings. Change the calculation from SUM to AVERAGE.

**Final Polish:** Sort the results from Largest to Smallest to easily see the winner.

## Question 2: "What is the actual Profit for these genres? We only have columns for Budget and Revenue."

*The Challenge:* You need a new data point (Profit), but you don't want to mess up your raw data tab by typing hundreds of new =Revenue - Budget formulas in a new column.
___________________________
### The Pivot Table Solution:

**Rows:** Drag Genre here.

**The "Continued" Trick (Calculated Fields):** Go to the Pivot Table menu ribbon at the top of your screen. Look for Fields, Items, & Sets -> Calculated Field.

**The Formula:** Name your new field "Net Profit". In the formula bar, tell the pivot table to subtract the two existing columns: = 'Box Office Revenue' - 'Budget'.

**Result:** The pivot table instantly generates a brand-new "Profit" column inside your summary table without ever touching your raw data.

## Question 3: "Sci-Fi movies make a lot of money, but what percentage of our TOTAL market pie do they actually represent?"

*The Challenge:* The executives don't want to see raw dollar amounts (like $5,000,000,000). They want to see percentages (like 25% of all revenue).
___________________________
### The Pivot Table Solution:

**Rows:** Drag Genre here.

**Values:** Drag Box Office Revenue here.

**The "Continued" Trick (Show Values As):** Click on the Revenue value again and go to Value Field Settings. This time, click the tab that says Show Values As.

**The Selection:** Change it from "No Calculation" to % of Grand Total.

**Result:** The pivot table automatically turns all those giant dollar amounts into clean percentages that total exactly 100% at the bottom.
