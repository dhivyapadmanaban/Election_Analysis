# Election_Analysis

## Project Overview
A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote. 

## Resources
- Data source : election_results.csv
- Software : Python 3.9.5 , Visual Studio Code, 1.56.1

## Summary
The analysis of the election show that:
- There weere 369,711 votes cast in the election
- The candidates were:
  - Charles Casper Stockham
  - Diana DeGette
  - Raymon Anthony Doane
- The candidate results were: 
  - Charles Casper Stockham received 23.0% of the votes and 85,213 number of votes.
  - Diana DeGette received 73.8% of the votes and 272,892 number of votes.
  - Raymon Anthony Doane received 3.1% of the votes and 11,606 number of votes.
- The winner of the election was:
  - Diana DeGette, who received 73.8% of the votes and 272,892 number of votes.
  
  
## Challenge Overview
The election commision has requested following additional information to complete the audit.

1. The voter turnout for each county.
2. The percentage of votes from each county out of the total count.
3. The county with the highest turnout.

### Election Audit results
- Total number of votes cast in this election is 369,711.
- Break down of votes by county:
  - Jefferson county registered 38,855 votes which is 10.5%
  - Denver county registered 306,055 votes which is 82.8%
  - Arapahoe county registered 24,801 votes which is 6.7%
- Out of these counties, Denver registered most number of votes.
- Break down of votes by candidates:  
  - Charles Casper Stockham got 23.0% of votes - 85,213 votes
  - Diana DeGette got 73.8% of votes - 272,892 votes
  - Raymon Anthony Doane got 3.1% of votes - 11,606 votes
- Find result of election:
  - -----> Winner: Diana DeGette <----------
  - -----> Winning Vote Count: 272,892 <--------
  - -----> Winning Percentage: 73.8% <----------

![image](https://user-images.githubusercontent.com/83181834/118048284-e82d0a00-b330-11eb-8d39-51d3d4a787f5.png)


## Challenge Summary
While this deliverable is for the Colorado Board of Elections, We can reuse the same script with some modifications for any election commission.
1. Input file name is hardcoded in the script. In case of different file name from new Election commission the same script need to be mofied @ line 9 with new file name.
  - file_to_load = os.path.join( "Resources", **NEWFILENAME**)
2. Also if the new csv file structure is different with header like - << County , Candidate name , Ballot ID >>, we can modify the same script by changing dictionary values in the script. Few sample from the code below:
   - candidate_name = row[**ROWINDEX**]
   - county_name = row[**ROWINDEX**]
3. This script analyze the election data provide results on Candiate and County . However if the new election results file has additional columns - Form of voting (mail in ballot , voting machine ), date of election etc. we can add new functionality and reuse similar calculation performed on Candidate and county results. 
4. It is easy to re use the same code on election analysis history file to find Turn out rate in every election year. We can run the same calculation based on year to find voter Turn out for every election .



