<h1><p align=center> School District Analysis</p></h1>

<h3> Background & Purpose </h3>
In this analysis data for student funding and standardized test scores is cleaned, aggregated and analyzed to provide insights about school performance trends and patterns. These insights are being used to inform discussions and strategic decisions at the school and district level. The analysis will help school board in making decisions regarding the school budgets and setting priorities. The students' record data used for this analysis is protected by the Family Educational Rights and Privacy Act (FERPA).

<h3> Resources </h3>

  - Data Source: schools_complete.csv, students_complete.csv
  - Software: Python 3.7.10, Jupyter Notebook
  
<h2><p align=center> Project Overview </p></h2>

<p>
<h3> Data Preparation </h3>
The data from students_complete.csv was cleaned and combined with schools_complete.csv to form a new clean, merged dataframe named school_data_complete_df.
The school board notified that there is an evidence on the academic dishonesty about the student records for the 9th graders at Thomas High School. Due to which, the analysis is performed again, while replacing all the 9th grader Thomas High School records with NaN and cleaning the dataset.
This dataset is then subjected to complete school district analysis consisting of following steps:
</p>


<h2> <p align=center>Analysis Overview </p></h2>


<h4> 1. District Summary:</h4>

<p align=center  >
district_summary_df
<kbd><img width="932" alt="district_summary_df" src="https://user-images.githubusercontent.com/90424752/141746940-81c5ac5a-daad-4252-8320-1c1403a323ea.png"></kbd>
</p>
Multiple columns for the district_summary_df are individually calculated and then are created into a dataframe by passing them into a dictionary, column names as keys and calculated series as columns.The district_summary_df above, displays the values before removing the 9th grader Thomas high School data. The  district_summary_df_challenge shown below displays the values after removing the fraudulent data.

<p>
After removing the data for 9th graders from Thomas high school, slight drop in Average Math Score (- 0.1% ), Percentage of students passing Math (- 0.2%) , Percentage of students passing Reading (- 0.3%) and Overall Passing percentage (- 0.1%) is observed. This is because, 9th graders from Thomas high School only made up a small fraction of the total number of students.
</p>

<p align=center>  
  district_summary_df_challenge
<kbd><img width="990" alt="district_summary_challenge" src="https://user-images.githubusercontent.com/90424752/141745457-42a8bd5a-650a-44de-bdbd-e3379a316bf9.png"></kbd>
</p>  

<p><h4>
 2. School Summary </h4>
The school summary groups all the school data for the schools and summarizes all the average scores and passing percentages for 15 schools in our dataset. Apart from the results for the Thomas High School, no difference was observed in the school summary analysis. The effects of replacing the grades for the 9th graders from Thomas High School with NaNs has been discussed in detail in the following section.
 </p>
  
  
  
  <p><h4>
  3. Thomas High School's Performance </h4>
  
 <p align=center> Old School Summary
 <kbd><img width="1481" alt="header" src="https://user-images.githubusercontent.com/90424752/142552261-d058dedb-6470-4d7c-b5f8-9c19c1912fcf.png">
 <img width="1396" alt="Old_School summary" src="https://user-images.githubusercontent.com/90424752/142529212-e45e9497-fc90-43a9-ab33-a1e6bdc06be7.png"></kbd>
  </p>
<p>The individual results for Thomas High School with all the grades included, referred to as Old School Summary can be seen in the figure above. The Revised School Summary, which excludes 9th grade results, reflects small changes in all it’s resulting averages and percentages of all the scores due to removal of adulterated scores. Average Math Score decreased by 0.067 while Average Reading score increased by 0.047. Passing Math percentage decreased by almost 0.1% , passing percentage for Reading by 0.3 % and Overall passing percentage dropped by 0.3%.</p>
<p align =center>  Revised School Summary  
   <kbd><img width="1481" alt="Screen Shot 2021-11-18 at 5 25 38 PM" src="https://user-images.githubusercontent.com/90424752/142535651-c3aca146-aab7-4b93-9ba9-7c986e1ab258.png"></kbd> </p>

<p>
  
</p>
  
  4. How replacing ninth grader scores affectes the following 4 analyses:
    
- Math and reading scores by grade
<p>Thomas High School 9th grade scores were replaced by NaN. It can be observed in the image below.
             <p align=center>
            <kbd><img width="303" alt="Screen Shot 2021-11-18 at 3 52 04 PM" src="https://user-images.githubusercontent.com/90424752/142515058-ebfd355c-2ca5-4dc3-bdd7-52237ae88acd.png"></kbd>
            <kbd><img width="303" alt="Screen Shot 2021-11-18 at 3 52 45 PM" src="https://user-images.githubusercontent.com/90424752/142515069-c263c6ce-b2a9-47ce-a0e9-859afc96c408.png"> </kbd></p>
       </p>
       
- Scores by School Spending
      
<p>The school spending summary was unaffected by the changes made as the changes were only limited to the math and reading scores. Hence the changes affected the math and reading scores and their percentages.
 <img width="833" alt="spending suammry" src="https://user-images.githubusercontent.com/90424752/142579894-cb49036c-462d-4fcc-9f3c-774cc5740ddb.png">
        </p>

 
- Scores by School Size

<p>The scores by school size metric shows higher average scores and passing percentages for small to medium sized schools. Scores and passing percentages drop significantly for large sized (2000-5000 students) schools.
             <p align=center>
            <kbd><img width="973" alt="size summary" src="https://user-images.githubusercontent.com/90424752/142583174-af1e1d70-66a1-449d-9cd7-472cba0f2f16.png">             </kbd>
       </p>
       
       
- Scores by School Type
 
<p> The school type summary compares the performance of Charter schools against the performance of District schools. It is observed that the Charter schools surpass the Districts schools in all the Average scores and percentages.Overall passing percentage of Charter schools (90%) is well above that of the District schools (54%).
            <img width="924" alt="Type summary" src="https://user-images.githubusercontent.com/90424752/142586622-414fe6c4-b5b8-4a81-9f1e-7964d2b668a2.png">
         </p>
       

<h3><p align=center> Summary </p></h3>
Replacing the reading and math scores for the ninth grade at Thomas High School with NaNs mostly affected the Thomas High School Scores in the School District Summary analysis.
The following changes can be observed after reading and math scores for the ninth grade at Thomas High School are replaced with NaNs.

- The Average Math Score for Thomas High School decreased from 83.418349 to 83.350937
- The Average Reading Score for Thomas High School went up from 83.84893 to 83.896082
- The percentage of students passing in mathematics decreased by 0.1% from 93.272 to 93.185 and percentages of students passing in reading decreased by 0.3%
- The overall passing percentage was affected by almost 0.3% as well, going down to 90.63 from 90.94
- Since the proportion of the dishonest data with the entire data in this dataset is very small i.e. about 1%, the average scores and percentages resulting after removal of dishonest data are affected by a very small amount.
