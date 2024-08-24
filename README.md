# Dax = Intelligent-function
##https://app.powerbi.com/reportEmbed?reportId=26b1aef2-5f73-41a3-a3b3-96ca455b62fe&autoAuth=true&ctid=59b97b95-46c2-4b4b-8f1e-16a856dc6629

![time iteligent function](https://github.com/user-attachments/assets/e95e2c3b-3d7e-46ec-a91a-f277ccd6273f)

![choclate image](https://github.com/user-attachments/assets/eb6f7dd2-0959-4a46-9d77-e33e25c19dcb)

###Time_Intelligent Function Dax 
MTD / QTD / YTD 
=calculate([ Expression , datesMTD / DatesQTD / DatesYTD , calender dates , month / Quater / Year ])

Previous Last Month / last Quater / Last Year 
=calculate ([ Expression, parallelperiods ,claenderdates -1 month / quater / year ])

diff = current - previous 

% = divide ( diff , previous )


# Calculation Group 
GO in Model View and select calculation group and allow the pop-up as Yes 
then 

create measure as Name Current = selectedmeasure

then go and rename the calculation group to easy identify it

and aslo rename the calculation collumn 

then select the item group and create more measure 

MTD = calculate (selectedmeasure , datesMTD )

QTD = calculate (selectedmeasure ,datesQTD)

YTD = calculate (selectedmeasure , datesYTD)

Previous Year = calculate (selectedmeasure ,sameperiodlastyear ,dates)


YOY % = 
       var cv = slelectedmeasure 
       var pv = calculate (selectedmeasure ,sameperiodlastyear ,dates)
       var diff = cv - pv 
       return 
       divide = diff,pv 


       then add this with matrix visual and select the expression like profit , sales , cost , discount etc .
       aside add this calculation group with the same in visual 
       and to make dynamic the matrix 
       make parameter for the expression of sales, profit , cost 
       at the end the result will apper as dyanamic .

