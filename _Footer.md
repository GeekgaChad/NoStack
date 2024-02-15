# Event
### Main Activity
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Manages the main user interface and navigation within the app  | Profile  |
| Handles authentication and user sessions  | Content Cell  |
| Displays appropriate pages based on user roles  |  |

***
### Profile
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Contain and display a user’s personal info  | Attendee, |
| Manage profile picture upload and deletion | Organizer|
| Generate a profile picture from the profile name  | Admin |
|                                                 | UploadImages|
|                                                 | Image|

### Profile
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

### Admin
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Browse and display Profiles, Events, and Images  | Profiles, Events, and Images  |
| Remove Profiles, Events, and Images  | Profiles, Events, and Images  |

### Organizer
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Be able to generate a unique QR code for the event  | QRCodeGenerator  |
| Monitor real-time attendance through the AttendeeList  | AttendeeList  |
| Sends push notifications to all attendees through the app  | Notifications  |

### Event
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Contains information on an event (name, dates, location, description, QR code)  | Organizer, QRCodeDB  |
| Contain images for the event profile  | Image  |
| Generate a QR code or have the ability to reuse one  | QR code generator, QRCodeDB  |
| Has a unique AttendeeList  | AttendeeList  |

### QRCode
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Contains a unique QR code  | QRCodeScanner, Organizer, MainActivity  |
| Content Cell  | Content Cell  |

### QRCodeGenerator
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Generate a unique QR code for organizers  | QRCodeDB  |
| Have each QR code be connected to an event  | Events  |
| Retain previous QR codes for reuse  | QRCodeDB  |

### QRCodeScanner
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Check attendees into the event  | Attendee, QRCode  |


### QRCodeDB
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Stores a new QR code in the Firebase Firestore database | QRCodeConnector  |
| Updates QR codes in the Firebase Firestore database  | QRCodeConnector  |
| Deletes QR codes in the Firebase FIrestore database  | QRCodeConnector  |

### Profile
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

### Profile
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
