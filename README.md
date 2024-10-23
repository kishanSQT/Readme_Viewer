### Machine Overview
- Machine Name: GeminiAIHiltonGuestSummaryReport
- Title: Raj's in house guest report workflow
- Short Description: This machine will get the guest list and in house list from dependant and process using gemini ai to generate summary.
- Detail Description: From the hilton PMS we are fetching the in house guest reports in csv on email and this is the chain machine to the emai fetching machine it will use Gemini AI to generate the summary report.

-------------------------------------

#### Classification
- Industry: Hospitality
- Category: Data Processing
- Sub Category: AI

-------------------------------------

#### Compatibility and Dependencies
- Dependent Machines:
  - HiltonGuestSummary
- Compatible Machines
  - OpenAIHiltonGuestSummaryReport
  - EmailSummaryReportService

-------------------------------------
#### Specifications

##### INPUT
- gen_ai_model
  - type: String
  - example: gpt-4o-mini
  - required: true
- prompt
  - type: String
  - example: Here is the report from this hotel run from last night's audit.
  - required: true
- instructions
  - type: String
  - example: You role is to generate a well defined summary
  - required: true


##### DEPENDANT
- inhouseguests_csv
  - type: String
  - machine: HiltonGuestSummary
  - content: csv
  - required: true
- todays_guest_csv
  - type: String
  - machine: HiltonGuestSummary
  - content: csv
  - required: false

##### OUTPUT <u>[Sample Link 🔗](https://drive.google.com/file/d/15JXnJsUo9h9ofkJ3PH0tNYKH-LAmvB4a/view?usp=sharing)</u>
- gai_content
  - type: String
- gai_type
  - type: String
