Download Link: https://assignmentchef.com/product/solved-csci251-assignment3-stl-containers-iterators-and-generic-algorithm
<br>
This assignment aims to provide you with some experience in writing codes using C++ programming language that covers the following topics

 STL Containers, Iterators, and Generic Algorithm

<table width="732">

 <tbody>

  <tr>

   <td width="732"><strong> </strong><strong>Remember that: </strong><strong>1.         </strong><strong>All programs should be able to run on the lab’s computers. </strong><strong>2.         </strong><strong>You must put the following information on the header of each text and source file you will be submitting in this assignment:  </strong><strong>     Student’s full name:   </strong><strong>     Student’s ID:   </strong><strong>     Modification Date:  </strong><strong>     Purpose of this file (or program):   </strong><strong>3.         </strong><strong>Assignments that are not able to be compiled will result in zero mark given to the assignment. </strong><strong>4.         </strong><strong>You must only use the C++ features that have already been covered in the lectures </strong><strong> </strong></td>

  </tr>

 </tbody>

</table>




<strong>TASKS: </strong>

For this task, you are required to write a program using STL to simulate the process of managing sports facility available at a sport center. A sport center may provide a variety of sport facility such as futsal court, badminton court, softball batting cages, etc. The sport center may have more than one place for each sport facility. Each member who would like to use the facility at the sport center will have to register for booking. A facility can be assigned to the member upon availability of the facility. Assignment is done on a first come first serve basis.




Design and implement a class called SportFacility. Each object from this class should keep the information of the facility number/id (this could represent the court number or batting cage number), the description (such as “Futsal Court”, “Badminton Court”, etc), the capacity (how many member can use the facility at a time), an indicator to mark whether the facility is occupied or not, a duration (number of hours the court is occupied), the start time (the starting time for the facility to be occupied), and rental fee for the facility.

Use the STL multiset to keep the SportFacility objects that are sorted according to the description. You will need to implement a suitable function object to describe how to order the SportFacility objects. At the start of the program, populate the set using data read from a text file. Design a suitable file format for this purpose.

Next, design and implement a Member class holding data that represents the name and id number of a member of the sport center. When a member arrives to book a facility a new object from this class should be instantiated and push into a STL Adapter class queue. Each member will be assigned to a facility of their choice on a first come first serve basis. You may need to create multiple queues for different types of facility available at the sport center. Think of how this can be done.

Lastly, create a STL map container that will be used to keep the records of booking. The Member object should be the key and the SportFacility id should be the value stored in each pair of the map items. A map item will be added when a booking is made and removed when the facility is no longer used by the member.

Use a menu driven program to simulate the arrival of members, booking of sport facility, and leaving the sport facility. When a member arrives, dynamically create a member object and push it to the queue containing the members waiting to book a facility.

When booking a sport facility, search for the sport facility record in the STL multiset and if the facility is not occupied remove the member’s record from the queue and add a new booking record to the STL map. There may be multiple instances of the same type of facility. Your program should be able to check all facility of the same type before indicating that the facility is not available.

When a member leaves the sport facility, the related object should be updated to indicate it is now no longer occupied and remove the record from the STL map. In addition to that, your program should also instantly check the queue if there are any member waiting to use the facility. If there are, perform the booking operation for this member.

Additional functions such as displaying all available sport facility and all occupied sport facility should be implemented. Think of suitable operators to be overloaded for your classes to allow operations to be performed correctly when you store your objects in the STL containers.


