Overview and Motivation

The included Jupyter notebook deals with several questions that I as a beginning Data Scientist with
a non-technical educational background have such as how my background might or might not limit me and what kinds of skills are most important to focus on. I figured that many others might have the same sorts of questions.

Files
kernel.ipynb                      A Jupyter notebook where the work was done
README.md                         The file you are reading
input/multipleChoiceResponses.csv The survey data used

Libraries used
Seaborn       Create plots and charts
Numpy         For a few issues with numbers
Pandas        Read csv, group/compare data

Methodology

Business Understanding- Career change is a common thing today. This CNBC headline proclaims <a href="https://www.cnbc.com/2016/04/26/career-change-is-the-new-normal-of-working.html">"career change is the new normal of working."</a> A common statistic is the average person will have 5-7 careers in their lifetime though some would <a href="https://www.wsj.com/articles/SB10001424052748704206804575468162805877990"> consider this dubious.</a> Regardless of the actual statistics, the truth is career change is quite common and undergoing the process personally, I can relate to the concerns.

Data Science has often been the "sexiest job" to have. There is a lot of hype about it and many people seeking a new career are likely to be attracted to it. As I move into a data science career, I find myself wrestling with the questions listed in the motivation section above.

Data Understanding- To attempt to answer these questions, we'll look at <a href="https://www.kaggle.com/kaggle/kaggle-survey-2018"> The 2018 Kaggle Survey Data</a>, specifically the multipleChoiceResponses.csv file a csv with 23860 rows and 395 columns. The first row is the text of the question and the remaining rows each represent an individual survey participant. The columns represent the 50 questions asked of each respondent. When a question can have multiple answers selected each answer has it's own column.

Data Preparation- The data we're presented is in great shape. In many cases it can be used as is, a great testament to the work Kaggle does to make the data usable. In the end two changes will be necessary for our work. 1) To remove the first row from the set. 2) To convert the answers to Question 9 from a str denoting a range of compensation to a int of the average of that range.

Modeling- A simple comparison of mean salary based on response to certain questions is sufficient to tell us what we need to know.

Results- Relating undergraduate majors to salary provided an unexpected result in that CS majors were the second lowest average salary (only better than IT). When we removed current students (many weren't making money) and separate countries with low average salaries from countries with high average salaries the averages evened out quite a bit. We have some outliers but it would seem we should treat them as just that.

Relating coding experience and ML experience to salary shows that both make you a high earner over time. But the point at which you are likely to earn more than the average worker with no skill in the area happens much faster with ML.

Relating the answer to the question "Do you consider ML models to be "black boxes" with outputs that are difficult or impossible to explain?" yields an interesting if not (perhaps ironically) easy to interpret result. I take a stab at one possibility (that type of ML worked with has an affect) but there doesn't seem to be any data to back it up.

Deploy- These insights are shared on a blog post found at https://medium.com/@rntrapnell/this-shocking-new-data-will-make-you-rethink-the-path-to-the-sexiest-job-of-2019-cbc0d1b42175

Acknowledgements
Thanks to Mark Lindsay for his review of the blog and helping me to refine the conclusions further.

Thanks to Kaggle for putting together such easy to use data. Clean data is such a joy to work with.

Thanks to all the folks at Udacity who work to give us the coding, ML and other skills to succeed.
