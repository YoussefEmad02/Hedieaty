# Hedieaty

Hedieaty is a gift list management app designed to streamline the process of creating, managing, and sharing wish lists for special occasions such as birthdays, weddings, engagements, graduations, and holidays. The app features a user-friendly interface that allows users to easily add gifts to their lists, either manually or through an integrated barcode scanner. With Hedieaty, users can manage their lists flexibly, including adding, deleting, and modifying items at any time—except for items that have been pledged. The app also enables users to publish their lists to the cloud, allowing friends and family to view and pledge to purchase gifts, enhancing the joy of gift-giving. The app should be designed using Flutter and published on Appstore, Google Play Store, and/or Amazon App Store.

## Pages

### 1. UI Layout and Design (Minimum 6 Pages)

#### Home Page:
- A list of friends displayed with their names and profile pictures.
- For each friend, indicate if there are any upcoming events created (e.g., "Upcoming Events: 1" or "No Upcoming Events" or use numbers like WhatsApp message numbers).
- Clicking on a friend's name navigates to their gift lists, allowing users to view details of their lists and pledge gifts.
- Users can add friends via phone numbers manually or from their contact list.
- Search functionality to find friends' gift lists.
- At the top of the home page, include a prominent button to create a new event or gift list, labeled "Create Your Own Event/List."

#### Event List Page:
- Display list of events, sortable by name, category, and status (Upcoming/Current/Past).
- Buttons for adding a new event, editing existing events, and deleting events.
- Editing Support: Users can modify/delete event details at any time.

#### Gift List Page:
- Display gifts associated with the selected event, sortable by name, category, and status.
- Buttons for adding new gifts, editing existing gifts, and deleting gifts.
- Visual indicators for pledged gifts (color-coded).
- Editing Support: Users can add, delete, or modify gifts until they are pledged.

#### Gift Details Page:
- Input fields for gift name, description, category (e.g., electronics, books, etc.), and price.
- Option to upload an image of the gift.
- Status toggle (available, pledged) with a restriction that pledged gifts cannot be modified.

#### Profile Page:
- User profile management with options to update personal information and notification settings.
- List of user’s created events and associated gifts.
- Link to My Pledged Gifts Page.

#### My Pledged Gifts Page:
- Overview of gifts that the user has pledged, along with friend names and due dates for each pledged item.
- Options to modify the list if the pledge is still valid (pending gifts).

### 2. Database Integration

- Implement SQLite for local storage of user events, gift lists, gift details, and user profiles.
- Structure tables for:
    - Users (ID, name, email, preferences)
    - Events (ID, name, date, location, description, user ID)
    - Gifts (ID, name, description, category, price, status, event ID)
    - Friends (User ID, Friend ID)

### 3. Real-time Database Integration

- Use Firebase Realtime Database for syncing published gift lists across devices.
- Implement user authentication with Firebase Authentication to manage user accounts and secure data.
- Allow users to update the status of gifts (e.g., changing from "available" to "pledged" or "purchased") in real-time.
- Color-code gifts based on their status (e.g., green for pledged, red for purchased), updated in real-time.

### 4. Barcode Scanner Integration

- Integrate a barcode scanning functionality using a Flutter plugin, enabling users to scan products in stores and automatically add them to their gift list.

### 5. Quality Enhancement Features

- Introduce animations for transitions between pages and visual feedback for user actions.
- Implement a notification system using Firebase Cloud Messaging to alert the gift list creator when another user pledges to buy a gift.
- In-app notifications for updates on gift status changes.
- Develop advanced querying features for searching and filtering gifts by name, category, or event date.
- Code structure follows clean architecture.
- Enable data validation to ensure the integrity of user inputs (e.g., valid date formats, required fields).

### 6. Auto-Test Script

- Create a test suite that contains a number of test cases using Flutter’s testing framework, including unit tests and integration tests for app workflows. The list of test cases should be written in the project document.
- Create an auto-test script (PowerShell test script that runs from the command prompt or bash script in Linux that runs from the Linux shell) to automate the test procedure and to run the test cases and generate logs without human interaction through the utilization of adb commands.
- Package the test scripts alongside the app for easy execution so that running the auto-test script can run all test cases and generate the test results in a log file.

### 7. Documentation and QA

- Provide comprehensive project documentation detailing app functionality and user guides. The document should include the following sections:
    - Introduction,
    - Survey of Similar Apps in the market with a comparative analysis of the advantages and disadvantages of each app.
    - UI Design including a detailed description of and screenshots of the UI pages.
    - Code Description and Navigation scenarios.
    - Test plan and scoreboard of test cases.
    - Known bugs.
    - Version Control Activity Report. On GitHub, navigate to the main page of the repository. There are two ways to enter the activity view: On the main page of the repository, to the right of the list of files, click Activity. Alternatively, click Branches, then to the right of any branch, click.
    - The app should be published on Appstore, Google Play Store, and/or Amazon App Store, and a link to the store landing page should be added to the project document.
- Students should prepare a 2-minute video, post it on YouTube, and demonstrate it to the instructor. Provide the link to the video in the project document.
- The project should be maintained using version control software (such as git). A screenshot of the git activity and link to the online private repo should be added to the project document. Access to the instructor should be given to allow viewing of commit days/times and version control utilization.
