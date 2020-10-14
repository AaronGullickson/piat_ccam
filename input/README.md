# Data Source Description

The data here come from the [Climate Change in the American Mind](https://climatecommunication.yale.edu/visualizations-data/americans-climate-views/)(CCAM) survey administered by the Yale Progam on Climate Communication.

The CCAM has been administered to a representative sample of US adults aged eighteen and over every year from 2008 to 2018. The survey was self-administered by respondents in a web interface. 

The sample sizes each year have varied between roughly 830 and 2164 respondents, but have typically included slightly over 1000 respondents. We will use data that includes all survey waves in order to maximize sample size, but you should be aware that there may be changes in public opinion over time that complicate our results.

From the original CCAM data, I have extracted and recoded the following variables for our use as an analytical dataset. To load this dataset in R, you just need to run the setup code chunk in the full_report.Rmd R Markdown document. The name of the dataset in R is `ccam`.

* **cc_happening**: This is an ordinal variable in which the respondent was asked "Do you think that global warming is happening?". Respondents could say No, Don't Know, or Yes. We consider the Don't Know category to be intermediate between yes and no. For the final analysis in the models, you will analyze yes vs all other responses, where yes is scored as a 1 and all other responses as zero.
* **income**: The income of the respondent in 1000s of US dollars. In actuality, respondents were asked to select from a range of income bracket. I have converted this into a quantitative variable by taking the midpoint value of each bracket. For example, if the range was from $50,000 to $59,999, then I assigned the respondent $55,000.
* **party_affil**: The party affilation of the respondent. The choices are Democrat, Republican, Independent, and Other. The Other category includes both respondents who supported a third party and those who said they had no interest in politics.
* **age**: The age of the respondent.
* **gender**: The gender of the respondent. Respondents were only allowed a binary choice of Male or Female. 
* **race**: The race of ther respondent. The survey only report four categories: White, Black, Hispanic, Other.
* **education**: The highest educational degree of the respondent. I have collapsed this into four categories of less than high school, high school diploma, associate's degree, and bachelor's degree or more. 
* **conservative**: This is a five-point scale measuring how conservative the respondent reported being. The zero value indicates respondents who described themselves as "moderate" or "middle of the road." Negative values indicate respondents who identified themselves as liberal while positive values indicate respondents who identified themselves as conservative. 
* **employ_status**: The employment status of the respondent.
