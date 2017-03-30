# Doctors and Patients

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/modern-framework/doctor-patients && cd $_
```

> Ensure you have Angular, ng-route, and the Firebase libraries installed and linked in your HTML file.

## Requirements

For this project, you must use Angular and Firebase. You will be creating a basic application that lists all of the doctors in a medical practice, and then provide a link that shows all the patients for a doctor.

### Doctors View

This view will simply list all doctors contained in a Firebase collection. Each object in the collection will have the following properties.

1. Doctor first name
1. Doctor last name
1. Doctor speciality

In the list show the doctor's full name and the speciality. The doctor's full name should be a hyperlink that, when clicked, will load the patient list for that doctor.

### Patient List

This view will list all of the patients that are assigned to the doctor. Each object in the patient collection will have the following properties.

1. Patient first name
1. Patient last name
1. Patient ailment

Provide an affordance to show the list of doctors.

### Data Relationship

Since this application does not have forms for creating doctors and patients, create a JSON file locally that you will upload to Firebase.

> Sample format

```js
{
    "doctors": [
        "killigrew": {
            "first_name": "Johan",
            "last_name": "Killigrew",
            "speciality": "Pediatrics"
        }
    ],
    "patients": [
        "svenson": {
            "first_name": "Margot",
            "last_name": "Svenson",
            "ailment": "Arthritis",
            "doctor_id": "killigrew"
        }
    ]
}
```

1. Create a new Firebase application
1. Upload your JSON file into the new application
1. Use the Firebase REST API to query the list of doctors.
1. Use the Firebase REST API to query the list of patients for each doctor using the `orderby` and `equalto` URL parameters.
