Detecting Fraudlent job postings and Job Market Trend Analysis, revolves around understanding the dynamic job market. As industries are rapidly changing, identification of the in-demand skill, differentiation between
technical and soft skill requirements have become critical. Moreover, fraudulent job posting detection will help improve the safety of job seekers. The research questions are targeted at finding legitimate job postings without being scammed, 
methodologies for fraud detection and exploring skill trends. Identification of skill trends and fraud patterns will help businesses design hiring policies, educational institutions design curriculum, and job seekers acquire skills in the right direction to meet market demand and reduce recruitment risks. The job
postings dataset has 17,880 job postings, with 18 columns, containing categorical, textual and boolean fea- tures. The dataset is clean however it needs to be prepro- cessed; it has to be encoded for categorical variables and for text. 

1) Data Selection: The dataset contains 18 features for
17,880 job postings. It has a mix of the textual, categorical
and numerical features for complete overview of each job
listing. Descriptive attributes include title, the location, and
department. Informative fields like company profile, description, requirements, and benefits contain textual information
about a company background, job responsibilities, necessary
qualifications, and benefits.

3) Data Preprocessing : To discover underlying patterns in
the dataset, data visualizations were conducted. Job openings
were seen to be largely full time. Companies with or without
a logo were compared on the number of postings that offer
telecommuting. Most employment postings that contained a
company logo. The distribution of job industries was shown
in the form of bar plots, where the largest proportion of job
postings is in the IT sector, then marketing and advertising, education, then finance and then healthcare. Finally, I compared
required experience across different types of employment and
found that most job postings require that full time employees
have mid to senior level experience. Fraudulent job postings
by the industry, employment type, and telecommuting status
were visualized, and it was shown that the fraudulent postings
are more likely to have less information about the industry,
employment type; (see Fig.1), and telecommuting options.
4) Data Transformation:
• Cleaning Textual data
Unstructured data in textual columns need lots of preprocessing to be made analysis ready. This process involves:
Case Normalization: To ensure uniformity, and avoid
duplicating text due to case sensitivity, text is converted
to lower case.
Tokenization: To make it easier to process further, text is
split up into individual words, or tokens.

4) Data Mining:
• Training and testing are done through Data Splitting :
To perform reliable evaluations of the predictive models,
80 percent of the dataset was used as the training subset
which was split 20 percent as testing subset. All features
but the target variable fraudulent (y) were the independent
variables (X). The train test split function from Scikit
learn library (with a random seed of random state=42 so
that it encourages reproducibility) was used to perform
this division. In addition, the machine learning models
were trained on the training subset (80%) and then tested
on the testing subset (20%). And this strategy is necessary
to assess a model’s ability to generalize.
• Hyperparameter Tuning : Six classification algorithms
were used hyperparameter optimization (Random Forest,
Decision Tree, K-Nearest Neighbors (KNN), AdaBoost,
Gradient Boosting and XGBoost) that attempted to improve the predictive capabilities of these algorithms. The
GridSearchCV is used to perform cross validation, as well
as to search for hyperparameters over a grid for each
model. Thus, we optimized the performance of the model
using parameters on unseen data.
The number of estimators, max tree depth and minimum
samples for splits and leaves for Random Forest was
tuned. The optimization of the Decision Tree has been
based on splitting criteria, depth and minimum sample
size used for splits and leaves. In KNN, we considered
hyperparameters such as number of neighbors, weight
function, and type of algorithm to be KNN hyperparameters. In the case of AdaBoost and Gradient Boosting,
changed the number of estimators, the learning rate, and
the tree depth. For learning rate, maximum depth, child
weight and estimators, XGBoost was tuned.
• Model Training :
Classification for real and fraudlent job postings : Random Forest model is chosen as the model showing
highest accuracy from the tuning phase which was used
to initialize the models with the best performing hyper
parameters. The training dataset (X train, y train) is
fitted and performed training.
Clustering to identify skill trends across industries, revealing patterns in demand : Clustering techniques can be
used to identify skill trends across various job categories,
depicting patterns in the requirement and demand of
particular skills across industries. The appropriate number
of clusters was identified as 8 based on inertia and
silhouette scores using K-means clustering. The word
cloud and top terms for each cluster were then generated,
highlighting distinctive themes. For instance, Cluster 0
emphasized customer and team management skills, while
Cluster 2 highlighted software development and design
expertise. Certain clusters like Cluster 3 and Cluster 4
reflected teaching credentials and marketing proficiencies,
respectively.
Industry representation analysis in clusters identified
dominant industries for each cluster, like ”Education” in
Cluster 3 and ”Marketing” in Cluster 4. Technical versus soft skills comparison across clusters had an interesting
trend: some clusters, like Cluster 2, had more technical
skills, while others, like Cluster 0 and Cluster 4, had a
greater number of soft skills, including management and
communication.
These insights-including the identification of highdemand skill clusters and the differentiation between
technical and soft skills-offer actionable guidance for
educators, policymakers, and job seekers alike. This
would further help institutions tailor their curriculum to
the needs of the industry and would help job seekers
in honing appropriate skills relevant to the industries or
roles they seek to apply to. Additionally, firms can refine
hiring strategies based on the identified skill clusters.
Future work could consider temporal trends that change
the market’s needs, further develop the sentiment and
semantic analysis, and consider more advanced clustering
methods to extract richer insights.

