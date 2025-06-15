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

## **3. Use Cases**

### **Use Case 1: User Registration with Phone Number**
- **Actor:** New User
- **Preconditions:**
  - User has a valid phone number
  - User has not registered before
  - User accepts terms of use
- **Basic Flow:**
  1. User opens the app and selects "Sign up with phone number"
  2. User enters phone prefix and phone number
  3. User accepts terms of use (2 checkboxes)
  4. System sends OTP via SMS
  5. User enters the 5-digit OTP
  6. System verifies OTP and creates account
  7. User is redirected to onboarding flow
- **Alternate Flow:**
  - If phone number already exists and needs email: System prompts for email
  - If OTP is invalid: System shows error message
  - If user requests resend: System resends OTP

### **Use Case 2: OAuth Authentication**
- **Actor:** New/Existing User
- **Preconditions:**
  - User has a Google or Apple account
  - Device has internet connection
- **Basic Flow:**
  1. User selects "Sign in with Google" or "Sign in with Apple"
  2. System redirects to OAuth provider
  3. User authenticates with provider
  4. System receives user data and token
  5. If new user: Redirect to phone number verification
  6. If existing user: Redirect to home screen
- **Alternate Flow:**
  - If OAuth fails: Show error message
  - If user cancels: Return to sign-in screen

### **Use Case 3: Create Profile Cards**
- **Actor:** Registered User
- **Preconditions:**
  - User is authenticated
  - User has completed basic profile
- **Basic Flow:**
  1. User navigates to profile screen
  2. User taps the "+" button
  3. User selects card type (text, audio, photo, music, movie)
  4. User selects a prompt for the card
  5. User adds content based on card type:
     - Text: Types response
     - Audio: Records voice message
     - Photo: Uploads/takes photo
     - Music: Searches and selects song
     - Movie: Searches and selects movie
  6. User saves the card
  7. Card appears in profile
- **Alternate Flow:**
  - User cancels: Return to profile without saving
  - Upload fails: Show error and retry option

### **Use Case 4: Swipe and Match**
- **Actor:** Verified/Unverified User
- **Preconditions:**
  - User is authenticated
  - Other profiles exist in the system
- **Basic Flow:**
  1. User navigates to home screen
  2. System displays profile cards of other users
  3. User swipes:
     - Right or taps like button: Like the profile
     - Left or taps X button: Dislike the profile
  4. If mutual like: System creates a match
  5. Match notification is displayed
  6. Users can now set up dates (if verified)
- **Alternate Flow:**
  - No more profiles: Show empty state with refresh option
  - Network error: Show error message

### **Use Case 5: Identity Verification (KYC)**
- **Actor:** Unverified User
- **Preconditions:**
  - User has completed profile
  - User wants to set up real dates
- **Basic Flow:**
  1. User navigates to verification section
  2. User uploads government-issued ID
  3. User takes a selfie for facial recognition
  4. System processes verification internally
  5. User receives temporary "Verified" status
  6. System completes verification
  7. User receives full verified status
- **Alternate Flow:**
  - Verification fails: User must retry with valid documents
  - Poor image quality: System requests better photos

### **Use Case 6: Set Match Preferences**
- **Actor:** Registered User
- **Preconditions:**
  - User is authenticated
  - User is in profile setup or settings
- **Basic Flow:**
  1. User navigates to preferences section
  2. User sets basic preferences:
     - Age range (min/max)
     - Height range (min/max)
     - Weight range (min/max)
     - Distance range (min/max)
  3. User sets exclusion preferences:
     - Genders to exclude
     - Political opinions to exclude
     - Religions to exclude
     - Lifestyle habits to exclude
  4. User sets sexual orientation
  5. User saves preferences
  6. System updates matching algorithm
- **Alternate Flow:**
  - Invalid ranges: System shows validation error
  - User skips: Default preferences are applied

### **Use Case 7: Manage Profile Cards**
- **Actor:** Registered User
- **Preconditions:**
  - User has existing profile cards
  - User is on their profile page
- **Basic Flow:**
  1. User views their profile with cards
  2. User can perform actions on cards:
     - Reorder: Use up/down arrows
     - Delete: Tap delete button
     - Edit: Tap edit button (navigates to edit flow)
  3. System updates card positions
  4. Changes are saved automatically
- **Alternate Flow:**
  - Network error during save: Show error and retry
  - Concurrent updates: Last change wins

### **Use Case 8: Setup a Date**
- **Actor:** Verified User with Match
- **Preconditions:**
  - Both users are verified
  - Users have matched
  - Date not already scheduled
- **Basic Flow:**
  1. User navigates to matches/appointments
  2. User selects a match
  3. User proposes a place from favorites or searches
  4. User selects available dates/times
  5. Other user receives notification
  6. Other user can:
     - Accept the proposal
     - Suggest alternative place/time
     - Decline
  7. Once agreed, date is confirmed
- **Alternate Flow:**
  - User cancels date: Date status updated
  - User reschedules: New negotiation flow
  - Match is cancelled: Date is automatically cancelled

### **Use Case 9: Manage Favorite Places**
- **Actor:** Registered User
- **Preconditions:**
  - User is authenticated
  - User is on profile/settings
- **Basic Flow:**
  1. User navigates to favorite places section
  2. User taps "+" to add a place
  3. User can:
     - Search for a place
     - Select from categories
     - Choose from suggestions
  4. User adds place (max 5)
  5. User can reorder places by priority
  6. User can remove places
- **Alternate Flow:**
  - Exceeds 5 places: System prevents addition
  - Place not found: User can manually add
  - Network error: Changes saved locally

### **Use Case 10: Report a User**
- **Actor:** User with Match/Date
- **Preconditions:**
  - User has matched with reported user
  - User is authenticated
- **Basic Flow:**
  1. User navigates to match/appointment details
  2. User taps "Report [Name]" button
  3. User selects report reason
  4. User provides additional details
  5. User submits report
  6. System confirms report received
  7. Reported user may be blocked
- **Alternate Flow:**
  - User cancels: No report filed
  - Network error: Report queued for later

### **Use Case 11: Complete Profile Onboarding**
- **Actor:** New User
- **Preconditions:**
  - User has verified phone number
  - User is in onboarding flow
- **Basic Flow:**
  1. User enters first name
  2. User enters birthday
  3. User selects gender (with optional precision)
  4. User uploads profile picture
  5. User sets location (GPS or manual)
  6. User fills profile details:
     - Physical attributes
     - Professional info
     - Lifestyle habits
     - Personality traits
  7. User sets match preferences
  8. Profile is complete
- **Alternate Flow:**
  - User skips optional fields: Defaults applied
  - Location denied: Manual selection required
  - Invalid data: Validation errors shown

### **Use Case 12: View and Manage Appointments**
- **Actor:** Verified User
- **Preconditions:**
  - User has scheduled dates
  - User is authenticated
- **Basic Flow:**
  1. User navigates to appointments section
  2. User sees list of appointments with status
  3. User can tap appointment to see details:
     - Match profile preview
     - Selected place details
     - Date and time
  4. User can perform actions:
     - Confirm appointment
     - Cancel appointment
     - Reschedule
     - View place details
     - Contact match
- **Alternate Flow:**
  - No appointments: Empty state shown
  - Past appointments: Different UI state
  - Cancelled by other: Notification sent

### **Use Case 13: Profile Matching Algorithm**
- **Actor:** System (Automated Process)
- **Trigger:** User opens home screen to view potential matches
- **Preconditions:**
  - User has completed profile with preferences
  - Other users exist in the system
  - Users have set their match preferences
- **Basic Flow:**
  1. System retrieves user's profile preferences:
     - Basic ranges: age, height, weight, distance
     - Exclusions: genders, political opinions, religions, origins
     - Lifestyle exclusions: smoking, drinking, drugs, weed habits
     - Other exclusions: pets, children preferences
     - Sexual orientation compatibility
  2. System queries potential matches based on:
     - Users within specified distance range
     - Users within age range (both ways)
     - Users not in excluded categories
     - Users matching sexual orientation preferences
  3. System filters out:
     - Users already liked/disliked
     - Users with incompatible preferences
     - Blocked or reported users
  4. System applies ranking algorithm:
     - Prioritize users with mutual preference compatibility
     - Consider profile completeness
     - Factor in recent activity
     - Apply any boost factors (new users, etc.)
  5. System returns ordered list of profiles
  6. Profiles are displayed in swipeable stack
- **Algorithm Details:**
  - **Two-way preference matching:** Both users' preferences must align
  - **Hard filters:** Age, distance, gender, sexual orientation
  - **Soft filters:** Lifestyle habits, political views, religion
  - **Scoring factors:**
    - Profile completeness (more cards = higher score)
    - Verification status (verified users prioritized)
    - Activity level (active users ranked higher)
    - Mutual interests (based on card content)
- **Data Used:**
  - ProfilePreference table (user's preferences)
  - ProfileDetail table (user's characteristics)
  - Profile table (basic info, verification status)
  - Like/Dislike history
  - Location data for distance calculation
- **Alternate Flow:**
  - No matches found: Show empty state
  - Insufficient profiles: Expand search criteria
  - User changes preferences: Re-run algorithm
  - Error in calculation: Use fallback basic matching

### **Profile Preferences Detail**

The matching algorithm uses a comprehensive preference system that allows users to fine-tune their matching criteria:

#### **Basic Range Preferences**
- **Age Range:** Minimum and maximum age (18-99 years)
- **Height Range:** Minimum and maximum height (140-220 cm)
- **Weight Range:** Minimum and maximum weight (40-150 kg)
- **Distance Range:** Maximum distance willing to travel (0-100 km)

#### **Exclusion Preferences**
Users can exclude profiles based on:

**Demographics:**
- **Gender Exclusions:** Specific genders to exclude from matches
- **Sexual Orientation:** User's orientation for compatible matching

**Personal Beliefs:**
- **Political Opinions:** Exclude specific political stances
- **Religions:** Exclude specific religious beliefs
- **Origins/Ethnicity:** Exclude based on cultural background

**Lifestyle Habits:**
- **Smoking Habits:** Never, Rarely, Sometimes, Often, Always
- **Drinking Habits:** Never, Rarely, Sometimes, Often, Always
- **Drug Use:** Never, Rarely, Sometimes, Often, Always
- **Cannabis Use:** Never, Rarely, Sometimes, Often, Always

**Life Choices:**
- **Pet Preferences:** Exclude based on pet ownership
- **Children Preferences:** Want/Don't want/Have children

#### **Preference Matching Logic**
1. **Mutual Compatibility:** Both users' preferences must be satisfied
2. **Hard Filters:** Cannot be overridden (age, distance, gender)
3. **Soft Filters:** Can be relaxed if matches are scarce
4. **Weighted Scoring:** Some preferences have higher impact on match score

#### **Default Preferences**
If user doesn't set preferences:
- Age Range: 18-99
- Distance: 50 km
- All other filters: No exclusions

---

## **4. Success Criteria**

| **Criterion** | **Description** | **Threshold for Success** |
|--------------|---------------|------------------------|
| Stability    | No major crashes or critical bugs | Zero crash reports during beta testing |
| Usability    | Users can navigate and understand features with minimal guidance | 80% positive feedback from testers |
| Performance  | App responds quickly to user actions and loads profiles smoothly | 95% of actions complete within 3 seconds |
| Matching Accuracy | Algorithm provides relevant matches based on preferences | 75% user satisfaction with suggested profiles |
| Verification System | KYC process completes successfully | 90% successful verification rate |
| Feature Adoption | Core features are used by testers | 70% usage rate for cards, preferences, and favorite places |

---

## **5. Known Issues & Limitations**

| **Issue**           | **Description**                                                        | **Impact** | **Planned Fix? (Yes/No)** |
| ------------------- | ---------------------------------------------------------------------- | ---------- | ------------------------- |
| User settings       | All changes to user settings are not taken into account                | Medium     | Yes                       |
| OTP                 | OTP isn't always sent, and can require to be found inside the database | High       | Yes                       |
| Map api             | Get places without expensive Google API                                | High       | No                        |
| Initial Language    | Support limited to primary languages                                   | Low        | Yes - Roadmap for multilingual expansion |
| User authentication | OAuth implementation not finished                                      | Medium     | Yes                       |

---

## **6. Conclusion**

This Beta Test Plan represents a critical milestone in Meo's development journey. By systematically testing all core functionalities and use cases, we aim to ensure a robust, user-friendly dating application that stands out in the market.

**Key Objectives:**
- **Quality Assurance:** Identify and resolve critical bugs before public launch
- **User Experience Validation:** Confirm that the unique features (profile cards, favorite places, identity verification) provide value
- **Performance Optimization:** Ensure smooth operation across devices and network conditions
- **Safety and Trust:** Validate that reporting and verification systems create a secure environment

**Expected Outcomes:**
- A stable application ready for market release
- Validated user flows that differentiate Meo from competitors
- Comprehensive feedback for future feature development
- Confidence in the matching algorithm's effectiveness

**Success Metrics:**
- Zero critical bugs in production
- 80%+ positive user feedback on core features
- Successful completion of all test scenarios
- Verified cross-platform compatibility

The beta testing phase will provide invaluable insights into real-world usage patterns and help us refine Meo into a premium dating experience that prioritizes authentic connections and user safety. Through rigorous testing and iteration, we're committed to launching an application that exceeds user expectations and establishes new standards in the online dating industry.
