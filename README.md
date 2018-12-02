# Train-Scheduler
https://byronthe123.github.io/Train-Scheduler/
Problem: Need a way to determine when trains are supposed to be arriving based on a set schedue.

Assumptions: Trains arrive on time (this obviously means this app can't be used in NY unless delays can be accounted for).

Solution: A program that allows users to input the first train arrival time and the frequency of that train's arrivals.  The app/program will be able to calculate all subsequent arrival times fromt this information. 

Requirement: Use Firebase to store Train arrival and frequeny information.

My Implementation: I used a form to capture Train data including Name, Destination, First Train time and Frequency. I built a Train class which is used to create Train objects from the data retrieved from the from for each train. Each Train object is stored in Firebase as a train record. At startup, the information for each train record is passed into a function that takes the train's name, destination, first arrival train, and frequency and creates a schedule for each train showing the next arrival time and minutes away. This data is refreshed every 30 seconds automatically. Users can also delete train recrods - this was accomplished by using the train's ID (set as a property for each train object) to delete the record from Firebase.
