# Casper, Wyoming Standardized Testing Approach Investigation

## Business Case

The city of Casper, Wyoming has commissioned a team to review nationwide ACT and SAT standardized test data in an effort to identify potential areas of policy improvement.  Casper is the main constituent of the Natrona County School District (NCSD), which is the second largest school district in the state.   The mayor is committed to exploring all opportunities to improve the outcomes for the city's high school students.  Unfortunately, he only had a single spreadsheet with Natrona County ACT information from 2017, which he provided to the team reviewing the data.  The ACT is currently mandatory in Wyoming, but it is possible that the choice of ACT over SAT may be limiting students in some way.  The city is asking for this analysis to determine if they should lobby the state to change to requiring the SAT, if the city should try and fund both tests, or if any other changes, based on the data, are recommended.

## Description of data
### Files Chosen:
* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State with section scores ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))

* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State with section scores ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))

* [`sat_act_by_college.csv`](./data/sat_act_by_college.csv): Ranges of Accepted ACT & SAT Student Scores by Colleges ([source](https://www.compassprep.com/college-profiles/))

* [`NCSD_2017.xlsx`](./data/NCSD_2017.xlsx): Data provided by the mayor of Casper with ACT score data from 2017.

### Data Dictionary

DataFrames:
- `act_sat` ACT and SAT data from states including scores and participation rates
- `tests_by_college` College admissions standardized test data

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**act_participation**|*float64*|2017 ACT Scores by State|ACT participation rate for the state| 
|**act_english**|*float64*|2017 ACT Scores by State|ACT English section score (from 1 to 36) | 
|**act_math**|*float64*|2017 ACT Scores by State|ACT Math section score (from 1 to 36) | 
|**act_reading**|*float64*|2017 ACT Scores by State|ACT Reading section score (from 1 to 36) | 
|**act_science**|*float64*|2017 ACT Scores by State|ACT Science section score (from 1 to 36) | 
|**act_composite**|*float64*|2017 ACT Scores by State|ACT Composite score (average of section scores)| 
|**sat_participation**|*float64*|2017 SAT Scores by State|SAT participation rate| 
|**sat_read_write**|*int64*|2017 SAT Scores by State|SAT Evidence-Based Reading and Writing section score (range 200–800)| 
|**sat_math**|*int64*|2017 SAT Scores by State|SAT Math section score range (200–800)| 
|**sat_total**|*int64*|2017 SAT Scores by State|SAT total score between range (400-1600)| 
|**test_opt**|*string*|Ranges of Accepted ACT & SAT Student Scores by Colleges|Indicates if testing is optional (Yes/No)| 
|**applicants**|*int64*|Ranges of Accepted ACT & SAT Student Scores by Colleges|Number of applicants to the school| 
|**accept_rate**|*float64*|Ranges of Accepted ACT & SAT Student Scores by Colleges|Acceptance rate of the school| 
|**sat_25p**|*float64*|Ranges of Accepted ACT & SAT Student Scores by Colleges|25th percentile of total SAT score for School acceptance | 
|**sat_75p**|*float64*|Ranges of Accepted ACT & SAT Student Scores by Colleges|75th percentile of total SAT score for School acceptance | 
|**act_25p**|*float64*|Ranges of Accepted ACT & SAT Student Scores by Colleges|25th percentile of composite ACT score for School acceptance | 
|**act_75p**|*float64*|Ranges of Accepted ACT & SAT Student Scores by Colleges|75th percentile of composite ACT score for School acceptance | 
|**act_med**|*float64*|Ranges of Accepted ACT & SAT Student Scores by Colleges|Calculated median composite ACT score for School acceptance | 
|**sat_med**|*float64*|Ranges of Accepted ACT & SAT Student Scores by Colleges|Calculated median total SAT score for School acceptance | 

## Analysis Summary
To inform decisions around the questions the city was asking, analysis was centered around standardized test scores and participation rates from all 50 states and the District of Columbia.  Wyoming was compared to the national score data as well as other states with 100% ACT participation for the reported year.  That information was cross-referenced with data from 405 colleges to see how the mean scores of Wyoming may impact college admissions for schools that listed their ACT and SAT score information.  This information, led to the following conclusions and recommendations:

## Conclusions and Recommendations
1. Most states have a clear preference for one test over the other. The ACT has an overall participation rate higher than the SAT, but there appears to be a regional preference as well.  
    - ACT participation is high in the central part of the United States.
    - SAT participation is higher in mostly coastal states, especially the northeast.
1. Some states with the highest participation rates, especially 100% participation, underperformed the national average scores by quite a bit. For either test, the highest mean scores were produced by states with the lowest participation rates.
1. Wyoming's mean scores are below the national average ACT score, but above average for the SAT. However, when compared to other states with 100% ACT participation, Wyoming outperforms those states on both tests.
    - For Natrona County & Casper, based on ACT scores (no data for SAT), they would be at or above the median for 
    - Based on their ACT scores, they would be at or above the median test score for 2.7% of colleges reviewed.
    - Based on their SAT scores, they would be at or above the median test score for 43.7% colleges reviewed.

Recommendations drawn from these conclusions:
- There was no evidence that pointed to a clear advantage in picking the SAT over the ACT.  Both tests are widely accepted by colleges and cover many of the same materials.
- Further, no evidence indicated that additionally requiring the SAT would improve testing scores, as it was found that states with 100% participation rates performed worse on the required test compared to the national mean.
    - There are no states that have 100% participation in both tests.  The three states that have high participation in both underperform compared to the national and Wyoming mean scores.
- While the ACT is still required, adding the ability for students to additionally take the SAT may improve ACT scores.  This would also allow students that are seeking post-secondary education opportunities to take advantage of some of the benefits outlined by the referenced articles, as to not limit any potential opportunities for students:
    - High scores (if received) could be a differentiator for college admission.
    - Certain financial aid may require standardized test scores even if the college does not.
    - Provides college admissions personnel more data about the applicant.
- Wyoming should consider a study on removing the ACT test mandate.  As stated above, overall mean test scores tend to fall below national performance with states that have 100% participation rates. Since Wyoming has it's own standardized test to measure school performance statewide, removing the ACT requirement should not interfere with other outcome related policy and decisions.



### Sources of additional information:

- "WDE FAQ - Assessment" Wyoming Department of Education, [https://edu.wyoming.gov/wp-content/uploads/2022/07/2022-FAQ-Assessment-FINAL.pdf](https://edu.wyoming.gov/wp-content/uploads/2022/07/2022-FAQ-Assessment-FINAL.pdf). Accessed November 2022.

- "SAT vs ACT: Which Test is Right for You?" The Princeton Review, [https://www.princetonreview.com/college/sat-act](https://www.princetonreview.com/college/sat-act). Accessed November 2022.

- "4 Reasons to Take BOTH the SAT and ACT" The Princeton Review, [https://www.princetonreview.com/college-advice/4-reasons-to-take-both-sat-and-act](https://www.princetonreview.com/college-advice/4-reasons-to-take-both-sat-and-act). Accessed November 2022.

- Moody, Josh. "ACT vs. SAT: How to Decide Which Test to Take" U.S. News & World Report, 20 March 2021, [https://www.usnews.com/education/best-colleges/articles/act-vs-sat-how-to-decide-which-test-to-take](https://www.usnews.com/education/best-colleges/articles/act-vs-sat-how-to-decide-which-test-to-take). Accessed November 2022.

- "SAT vs. ACT: Which Should I Take?" Coursera, 4 May 2022, [https://www.coursera.org/articles/sat-vs-act](https://www.coursera.org/articles/sat-vs-act). Accessed November 2022.