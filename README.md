### Machine Overview
- Machine Name: GeminiAIHiltonGuestSummaryReport
- Title: Raj's in house guest report workflow
- Short Description: This machine fetches the guest list and in-house list, processes them with Gemini AI, and generates a summary report.
- Detail Description: This machine is part of a chain integrated with the Hilton PMS system. It retrieves in-house guest reports in CSV format via email and processes the data using Gemini AI to generate a comprehensive summary report. The machine works in conjunction with an email-fetching system, ensuring seamless automation of guest report summaries.

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
  - example: gemini-1.5-pro
  - required: true
  - description: It is a mathematical or computational system trained to recognize patterns and make predictions or decisions based on data.
- prompt
  - type: String
  - example: Here is the report from this hotel run from last night's audit.
  - required: true
  - description: Prompts in AI are input instructions or questions given to a model, guiding it to generate a specific response or output.
- instructions
  - type: String
  - example: You role is to generate a well-defined summary
  - required: true
  - description: Instructions are input texts or questions that guide the model to generate a specific response or output.


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
  - description: This is the generated content using Gemini AI
- gai_type
  - type: String
  - description: It is the content type like html or text
