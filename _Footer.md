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


### Admin
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Browse and display Profiles, Events, and Images  | Profile  |
|  | Event  |
|  | Image  |
| Remove Profiles, Events, and Images  | Profile  |
|  | Event  |
|  | Image  |

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
| Contains a unique QR code  | QRCodeScanner  |
|  | Organizer  |
|  | MainActivity  |

### QRCodeGenerator
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Generate a unique QR code for organizers  | QRCodeDB  |
| Have each QR code be connected to an event  | Events  |
| Retain previous QR codes for reuse  | QRCodeDB  |

### QRCodeScanner
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Check attendees into the event  | Attendee  |
|  | QRCode  |



### QRCodeDB
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Stores a new QR code in the Firebase Firestore database | QRCodeConnector  |
| Updates QR codes in the Firebase Firestore database  | QRCodeConnector  |
| Deletes QR codes in the Firebase Firestore database  | QRCodeConnector  |

### QRCodeConnector
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Connects to the Firebase Firestore database  | QRcodeDB  |

### ManageImages
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Upload images  | UploadImage  |
|  | Image  |
| Delete any images uploaded to the app  | Image  |
| View images / display images on profiles or events  | Profile  |
|  | Event  |
|  | Image  |

### Images
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Hold image data  | UploadImage  |
|  | Attendee  |
|  | Event  |
|  | Organizer  |

### Maps
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Display geographical information of attendees and events  | Attendee  |
|  | Event  |
|  | Organizer  |
| Be able to be enabled or disabled  |   |

### Notifications
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Sends notifications to attendees   | AttendeeList  |
| Manages organizer interaction to edit/delete notification  | Organizer  |
| Manages attendee interaction to to ignore, or view notification in app  | Attendee  |

### LogIn
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Display a login form to users  | MainActivity  |
| Accept user credentials  | Organizer  |
|  | Attendee  |
| Validate user input   |   |
| Redirect authenticated users to the appropriate page based on their role  | Admin  |

### AttendeeListDB
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Stores a new Attendee in the Firebase Firestore database  | AttendeeListConnector  |
| Updates Attendee in the Firebase Firestore database  | AttendeeListConnector  |
| Deletes Attendee in the Firebase FIrestore database  | AttendeeListConnector  |

### AttendeeListDBConnector
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Connects to the AttendeeList Firebase Firestore database  | QRAttendeeListDB  |

### Profile
| Responsibilities | Collaborators |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |