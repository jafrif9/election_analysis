# Election Analysis

## Overview of Project
The following tasks were given by the Colorado Board of Elections, regarding the election audit of a recent local congressional election.
  
  1. Calculate the total number of votes cast.
  2. Get a complete list of candidates who received votes.
  3. Calculate the total number of votes each candidate received.
  4. Calculate the percentage of votes each candidate won.
  5. Determine the winner of the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.10.2, Visual Studio Code 1.65.2

## Summary
The analysis of the election show that:
- There were 369,711 votes cast in the election
- The candidates were:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
- The candidate results were:
    - Charles Stockham received 23.0% of the vote and 85,213 number of votes
    - Diana DeGette received 73.8% of the vote and 272,892 number of votes
    - Raymon Doane received 3.1% of the vote and 11,606 number of votes
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.

Execution of the code provided the following results in the terminal and the text file respectively:

<img width="288" alt="Screen Shot 2022-03-23 at 3 27 38 PM" src="https://user-images.githubusercontent.com/86126331/159795280-b7430528-7f73-45a4-aa42-feac068d5f58.png">


<img width="338" alt="Screen Shot 2022-03-23 at 3 28 18 PM" src="https://user-images.githubusercontent.com/86126331/159795334-e228d7b8-eefd-4b3a-8e67-f85c2bdf6e09.png">


## Challenge Overview
While the module exercise analyzed the election results by vote distribution amongst the candidates, the challenge analyzed the election results by distribution amongst the counties. The basis of the code were similar to that previously written; in essence the use of a list of counties and a dictionary, with the key being the counties and the value being the votes received. 

With slight modifications, the final code written can be used to analyze results from other elections aswell. For instance, the current code has variables pertaining to vote distribution based on counties, as the results were relevant for a congressional election. If looking at a Federal election, the below code could be altered to look at states/provinces instead. The variables would need to be changed, and the format may potentially require modification depending on the actual results themselves. 

    # 6a: Write a for loop to get the county from the county dictionary.
    for county in county_votes:

        # 6b: Retrieve the county vote count.
        county_vote = county_votes[county]
        # 6c: Calculate the percentage of votes for the county.
        county_percentage = float(county_vote) / float(total_votes) * 100
        county_results = (
            f"{county}: {county_percentage:.1f}% ({county_vote:,})\n"
        )

         # 6d: Print the county results to the terminal.
        print(county_results, end="")
         # 6e: Save the county votes to a text file.
        txt_file.write(county_results)
         # 6f: Write an if statement to determine the winning county and get its vote count.
        if (county_vote > largest_county_vote):
            largest_county_vote = county_vote
            largest_county_turnout = county

## Challenge Summary
When analyzing the election results through the challenge code, the following new observations can be made:
- The county results were:
  - Jefferson county received 10.5% of the vote and 38,855 votes in total.
  - Denver county received 82.8% of the vote and 306,055 votes in total.
  - Arapahoe county received 6.7% of the vote and 24,801 votes in total.
- Denver county had the largest number of votes

