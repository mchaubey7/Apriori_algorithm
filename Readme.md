Apriori or Association rule mapping :-

Association rule mining is a technique to identify underlying relations between different items. It is really about people who bought this also bought something else, who watched this also watched something else or who did something also did something else.
It analyzes this whole association rule when things comes in pair, in triplicates or any number. They are combined together for some reason, apriori looks for those rules and ways this happened.
This rules helps in business. For Example In supermarket usually the management tries to keep such products far from each other because it is understandable that if the two products hold strong association then other will be bought if one is bought. But while going from one corner to other customer tends to buy some other products also, which give more business to supermarket. While on while streaming platforms such videos are suggested by platform only so user can find related content and watch that easily and giving more business to the streaming platform.
In association rule mining we can come with many rules for association but some of them are weaker and some of them are stronger. we need to find the strength of these rule and use in our business or requirements accordingly.

For the algorithm we have 3 things support, confidence and lift
1. Support : It refers to the default popularity of an item and can be calculated by finding number of transactions containing a particular item divided by total number of transactions. Suppose we want to find support for item M. This can be calculated as:
	
	support(M)=data_containing_M /total_data

2. Confidence : It refers to the likelihood that an item M1 is also bought if item M2 is bought. It can be calculated by finding the number of transactions where M1 and M2 are bought together, divided by total number of transactions where M1 is bought. Mathematically, it can be represented as:	
	
	confidence(M1->M2)=data_containing_M1_&_M2/data_containing_M1
	
3. Lift : Lift(M1 -> M2) refers to the increase in the ratio of sale of M2 when M1 is sold. Lift(M1 –> M2) can be calculated by dividing Confidence(M1 -> M2) divided by Support(M2). Mathematically it can be represented as:
	lift(M1->M2)=confidence(M1->M2)/support(M2)
	lift is increase in prediction that if M1 happens then probability of M2
	
Algorithm : 
	Step 1 : Set a minimum support and confidence
	Step 2 : Take all the subsets in dataset having higher support than minimum support 
	Step 3 : Take all the rules of these subsets having higher confidence than minimum confidence
	Step 4 : Calculate lift and sort the rule by decreasing lift