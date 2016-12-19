# Basic Employee List

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/mjd/employees && cd $_
```

## Instructions

### Employees

Create a two-level prototype chain for creating employees in your business. Start off with an `Employee` function. Then create two other functions named `Clinician`, and `Operations` that have `Employee` on their prototype chain.

### Departments

Create a two-level prototype chain for creating departments in your business. Start off with a `Department` function. Then create two other functions named `FieldOffice`, and `Headquarters` that have `Department` on their prototype chain.

### Requirements

1. Every employee should have a first and last name.
1. Every department should have a name.
1. Every employee should be assigned to either the `FieldOffice` or `Headquarters` department. This is a `has-a` relationship.
1. `Clinician` employees should have a property for their area of medical expertise (e.g. physical therapist, phrenologist, anesthesiologist, etc.)
1. `Operations` employees should have a property for their area of responsibility (e.g. IT, revenue, compliance, etc.)
1. Every field office should have a unique city.
1. Create a minimum of 4 employees - 2 clinicians, and 2 operations - that have been assigned to a specific department.
1. Output the following information to the console for each employee.
    1. Full name
    1. Department name
    1. Expertise/responsibility

##### sample output

```js
Deborah Harris works as a clinician, in the Baltimore field office, and is a phrenologist.
Michael Slazinski works in operations, in headquarters, and is responsible for compliance.
Margaret Johnson works as a clinician, in the Indianapolis field office, and is a physical therapist.
```

