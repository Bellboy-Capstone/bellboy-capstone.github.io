*Bellboy* is a system designed for contactless interaction with public buttons. After being installed above door, elevator, and service buttons, it will enable the general public to 'press' these buttons through hover, voice, and frequent user identification interactions. This website stores the master copy of the project description and goals, and links to programs and work related to the project. The project code is divided into two repositories: embedded **System** code and the **Services** the Bellboy devices rely on.

Designed and implemented by Elma Khandaker, Sein Izumita, Shriya Gundala, Yusra Adinoyi, and Ryan Fleck. [Contact us.](#contact)

<br />

# System

![CI](https://github.com/Bellboy-Capstone/System/workflows/CI/badge.svg)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/4150c01ff4e54051a6d930103ea02747)](https://www.codacy.com/gh/Bellboy-Capstone/System/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Bellboy-Capstone/System&amp;utm_campaign=Badge_Grade)

The **System** repo stored at [/Bellboy-Capstone/System](https://github.com/Bellboy-Capstone/System) contains the embedded python program that runs on the Bellboy prototype hardware.  [_Read more here._](https://github.com/Bellboy-Capstone/System#system)

<br />

# Services

![CI](https://github.com/Bellboy-Capstone/Services/workflows/CI/badge.svg)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/8fb53c0f016b46889a92c8bc37d26bbe)](https://www.codacy.com/gh/Bellboy-Capstone/Services/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Bellboy-Capstone/Services&amp;utm_campaign=Badge_Grade)

The **Services** repo stored at [/Bellboy-Capstone/Services](https://github.com/Bellboy-Capstone/Services) contains the Django-based web application to support the Bellboy systems. [_Read more here._](https://github.com/Bellboy-Capstone/Services#services)

<br />

# Project Proposal

The *Bellboy* project aims to create a contactless switch-actuation system that will augment existing public buttons for opening doors, calling elevators, activating lights, and crossing streets. Using a Rasperry Pi, cameras, ultrasonic distance sensors, and LEDs for output, the system will enable users to hover their finger, speak, or stand by the switch and be recognized to activate their target button.

## Problem Statement

Every day, millions of public buttons are used by members of the general public.
Most of these inputs on doors, elevators, and walls rely on mechanical buttons for user input, which must be directly and physically actuated in order to convey the user’s intentions.
Additionally, these buttons may be difficult for those hard of sight or physically disabled to use.
How could we replace these interactions, removing a potential vector for disease transmission, while also increasing accessibility?

We need to provide a system where existing buttons can be pressed without physical contact between the button and the public user.
Let’s design a system that can fit above already-installed public switches, and trigger them when requested by public users.
People should be able to use this system without touching it, so we can use a variety of input methods to allow them to activate the buttons. This will make opening doors, selecting your elevator floor, and using other public controls much more sanitary.

## Solution

The Unit must:

1. Enable all users to select the floor they would like to travel to using contactless input methods
1. Be easy to integrate with existing public systems, without obstructing the current door/elevator panel/button interface

To achieve these goals, Bellboy will include:

1. Point-to-open hand recognition, where users may hover their finger above the button they wish to open, whereafter Bellboy will trigger the button for them.
1. Vocal command recognition, where users may speak the unit number (if many units are nearby) and a command like open, close, or a floor number.
1. Frequent user recognition, using facial recognition paired with nearby bluetooth radio IDs, to allow the system to predict and proactively repeat a users’ previous actions.

In addition, Bellboy will use the aforementioned features to provide:

1. Command-and-monitor system, where security personnel can utilize the built-in cameras to view and provide assistance to persons utilizing Bellboy.
1. User guidance system, where users may speak the location they would like to go, and Bellboy units on the premises will be able to recognize the user at each intersection and provide the next direction for them.

Both of these features will be provided by an enterprise-grade backend, as users are tracked, data is processed, and results are returned to our web GUI.


## Requirements

This set of requirements will be met by the *Bellboy* system and services.

### System: Physical Bellboy Device

1. Be configurable to allow a technician to calibrate it for these parameters:
    1. Organization of buttons below the switch, the button names, and keyword triggers.
    1. The location of the unit within a building
1. Recognize user input from a variety of methods:
    1. Voice commands indicating a button, direction, or location in the building to travel to.
    1. Hand gestures pointing at the physical buttons below the device.
    1. The face of the user as a method of repeating a common action or providing directions.
1. Provide feedback to the user, visually and audibly, to:
    1. Confirm with the user that their intended action is about to, or is, being carried out.
    1. Provide the user with navigation information or confirm a repeated action or voice command.

### Services: Backend

1. Collect data:
    1. Collect information from each Bellboy unit, when doors are activated, on nearby people, bluetooth radio IDs, and data associated with the method used to open the door.
1. Facilitate the connection between web client and Bellboy units:
    1. Allow the web GUI to see all connected Bellboy units.
    1. Provide STUN/TURN services for the frontend to begin a WebRTC session with the Bellboy in order to provide audio/video to security staff, enabling staff to provide assistance to Bellboy users.
1. Provide simplified commands based on data insights to Bellboy units:
    1. Actions to take when visited by a given user

### Services: Frontend

1. Provide a set of information to security personnel:
    1. Frequent accesses, including associated information about frequent users.
    1. The state of all switches, and whether the nearby door has been used recently.
1. Enable security personnel to interact with the Bellboy units:
    1. Provide a method of viewing the world through the Bellboy’s front-facing camera
    1. Provide a method of listening and speaking through Bellboy’s audio equipment


## Personal & Professional Expectations

Our group aims to successfully develop a touchless public interface for our current world alied by the ultra-scary COVID-19/SARS-2 virus.

We will also be doing research into which designs and functions would best suit the ideas we are planning to implement and consulting different literatures to support our design choices. Making sure that our design is intuitive and accessible is crucial so that end users are able to use it with ease. We will be learning how to interface our sensors with the raspberry pi and how to use the data we get from it to produce an output in our website dashboard. We want to be able to work efficiently in a group by setting deadlines and managing time. Lastly, we plan to make our design fun for ourselves as well as our end users.


## BOM: Bill of Materials

| ID | Description                           | Final Cost | Link | 
|----|---------------------------------------|------------|------|
| 1  | Raspberry Pi 3                        | $100 CAD   | Link | 
| 2  | 32GB MicroSD Card                     | $35 CAD    | Link | 
| 3  | Description                           | Final Cost | Link | 
| 4  | Description                           | Final Cost | Link | 

## Contact

For any questions about the project, please contact the group members with the information below.

| Name     | GitHub      | Email Address      |
|----------|-------------|--------------------|
| Ryan Fleck | [@RyanFleck](https://github.com/ryanfleck) | [rflec028@uottawa.ca](mailto:rflec028@uottawa.ca) |
| Shriya Gundala | [@gshriya](https://github.com/gshriya) | [sgund051@uottawa.ca](mailto:sgund051@uottawa.ca) |
| Yusra Adinoyi| [@yozohu](https://github.com/yozohu) |  [xxxxx@uottawa.ca](mailto:xxxxx@uottawa.ca) |
| Elma Khandaker | [@elmakhandaker](https://github.com/elmakhandaker) | [ekhan029@uottawa.ca](mailto:ekhan029@uottawa.ca) |
| Sein Izumita | [@seinizumita](https://github.com/seinizumita) | [sizum075@uottawa.ca](mailto:sizum075@uottawa.ca) |



<br />

<br />

<hr />

<br />

<br />


![Bellboy Logo](/assets/img/bellboy.png)


<br />

<br />

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
