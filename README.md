# Power-BI-ch-5-practice-Exercise

It contain both Traning exercise and practice excercise

## Chapter 5
In table
#gdb041 fact sales monthly [date]
     Is it sort out only date column 
List max (#gdb041 Fact Sales monthly" [date]) 
    It sort only max value in column 
# Finding Forecast 
Click on Column it shows
    = Table.Select Rows (source, each([date], #datetime (2017,9,1,0,0,0))) 
            Then Change into Table Select Rows (source, each ([date]> Last sales month))
# Append Face Sales and Remaining Forecast

In Fact_Actual_Estimate 
              Lacks several column according to data so manually add those
--> Fiscal_year Date year (Date Addmonth ([date] 4)) 
# Merge
gross price & Fact_actual_estimate using left Join
gross_Sales_amount [gross Price]* Qty 
Need pre-invoice 
# Merge
-->fact_actual_estimates &  Pre_Invoice_deduction

--> Pre_Invoice_discount_amt = [gross_sales_Amount]*[pre_invoice_deduction]

--> Net_invoice_amount = [gross_Sales_Amount] * [Pre_Invoice_discount_amt]

## key points
--> Having a correct understanding of business time intelligence concepts such as YTD (Year To Date), YTG (Year To Go), LE (Landing Estimates) can help you tremendously in the data analysis job.
--> Power Query has a convenient option to allow the merging of two tables.
--> Few best practices in Power Query
--> Giving meaningful query step names help everyone
--> Tables should be grouped in logical categories
--> Disabling the load of tables that are not going to be used outside helps with performance
--> Use consistent naming conventions for tables and measures

# power query best practices

  Naming qyery steps
  Grouping Tables
  Disable load for tables that will not ysed outside
  Keep table names minimized
