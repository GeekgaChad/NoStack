# CRC Cards
### Main Activity
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Manages the main user interface and navigation within the app  | Profile  |
| Handles authentication and user sessions  | LogIn  |
| Displays appropriate pages based on user roles  | Organizer Pages  |
|  | Admin Pages  |
|  | Attendee Pages  |

### LogIn
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Display a login form to users  | MainActivity  |
| Accept user credentials  | Organizer  |
| Validate user input   | Attendee  |
| Redirect authenticated users to the appropriate page based on their role  | Admin  |

***

### Profile
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Contain and display a user’s personal info  | Attendee, |
| Manage profile picture upload and deletion | Organizer|
| Generate a profile picture from the profile name  | Admin |
|                                                 | ManageImages|
|                                                 | Images|

***

### Admin
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Browse and display Profiles, Events, and Images  | Profile  |
| Remove Profiles, Events, and Images  | Event  |
|  | Images  |
***

### Attendee
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Scan the QR code using the QRcode scanner  | QRCodeScanner  |
| Be able to edit profile  | Profile  |
| Receive Notifications  | AttendeeList  |
| Register for events | Event  |
|  | Announcements  |

### AttendeeList
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Shows a list of checked in attendees  | Attendee  |
| Shows the amount of time an attendee has checked in  | QRCodeScanner  |
| Shows where the attendees are checking in from  | AttendeeList  |

### AttendeeListDB
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Stores a new Attendee in the Firebase Firestore database  | AttendeeListConnector  |
| Updates Attendee in the Firebase Firestore database  |   |
| Deletes Attendee in the Firebase FIrestore database  |  |

### AttendeeListDBConnector
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Connects to the AttendeeList Firebase Firestore database  | QRAttendeeListDB  |

***

### Organizer
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Be able to generate a unique QR code for the event  | QRCodeGenerator  |
| Monitor real-time attendance through the AttendeeList  | AttendeeList  |
| Sends push notifications to all attendees through the app  | Announcements  |

### Event
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Contains information on an event (name, dates, location, description, QR code)  | Organizer  |
| Display event poster  | QRCodeDB  |
| Contain images for the event profile  | Images  |
| Generate a QR code or have the ability to reuse one  | QRCodeGenerator  |
| Has a unique AttendeeList  | AttendeeList  |
| Optionally set limit for number of attendees that can sign up  |   |


### Milestones
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Notify organizer about milestone reached | Organizer  |
| Set milestones  | Announcements  |
| Contain all milestones  |   |

***

### QRCode
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Contains a unique QR code  | QRCodeScanner  |
|  | Organizer  |
|  | MainActivity  |

### QRCodeGenerator
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Generate a unique QR code for organizers  | QRCodeDB  |
| Have each QR code be connected to an event  | Events  |
| Retain previous QR codes for reuse  |   |

### QRCodeScanner
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Check attendees into the event  | Attendee  |
|  | QRCode  |


### QRCodeDB
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Stores a new QR code in the Firebase Firestore database | QRCodeConnector  |
| Updates QR codes in the Firebase Firestore database  |   |
| Deletes QR codes in the Firebase Firestore database  |   |

### QRCodeConnector
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Connects to the Firebase Firestore database  | QRcodeDB  |

***

### Images
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Hold image data  | ManageImages  |
|  | Attendee  |
|  | Event  |
|  | Organizer  |

### ManageImages
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Upload images  | Image  |
| Delete any images uploaded to the app  | Event  |
| View images / display images on profiles or events  | Profile  |

***

### Maps
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Display geographical information of attendees and events  | Attendee  |
| Be able to be enabled or disabled  | Event  |
|  | Organizer  |

### Announcements
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Sends notifications to attendees   | AttendeeList  |
| Manages organizer interaction to edit/delete notification  | Organizer  |
| Manages attendee interaction to to ignore, or view notification in app  | Attendee  |


