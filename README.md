URL Shortener in Java using Concourse DB

class URLShortener that shortens the given URLs using public method shorten

User Interactive code that creates a database of URLs and their shortened versions

A user can enter a new URL to shorten and also search for existing URLs using the record id or the URL string itself


For unit testing, the following sequence of user inputs can be used for determining if the add and search functionalities designed for the URL Shortener work fine:

Current DB:

+--------------------------------------------------------------------------------------------------------------------------------------+
| Record | expanded                                                                                          | shortened               | 
+--------------------------------------------------------------------------------------------------------------------------------------+
| 1      | https://github.com/cinchapi/concourse/blob/develop/concourse-driver-java/README.md#find           | http://bit.ly/DjqQdB6q5 | 
| 2      | www.google.com/                                                                                   | http://bit.ly/psAwoZkId | 
| 3      | www.google.com                                                                                    | http://bit.ly/psAwoZkId | 
| 4      | http://wiki.cinchapi.com/display/OSS/Concourse+Developer+Setup#ConcourseDeveloperSetup-UseGitBash | http://bit.ly/ATfWZUpvp | 
| 5      | https://mail.google.com/mail/u/1/#inbox/154d38b949bdb89c                                          | http://bit.ly/aLIax1fMe | 
| 6      | www.amazon.com                                                                                    | http://bit.ly/oHYGNGz8c | 
| 7      | www.amazon.com/page1abcgdlkasdklaksj.php                                                          | http://bit.ly/8KQ78UUj1 | 
| 8      | https://www.youtube.com/channel/UCCq1xDJMBRF61kiOgU90_kw                                          | http://bit.ly/Ds0cBaJh7 | 
| 9      | www.linkedIn.com                                                                                  | http://bit.ly/NGP4dekKY | 
| 10     | https://www.netflix.com/browse                                                                    | http://bit.ly/BeeBLPcb0 | 
| 11     | https://www.coursera.org/                                                                         | http://bit.ly/YrNsiJCJF | 
| 12     | www.techcrunch.com                                                                                | http://bit.ly/0Ev0TZlnn | 
| 13     | http://www.espncricinfo.com/ci/content/match/fixtures_futures.html                                | http://bit.ly/JFh2NaiyK | 
| 14     | https://www.facebook.com/nishit.shivhre                                                           | http://bit.ly/T5BK4V3XK | 
+--------------------------------------------------------------------------------------------------------------------------------------+

1. Enter new URL
2. Search for existing URL:
3. Exit: 
1                             //check results for a new URL
Enter URL: www.yahoo.com
Added Record:

+--------------------------------------------------+
| Record | expanded      | shortened               | 
+--------------------------------------------------+
| 15     | www.yahoo.com | http://bit.ly/RgAyDOI7U | 
+--------------------------------------------------+

Do you want to continue(y/n): 
y
1. Enter new URL
2. Search for existing URL:
3. Exit: 
2
1. Enter record id
2. Enter URL
1
Enter record id:
1 //Check results for an existing record id

+----------------------------------------------------------------------------------------------------------------------------+
| Record | expanded                                                                                | shortened               | 
+----------------------------------------------------------------------------------------------------------------------------+
| 1      | https://github.com/cinchapi/concourse/blob/develop/concourse-driver-java/README.md#find | http://bit.ly/DjqQdB6q5 | 
+----------------------------------------------------------------------------------------------------------------------------+

Do you want to continue(y/n): 
y
1. Enter new URL
2. Search for existing URL:
3. Exit: 
2
1. Enter record id
2. Enter URL
1
Enter record id:
19 						//Check results for a record id that does not exist

+--------+
| Record | 
+--------+
+--------+

Do you want to continue(y/n): 
y
1. Enter new URL
2. Search for existing URL:
3. Exit: 
2
1. Enter record id
2. Enter URL
2
Enter URL
www.google.com/ 				//Check results for an existing URL

+----------------------------------------------------+
| Record | expanded        | shortened               | 
+----------------------------------------------------+
| 2      | www.google.com/ | http://bit.ly/psAwoZkId | 
+----------------------------------------------------+

Do you want to continue(y/n): 
y
1. Enter new URL
2. Search for existing URL:
3. Exit: 
2
1. Enter record id
2. Enter URL
2
Enter URL
www.mysite.com 				//Check results for a URL that does not exist

+--------+
| Record | 
+--------+
+--------+

Do you want to continue(y/n): 
y
1. Enter new URL
2. Search for existing URL:
3. Exit: 
3
Exit

