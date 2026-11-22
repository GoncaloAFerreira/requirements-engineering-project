# 1. Problem, Stakeholders and Goals

## 1.1 Background and current situation
The community organization currently manages the sports pitches, halls, courts and activity facilities, Currently the bookings are handled through phone calls, emails, spreadsheets and calendars.

The main difficulties with the current approach are conflicting bookings, difficulty checking availability, cancellations, no-shows, staff spending time answering booking queries, difficulty keeping information up to date, different rules for each facility, protecting user information and accessibility and usability concerns.

These problems affect the community members and athletes using the activity booking system, as well as parents or any users with disabilities or accessibility needs or older adults who may experience difficulties using digital systems.

Others that are affected are the staff managing the system, such as IT specialists, front-desk staff or coaches, instructors & referees.
The organisation is considering a software system to improve the booking process.

One thing to consider that the stakeholder mentioned above such as IT specialists, parents, coaches, instructors and referees are potential stakeholders and not confirmed in the scenario.

## 1.2 Problem statement and goals

The current system has a lot of flaws such as: 

1. **Conflicting bookings**
   - The system shouldn’t allow the users to double-book and not allow closing times, for example one booking ends at 3pm and you can book one for 2pm onwards.
2. **Availability**
   - The system should allow the users to be able to check the dates and time for when the booking is available.
3. **Staff workload**
   - The system needs to reduce the current manual administration and allow a less prone method for difficult keeping information up to date
4. **Accessibility**
   - The system might be hard for people with disabilities or older adults so it might be good to access that problem using a simpler design and more straight forward way
5. **User Information**
   - The current system is concerned about user information so the system should be able to use a good encryption method to keep every information hard to get and also hidden from the normal user

## 1.3 Stakeholders, needs and proposed elicitation

| Stakeholder / role | Need or concern | Evidence / source |
| --- | --- | --- |
| Facility users | Booking and availability | Scenario C, difficulty checking availability and conflicting bookings |
| IT support | System maintenance and security | Scenario C, protect user data although the IT support is assumed and needs confirmation |
| Sports clubs and teams | Group bookings and recurring activities | Scenario C, Investigate question regarding individual and group booking. |
| Booking Staff | Managing bookings, reducing manual administration and handling cancellations. | Scenario C, Staff are spending time answering booking queries and difficulty keeping information up to date |
| Facility Managers | Managing facility specific rules, resolving booking conflicts and overseeing facility usage | Scenario C, different facilities having different rules but the manager responsibilities needs confirmation |
| Users with accessibility needs | Being able to navigate the system and make bookings without any troubles | Scenario C, Accessibility and usability concerns |

### Proposed elicitation techniques

The suitable techniques I would use to investigate stakeholder’s needs are:

1. Interviews which allow us to understand the stakeholder needs and business rules.
2. Questionnaires which are great to gather information from a larger number of users.
3. Prototyping/Wireframe which allows us to investigate usability and missing requirements.

### Elicitation questions

The two important questions I would ask are:

1. Should normal users and sports clubs follow the same booking rules?
   - Stakeholder to ask: Manager.

2. What difficulties do users experience with the current process?
   - Facility users.

## 1.4 Scope and system boundary

### In Scope

The proposed system will focus on:

| Capability | Reason to include it |
| --- | --- |
| Viewing sports and activity facilities | Helps users identify suitable facilities |
| Checking availability | Scenario shows difficulties finding available dates and times. |
| Making facility bookings | Supports the main purpose of the system. |
| Preventing conflicting bookings | Addressing the existing double-booking problem |
| Managing cancellations and booking changes | Scenario shows difficulties with booking changes. |
| Staff booking management | Reduces manual administration. |
| Managing facility-specific rules | Different facilities might have different booking rules |
| Protection of user data | Scenario enquires security and privacy concerns |
| Accessible user interface | Scenario talks about accessibility and usability concerns |

### Out of Scope

To keep the system focused on facility booking, these will be excluded:

| Capability | Reason for exclusion |
| --- | --- |
| Online payments | Payment processing is not talked in the scenario |
| Physical facility maintenance | The system focuses on managing bookings than maintaining the actual facility |
| Sports team management | The system is not responsible for managing players or teams |
| Tournament organisation | Organisition competitions is not the same as the facility booking |
| Equipment rental | The scenario is focused in booking facilities than equipment |

### Constraints

The system needs to run with these following constraints:

1. **Facility specific rules**
   - Different facilities might have different booking rules, although the specific restrictions are currently unknown and need clarification from the manager.

2. **Facility availability**
   - Bookings need to respect existing bookings and operating hours, because there are complains about conflict with bookings.

3. **Security and privacy**
   - User information must be protected from unauthorized access, it was mentioned in the scenario that the security was a concern.

4. **Accessibility and usability**
   - Users with different abilities and levels of technical experience needs to be considered, the specific type of users and level of technical experience was not specified so it needs clarification.

5. **Booking policies**
   - Consider the restrictions regarding eligibility, cancellations and advance bookings but these policies are currently unknown and needs clarification.

## 1.5 Assumptions, Candidate Requirements and Open Questions

| ID | Type | Description | Evidence/Status | Action Needed |
| --- | --- | --- | --- | --- |
| A01 | Assumption | Each booking involves one facility | Not confirmed | Clarify with facility manager |
| A02 | Assumption | Different permissions for staff and facility users | Not confirmed | Clarify with staff responsibilities and permissions |
| A03 | Assumption | Consecutive bookings without a time gap | Not confirmed | Confirm where preparation time is required |
| CR01 | Candidate requirement | Booking confirmation messages | Proposed feature | Check whether the users need confirmation messages |
| CR02 | Candidate requirement | User registration and accounts | Proposed feature | Confirm where registration is necessary |
| CR03 | Candidate requirement | Bookings reminders | Proposed feature | Investigate if reminders would reduce no-shows |
| Q01 | Open question | How far in advance can facilities be booked? | No rule supplied | Confirm advance booking policy |
| Q02 | Open question | What happens when a user cancels a booking? | No rule supplied | Confirm cancellation policy |
| Q03 | Open question | What happens when a user doesn’t attend a booking | No rule supplied | Clarify no show policy |
| Q04 | Open question | Can staff override existing bookings? | No rule supplied | Confirm staff authority |
| Q05 | Open question | What personal information is needed when making | No rule supplied | Check booking information and privacy needs |
