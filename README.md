Soft_Engineering_Project
========================

Project for Software Engineering, shared between Jane Valenti, Dan Dunning, and Bob Dayton.


Online Scheduling System for Spa/Salon

Project Description

All businesses are charged with two major tasks: providing quality service in their respective industry, and 
advertising themselves as a means of securing future clients.  In the modern era, both of these tasks are 
accomplished through the use of up-to-date, customized technology.  Every business needs to have management 
software that allows them to keep track of their employees and clients, and they also must have a presence on 
the Internet that allows them to reach the attentions of more customers.

For this project, our group will be building software that fulfills both of these needs.  We will create management 
software for a mock spa and salon based in the Baltimore area.  The software’s primary purposes are to manage client 
and employee schedules and advertise the business on the Web.  The specifics of the web design will be determined as 
the project progresses, but we already know that the web page will include several features.  First, it will have an 
inviting and engaging homepage that catches the immediate attentions of prospective clients.  The homepage will 
contain links detailing the services that the spa/salon provides (hair, nail, and makeup design, as well as spa 
treatments such as massages and facials), and each service will include the price associated with it.  Also on the 
homepage will be a link containing the biographies of each cosmetologist employed.  The biography will include a brief 
description of the cosmetologist’s background, experience, and which services they provide.

Another feature of the webpage will be a way for both employees and clients to “login” to the system.  Each employee 
and client will have their own unique account, and if a new client does not have an account, then there will be a way 
for them to register with the site.  A client also has the option of using the system as a “guest,” in case they want 
to use it to make appointments but do not want their information stored in the system.  When registering the client 
can enter any information that they wish to enter, such as their address, although the only piece of required 
information will be a phone number that can be used to contact them.  All clients, registered or not, are required to 
enter a phone number, and there will be a checkbox for them to say whether their phone number is a cell phone number 
or a landline number.  When a client logs in, they will be able to make online appointments for any services they wish.  
There are a couple of ways they will be able to do this.  First, they may search for a particular cosmetologist that 
they may have seen in the past and view that cosmetologist’s availability.  If the cosmetologist has an open time slot, 
the client may make an appointment within that time slot.  If a client does not have a particular cosmetologist in mind, 
then they can search using the type of service for which they wish to make an appointment and, optionally, whatever 
particular time slot they have in mind.  The system will return names of stylists available that provide that service 
and are available during that period of time.

Given these capabilities, the system must have built in constraints that would never allow the clients to perform certain
tasks.  For example, a customer may try to book an appointment with a cosmetologist when the cosmetologist already has a 
client in that time slot.  The system will be able to recognize that the time slot has been taken prior to the client 
attempting to make a reservation. On a similar note, the system must know exactly how much time a particular type of 
appointment takes—a manicure may take only 30 minutes, while a complicated hairstyle make take 2 hours.  When a client 
books an appointment, the system must know this duration in order to block off the correct period of time.  Also, each 
cosmetologist performs certain services but not others; a hair stylist most likely does not do massages.  The system must
also keep track of this, so a client would never be able to make an appointment with a cosmetologist for a service that 
the cosmetologist does not perform.

As mentioned before, employees will also have an account that they use to login to the system.  Employees, once logged 
in, can perform several functions.  The system will allow the employee to view their schedule for the weeks that the 
schedule has been created.  Employees will be able to schedule any days off they may wish to have, schedule appointments 
for clients, and confirm upcoming client appointments.  Also, it was mentioned earlier that employees have a personal 
biography included on the web page.  Employees may alter their own biography at any time, possibly updating the services 
they provide or mentioning if they have received any new certifications.

Like with clients, the system must have built in constraints that recognize potential errors that employees make.  The 
system will not allow the cosmetologist to create an appointment for services that they do not offer.  Employees are only
allowed to update their own biography page; as the system will not allow them access to other employee’s pages.

There will also be an “extended” employee account that is reserved for managers.  The system will know based on an 
employee’s login information whether the employee is entitled to the special privileges given to managers.  Managers can 
do everything employees can do, but with a few additions.  A manager is the only one who can change the schedules of all 
the employees; so, if an employee calls in sick, the manager is the one who shuffles that employee’s schedule and assigns
his or her appointments to another cosmetologist.  A manager is also capable of approving days off requested by employees
(the day off is blocked off from new appointments only after the manager has approved the request).  The manager can add,
delete, or modify the biographical pages of any and all employees, and can add, delete, and manage clients in the system 
as well.

The constraints for managers mostly reflect how the system must be able to discern between regular employees and 
managers.  The system will distinguish the level of access between managers and employees and only allow the manager 
accounts to access the manager privileges.  Also, as was mentioned before, all clients, registered or not, are required 
to give a contact phone number before making any appointments.  If the phone number is listed as a cell phone number, 
then the customer will be notified of any changes (i.e., if the manager or an employee needs to cancel an appointment) 
via an e-mail sent to their phone.  If the phone number is a landline phone number, then the customer will be added to a 
“Call” list.  These customers will be contacted by an employee of the spa/salon who will tell them their appointment 
needs to be rescheduled.  Only managers can access the “Call” list, and only they can remove people from the list (which 
they will do once the person has been called).  

Technical Specifications

As for the technical specifications of this project, the software will be web-based and will be written primarily in 
PHP/CSS driven by a MySQL database.  We plan to use Xampp/Wampp for code development and database management.

User Stories

For describing the user stories of all potential users of this system, the “As who, I want what, so that why” format was 
used.

Client

1.     As a client, I want to be able to register with the system so that I can use it to make appointments.
2.     As a client, I want to be able to reset my password so that if I forget my original password I can still use the 
      system.
3.     As a client, I want to be able to make appointments online so that I don’t have to call.
4.     As a client, I want to be able to view the employees of the spa/salon so that I can pick the best one for my 
      desired service.
5.     As a client, I want to be able to view the schedule of my desired cosmetologist so that I can schedule an 
      appointment whenever he/she is not busy.
6.     As a client, I want to be able to view all available cosmetologists at a particular time so that I can pick one 
      for my desired time slot and service.
7.     As a client, I want the option of making appointments without registering so that I don’t have to have my 
      information stored by the system if I do not want it stored.
8.     As a client, I want to be able to view my past appointments, so that I can track my spending as well as know what 
      I have had done recently.
9.     As a client, I want to be notified of any changes to my appointment, so I can decide if I want to reschedule it 
      or not.
10.   As a client, I want to be able to cancel my appointment so that I can let the employee know that they now have a 
      free timeslot.
11.   As a client, I want to be able to make appointments without registering, so that I can still use the system without
      divulging any details I do not wish to share.

Employee

1.     As an employee, I want to be able to login to the system so that I can view my relevant information.
2.     As an employee, I want to be able to see my appointments for the day so that I know my schedule and when I am 
      free or not free.
3.     As an employee, I want to be able to confirm appointment times so that I can know my schedule and/or shuffle 
      appointments around if I need to.
4.     As an employee, I want to be able to view and potentially change my personal biographical page so that clients 
      know what services I provide.
5.     As an employee, I want to be able to request days off, so that I can take personal time when I wish.
6.    As an employee, I want to be able to cancel appointments I have in case something comes up, so that my clients are 
      informed and not upset.

Manager

1.     As a manager, I want to be able to add, delete, or modify client information so that the system reflects the most 
      up to date client data.
2.     As a manager, I want to be able to add, delete, or modify employee information so that the system reflects the 
      most up to date employee data.
3.     As a manager, I want to be able to award requested days off the employees so that they can take personal time as 
      they wish, provided that the requested days do not contain any previously scheduled appointments.
4.     As a manager, I want to be able to modify the schedule of any employee in case of illness or unforeseen 
      circumstances so that appointments are still honored, even if they’re not with the originally scheduled
      cosmetologist.
5.    As a manager, I want to be able to cancel any appointment, so that an employee that was unable to make it to work 
      can still have their appointments cancelled.
6.    As a manager, I want to be able to access the “Call” list, so that I can contact clients and inform them of any 
      changes to the schedule, such as an employee cancellation.




  
