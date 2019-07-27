# Proof-Of-Vote CodeFunDo++ 2019
<hr></hr>

![Inroduction](https://user-images.githubusercontent.com/44934630/61998454-0844f800-b0ce-11e9-8dc3-856ea4d8d8d3.png)

<h3>What can be done?</h3>

<h1>Decentralized Voting System using the Azure Blockchain</h1>

<h2>Proposals</h2>

1. <h3>Ballot Coin</h3>
 
     Prior to the Elections, the Election commission produces some 'N' number of Ballot Coins based on the number of Eligible
     voters for that specific term. <b>Each voter will be provided 1.0X Ballot coins</b> ( X can be any number that the Election 
     Commission wishes to choose). Each Voter will have to spend 1 Ballot Coin to cast their vote to his/her desired party. 
     This vote casting process is treated as a Transaction between the Voter and the Party and 1 Ballot coin will be 
     transacted to the Party's Wallet.
     
     Each voter is supposed to be given 0.0X Ballot coins for voting, but also each voter's stake depends not only on his vote but also 
     the number of citizens who do not to vote in that particular Constituency. How is this achieved?
     
     Let's consider the case of the 2019 elections in INDIA:-
     
     ![Voters](https://user-images.githubusercontent.com/44934630/61799146-2dc0d000-ae48-11e9-8cb0-a749c41fefc0.png)
     
     We introduce Ballot coins to resolve this issue since the number of Ballot coins each person receives is not only dependent on the people who voted but also on the people who did not.
     
     Let's Scale the problem down to 5 people:-
     
     ![Ballot Coin Schema](https://user-images.githubusercontent.com/44934630/61800748-39fa5c80-ae4b-11e9-8634-d763cdcd7769.png)

     Since the person 'E' did not vote in the second case the stake of the others who have voted has decreased. So instead
     of 0.05 Ballot coins each of the people who voted get only 0.04 beacuse of the person 
     E. This loss incurred by each person will be larger if the number of people increase. This create a constraint between 
     the people to Vote, because there will be pressure from the society to vote as lack of a few votes can decrease each 
     person's stake. 
     
     ![Ballot Coin Scaling](https://user-images.githubusercontent.com/44934630/61804518-a5dfc380-ae51-11e9-86bb-588befe5105f.png)
 
2. <h3>Handling the overload</h3>

   Having 543 Blockchains for 543 Constituencies is practically not ideal, so we can use the concept of <b>Lightning Network</b> and implement it 
   using <b>Micropayment Channels</b>. Each constituency has one Micropayment channel where all the transactions (votes) will be recorded.
   At the end of the Election Process, the Channel will be broken and the transactions will be mined into the Global Blockchain.

<img src="https://user-images.githubusercontent.com/44934630/61872969-4ee5f700-af02-11e9-88eb-a4301f750150.png"/>

3. <h3>Avoiding Multicasting of Votes</h3>
 
    The traditional method of using ink to detect the status of voting is not a fair way to determine if a person has voted or not. We can check the Micropayment Channel for the existence of balance in his/her Wallet of a particular citizen associated with that 
    unique ID.

4. <h3>Dynamic Voter ID</h3>

   Each time a person votes a unique Voter Id is generated by hashing his/her Aadhaar Card, Timestamp, name, etc... and associated to their transaction.


5. <h3>Counting the Votes</h3>

   After election ends we just need to check the total number of Ballot Coins in each party's wallet. 

<h1>Why Old School again?</h1>

![old school](https://user-images.githubusercontent.com/44934630/61998458-1430ba00-b0ce-11e9-975d-d91635db1362.png)
  
<h1>Why does one need any Ballot coins in the first place?</h1>

   <b>People can use these remaining Ballot coins to get subsidy on the Government bills like Gas, Electricity, etc.</b>
