Identify the missing values
Count missing values in each column -=COUNTIF(C2:C1001,"~?")
Fill missing months with September - =IF(B2="?","Sep",B2)
Fill missing years with the rounded average - =ROUND(AVERAGE(C2:C1001),0)
Title, First Name, and Last Name - =TEXTBEFORE(A2," "),=TEXTBEFORE(TEXTAFTER(A2," ")," ") , =TEXTAFTER(A2," ",-1)
=IF(LOWER(TRIM(F2))="yes","Yes",IF(LOWER(TRIM(F2))="no","No",IF(F2="?","Unknown","Review")))
Weight Status column using BMI - =IF(C2="?","Unknown",IFERROR(IF(VALUE(C2)<18.5,"Underweight",IF(VALUE(C2)<25,"Normal Weight",IF(VALUE(C2)<30,"Overweight","Obesity"))),"Review"))
Diabetes Status column using HbA1C - =IF(D2="?","Unknown",IFERROR(IF(VALUE(D2)<5.7,"Normal",IF(VALUE(D2)<6.5,"Prediabetes","Diabetes")),"Review"))
Combine year, month, and date into Date of Birth - =DATE(VALUE(B2),MONTH(DATEVALUE("1 "&C2&" 2000")),VALUE(D2))
=DATEDIF(E2,DATE(2023,6,8),"Y")
VLOOKUP -=IFERROR(VLOOKUP($A2,'Customer Names'!$A$2:$C$1001,3,FALSE),"Not Found")
Distribution of cancer history among smokers and non-smokers
Creating pivot tables, chart 
Dashboard
Slicers
