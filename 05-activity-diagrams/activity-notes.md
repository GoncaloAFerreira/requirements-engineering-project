# Week 5 — Activity Diagram
## 1. Process Modelled
This model is the Create Equipment Booking process for the College Equipment booking system. it shows how the user selects equipment, check its availability and submits bookings.
## 2. Purpose
The purpose of this Activity Diagram is to show the steps and decisions for when a user wants to book equipment and it also helps us understand how the process over all works. It shows what happens at each stage and where more information is needed.
## 3. Activities
The diagram has the following activities.
1. Select equipment - The user selects the equipment
2. Select Date - User chooses the date they want the equipment
3. Check Availability - the system checks when the selected equipment is available
4. Enter Booking Details - If it is available, the user is prompted to enter the required booking information
5. Submit Booking - The user submits the booking.
6. Booking Recorded - The booking is recorded by the system.

This are what the diagram follows in order.
## 4. Decision and Guards
The diagram contains a decision called "Equipment available" it has two possible possibilities:

1. Available - when the user can continue with the booking
2. Not available - when the user can't continue with the booking because it doesn't hit the requirements
## 5. Unknowns
One important unknown is what happens when the requested equipment is not available

The requirements doesn't explain when the user should another date, select different equipment or just unable to continue with the booking.

One other question is when a recording booking means it has been approved or the staff needs to review it first.
## 6. Stakeholder Question
Stakeholder: Equipment Manager or Technician

Question: What needs to happen when a student tries to book an equipment that is already booked.

This question should help understand the process and see if additional activities is required.
## 7. Modelling Decision
I choosed to represent the unavailable equipment as an UNKNOWN because the specifications doesnt specify what should happen.

So instead of assuming that the system would offer another date, I left this part unresolved.
## 8. Reflection
Creating this diagram hel+ed me understand the difference between UCM and an Activity Diagram.
