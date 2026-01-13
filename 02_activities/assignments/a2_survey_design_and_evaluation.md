# Assignment: Questionnaire Design and Sample Evaluation

## Requirements

The goal of this assignment is to practice developing and evaluating sampling materials.

### Part A - Survey Design:

Select one of the scenarios below and design a survey to meet the need(s) outlined in the prompt.

1.	In two to three sentences, describe the purpose of your survey
2.	Describe your target population, sampling frame, sampling units, and overall sampling strategy.
3.	Write a 5-10 question survey to address your chosen scenario below.

##### Scenarios
1.	You work in the Human Resources Department at a large tech company. Over the past few months, the company has been experiencing a high turnover rate across many of its departments, specifically within the entry- and lower-level positions. The company wishes to understand why this turnover is happening, and what changes need to occur to improve employee satisfaction.
2.	You work for a Canadian national political party during a federal election. Throughout the campaign period, your party has seen relatively high approval ratings, but an opposing party is also polling favorably and may still have a chance to win the election. You are one month away from the election and you want to understand what voters want from your party and its leader in order to maintain your lead and eventually win the election.
3.	You are a student researcher in the sociology department at the University of Toronto. You are working on a research project that concerns the relationship between music taste and age. This involves both comparisons between different people of different ages and comparisons of the same individual at different ages during their lifetime. You wish to understand to what extent age influences music taste, specifically as it relates to perceptions of popular music. Your results will be written into an academic paper that you hope to publish.

### Part B - Survey Evaluation:

For the **Canadian General Social Survey on Giving, Volunteering, and Participating, 2018 (cycle 33)**, conducted by Statistics Canada find any and all available documentation for the data gathered and identify and describe the survey features indicated below.

1. Sample type
```
Per the description of the survey, this is a multi-stage sample survey "with a cross-sectional design". Using phone numbers, the survey first stratifies on census metropolitan areas (e.g., Toronto, Markham, Oakville...), then determines the number of samples that would reflect the CMA with acceptable variability.

The sample unit (a home/cell phone number) is then used to conduct, using simple probability sampling, 1 member per household is randomly selected.
```
2. Sample size
```
The sample size of ~50,000 units was used, and resulted in ~40,000 questionnaires being disseminated (expected 24,000 responses)
````

3. Target population
```
The target population of this survey was every individual older than 15 living in Canadian provinces not living full-time (defined as > 6 months) in institutions.
```
4. Sampling frame
```
According to the documentation, the frame uses Canadian phone numbers that are on file (from previous surveys, census, and other official sources) in conjunction with the "dwelling frame". This combines the information of phone number(s) and associates it with an address if possible. The justification of using this frame is to capture a household as a group using telephone numbers.

Notably, "rejective sampling" was used as it was expected that the population of individuals who volunteer are much fewer than those that do not volunteer. The individuals who are not volunteers are then subsampled.
```
5. Survey mode(s) 
```
This survey was administered through first sending of 40,000 invitation letters, then collected directly from an individual using either online questionnaires or telephone interviewing, averaging around 44 minutes for the survey.
```
6. Timeline
```
This survey is collected every 5 years, with this cycle (33) being from September 4th, 2018 to December 28th, 2018.
```
7. Response rate
```
The response rate was 41.9%
```
8. Weights
```
Being a simple probably sampling survey, each individual can be thought of to represent multiple "unselected" individuals. Since rejective sampling was used, the non-volunteer, non-rejected individuals are weighted by a factor to make up for that process. The weights were also adjusted so that income distribution reflected the results of the Canada Income Survey in the previous year (e.g., so that the overall income of the sample is more reflective of the population). Similarly, other estimates such as age, sex, and other demographics are also accounted for with weighting, to better reflect the general population.

Additionally, the weights are bootstrapped, which means that the data is resampled (with replacement) and then weights are assigned based on the observed variances from that resampling to better capture the population from the survey design.
```
9. Data processing
```
Based on information contained in other Govt' of Canada documents, the data is processed in the Social Survey Processing Environment, which is a generalized, internal pipeline used throughout Stats Canada. Basically, each step of data processing (e.g., receipt of raw data, clean up, recodes, flows, coding, edits and imputations, derived variables, creation of final processing file, creation of dissemination files - per GoC) is established for the survey to maintain consistency. While the exact process is internal, the processing follows the overall above structure.

Within the steps, clean up includes making sure the data is anonymous and removing errors and/or identifiers, while recodes/flows establish how the answers in the data relate to each other and the overall structure of what questions were asked/skipped/missed. Coding is essentially translating a complicated statement or comment to numerical code. Edits and imputations essentially tries to fill in data that might be missing/contradictory/invalid, using different strategies depending on the case. Deriving variables uses the data collected to generate additional information from the raw data (e.g., assigning a generation based on birth year) for more analysis parameters. Finally the results are recorded in the final processing file (internal), and after processing to ensure accuracy and no sensitive information is still retained, disseminated to the public.
```
10. Cleaning, imputation, etc
```
For the cycle 33 GVP survey, the SSPE was used as above, then automatic and manual edits / were made where needed. Data like family structure were checked to see if they made sense, and if the survey data was correct (the example given is checking age against birthday). Flows were checked to make sure the sequence of answers provided was as expected. The Computer-Assisted Telephone Interview system also conducted error detection for those cases, and assigned codes + edits for questions. Manual edits were escalated where the system/interviewer was not able to resolve the errors.

Imputation for missing data was made by selecting the nearest 'donor record' (e.g., a complete, high quality record similar to the one that is missing data) via scoring. Depending on the case, the imputation was either carried out using the closest donor, one randomly selected donor if 1+ were identical in scoring, or if no donors were appropriate, the mean from a pool of donors, while maintaining valid fields for edits.

First, imputation for individual and family income was used where linked tax data from the previous year for a respondent was not present. Then formal volunteering variables were imputed, followed by informal. Then donations and solicitation methods.
```
11. Sources of error
```
Sampling error is present as this was not a complete census (offset by estimating variance through bootstrap weights). Other errors like coverage errors (no permanent phone numbers), non-response error and/or bias from either a household or individual. Other errors such as biases were mainly addressed through questionnaire refinement, using previously established effective methodology, and strict training and quality control.
```
12. Limitations, known biases, etc
```
Some limitations and biases are present (though are presumably small), but those without phone numbers are excluded, non-responders, and biased questions could still be present.
```
13. Link to documentation and any additional sources used
```
Based on the provided information, I used the documentation found here to answer the majority of the sections above:
https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&Id=796234
Information on bootstrap weights was supplemented with information from this technical documents: https://ftp.cdc.gov/pub/health_statistics/nchs/bootstrap/JCUSH/sas/Bootdoc_eng.pdf
For data processing: https://www150.statcan.gc.ca/n1/pub/89-653-x/2018001/dp-td-eng.htm, https://www150.statcan.gc.ca/n1/pub/75-005-m/75-005-m2019001-eng.htm, and https://www150.statcan.gc.ca/n1/pub/89-653-x/2013002/05-eng.htm were used to understand the way that Statistics Canada processes their survey data from a related social survey.
```

# Your Changes

## Part A - Survey Design: 

The number of your chosen topic: `2`

```
2. You work for a Canadian national political party during a federal election. Throughout the campaign period, your party has seen relatively high approval ratings, but an opposing party is also polling favorably and may still have a chance to win the election. You are one month away from the election and you want to understand what voters want from your party and its leader in order to maintain your lead and eventually win the election.
```

Describe the purpose of your survey:
```
The purpose of my survey is to understand the perspective of the voters before the election, and gather responses of what aspects of our leadership and areas of interest and improvement people are satisfied and unsatisfied with. I will then use this information to inform the party of topics and that have been highlighted as important from our voters, and solidify our stances and action plans in advance of the election.
```

Describe your target population, sampling frame, sampling units, and observational units:
```
Target population:
The target population of this survey will be every individual eligible to vote in the coming federal election outlined by this document: https://www.elections.ca/content.aspx?section=vot&dir=bkg&document=ec90518&lang=e

Sampling frame:
I think that the frame established by the Statistic Canada survey above provides a good starting point for the frame that I would like to target. 

Instead of using phone numbers, I would like my frame to include addresses of all voters included in the National Register of Electors, again capturing a household under a single "address", and a randomly selected individual to complete the poll. This would also likely _select_ for  individuals who are eligible to vote for the upcoming election. However, this does present bias in terms of previous voters, those with permanent mailing addresses, and access to computers or a phone line (non-exhaustive list), which would likely need to be considered for with downstream weighting and other processing methods.

Sampling Units, and Observational Units:
I would send out an letter, with a unique code, for the individual at the address to either complete online, or on the telephone with guidelines on confirming there are no proxy answers etc. The sample unit in this case would be an address, and simple probability sampling will be used to select 1 member per sampling unit. The observational unit would be the individual who is selected for the survey in the address.
```

Your 5-10 question survey:
```
All information recorded in this survey is confidential and will not be utilized or shared outside of internal [political party] databases and analyses. The survey results will be stored anonymously and securely for 6 months, after which only bulk statistical data will be retained (see [political party] privacy guidelines). At any point, you may choose to pause the survey and return to it, or abstain from answering.
```
1. Please rate your overall satisfaction with [political party] between 2021-2025.
```
 1    2    3    4    5    6    7    8    9    10
(very unsatisfied)                           (very satisfied)
```
2. Our core platform is to increase the overall quality of life for Canadians, by A) increasing housing affordability, B) increasing job availability, C) reducing the cost of living, D) increasing funding for education, and E) strengthening our public healthcare capacity.
Please rank the impact of each of these aspects from 1 (being the most important) to 5 (being the least important) when deciding your vote for the upcoming federal election.

```
Example: Rank X:  ____F)____

         Rank 1 __________ (most important)
         Rank 2 __________
         Rank 3 __________
         Rank 4 __________
         Rank 5 __________ (least important)
```
3. For each of the above aspects, please indicate your _current_ satisfaction with each from 1 to 10, with 1 being very unsatisfied and 10 being very satisfied. Where possible, please elaborate on the chosen level of satisfaction.

```
A) Housing affordability:
       1    2    3    4    5    6    7    8    9    10
(very unsatisfied)                           (very satisfied)

Comments: _________________________ (250 word limit)


B) Job availability:
       1    2    3    4    5    6    7    8    9    10
(very unsatisfied)                           (very satisfied)

Comments: _________________________ (250 word limit)


C) The cost of living:
       1    2    3    4    5    6    7    8    9    10
(very unsatisfied)                           (very satisfied)

Comments: _________________________ (250 word limit)


D) Educational funding:
       1    2    3    4    5    6    7    8    9    10
(very unsatisfied)                           (very satisfied)

Comments: _________________________ (250 word limit)


E) Public health services:
       1    2    3    4    5    6    7    8    9    10
(very unsatisfied)                           (very satisfied)

Comments: _________________________ (250 word limit)
```

4. Please select the aspect that you view as the _most_ pressing issue for the upcoming election.
```
A) Housing affordability
B) Job availability
C) The cost of living
D) Educational funding
E) Public health services
```

5. Are there additional issues that you would like to see addressed by [political party]?

```
Comments: _________________________ (500 word limit)
```

6. Overall, how likely are you to vote for [political party] in the upcoming election?
```
       1    2    3    4    5    6    7    8    9    10
(very unlikely)                               (very likely)
```
Thank you for your time in filling out this survey. Your response plays a vital part in the continuing effort for us to better represent voters and their challenges at a federal level. Please contact our office at 123-456-6789 from 9AM to 5PM EST daily if any questions or concerns arise.

## Part B - Survey Evaluation:

Identify and describe survey features:

```
Added above within the question framework.
```

## Rubric

-	All required components are present and complete **Complete / Incomplete**
-	Choice of sampling strategy for Part A is justified and related to survey purpose **Complete / Incomplete**
-	Information for Part B is complete and correct **Complete / Incomplete**

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 14 January 2026`
* The branch name for your repo should be: `assignment-2`
* What to submit for this assignment:
    * This markdown file (a2_survey_design_and_evaluation.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<p                                          r_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-2`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
