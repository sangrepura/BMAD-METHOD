# Create Technical Spike Task

## Purpose
To define a small, focused, time-boxed development task designed to answer a specific technical question or mitigate a high-risk architectural assumption.

## When to Use
This task is typically initiated by the `architect` agent after the initial `Technical Architecture Document` is drafted. It is used when there is significant uncertainty about a proposed technology or integration.

## Instructions

### 1. Define the Risk
* Clearly articulate the architectural risk that the spike is intended to address.
* **Example Risk:** "There is a risk that integrating the third-party `XYZ-Booking-API` is more complex than anticipated and may not be able to support our real-time availability needs."

### 2. Formulate the Hypothesis
* State a clear, testable hypothesis.
* **Example Hypothesis:** "We believe we can build a proof-of-concept that successfully connects to the `XYZ-Booking-API`, fetches availability for a single service, and displays it in a simple UI within a 4-hour timebox."

### 3. Create a Single User Story
* Generate a single, self-contained user story for the `dev` agent to execute.
* The story should have a strict timebox and very clear acceptance criteria focused on answering the technical question.
* **Example Spike Story:**
    * **Title:** Technical Spike: XYZ Booking API Integration
    * **Timebox:** 4 hours
    * **Story:** As a Developer, I want to create a minimal Next.js page that connects to the `XYZ-Booking-API` using the provided credentials and displays the raw JSON response for `getAvailability(serviceId: '123')`, so that we can validate that the connection is possible and the data format is as expected.
    * **Acceptance Criteria:**
        1.  The application successfully authenticates with the XYZ API.
        2.  A successful API call is made to the `getAvailability` endpoint.
        3.  The raw JSON response from the API is successfully rendered on the page.
        4.  No time should be spent on styling or UI; this is purely a technical validation task.

### 4. Output
* The output is a single, complete user story in the standard format, ready to be passed to the `sm` agent or directly to the `dev` agent for execution.