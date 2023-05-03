Download Link: https://assignmentchef.com/product/solved-cs385-week-3-assignment-task-scheduling
<br>
<h1>Problem Description</h1>

Suppose that you are scheduling a room. You are given a group of activities each of which has a start and stop time. Two activities are compatible if they do not overlap (one activity finishes before another one starts). For example, in the following activities, activity A is compatible with activities B and D but not activity C:




<table width="212">

 <tbody>

  <tr>

   <td width="61"><strong>Activity </strong></td>

   <td width="77"><strong>Start Time </strong></td>

   <td width="73"><strong>Stop time </strong></td>

  </tr>

  <tr>

   <td width="61"><strong>A </strong></td>

   <td width="77"><strong>1 </strong></td>

   <td width="73"><strong>2 </strong></td>

  </tr>

  <tr>

   <td width="61"><strong>B </strong></td>

   <td width="77"><strong>2 </strong></td>

   <td width="73"><strong>5 </strong></td>

  </tr>

  <tr>

   <td width="61"><strong>C </strong></td>

   <td width="77"><strong>1 </strong></td>

   <td width="73"><strong>3 </strong></td>

  </tr>

  <tr>

   <td width="61"><strong>D </strong></td>

   <td width="77"><strong>5 </strong></td>

   <td width="73"><strong>6 </strong></td>

  </tr>

 </tbody>

</table>










The room has a start time and an end time in which it is available.

Your goal is to write a recursive method to schedule compatible activities that result in the maximum usage of the room.  The usage of the room is defined as the total duration of the scheduled activities, that is, the sum of (stop time – start time) for all the activities scheduled to run in the room.

For example suppose that the start time and end time in which the room is available is [1,7] for the above table. Hence, the possible schedules are:

<ol>

 <li>Activities A, B,D: with room usage = (2-1)+(5-2) +(6-5) = 5</li>

 <li>Activities C, D: with room usage = (3-1)+(6-5) = 2</li>

 <li>Activities A,D: with room usage (5-2)+(6-5) =4</li>

 <li>Activities A, B: with room usage (2-1)+(5-2)= 4</li>

 <li>Activities B, D: with room usage (5-2)+(6-5) = 4</li>

</ol>

Therefore, the set of activities {A,B,D}  gives the optimal schedule with the maximum room usage.

What you need to do:

<strong>1-</strong><strong> Create a class Activitiy.java </strong>with three data fields : activityName, startTime, and stopTime .

Create accessor (get)  and mutator (set) methods  for each data field.<strong> 2-</strong><strong> Create a class Scheduling.java </strong> with the following method in it:




public Activity[] <u>getOptimalSchedule( </u><u>int</u><u> roomStartTime, </u><u>int</u><u> roomEndtime,</u> <u>Activity[] activities)</u>




This method gets the availability span of the room as well as a set of activities to choose from and returns an optimal schedule i.e.,  a selected set of non-overlapping activities that can be scheduled to run in the room and gives the maximum possible usage of the room.  Note, depending on your input,  the correct answer may not be unique (that is, there might be several valid schedules with the same total room usage)

<strong>Note: </strong>it is important that your getOptimalSchedule method has the signature above for ease of testing and grading.  <u>Also you can use any additional utility methods in your classes as long as you provide</u> <u>comments explaining what each utility method does.</u>

What you need to turn in:

You need to submit your two java files : <strong>Activity.java </strong>and <strong>Scheduling.java   </strong>

<strong>Attention: </strong> To get a full credit, your algorithm must be recursive.

Grading Rubric:

<table width="638">

 <tbody>

  <tr>

   <td width="319"><strong>Criteria </strong></td>

   <td width="319"><strong>Points </strong></td>

  </tr>

  <tr>

   <td width="319">The Activity.java class is correctly written with correct data fields and accessor and mutatormethods</td>

   <td width="319">5 pts<strong> </strong></td>

  </tr>

  <tr>

   <td width="319"> getOptimalSchedule correctly returns an optimal schedule with maximum room usage</td>

   <td width="319">10 pts </td>

  </tr>

  <tr>

   <td width="319">getOptimalSchedule has a correct base  case  and terminates without error</td>

   <td width="319">5pt</td>

  </tr>

  <tr>

   <td width="319">getOptimalSchedule has correct recursive calls</td>

   <td width="319">10 pts</td>

  </tr>

 </tbody>

</table>




Hint:

Consider two recursive cases 1- The first activity is not included in the final optimal schedule, and 2- the first activity is included in the final optimal schedule. Solve the problem recursively for each of these two cases to get the optimal schedule for each case and compare their room usages. The final answer will be the optimal schedule of the case with the higher room usage. Please refer to the practice problem 4 in module 3 lectures for an example of a problem with a similar recursive logic.


