# Module 3 Challenge - PyPoll
## Purpose
Apparently, the results of an election were brought into question once again.  The purpose of this analyis is to audit the raw election results from three separate counties to validate the winner, and to provide additional insights on the voter turnout by county.
## Results

The following is a copy of the script's output:
```
Election Results
-------------------------
Total Votes: 369,711
-------------------------

County Votes:
Jefferson: 10.5% (38,855)
Denver: 82.8% (306,055)
Arapahoe: 6.7% (24,801)

-------------------------
Largest County Turnout: Denver
-------------------------
Charles Casper Stockham: 23.0% (85,213)
Diana DeGette: 73.8% (272,892)
Raymon Anthony Doane: 3.1% (11,606)
-------------------------
Winner: Diana DeGette
Winning Vote Count: 272,892
Winning Percentage: 73.8%
-------------------------
```
- The total number of votes cast was **369,711**
- The breakdown of votes for each county and the percentage share can been seen in the **County Votes** section above
- The county with the largest number of votes was **Denver**
- The breakdown of votes for each candidate and the percentage share can been seen above
- The winner of the election was **Diana DeGette** with **272,892** votes, or **73.8%** of the vote share.

## Summary Statement
The script above could immediately benefit the election commission for re-use in future elections. It offers a number of benefits over using Excel / VBA.  Primarily, its performance will be much better, especially when used in a larger election with millions of votes.  Secondly, the python script can be used, maintained, and improved outside of the data set (for example, by pushing it into GitHub) for use in other elections.  This would allow the public to review the code in addition to the results.  Some other ways in which the script could be improved:

- If the order of the columns are different from election to election, the user could first be prompted to input the column numbers of the relevant headers. For example, the prompt might say 
    ```
    Please enter the column number that corresponds to 'County': 2
    Please enter the column number that corresponds to 'Candidate Name': 3
    ```

- If multiple .csv files are needed for the analysis, the script could be modified to take in any number of files in the `Resources` folder, and aggregate the results for all files.  This would prevent the user from needing to run the script for every file.
