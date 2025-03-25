### **BETA TEST PLAN – MEO**

## **1. Core Functionalities for Beta Version**

Below are the essential features that must be available for beta testing, along with any changes made since the initial Tech3 Action Plan.

| **Feature Name**                                      | **Description**                                                                                                                                                                                                                                                                                       | **Priority (High/Medium/Low)** | **Changes Since Tech3**                                                                    |
| ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ | ------------------------------------------------------------------------------------------ |
| Creating a profile with a phone number                | The user should be able to create an account using only it's phone number and a OTP (one-time password) send by text.                                                                                                                                                                                 | High                           | -                                                                                          |
| Matching with another user through likes and dislikes | A user must be able to like/dislike another user on the app's home page by swiping or pressing associated buttons. When 2 users like each-other they create a 'match', with appropriate feedback                                                                                                      | High                           | -                                                                                          |
| Adding cards to build your own profile                | The user must be able to create a complete and original profile through the creation of various "card blocks". A card block is made of a "prompt" (a sentence that gives context to the card's content) and content which can be text, an image, an audio message, a music snippet or a movie poster. | High                           | Book covers are no longer valid options for the content part of the card                   |
| Identity Verification                                 | To be allowed to go on real-world dates, the user must verify it's identity through ID analysis. When waiting for ID to be verified, the user will obtain a temporary 'Verified' status.                                                                                                              | High                           | The KYC (know your custommer) feature will not be outsourced                               |
| Date setup and management                             | After matching with another user, the user should be able to setup a date by proposing a place or accepting the other user's proposal, and by entering it's availabilities or by selecting one of the other user's availabilities. The user should also be able to cancel the date or the match.      | Medium                         | -                                                                                          |
| Potential matches preferences                         | A user should have the possibility to edit various filters, to better target the suggested profiles. Examples of those filters are the height range, political stance or age range.                                                                                                                   | Medium                         | All filters will be accessible to the user instead of only a few, with the other paywalled |
| Editing an already setup date                         | Once a date has been setup, the user should be able to request changes to both the date and place, or simply cancel the date                                                                                                                                                                          | Medium                         | -                                                                                          |
| Choosing your favorite places to have dates           | A list of the user's favorite places to have dates must be displayed on its profile. The user should be able to add, remove and edit the ranking of those places in said list.                                                                                                                        | High                           | A maximum of 5 places can be selected                                                      |
| Reporting another user                                | The user should be able to report a user with whom it went on a date, with extensive options                                                                                                                                                                                                          | Low                            | -                                                                                          |

---

## **2. Beta Testing Scenarios**

### **2.1 User Roles**

The following roles will be involved in beta testing.

| **Role Name**   | **Description**                                                     |
| --------------- | ------------------------------------------------------------------- |
| Unverified User | Creates and customizees its own profile, likes/dislikes other users |
| Verified User   | Same as Unverified User, but can set up dates with other users      |

### **2.2 Test Scenarios**

For each of the test scenarios, the user(s) must be using a device connected to the internet. Some of the test scenarios require access to multiple profiles, therefore it is advised to have access to at least 2 devices with internet connectivity, each connected to a different profile.

#### \*\*Scenario 1: Profile Creation with Phone Number

- **Role Involved:** Unverified User
- **Objective:** Verify user can create a profile using phone number and OTP
- **Preconditions:**:

  - User has a valid phone number
  - Mobile device with SMS capabilities
  - Phone number is not already registered

- **Test Steps:**
  1. Open the app and navigate to registration
  2. Enter a valid phone number
  3. Request OTP
  4. Receive and enter the 6-digit OTP
  5. Complete initial profile setup
- **Expected Outcome:**
  - OTP verification works correctly
  - User is directed to onboarding screen
  - After completing onboarding, user is directed to app's home screen

#### \*\*Scenario 2: User Matching Mechanism

- **Role Involved:** Unverified User
- **Objective:** Verify the like/dislike matching process
- **Preconditions:**:

  - User has a complete profile (has completed onboarding)
  - At least 2 user profiles are available
  - One of the other profiles has already liked the user

- **Test Steps:**
  1. Navigate to the home screen with user profiles
  2. Swipe left (dislike) on another profile (not the one already liked)
  3. Swipe right (like) on a profile (that has already liked the user)
  4. Check if a mutual like creates a match
  5. Verify match feedback appears
- **Expected Outcome:**
  - Like and dislike actions register correctly
  - Mutual likes trigger a match
  - Match notification is displayed

#### **Scenario 3: Profile Card Creation**

- **Role Involved:** Unverified User
- **Objective:** Verify user can create profile cards with various content types
- **Preconditions:**
  - User is logged in
  - Device has access to images, audio, and media
- **Test Steps:**
  1. Navigate to profile editing section
  2. Create a card with a text prompt
  3. Choose a card type
  4. Add the appropriate content to the card (image, audio, movie, etc.)
  5. Verify card appears on profile
  6. Repeat steps 2-5 for each card type
  7. Delete a card
  8. Reorder cards by pressing the up/down arrows
- **Expected Outcome:**
  - User can create cards with different content types
  - Cards display correctly on profile
  - Cannot use book covers as card content
  - Cards can be reordered
  - Cards can be deleted

#### **Scenario 4: Identity Verification**

- **Role Involved:** Unverified User
- **Objective:** Verify the identity verification process
- **Preconditions:**
  - User has completed initial profile creation
  - User has a valid ID document
- **Test Steps:**
  1. Navigate to identity verification section
  2. Upload a government-issued ID
  3. Take a selfie for facial recognition
  4. Submit verification documents
  5. Obtain temporary 'Verified' status
  6. Wait for verification status
- **Expected Outcome:**
  - ID upload process works smoothly
  - Verification status updates correctly
  - Verification is processed internally (not outsourced)

#### **Scenario 5: Date Setup and Management**

- **Role Involved:** Verified User
- **Objective:** Verify date setup and editing capabilities
- **Preconditions:**
  - Users have matched
  - Must have access to the 2 profiles (Profile a and Profile b)
- **Test Steps:**
  1. Profile A initiates date setup after matching
  2. Profile A proposes a meeting place
  3. Profile A selects available date and time
  4. Profile B proposes an alternative date place
  5. Profile B accepts one of Profile A's time slots
  6. Profile A accepts Profile B's alternative date place
  7. One of the users cancels the date
  8. One of the users cancels the match
- **Expected Outcome:**
  - Date can be proposed and accepted
  - Users can edit date details
  - Users can cancel a date
  - Users can cancel a match

#### **Scenario 6: Favorite Date Places**

- **Role Involved:** User
- **Objective:** Verify management of favorite date locations
- **Preconditions:**
  - User is logged in
  - Multiple location options available
- **Test Steps:**
  1. Navigate to the user's profile page
  2. Add first favorite location using the '+' button (tester can use the searchbar, categories or suggested locations)
  3. Add second favorite location by repeating steps 2-3
  4. Continue adding up to 5 locations
  5. Attempt to add 6th location (should be prevented)
  6. Reorder locations in the list
  7. Remove a location
- **Expected Outcome:**
  - Can add up to 5 favorite locations
  - Locations can be reordered
  - Cannot add more than 5 locations
  - Can use different ways to add locations (categories, suggested locations, search bar)

#### **Scenario 7: User Reporting**

- **Role Involved:** User
- **Objective:** Verify user reporting functionality
- **Preconditions:**
  - User has a match with another user (doesn't need to already have completed a date)
- **Test Steps:**
  1. Navigate to the match list page
  2. Select the match to report
  3. Scroll down and click on the report button
  4. Complete the report form
  5. Submit the report
- **Expected Outcome:**
  - Comprehensive reporting options available
  - Report can be submitted successfully
  - User feels safe and supported
  - Feedback is displayed to the user after the report is submitted

#### **Scenario 8: Preference and Matching Algorithm**

- **Role Involved:** User
- **Objective:** Validate the app's matching algorithm and preference settings
- **Preconditions:**
  - User has a detailed profile
  - Multiple user profiles in the system
- **Test Steps:**
  1. Set detailed user preferences
  2. Configure age range
  3. Set location-based matching radius
  4. Define interests and compatibility factors
  5. Swipe through potential matches
  6. Analyze suggested matches
  7. Modify preferences and check match changes
- **Expected Outcome:**
  - Matching algorithm provides relevant suggestions
  - Preferences significantly impact match results
  - Location and interest-based matching works
  - Users can fine-tune matching criteria

#### **Scenario 9: App Performance and Cross-Platform Compatibility**

- **Role Involved:** User
- **Objective:** Verify app performance across different devices and network conditions
- **Preconditions:**
  - Multiple devices (iOS and Android)
  - Various network conditions (WiFi, 4G, 3G)
  - Different screen sizes and resolutions
- **Test Steps:**
  1. Install app on smartphone with small screen
  2. Install app on tablet or larger device
  3. Test app functionality on different OS versions
  4. Check app performance on weak/unstable internet
  5. Verify smooth transition between different app screens
- **Expected Outcome:**
  - App functions consistently across devices
  - No crashes or significant performance issues
  - Responsive design adapts to different screen sizes

---

## **3. Success Criteria**

| **Criterion** | **Description** | **Threshold for Success** |
|--------------|---------------|------------------------|
| Stability    | No major crashes or critical bugs | No crash reported |
| Usability    | Users can navigate and understand features with minimal guidance | 80% positive feedback from testers |
| Performance  | File analysis completes within an acceptable time frame | 95% of files analyzed within 10 seconds |
| Accuracy    | Tidyscore and duplicate detection provide reliable results | 90% accuracy in test cases |

---

## **4. Known Issues & Limitations**

[List any known bugs, incomplete features, or limitations that testers should be aware of.]

| **Issue**           | **Description**                                                        | **Impact** | **Planned Fix? (Yes/No)** |
| ------------------- | ---------------------------------------------------------------------- | ---------- | ------------------------- | ---------------------------------- |
| User settings       | All changes to user settings are not taken into account                | Medium     | Yes                       |
| OTP                 | OTP isn't always sent, and can require to be found inside the database | High       | Yes                       |
| Map api             | get places without expensive google api                                | Hight      | No                        |
| Initial Language    | SupportLimited to primary languages                                    | Low        | Yes                       | Roadmap for multilingual expansion |
| User authentication | OAuth implementation not finished                                      | Medium     | Yes                       |

---

## **5. Conclusion**

[Summarize the importance of this Beta Test Plan and what the team expects to achieve with it.]
