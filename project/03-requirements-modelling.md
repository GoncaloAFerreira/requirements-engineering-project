# 3 Requirements modelling


# 3.1 Use Case Diagram

![UC-D01 — Use Case Diagram](<images/UC-D01.drawio.png>)


# 3.2 One Use Case Narrative

## Use case / ID

Use case: UC01 — ID: FR02 Make Booking

## Primary actor / goal

Primary Actor: Facility user, the person attempting to reserve a facility / Goal: Successfully reserve an available sports facility for a selected date and time

## Preconditions / trigger

Preconditions: The user must be an authorised user to make a booking. Trigger: The facility user chooses to begin a new booking.

## Main successful flow

1. Facility User: Begins the process of making a new booking (FR02)
2. Facility User: Chooses a facility, date and time (FR02)
3. System: Checks the availability for that facility and period also checking existing bookings (FR01, FR03)
4. System: Reviews if the requested booking follows the facility specific rules (FR11)
5. System: Shows the booking details for the user to view. (FR02)
6. Facility User: Submits the booking requests with the information that is required (FR02)
7. System: Checks the submission and records the booking making sure there is no conflict or rule violation. (FR02, FR03, FR11)
8. System: Displays the booking outcome and allows the user to know if the reservation was made (FR02)

## Alternative / exception flows

### 3a – facility unavailable (FR03)

- If the facility is already booked for the selected date and time the system will inform that specific date and time is not available and the user can then book for
- another date and time and no booking record is created of this unfinished booking

### 4a - Facility restriction (FR11)

- If the requested booking does not follow the facility specific rules the system will inform the user that the request doesn’t meet with that specific facility rules. The
- booking will only continue if the user adjusts their booking to follow the specific rules or cancel the attempt. No invalid booking is created

### 7a – Booking Submission timeout (NFR06)

- If the booking submission times out, the system will inform the user that the booking status needs to be checked again and the user should only retry when the system
- determines if the booking was successfully recorded or not before allowing another submission. This prevents creating a duplicate booking

## Outcome / postconditions

**Successful Outcome:** The booking is created for the selected facility, date and time and that period is no longer available so there are no conflicting reservations.

**Unsuccessful outcome:** No new booking is created if the request fails the required checks or the user abandons it. A timeout must be resolved before the attempt is 
treated as failed.

## Related requirements

1. FR01 – checks facility availability
2. FR02 – allows the users make bookings
3. FR03 – Prevents overlapping bookings
4. FR11 Checks facility-specific booking restrictions.
5. NFR06 Handles submission timeouts and prevents bookings being duplicated


# 3.3 Activity Diagram

![AD01 — Activity Diagram](<images/Activity Diagram (AD01).png>)

# 3.4 Conceptual UML Class Diagram

![CD01 - Conceptual Class Diagram](<images/CD01 - Conceptual Class Diagram.drawio.png>)

| Association / feature | Requirement evidence | Open question / assumption |
|---|---|---|
| Facility – Booking | FR02, FR03, A01 | Does the booking involve more than one facility? |
| FacilityUser - Booking | FR02, FR05 | Can multiple users join in the same booking? |
| Facility – FacilityRule | FR11 | Can the same rule be used in several facilities? |
| Facility - UnavailablePeriod | FR01, FR10 | When the facility closes does it apply to multiple facilities at the same time? |
| FacilityUser attributes | NFR02, Q05 | What personal information is required to create and manage bookings. |

## 3.5 Model consistency check

Explain how your models agree with your written requirements. Identify important inconsistencies, missing information or new requirements questions discovered through modelling.
While making my UML models, I checked if they were consistent with the requirements catalogue and if they were true to them.

The Use Case Diagram (UC-D01) represents the two actors which are facility user and booking staff and represented their responsibilities and how different they are, for example how the facility user can check 
availability and modify own booking while Booking staff can modify an existing booking and manage the availability.

References for UC-D01 are FR01, FR06, FR09, FR10

The Use Case Narrative (UC01) and the Activity Diagram (AD01) both represent the process on how the booking is done, while the Use Case Narrative explains how a user makes the booking and includes the successful steps 
and alternative situations the Activity Diagram is a visual representation of that but includes the availability checks the facility restrictions and the timeout handling.

References for UC01 and AD01 are FR01, FR02, FR03, FR11, NFR06

The Conceptual Class Diagram (CD01) shows the important domain concepts and what their attributes and relationships are which contains the Facility, Booking, FacilityUser and their relationship is That FacilityUser can 
have 0 or many Booking but each booking can only have one FacilityUser, the Booking can have only one facility but the facility can have 0 or many bookings which supports my booking requirements.

There are also two other classes which support the requirements FR10 and FR11, they are UnavailablePeriod and FacilityRule, these two classes support the facility availability management and facility specific 
restrictions that was talked before

References for CD01 FR02, FR05, FR07, FR10, FR11

While developing my UML models I also identified that there was some issues and missing information that required clarification, for example:

While making my Activity Diagram (AD01) I realized that when checking for availability only once could allow for a user to reserve a facility between the initial availability check and the final submission, so I added a 
second check that helps prevent that overlapping booking.

Another issue that I discovered was related to NFR06 which is about Timeout Handling and I figured out that a booking could have been recorded when a timeout occurs because I had initially that the user can retry 
without checking the status of the booking which could duplicate the booking which would be a bad thing because the requirements need no double booking.

While making my Conceptual Class Diagram (CD01) I made assumptions about the relationship for example how each booking belongs to a Facility and one FacilityUser but a FacilityUser can have multiple bookings and the 
Facility can have multiple bookings, these are assumptions and they helped me establish the relationship but they require confirmation because multiple facilities or booking ownership might be allowed.

One other remaining inconsistency between UC01 and AD01 is that UC01 allows a user to abandon the booking attempt if it violates a facility-specific rule but in my AD01 they would be automatically returned to the 
facility selection. This is a remaining inconsistency that needs to be reviewed later.
