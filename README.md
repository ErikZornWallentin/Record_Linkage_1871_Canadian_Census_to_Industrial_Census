# Record Linkage 1871 Canadian Census to Industrial Census
****************************************************
	Author: Erik Zorn - Wallentin.
	Last Edit: April. 4 / 2017.
	
	** IMPORTANT NOTE: The 3.6 million record data is unable to be uploaded on my free GitHub account, if you want to see the full working data and full results please email me at erikzornwallentin@gmail.com/questions/2972212/creating-an-empty-list-in-python
	Since I cannot upload the large dataset, the program will not work.				
	
	Results: Provided in the same directory this README is in. 
	For each specific "pass" results they have their own folder.
	For the FULL results of first pass see: "firstpass_matches.xlsx" or "firstpass_nomatches.xlsx" in First Pass Results folder.
	For the FULL results of second pass see: "secondpass_matches.xlsx" or "secondpass_nomatches.xlsx" in Second Pass Results folder.
	For the FULL results of possible matches see: "possible_matches.xlsx" or "possible_nomatches.xlsx" in Possible Matches Results folder.
	
	My code is all in the Python file called "a.py" which contains more info below:
	*** IMPORTANT READ *** 
	The code will probably not compile on your computer because of the import settings, please change the import settings based on your computer!
	Which is probably not the same way yours is setup!
	
	Python libraries being used:
	Openpyxl, csv, re, sys, timeit, datetime, time
	
	*** IMPORTANT READ *** 
		
	This program was created for CIS*4910 record linkage project with Luiza Antonie.
		
	The program will attempt to perform record linkage with several passes.
	1. First pass requirements: Hard coded district range see a.py and change lower and upper range in menu option "1", also needs files "1871full.txt" and "industrial.csv" in project directory to work.
	2. Second pass requirements: Hard coded district range see a.py and change lower and upper range in menu option "2", also needs files "1871full.txt" and "firstpass_nomatches.csv" in project directory to work.
	3. Possible matches requirements: Hard coded district range see a.py and change lower and upper range in menu option "3", also needs files "1871full.txt" and "secondpass_nomatches.csv" in project directory to work.
	
	The program contains error checking in the menu.
		
	It starts off by waiting for user input with a menu displayed to the user.
	Menu:
		1) First pass
		2) Second pass
		3) Find Possible Matches
		4) Quit the program (q)
	Choosing an option from the menu will allow you to do a specific task and you will need to wait for it to complete.
	Once it gives you the result from the task it will return you to the menu.
	
	Example Use:
		Choose menu option 3.
		It has hard coded file and district range so see a.py and menu option "3" to change.
		NOTE: Need "1871full.txt" and "firstpass_nomatches.csv" in project directory to work.
		Wait a for districts filtering and record linkage to finish.
		New excel file called "possible_matches.xlsx" will be created based on district range to be viewed.
		Choose a new menu option to do any more tasks.
		
	Limitations:
	- For safe record linkage and not run into memory issues, only compile from a range of 50 districts at once, do not do 1-206 (max district range) or it will crash because of Openpyxl library.
	- Does not handle matching of people from different districts.
	- Everything is hard coded, so not user friendly and programmer will need to change district range and files inside of the a.py file in the menu options as described above.
	
	References:
	https://openpyxl.readthedocs.io/en/default/
	http://stackoverflow.com/questions/2972212/creating-an-empty-list-in-python
	http://stackoverflow.com/questions/53513/best-way-to-check-if-a-list-is-empty
	https://docs.python.org/2/library/re.html
	https://docs.python.org/2/library/time.html
	https://docs.python.org/2/library/sys.html
	https://docs.python.org/2/library/datetime.html
	
****************************************************