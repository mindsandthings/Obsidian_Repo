# What Sunrise  data mgt entry system does
https://zapier.com/help/troubleshoot/behavior/zap-isnt-being-triggered

https://zapier.com/help/create/basics/why-isnt-my-zap-triggering-on-existing-records

https://zapier.com/help/create/basics/data-deduplication-in-zaps





Or maybe changing the option label in the zap creation process to read "When A Zap Creates Or Updates A Row In Google Spreadsheet"? The option "New Or Update Row In Google Spreadsheet" is misleading because it implies that the zap will trigger when the row is updated, even though it actually only triggers when the row is updated by the zap. 

I have some reservations about doing something complex and multi-stage with zaps, but they would be easier for someone else to maintain than our current custom thousand lines of google apps script, so if you think it can be done I'd be interested in hearing how, and how long you think it would take to set this up (at least to set up the numbered steps). 

1. Send an airtable row to a google sheet when it's new in a particular airtable view (handled by an existing zap)

2. Create a google sheet (sheet #1).

3. Based on two values in the airtable row, check a second google sheet (sheet #2) to determine it contains an entry for those two values, that the entry also contains a URL, and that the URL leads to a google sheet which can be successfully opened (sheet #3). If any of this is not true, send a specific email with some variables from the airtable row and sheet #2 and (if applicable) #3 filled in.

4. Based on a value in the airtable row, look up data in a different google sheet (sheet #4) and copy it into sheet #1. Then, format sheet #1 based on formatting info in sheet #4 (adding checkboxes and setting Google Sheet's inbuilt data validation and formatting for other columns to text, email address, number, and date formats. Which columns are what will be different for different sheets and depends on info in sheet #4.

5. Share the sheet with an email address contained in the email row, but only if the email address is a gmail address. 

6. Email a notification to another email address, with some set text and some variables (data from the airtable, URL of the just-created sheet, info on whether the sheet has already been shared with a gmail address or needs to be shared with a non-gmail address). 

I won't write up the remaining parts unless the previous steps can be done with a zap, but without going into all details, they include waiting for data to be manually entered into sheet #1, sending an email when it's done, then manually checking the newly entered data against regular expressions based on whether sheet #4 specifics that a column in sheet #1 consists of zip codes or phone numbers (neither of which Sheets' inbuilt data validation can handle in the ways we need). The next step involves a separate person manually making corrections to the sheet. When they're done, the data in the sheet need to be added to the end of whichever sheet that this particular sheet is supposed to submit to (based on sheet #3 from before). 


Also: periodically, all of the sheet #3's (I think we're at like...50 now?) need to be automatically submitted to a database. Currently, we do this with a zap for each sheet, although it sounds like using zaps for the purpose of managing 


#z-archives/sunrise
