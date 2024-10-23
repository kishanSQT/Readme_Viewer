### Machine Overview
- Machine Name: HiltonGuestSummary
- Title: Raj's in house guest report workflow
- Short Description: This machine will get the guest list and in house list from email and pass csv text and files on to the next machine.
- Detail Description: From the hilton PMS we are fetching the in house guest reports in csv on email and this machine is retrieving and processing that CSV


-------------------------------------

#### Classification
- Industry: Hospitality
- Category: Data Collection
- Sub Category: Email

-------------------------------------

#### Compatibility and Dependencies
- Dependent Machines:
  - None
- Compatible Machines
  - GeminiAIHiltonGuestSummaryReport
  - OpenAIHiltonGuestSummaryReport
  - EmailSummaryReportService

-------------------------------------
#### Specifications

##### INPUT
- email_id
  - type: String
  - example: email@mail.com
- password
  - type: String
  - example: Your App Password
- label_name
  - type: String
  - example: TEST


##### DEPENDANT
- NONE

##### OUTPUT <u>[Sample Link 🔗](https://drive.google.com/file/d/1f7GlQqoiVkIm5uiPcJOwnFnOXC4s867w/view?usp=sharing)</u>
- inhouseguests_csv
  - type: String
  - content: CSV
- inhouseguests_file_obj
  - type: String
  - content: base64String
- inhouseguests_file_name
  - type: String
- todays_guest_csv
  - type: String
  - content: CSV
- todays_guest_file_obj
  - type: String
  - content: base64String
- todays_guest_file_name
  - type: String
