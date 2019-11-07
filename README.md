# WeakestLink
Scrapes employees from a LinkedIn company page, performs a number of clean up steps to remove any junk and then generates a range of possible username formats so they can be used in username enumeration and password attacks.

** Use of this extension is against LinkedIn TOS and your account may be restricted. **

Firefox support coming soon!

Currently the following clean up actions are performed:

* Normalises any NFD characters for example ó to o
* Removes any none printable ASCII characters
* Downloads a file of postnominals (Which is updated frequently) and removes them
* Removes any separators and quotes
* Removes any data after a comma or curly bracket
* Removes the dot that follows a hidden surname
* Attempts to identify the first and last name of user (Might not be great for international companies!)
* Converts to lowercase and trims any redundant white space

As the first and last name fields on LinkedIn are free form text fields then there can be any random combination of data in them. Please ensure you check over the exported list as there will be dodgy names still

## Installation

1. From the Chrome store - https://chrome.google.com/webstore/detail/weakestlink/jiobcfh amdgbhhhnkmoblghheddjfnpo  - Recommended as this will auto-update
2. Load unpacked extension
    * Clone repository
    * Browse to "chrome://extensions/"
    * Enable Developer mode
    * Click Load Unpacked extension and select the folder where you cloned the repository to

## Usage

* Sign into LinkedIn
* Browse to the required company page
* Click 'See all ### employees on LinkedIn'
* If there are more than 1000 results (100 pages) then use the filters to reduce the number and run multiple dumps
* Click the Dump Users button
* The target page will be scraped and will move onto the next page until there are no more results or the max limit is hit.
* Once the scraping is complete a message box will popup and a CSV with containing the results will be downloaded
* If you need to cancel the dump then close the LinkedIn tab
