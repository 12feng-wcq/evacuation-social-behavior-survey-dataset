# Emergency Evacuation Social Behavior Questionnaire Dataset

## 1. Overview

During emergency evacuation, individual behavior is influenced not only by environmental conditions, hazard levels, and evacuation goals, but may also be affected by social relationships with accompanying individuals. When evacuating with family members, friends, or romantic partners, individuals may exhibit behaviors such as waiting for companions, moving together, adjusting movement speed, maintaining companion distance, and changing their original evacuation strategies according to the state of their companions.

This questionnaire focuses on the above social behaviors and is mainly used to investigate individual behavioral preferences in terms of risk perception, waiting, companion movement, distance maintenance, and behavioral adjustment under different social relationship conditions. The survey results also provide a data basis for calculating related social behavior parameters and calibrating evacuation models.
The dataset contains **506 valid questionnaires**, and the complete questionnaire consists of **102 items**.


## 2. Questionnaire Design and Structure

### 2.1 Questionnaire Design

Based on social behavior phenomena during emergency evacuation and the requirements of subsequent behavioral modeling, the questionnaire was designed around the following five aspects:

| Behavioral Aspect | Main Content |
| --- | --- |
| Risk-Time Perception | Risk perception and time pressure |
| Social Relationship Influence | Social influence strength |
| Waiting Behavior | Waiting tendency, maximum waiting time, waiting trigger distance, and maximum waiting distance |
| Companion Behavior | Companion tendency and desired companion distance |
| Behavioral Adjustment and Switching | Exit proximity, local congestion, passage obstruction, waiting duration, and risk perception |

The questionnaire mainly focuses on the following three types of stable social relationships:

- Family members
- Friends
- Romantic partners

Some items also include strangers as a reference condition to analyze behavioral differences between stable social relationships and unfamiliar individuals.
The family, friend, and romantic-partner conditions were answered by the same participants. Therefore, the corresponding data constitute repeated-measures data from the same participants.


### 2.2 Questionnaire Structure

The complete questionnaire contains **102 items**, organized as follows:

| Item Range | Main Content |
| --- | --- |
| Q1–Q7 | Basic demographic information, emergency evacuation knowledge, physical condition, and related experience |
| Q8–Q17 | Risk perception, time urgency, and general evacuation behavior judgment |
| Q18–Q20 | Daily accompanying situations in public places |
| Q21–Q48 | Social relationship influence and evacuation behavior preferences under different relationship conditions |
| Q49–Q69 | Waiting behavior, waiting time, waiting distance, and conditions for terminating waiting |
| Q70–Q84 | Companion behavior, companion coordination, and companion distance maintenance |
| Q85–Q99 | Behavioral adjustment, safety-companionship trade-offs, and behavioral switching |
| Q100–Q102 | Initial distance under different social relationships during normal walking |

The questionnaire includes five-point behavioral preference items, binary-choice items, categorical-choice items, time-interval items, and distance-interval items.

Most five-point behavioral preference items use a response scale ranging from “Strongly Disagree” to “Strongly Agree.” Time- and distance-related items are mainly used to obtain behavioral time and distance parameters with practical meanings.
The complete 102 questionnaire items and all response options are provided in:
`questionnaire.pdf`


## 3. Data Collection and Sample Characteristics

The questionnaire survey was conducted online through the **Wenjuanxing** platform in **May 2026**, using convenience sampling to recruit participants.
A total of **600 questionnaires** were collected. Based on response completeness, obvious patterned responses, and logical consistency among related items, **94 invalid questionnaires** were excluded. Finally, **506 valid questionnaires** were retained, corresponding to a valid response rate of **84.33%**.

The basic characteristics of the valid sample are shown below:

| Variable | Category | Number | Percentage |
| --- | --- | ---: | ---: |
| Gender | Male | 244 | 48.22% |
|  | Female | 262 | 51.78% |
| Age | 18 years or younger | 69 | 13.64% |
|  | 19–30 years | 208 | 41.11% |
|  | 31–40 years | 110 | 21.74% |
|  | 41–50 years | 69 | 13.64% |
|  | 51 years or older | 50 | 9.88% |
| Education Level | Primary school or below | 15 | 2.96% |
|  | Junior high school | 26 | 5.14% |
|  | Senior high school or vocational school | 161 | 31.82% |
|  | College or undergraduate degree | 240 | 47.43% |
|  | Master's degree or above | 64 | 12.65% |

Because convenience sampling was used in this survey, the questionnaire data are mainly intended to identify emergency evacuation behavior preferences under different social relationship conditions and to support model parameter calibration. They should not be used to infer behavioral proportions of the general population in real disaster situations.


## 4. Questionnaire Data Analysis and Behavioral Parameters

### 4.1 Data Quality and Statistical Methods

Based on the five predefined behavioral aspects, **29 core behavioral items** were selected from the complete questionnaire for internal consistency analysis:

| Behavioral Aspect | Corresponding Items |
| --- | --- |
| Risk-Time Perception | Q8, Q9, Q10, Q13, Q14, Q15 |
| Social Relationship Influence | Q28, Q32, Q33, Q37, Q38, Q42 |
| Waiting Behavior | Q49, Q50, Q51, Q52, Q53, Q54 |
| Companion Behavior | Q73, Q76, Q77, Q78, Q79 |
| Behavioral Adjustment and Switching | Q85, Q86, Q87, Q88, Q96, Q97 |

The Cronbach's α values for the five behavioral aspects are shown below:

| Behavioral Aspect | Cronbach's α |
| --- | ---: |
| Risk-Time Perception | 0.830 |
| Social Relationship Influence | 0.856 |
| Waiting Behavior | 0.904 |
| Companion Behavior | 0.898 |
| Behavioral Adjustment and Switching | 0.714 |

In addition, KMO and Bartlett's tests were performed on the above 29 items:

- **KMO: 0.904**
- **Bartlett's approximate chi-square: 6836.454**
- **Degrees of freedom: 406**
- **p < 0.001**

The five behavioral aspects were predefined during the questionnaire design stage according to emergency evacuation behavior phenomena and modeling requirements. Therefore, the above analyses were mainly used to evaluate the internal consistency and overall correlation of the related items, rather than to redefine the questionnaire dimensions through statistical analysis.

For behavioral differences among the family, friend, and romantic-partner conditions, the **Friedman test** was first used for overall comparison. When the overall difference was statistically significant, paired **Wilcoxon signed-rank tests** were further conducted for pairwise comparisons. The **Holm method** was used for multiple-comparison correction, and **Kendall's W** was used to describe effect size.


### 4.2 Behavioral Parameter Calculation

The questionnaire results were further used to convert participants' reported behavioral preferences into quantitative social behavior parameters.
For five-point behavioral preference items, the original scores were normalized to the range `[0,1]`:
`x' = (x - 1) / 4`

The corresponding mapping is shown below:

| Original Score | Normalized Value |
| ---: | ---: |
| 1 | 0.00 |
| 2 | 0.25 |
| 3 | 0.50 |
| 4 | 0.75 |
| 5 | 1.00 |

When multiple questionnaire items were used to represent the same behavioral parameter, the normalized values of the corresponding items were averaged with equal weights.

Time- and distance-related parameters were calculated using weighted averages based on the representative values of each response interval and the observed response frequencies. For bounded intervals, the midpoint of the interval was used as the representative value.


### 4.3 Main Behavioral Parameters

The main relationship-specific behavioral parameters obtained from the questionnaire are shown below:

| Behavioral Parameter | Family | Friend | Romantic Partner |
| --- | ---: | ---: | ---: |
| Overall Social Influence Strength | 0.687 | 0.637 | 0.670 |
| Waiting Tendency | 0.694 | 0.646 | 0.686 |
| Maximum Waiting Time / s | 15.372 | 13.666 | 14.227 |
| Waiting Trigger Distance / m | 3.895 | 3.887 | 3.857 |
| Maximum Waiting Distance / m | 7.262 | 7.098 | 7.479 |
| Companion Tendency | 0.684 | 0.616 | 0.614 |
| Desired Companion Distance / m | 0.726 | 1.017 | 0.747 |

In addition, the questionnaire yielded the following behavioral adjustment parameters shared across different relationship types:

| Behavioral Parameter | Parameter Value |
| --- | ---: |
| Risk Perception Weight | 0.692 |
| Time Pressure Weight | 0.610 |
| Overall Social Influence Weight | 0.709 |
| Exit Proximity Influence Weight | 0.693 |
| Local Congestion Influence Weight | 0.709 |
| Passage Obstruction Influence Weight | 0.687 |
| Waiting Duration Influence Weight | 0.717 |
| Risk Perception Behavioral Adjustment Weight | 0.702 |

These parameters are used to establish the correspondence between subjective behavioral preferences reported in the questionnaire and quantitative behavioral variables used in evacuation models.


## 5. Repository Files and Data Usage

This repository mainly contains the following files:

| File | Description |
| --- | --- |
| `questionnaire.pdf` | Complete questionnaire containing Q1–Q102 and all response options |
| `survey_responses.xlsx` | Complete response data from 506 valid questionnaires |
| `README.md` | Description of questionnaire design, sample characteristics, data structure, and data usage |

The Excel dataset contains the complete responses of **506 valid participants to Q1–Q102**.
The publicly released dataset does not contain direct personal identifiers such as names, identification numbers, telephone numbers, or email addresses.

The dataset can be used for research on social behavior in emergency evacuation, comparison of behavioral preferences under different social relationship conditions, analysis of waiting and companion behaviors, companion-distance research, social behavior parameter calculation, and related evacuation model calibration.


## 6. Citation

If you use this questionnaire or dataset in academic research, please cite the corresponding research paper.

The complete citation information will be added here after the paper is formally published.
