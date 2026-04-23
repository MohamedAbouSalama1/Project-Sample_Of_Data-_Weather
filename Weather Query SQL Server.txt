Select * From Cities;

Select * From Fact_Table;

Select City , Condition From Cities;

Select City , Condition From Cities 
Where City Like 'M%';

Select City , Condition From Cities 
Where Condition ='Rainy';

Select P_K , Humidity From Fact_Table;

Select Temperature ,P_K, 
Case
     When Temperature >= 25


         Then'Sunny'

     When Temperature <= 10

     Then'Cold'

  Else 'Cloudy'
  End As Measure_Tempreture

  From Fact_Table;

Select C.City , C.Condition , F.Humidity , F.Wind_Km
From Cities C Full Outer Join Fact_Table F On C.P_K =F.P_K;

 Select Max (Temperature) As Max_Temperature From  Fact_Table ;

 Select Max (Temperature) As Max_Temperature From  Fact_Table ; 

  Select C.City , F.Temperature From  Fact_Table F  
 Join  Cities C On  F.P_K = C.P_K; 

 Select P_K,Temperature ,Wind_Km ,Last_Value (Wind_Km) Over ( Order By Temperature Desc) As Last_Value
 From Fact_Table;


