---
title: Release notes
tags:
  - Release notes
  - Moodle 4.0
---

Release date: 19 April 2022

Here is [the full list of issues fixed in 4.0](https://tracker.moodle.org/secure/IssueNavigator!executeAdvanced.jspa?jqlQuery=project+%3D+mdl+AND+resolution+%3D+fixed+AND+fixVersion+in+%28%224.0%22%29+ORDER+BY+priority+DESC&runQuery=true&clear=true).

If you are upgrading from a previous version, please see the [Moodle 4.0 Upgrade notes](https://docs.moodle.org/400/en/Upgrading).

## Server requirements

These are just the minimum supported versions. We recommend keeping all of your software and operating systems up-to-date.

- Moodle upgrade: Moodle 3.6 or later
- PHP version:
  - minimum PHP 7.3.0 __Note: the minimum PHP version has increased since Moodle 3.10__.
  - PHP 7.4.x is also supported.
  - [PHP 8.0 support](https://docs.moodle.org/dev/Moodle_and_PHP) is being implemented (see [MDL-70745](https://tracker.moodle.org/browse/MDL-70745)) and **not ready for production** yet.
- PHP extensions:
  - The [`intl`](https://www.php.net/manual/en/book.intl.php) extension is now *required*.
  - The [`exif`](https://www.php.net/manual/en/book.exif.php) extension is now _recommended_.
  - The [`sodium`](https://www.php.net/manual/en/book.sodium.php) extension is now _recommended_. It will be _required_ from Moodle 4.2 onwards - see [Environment - PHP extension sodium](https://docs.moodle.org/400/en/Environment_-_PHP_extension_sodium) for more information.
- PHP setting **max_input_vars** is recommended to be >= 5000 for PHP 7.x installations. It's a requirement for PHP 8.x installations. For further details, see [Environment - max input vars](https://docs.moodle.org/400/en/Environment_-_max_input_vars).

### Database requirements

Moodle supports the following database servers. Again, version numbers are just the minimum supported version. We recommend running the latest stable version of any software.

| Database | Minimum version | Recommended |
| --- | --- | --- |
| [PostgreSQL](http://www.postgresql.org/) | 10 (increased since Moodle 3.11) | Latest |
| [MySQL](http://www.mysql.com/) | 5.7 | Latest |
| [MariaDB](https://mariadb.org/) | 10.2.29 | Latest |
| [Microsoft SQL Server](http://www.microsoft.com/en-us/server-cloud/products/sql-server/) | 2017 (increased since Moodle 3.10) | Latest |
| [Oracle Database](http://www.oracle.com/us/products/database/overview/index.html) | 11.2 | Latest |

## Client requirements

### Browser support

Moodle is compatible with any standards compliant web browser. We regularly test Moodle with the following browsers:

Desktop:

- Chrome
- Firefox
- Safari
- Edge

:::important Internet Explorer

Please note that Moodle 4.0 does _NOT_ support Internet Explorer 11.

:::

:::note Safari

Safari 7 and below has known compatibility issues with Moodle 4.0.

:::

Mobile:

- MobileSafari
- Google Chrome

For the best experience and optimum security, we recommend that you keep your browser up-to-date.

## Major UX improvements

### Navigation improvements

- [MDL-70208](https://tracker.moodle.org/browse/MDL-70208) - Implement frontend functionality for primary navigation
- [MDL-70207](https://tracker.moodle.org/browse/MDL-70207) - Implement backend functionality for primary navigation
- [MDL-70202](https://tracker.moodle.org/browse/MDL-70202) - Implement frontend functionality for secondary navigation
- [MDL-70198](https://tracker.moodle.org/browse/MDL-70198) - Implement backend functionality for secondary navigation
- [MDL-70196](https://tracker.moodle.org/browse/MDL-70196) - Create a module based navigation bar
- [MDL-72352](https://tracker.moodle.org/browse/MDL-72352) - Ensure that secondary navigation is backwards compatible
- [MDL-73462](https://tracker.moodle.org/browse/MDL-73462) - Course and category management secondary and tertiary navigation
- [MDL-71977](https://tracker.moodle.org/browse/MDL-71977) - Define the secondary navigation nodes that should be always displayed in the more menu in the module context
- [MDL-71901](https://tracker.moodle.org/browse/MDL-71901) - Allow plugins to define their own secondary nav ordering
- [MDL-70844](https://tracker.moodle.org/browse/MDL-70844) - Update the secondary navigation view to send site administration information in tab form
- [MDL-72396](https://tracker.moodle.org/browse/MDL-72396) - Allow easy setting of the active tab for navigation views
- [MDL-71912](https://tracker.moodle.org/browse/MDL-71912) - Implement tertiary navigation for plugins (also see [MDL-71913](https://tracker.moodle.org/browse/MDL-71913), [MDL-71914](https://tracker.moodle.org/browse/MDL-71914) and [MDL-71914](https://tracker.moodle.org/browse/MDL-71914))
- [MDL-73863](https://tracker.moodle.org/browse/MDL-73863) - Tertiary navigation in course completion
- [MDL-72875](https://tracker.moodle.org/browse/MDL-72875) - Add tertiary navigation to the participants page
- [MDL-72904](https://tracker.moodle.org/browse/MDL-72904) - Add tertiary navigation to the badges pages
- [MDL-72873](https://tracker.moodle.org/browse/MDL-72873) - Add tertiary navigation to the gradebook
- [MDL-72094](https://tracker.moodle.org/browse/MDL-72094) - Update the course reports page styling and functionality
- [MDL-71083](https://tracker.moodle.org/browse/MDL-71083) - Move the user menu in the top bar into the primary navigation menu in the mobile view
- [MDL-73393](https://tracker.moodle.org/browse/MDL-73393) - Ensure that existing third party themes still work with latest navigation changes
- [MDL-71943](https://tracker.moodle.org/browse/MDL-71943) - Dynamic (AJAX) tabs in Moodle LMS
- [MDL-72090](https://tracker.moodle.org/browse/MDL-72090) - Convert course admin pages from link farms to dropdowns
- [MDL-72413](https://tracker.moodle.org/browse/MDL-72413) - Move the activity modules title, description, and activity completion into a standard module API
- [MDL-72736](https://tracker.moodle.org/browse/MDL-72736) - Remove section navigation on one section per page
- [MDL-72834](https://tracker.moodle.org/browse/MDL-72834) - Move the calendar link into the user menu
- [MDL-72450](https://tracker.moodle.org/browse/MDL-72450) - Remove the next and previous activity links from all activity modules in Boost
- [MDL-71148](https://tracker.moodle.org/browse/MDL-71148) - Combine both the custom menu & primary navigation renderers
- [MDL-71683](https://tracker.moodle.org/browse/MDL-71683) - Update language menu to move from the top navigation into the user menu when logged in
- [MDL-72005](https://tracker.moodle.org/browse/MDL-72005) - Update the context_header in Boost to move the breadcrumb to the top

### Course index

- [MDL-71209](https://tracker.moodle.org/browse/MDL-71209) - Create the new course index list
- [MDL-72660](https://tracker.moodle.org/browse/MDL-72660) - Add activity completion indicators to the course index
- [MDL-71228](https://tracker.moodle.org/browse/MDL-71228) - Implement drag and drop option for sections and activities in the course index
- [MDL-71211](https://tracker.moodle.org/browse/MDL-71211) - Keep the status of the course index collapsed and expanded sections per user and course
- [MDL-71795](https://tracker.moodle.org/browse/MDL-71795) - Course index on activity view page
- [MDL-71828](https://tracker.moodle.org/browse/MDL-71828) - Implement section links' behaviour in course index
- [MDL-71664](https://tracker.moodle.org/browse/MDL-71664) - Enable drag & drop from course index to course content and vice versa
- [MDL-72463](https://tracker.moodle.org/browse/MDL-72463) - Add 'highlighted' label to course index
- [MDL-71727](https://tracker.moodle.org/browse/MDL-71727) - Sync course index and course content when an element is dragged
- [MDL-72897](https://tracker.moodle.org/browse/MDL-72897) - Mark the current section in the course index
- [MDL-73340](https://tracker.moodle.org/browse/MDL-73340) - Open course index by default first time a user access the course
- [MDL-73310](https://tracker.moodle.org/browse/MDL-73310) - Show the course index on all pages within a course

### Course experience

- [MDL-71037](https://tracker.moodle.org/browse/MDL-71037) - Sections are now collapsible for Topics and Weekly course formats
- [MDL-71691](https://tracker.moodle.org/browse/MDL-71691) - Created a new activity UI component
- [MDL-71689](https://tracker.moodle.org/browse/MDL-71689) - Improvements to add activity and add section design
- [MDL-71663](https://tracker.moodle.org/browse/MDL-71663) - Created a new "move" option in the sections and activity cog menu in the course editor
- [MDL-71779](https://tracker.moodle.org/browse/MDL-71779) - Made 'Add a new topic/week' option client side on Topics and Weekly formats
- [MDL-72311](https://tracker.moodle.org/browse/MDL-72311) - Proceed straight to course content when creating a new course
- [MDL-71863](https://tracker.moodle.org/browse/MDL-71863) - Created core_courseformat subsystem
- [MDL-72578](https://tracker.moodle.org/browse/MDL-72578) - Moved activity UI component to output classes and templates
- [MDL-73343](https://tracker.moodle.org/browse/MDL-73343) - New quick access to create a new course from My courses page when there is no course available

### My Courses page and overview block

- [MDL-70801](https://tracker.moodle.org/browse/MDL-70801) - Implement "My courses" page
- [MDL-58579](https://tracker.moodle.org/browse/MDL-58579) - Allow searching / filtering of courses in myoverview
- [MDL-73231](https://tracker.moodle.org/browse/MDL-73231) - Provide option of having My courses as defaulthomepage

### Timeline block

- [MDL-72276](https://tracker.moodle.org/browse/MDL-72276) - Update timeline block dropdowns to display current selection
- [MDL-72277](https://tracker.moodle.org/browse/MDL-72277) - Improve the layout and usability of the items in the timeline block
- [MDL-73068](https://tracker.moodle.org/browse/MDL-73068) - Only display courses in the timeline block if they contain events
- [MDL-72295](https://tracker.moodle.org/browse/MDL-72295) - Add text search to the timeline block
- [MDL-72594](https://tracker.moodle.org/browse/MDL-72594) - Improve displaying of overdue items in the timeline block
- [MDL-72603](https://tracker.moodle.org/browse/MDL-72603) - Replace timeline block pagination with "show more" lazy loading
- [MDL-72543](https://tracker.moodle.org/browse/MDL-72543) - Change the display of the event names of the items on the timeline block

### Calendar usability

- [MDL-71817](https://tracker.moodle.org/browse/MDL-71817) - Render the calendar in the calendar block in month view
- [MDL-72237](https://tracker.moodle.org/browse/MDL-72237) - Limit number of events shown per day in calendar month view
- [MDL-71810](https://tracker.moodle.org/browse/MDL-71810) - Add a current date indicator and make calendar block responsive when switching between small and large views
- [MDL-71808](https://tracker.moodle.org/browse/MDL-71808) - Move the import calendar form to its own page
- [MDL-72045](https://tracker.moodle.org/browse/MDL-72045) - Improve help information provided on the calendar export page
- [MDL-71790](https://tracker.moodle.org/browse/MDL-71790) - Revamp the manage subscriptions page
- [MDL-71788](https://tracker.moodle.org/browse/MDL-71788) - Make it easier to copy the export URL
- [MDL-71775](https://tracker.moodle.org/browse/MDL-71775) - Add footer links to the calendar block
- [MDL-72810](https://tracker.moodle.org/browse/MDL-72810) - Remove 3-month calendar view

### Dashboard

- [MDL-72092](https://tracker.moodle.org/browse/MDL-72092) - Arrange blocks between My courses & My dashboard
- [MDL-73114](https://tracker.moodle.org/browse/MDL-73114) - Display a title in the dashboard page
- [MDL-71964](https://tracker.moodle.org/browse/MDL-71964) - Welcome message for users
- [MDL-73233](https://tracker.moodle.org/browse/MDL-73233) - Provide option to disable the Dashboard
- [MDL-72116](https://tracker.moodle.org/browse/MDL-72116) - Remove some of the default blocks from the Dashboard

### User tours

- [MDL-61674](https://tracker.moodle.org/browse/MDL-61674) - Allow user tours to be created using the Atto text editor
- [MDL-72385](https://tracker.moodle.org/browse/MDL-72385) - Improve and simplify design of user tours
- [MDL-71938](https://tracker.moodle.org/browse/MDL-71938) - Display number of steps in a user tour
- [MDL-72783](https://tracker.moodle.org/browse/MDL-72783) - Add new user tours
- [MDL-72781](https://tracker.moodle.org/browse/MDL-72781) - Remove previous user tours
- [MDL-72557](https://tracker.moodle.org/browse/MDL-72557) - Implement customisable confirmation button for single step user tours
- [MDL-71931](https://tracker.moodle.org/browse/MDL-71931) - Update user tours to emit events

### Other usability and user experience improvements

- [MDL-69371](https://tracker.moodle.org/browse/MDL-69371) - Redesign the Moodle login page (also see [MDL-72928](https://tracker.moodle.org/browse/MDL-72928))
- [MDL-71457](https://tracker.moodle.org/browse/MDL-71457) - Update the Moodle activity icons
- [MDL-71963](https://tracker.moodle.org/browse/MDL-71963) - Turn confirmation page into modals
- [MDL-71965](https://tracker.moodle.org/browse/MDL-71965) - New footer
- [MDL-71456](https://tracker.moodle.org/browse/MDL-71456) - Create page drawers for the block and course index areas
- [MDL-72095](https://tracker.moodle.org/browse/MDL-72095) - Set a main container width of Boost pages
- [MDL-71610](https://tracker.moodle.org/browse/MDL-71610) - Move the turn editing on button into the navbar
- [MDL-72305](https://tracker.moodle.org/browse/MDL-72305) - Show user initials as a placeholder for the user profile picture
- [MDL-72278](https://tracker.moodle.org/browse/MDL-72278) - Fake blocks now in drawer are made visible on first visit
- [MDL-72454](https://tracker.moodle.org/browse/MDL-72454) - Removal of back to top link
- [MDL-72088](https://tracker.moodle.org/browse/MDL-72088) - Update styling across top level pages
- [MDL-70888](https://tracker.moodle.org/browse/MDL-70888) - Update the layouts in Boost theme
- [MDL-71292](https://tracker.moodle.org/browse/MDL-71292) - Update the page header and include course image / activity icon
- [MDL-73608](https://tracker.moodle.org/browse/MDL-73608) - Provide a contact form which sends to the site support email and replace mailto link in footer
- [MDL-73935](https://tracker.moodle.org/browse/MDL-73935) - Improved flexibility of site support form and consistency of site support info provided in Moodle
- [MDL-61564](https://tracker.moodle.org/browse/MDL-61564) - Allow multiple cohort selection in cohort enrolment
- [MDL-66539](https://tracker.moodle.org/browse/MDL-66539) - Better handling of link names and URLs with Atto
- [MDL-73797](https://tracker.moodle.org/browse/MDL-73797) - Dialogues now have the action button on the right
- [MDL-60917](https://tracker.moodle.org/browse/MDL-60917) - Add highest ranked results section to global search
- [MDL-73917](https://tracker.moodle.org/browse/MDL-73917) - Notification preferences page improvements
- [MDL-72500](https://tracker.moodle.org/browse/MDL-72500) - Easier to find a specific component in event list report
- [MDL-32103](https://tracker.moodle.org/browse/MDL-32103) - Course completion is instant for activity based completion criteria (single user completions only)

## Other major features

### Report builder integration (from Moodle Workplace)

- [MDL-70795](https://tracker.moodle.org/browse/MDL-70795) - Implement functionality for creating custom reports
- [MDL-70794](https://tracker.moodle.org/browse/MDL-70794) - Implement functionality for creating system reports
- [MDL-72588](https://tracker.moodle.org/browse/MDL-72588) - Implement custom report audiences
- [MDL-72598](https://tracker.moodle.org/browse/MDL-72598) - Implement custom report schedules
- [MDL-73598](https://tracker.moodle.org/browse/MDL-73598) - Allow Custom Reports to be disabled by site admin
- [MDL-72280](https://tracker.moodle.org/browse/MDL-72280) - Create "Courses" custom report source
- [MDL-73069](https://tracker.moodle.org/browse/MDL-73069) - Report condition to limit returned data to current user
- [MDL-73180](https://tracker.moodle.org/browse/MDL-73180) - Improve definitions of previous/next relative date filters
- [MDL-72662](https://tracker.moodle.org/browse/MDL-72662) - Implement relative date options in the Reportbuilder date filter
- [MDL-72172](https://tracker.moodle.org/browse/MDL-72172) - Create "Cohort members" custom report source
- [MDL-72962](https://tracker.moodle.org/browse/MDL-72962) - Format editable report elements (column, filters, etc)
- [MDL-72826](https://tracker.moodle.org/browse/MDL-72826) - Custom report option to display unique row values
- [MDL-71153](https://tracker.moodle.org/browse/MDL-71153) - Convert task logs report to a system report
- [MDL-71070](https://tracker.moodle.org/browse/MDL-71070) - Convert configuration changes report to a system report

### BigBlueButton integration

- [MDL-70658](https://tracker.moodle.org/browse/MDL-70658) - Integrate the BigBlueButton plugin into Moodle LMS

### Quiz and Questions

- [MDL-71516](https://tracker.moodle.org/browse/MDL-71516) - Create new plugin type - Qbank (for the full list of qbank plugins added to core, see [MDL-70329](https://tracker.moodle.org/browse/MDL-70329))
- [MDL-71679](https://tracker.moodle.org/browse/MDL-71679) - Update mod_quiz for new question bank
- [MDL-71636](https://tracker.moodle.org/browse/MDL-71636) - Add a columnsortorder settings page
- [MDL-71696](https://tracker.moodle.org/browse/MDL-71696) - Add question versions
- [MDL-72076](https://tracker.moodle.org/browse/MDL-72076) - Question bank bulk action UI
- [MDL-72553](https://tracker.moodle.org/browse/MDL-72553) - Add custom fields to questions
- [MDL-52206](https://tracker.moodle.org/browse/MDL-52206) - Move "Require passing grade" completion option to core
- [MDL-52456](https://tracker.moodle.org/browse/MDL-52456) - Add notification message for students after questions have been manually graded
- [MDL-71984](https://tracker.moodle.org/browse/MDL-71984) - Add logging to quiz auto-save, process_attempt and redo_question
- [MDL-73337](https://tracker.moodle.org/browse/MDL-73337) - Log editing quizzes in detail
- [MDL-73699](https://tracker.moodle.org/browse/MDL-73699) - Question status UI/UX update
- [MDL-72448](https://tracker.moodle.org/browse/MDL-72448) - Add qbank_history to core
- [MDL-71614](https://tracker.moodle.org/browse/MDL-71614) - Add qbank_previewquestion to core

### Update LTI tool provider feature to support 1.3

- [MDL-69543](https://tracker.moodle.org/browse/MDL-69543) - Update tool to support 1.3 OAuth2/OIDC launch flow
- [MDL-71371](https://tracker.moodle.org/browse/MDL-71371) - Provide upgrade path for 1.1 preconfigured tools
- [MDL-72745](https://tracker.moodle.org/browse/MDL-72745) - Provide account provisioning options for LTI Advantage launches
- [MDL-69547](https://tracker.moodle.org/browse/MDL-69547) - Update tool enrolment code so that a user is automatically created and enrolled when launching via 1.3
- [MDL-69545](https://tracker.moodle.org/browse/MDL-69545) - Update user sync task to support 1.3 messages
- [MDL-69544](https://tracker.moodle.org/browse/MDL-69544) - Update grade sync task to support 1.3 messages
- [MDL-72288](https://tracker.moodle.org/browse/MDL-72288) - Update library and model code to support issuer and clientid uniqueness on registrations
- [MDL-69862](https://tracker.moodle.org/browse/MDL-69862) - Add dynamic registration support to the tool
- [MDL-70354](https://tracker.moodle.org/browse/MDL-70354) - Return line item information during content selection

### Assignment

- [MDL-68913](https://tracker.moodle.org/browse/MDL-68913) - Per attempt timing now available in assignments

### Admin configuration presets

- [MDL-72112](https://tracker.moodle.org/browse/MDL-72112) - Integrate admin_presets third-party plugin in Moodle LMS
- [MDL-73145](https://tracker.moodle.org/browse/MDL-73145) - Add a $CFG setting to define the preset to be installed
- [MDL-72114](https://tracker.moodle.org/browse/MDL-72114) - Include pre-installed admin presets
- [MDL-72113](https://tracker.moodle.org/browse/MDL-72113) - Add feature to import/export plugins visibility from Admin presets tool
- [MDL-73394](https://tracker.moodle.org/browse/MDL-73394) - Store the latest site admin preset applied

### Content bank and H5P

- [MDL-68394](https://tracker.moodle.org/browse/MDL-68394) - Integrate mod_h5pactivity with recent activity plugins
- [MDL-72099](https://tracker.moodle.org/browse/MDL-72099) - Add navigation by contexts in the content bank
- [MDL-71885](https://tracker.moodle.org/browse/MDL-71885) - Inline editing H5P content for mod_h5pactivity
- [MDL-71956](https://tracker.moodle.org/browse/MDL-71956) - Inline editing H5P content anywhere

### Badges

- [MDL-72141](https://tracker.moodle.org/browse/MDL-72141) - Simplifying the external badge page

### Accessibility improvements

- [MDL-67853](https://tracker.moodle.org/browse/MDL-67853) - Remove online-offline options on notifications
- [MDL-72078](https://tracker.moodle.org/browse/MDL-72078) - Give users an indication that they encountered an editor
- [MDL-71604](https://tracker.moodle.org/browse/MDL-71604) - Move the screen reader helper button to the first row
- [MDL-72896](https://tracker.moodle.org/browse/MDL-72896) - Make html_tables responsive by default

## Other Highlights

### Functional changes

- [MDL-70456](https://tracker.moodle.org/browse/MDL-70456) - Add custom user field support to all places that display user identity [0,Minor] Improvement
- [MDL-73342](https://tracker.moodle.org/browse/MDL-73342) - Disable some blocks by default (such as feedback, RSS and self-completion)
- [MDL-70905](https://tracker.moodle.org/browse/MDL-70905) - Updated media default width/height to use 16:9
- [MDL-72118](https://tracker.moodle.org/browse/MDL-72118) - Rename "HTML block" to the more easily understood "Text block"
- [MDL-72706](https://tracker.moodle.org/browse/MDL-72706) - Change default value of "Hidden sections" course format setting
- [MDL-72115](https://tracker.moodle.org/browse/MDL-72115) - Rename "Miscellaneous" category to "Category 1"
- [MDL-72119](https://tracker.moodle.org/browse/MDL-72119) - Make "Enable xxxxx" features consistent (hide menus for disabled features)

### For administrators

- [MDL-71347](https://tracker.moodle.org/browse/MDL-71347) - Add a filter to "browse list of users" for date of user account creation
- [MDL-72031](https://tracker.moodle.org/browse/MDL-72031) - Separate out max_time for audio and video files in Atto/RecordRTC
- [MDL-71515](https://tracker.moodle.org/browse/MDL-71515) - Improve the test outgoing mail configuration admin page
- [MDL-67686](https://tracker.moodle.org/browse/MDL-67686) - Add more filters to task log (/admin/tasklogs.php)
- [MDL-72984](https://tracker.moodle.org/browse/MDL-72984) - Ensure support email address is mandatory
- [MDL-73592](https://tracker.moodle.org/browse/MDL-73592) - MoodleNet integration now enabled by default
- [MDL-71621](https://tracker.moodle.org/browse/MDL-71621) - Parent role cannot edit custom fields in child profile
- [MDL-73918](https://tracker.moodle.org/browse/MDL-73918) - Allow admins to change the page width using custom SCSS
- [MDL-71927](https://tracker.moodle.org/browse/MDL-71927) - Logs and question attempt history now show time to the second, to help investigate issues
- [MDL-71466](https://tracker.moodle.org/browse/MDL-71466) - Custom user field support: Admin role screens (check permissions, assign)
- [MDL-72619](https://tracker.moodle.org/browse/MDL-72619) - Provide admin page to view cache size estimates
- [MDL-67822](https://tracker.moodle.org/browse/MDL-67822) - New check_database_schema performance check
- [MDL-70271](https://tracker.moodle.org/browse/MDL-70271) - Dropbox token and Permission Updates
- [MDL-58395](https://tracker.moodle.org/browse/MDL-58395) - LDAP auth sync now skip and report problematic user accounts
- [MDL-72251](https://tracker.moodle.org/browse/MDL-72251) - Tasks admin UI now shows time to nearest second

### Mobile

- [MDL-67807](https://tracker.moodle.org/browse/MDL-67807) - Return concurrent sessions information to apply concurrent login limit in the mobile app
- [MDL-69555](https://tracker.moodle.org/browse/MDL-69555) - Make duration of QR login and auto-login time between requests configurable
- [MDL-73794](https://tracker.moodle.org/browse/MDL-73794) - Update the footer in the mobile view

### Performance

- [MDL-72596](https://tracker.moodle.org/browse/MDL-72596) - Caching: Track cache I/O size in perfdebug
- [MDL-69088](https://tracker.moodle.org/browse/MDL-69088) - Make file cache store purges instant with a safe and async purge
- [MDL-68164](https://tracker.moodle.org/browse/MDL-68164) - Additional caching of pg_field_type postgres field metadata
- [MDL-63983](https://tracker.moodle.org/browse/MDL-63983) - Improve the performance of non-contact searches in messaging when site-wide messaging is disabled (default)
- [MDL-71014](https://tracker.moodle.org/browse/MDL-71014) - Cache the siteidentifier and site contextid in local cache
- [MDL-72328](https://tracker.moodle.org/browse/MDL-72328) - Add TTL support for Redis caches
- [MDL-72837](https://tracker.moodle.org/browse/MDL-72837) - Cache API should support versioned data

## Security improvements

- [MDL-56873](https://tracker.moodle.org/browse/MDL-56873) - Set more secure defaults for the cURL allow/deny lists
- [MDL-66776](https://tracker.moodle.org/browse/MDL-66776) - Send notifications when new devices are used to log in into the site
- [MDL-71627](https://tracker.moodle.org/browse/MDL-71627) - Add check API for anti virus and optionally remove admin notifications
- [MDL-71806](https://tracker.moodle.org/browse/MDL-71806) - Improved the UX of the Moodle security report
- [MDL-71176](https://tracker.moodle.org/browse/MDL-71176) - New password and change forms should have autocomplete="new-password"

## For developers

- [MDL-61460](https://tracker.moodle.org/browse/MDL-61460) - Introduce the UI components library
- [MDL-74229](https://tracker.moodle.org/browse/MDL-74229) - Add navigation node keys to allow themers to hide navigation tabs
- [MDL-74235](https://tracker.moodle.org/browse/MDL-74235) - Rename the icons for activities to allow support of multiple icons for multiple versions
- [MDL-74033](https://tracker.moodle.org/browse/MDL-74033) - Allow full customisation of the primary navigation
- [MDL-72779](https://tracker.moodle.org/browse/MDL-72779) - Set more than one value on a persistent at the same time
- [MDL-70862](https://tracker.moodle.org/browse/MDL-70862) - Implement a new callback to extend gradebook plugininfo
- [MDL-72289](https://tracker.moodle.org/browse/MDL-72289) - Allow callers to customise the rendered icon of inplace editable elements
- [MDL-73347](https://tracker.moodle.org/browse/MDL-73347) - Allow themes to define un-addable blocks
- [MDL-46778](https://tracker.moodle.org/browse/MDL-46778) - Allow use a separate DB configuration (not just prefix) for Behat similar to PHPUnit
- [MDL-73270](https://tracker.moodle.org/browse/MDL-73270) - Warn where XMLRPC is currently in use
- [MDL-67228](https://tracker.moodle.org/browse/MDL-67228) - Tool_replace maturity set

### Web service additions and updates

- [MDL-71135](https://tracker.moodle.org/browse/MDL-71135) - Create core_course_get_state web service
- [MDL-71165](https://tracker.moodle.org/browse/MDL-71165) - Create core_course_update_course web service

### Core plugins removed

- [MDL-71473](https://tracker.moodle.org/browse/MDL-71473) - Jabber removed as a standard notification plugin
- [MDL-58939](https://tracker.moodle.org/browse/MDL-58939) - Picasa repository and portfolio removed from core
- [MDL-72335](https://tracker.moodle.org/browse/MDL-72335) - Tool_health removed from core
- [MDL-72615](https://tracker.moodle.org/browse/MDL-72615) - Boxnet plugins removed from core
- [MDL-72616](https://tracker.moodle.org/browse/MDL-72616) - Quiz results block removed from core
- [MDL-72348](https://tracker.moodle.org/browse/MDL-72348) - Microsoft OneDrive (legacy) repository (repository_skydrive) removed from core
- [MDL-72347](https://tracker.moodle.org/browse/MDL-72347) - Word censorship filter (filter_censor) removed from core
- [MDL-72407](https://tracker.moodle.org/browse/MDL-72407) - VideoJS Flash plugin removed from core
- [MDL-72042](https://tracker.moodle.org/browse/MDL-72042) - Flash animation media player removed from core
- [MDL-72041](https://tracker.moodle.org/browse/MDL-72041) - WebCT question import format removed from core
- [MDL-72517](https://tracker.moodle.org/browse/MDL-72517) - Examview question import format removed from core

### Deprecations

- [MDL-53544](https://tracker.moodle.org/browse/MDL-53544) - Typo3 library removed
- [MDL-72004](https://tracker.moodle.org/browse/MDL-72004) - Quiz 4.0 Class renaming and deprecation
- [MDL-73756](https://tracker.moodle.org/browse/MDL-73756) - Deprecate $modinfo param to completion_info::get_data()
- [MDL-65799](https://tracker.moodle.org/browse/MDL-65799) - Phase 2 of deprecation of functions in lib/deprecatedlib.php initially deprecated in 3.8
- [MDL-71175](https://tracker.moodle.org/browse/MDL-71175) - Deprecate some plagiarism functions that are not used, or have replacements
- [MDL-66266](https://tracker.moodle.org/browse/MDL-66266) - Remove deprecated functions in messages/classes/api.php
- [MDL-72098](https://tracker.moodle.org/browse/MDL-72098) - deprecate grade_grade::insert method that just calls its parent
- [MDL-72433](https://tracker.moodle.org/browse/MDL-72433) - Final deprecation of get_grades() in lib/classes/grades_external.php
- [MDL-71476](https://tracker.moodle.org/browse/MDL-71476) - Remove mysql_engine.php
- [MDL-65252](https://tracker.moodle.org/browse/MDL-65252) - Final deprecations of forum_count_replies and get_forum_discussion_posts
- [MDL-67412](https://tracker.moodle.org/browse/MDL-67412) - Remove deprecated functions in lib/setuplib.php
- [MDL-65801](https://tracker.moodle.org/browse/MDL-65801) - Remove strings deprecated in 3.8

### Component API updates

- [admin/tool/generator/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/admin/tool/generator/upgrade.txt)
- [admin/tool/log/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/admin/tool/log/upgrade.txt)
- [admin/tool/mobile/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/admin/tool/mobile/upgrade.txt)
- [admin/tool/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/admin/tool/upgrade.txt)
- [admin/tool/usertours/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/admin/tool/usertours/upgrade.txt)
- [admin/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/admin/upgrade.txt)
- [analytics/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/analytics/upgrade.txt)
- [auth/shibboleth/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/auth/shibboleth/upgrade.txt)
- [availability/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/availability/upgrade.txt)
- [backup/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/backup/upgrade.txt)
- [badges/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/badges/upgrade.txt)
- [blocks/section_links/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/blocks/section_links/upgrade.txt)
- [blocks/tag_youtube/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/blocks/tag_youtube/upgrade.txt)
- [blocks/timeline/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/blocks/timeline/upgrade.txt)
- [blocks/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/blocks/upgrade.txt)
- [cache/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/cache/upgrade.txt)
- [calendar/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/calendar/upgrade.txt)
- [completion/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/completion/upgrade.txt)
- [contentbank/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/contentbank/upgrade.txt)
- [course/format/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/course/format/upgrade.txt)
- [course/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/course/upgrade.txt)
- [customfield/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/customfield/upgrade.txt)
- [dataformat/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/dataformat/upgrade.txt)
- [enrol/database/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/enrol/database/upgrade.txt)
- [enrol/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/enrol/upgrade.txt)
- [filter/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/filter/upgrade.txt)
- [grade/grading/form/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/grade/grading/form/upgrade.txt)
- [grade/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/grade/upgrade.txt)
- [group/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/group/upgrade.txt)
- [h5p/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/h5p/upgrade.txt)
- [lib/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/lib/upgrade.txt)
- [media/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/media/upgrade.txt)
- [message/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/message/upgrade.txt)
- [mod/assign/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/assign/upgrade.txt)
- [mod/book/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/book/upgrade.txt)
- [mod/feedback/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/feedback/upgrade.txt)
- [mod/forum/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/forum/upgrade.txt)
- [mod/glossary/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/glossary/upgrade.txt)
- [mod/h5pactivity/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/h5pactivity/upgrade.txt)
- [mod/lesson/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/lesson/upgrade.txt)
- [mod/lti/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/lti/upgrade.txt)
- [mod/page/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/page/upgrade.txt)
- [mod/quiz/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/quiz/upgrade.txt)
- [mod/resource/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/resource/upgrade.txt)
- [mod/scorm/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/scorm/upgrade.txt)
- [mod/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/upgrade.txt)
- [mod/url/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/url/upgrade.txt)
- [mod/wiki/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/wiki/upgrade.txt)
- [mod/workshop/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/mod/workshop/upgrade.txt)
- [my/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/my/upgrade.txt)
- [payment/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/payment/upgrade.txt)
- [plagiarism/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/plagiarism/upgrade.txt)
- [portfolio/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/portfolio/upgrade.txt)
- [question/bank/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/question/bank/upgrade.txt)
- [question/behaviour/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/question/behaviour/upgrade.txt)
- [question/engine/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/question/engine/upgrade.txt)
- [question/format/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/question/format/upgrade.txt)
- [question/type/multichoice/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/question/type/multichoice/upgrade.txt)
- [question/type/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/question/type/upgrade.txt)
- [question/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/question/upgrade.txt)
- [report/eventlist/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/report/eventlist/upgrade.txt)
- [report/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/report/upgrade.txt)
- [repository/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/repository/upgrade.txt)
- [search/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/search/upgrade.txt)
- [theme/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/theme/upgrade.txt)
- [user/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/user/upgrade.txt)
- [webservice/upgrade.txt](https://github.com/moodle/moodle/blob/v4.0.0/webservice/upgrade.txt)

## See also

- [Moodle 3.11 release notes](https://docs.moodle.org/dev/Moodle_3.11_release_notes)
