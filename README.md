# Module 3 Challenge - PyPoll
## Purpose
Apparently, the results of an election were brought into question once again.  The purpose of this analyis is to audit the raw election results from three separate counties to validate the winner, and to provide additional insights on the voter turnout by county.
## Results

The following is a copy of the script's results:
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
The script above could immediately benefit the election commission for re-use in future elections. It offers a number of benefits over using Excel / VBA.  Primarily, its performance will be much better, especially when used in a larger election with millions of votes.  Secondly, the python script can be used, maintained, and improved outside of an Excel file for use in other elections.  Some ways in which the script could be improved:

- If the order of the columns are different from election to election, the user could first be prompted to input the column numbers of the relevant headers. For example, the prompt might say 
    ```
    Please enter the column number that corresponds to 'County': 2
    Please enter the column number that corresponds to 'Candidate Name': 3
    ```

- If multiple .csv files are needed for the analysis, the script could be modified to take in any number of files in the `Resources` folder, and aggregate the results for all files.





The raw results were provided in a .csv file with over 369,000 rows.  Each row contains the following information:
```
Ballot ID,County,Candidate
```
Where `Ballot ID` is an anonymous identifier for the person casting the vote, `County` is the county where the ballot was cast, and `Candidate` is one of three possible candidates. A sample row of data looks like this:
```
4714965,Arapahoe,Raymon Anthony Doane
```

In order to parse and analyze the data, a python script was used, in conjunction with the `csv` module.  This guaranteed re-usability and improved performance over Excel & VB Script. 

The script reads through every row once, incrementing the vote count for each of three candidates as well as the three counties.  Both sets of results are stored in dictionaries:
```
candidate_votes = { "Candidate Name": Num_Votes}
county_votes = {"County Name": Num_Votes}

```
Where `Num_Votes` is an integer holding the vote count.

After the script collects the results into the above dictionaries, a new text file `analysis\election_analysis.txt` is opened in write mode to collect the results.  A few simple calculations are made using the vote totals for each county and candidate, and the results are written to this file.  The same results are also written to the console, for debugging purposes.




