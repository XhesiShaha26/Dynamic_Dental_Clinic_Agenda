# Dynamic_Dental_Clinic_Agenda_System
Appointment Class
The Appointment class represents a single appointment in the dental clinic system. It has several private members that store the details of the appointment and public methods for interacting with these details:

Private Members:

patientName: Stores the name of the patient.
appointmentType: Describes the type of appointment (e.g., checkup, cleaning).
description: A brief description of the appointment.
startTime and endTime: std::tm structures that store the start and end times of the appointment.
Constructor: Initializes an appointment with all necessary details.

conflictsWith() Method:

This method checks if there is a time conflict between this appointment and another one. It returns true if there is an overlap in time, which helps prevent scheduling conflicts.
print() Method:

Formats and prints the details of the appointment, including start and end times, using the std::strftime function to convert std::tm time structures to readable strings.
Schedule Class
The Schedule class manages a collection of appointments:

Private Members:

appointments: A vector that stores multiple instances of the Appointment class.
addAppointment() Method:

Takes an Appointment object as an argument and checks it against all existing appointments for conflicts. If no conflicts are found, the appointment is added to the appointments vector and returns true; otherwise, it returns false.
deleteAppointment() Method:

Removes an appointment from the schedule based on the patient's name and the start time. It iterates through the appointments vector, finds a matching appointment, and removes it.
printSchedule() Method:

Prints all scheduled appointments by calling the print() method of each Appointment in the appointments vector. If no appointments are scheduled, it outputs a message indicating so.
Main Program
The main function provides a simple text-based user interface for interacting with the schedule system. Here's what each part does:

While Loop: The main loop that keeps the program running until the user chooses to exit.

Menu System:

The user is presented with options to add an appointment, delete an appointment, show all appointments, or exit the program.
Based on the user's input, the program executes the corresponding function:
Add Appointment: Prompts the user to enter the details of a new appointment, creates an Appointment object, and attempts to add it to the schedule.
Delete Appointment: Prompts for the details needed to identify an appointment and attempts to delete it.
Show All Appointments: Calls printSchedule() to display all current appointments.
Exit: Sets the running flag to false, which exits the loop and ends the program.
