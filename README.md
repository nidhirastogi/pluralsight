# pluralsight

Here is the written response to the questions asked in the ML Code Challenge by pluralsight:

1. I used the kNN (k Nearest Neighbors) clustering algorithm since it is simple to implemenet and yet can be used in many complex problems w/ high dimensions. In the kNN implementation, I experimented with a few distance measures, and have chosen Manhattan Distance (other options - Cosine (apt for text), Mahalanobis, Manhattan) due to better performance -> lowest accuracy. I converted the data to a 2D matrix, then transformed the data intp scipy sparse matrix for more efficient calculations.Using unsupervised algorithms, we computed nearest neighbors and specify "metric = manhattan". FInally, we fit the model. Later, the model is tested and as an extension, make recommendations determined by the closeness factor of instances. The algorithm then classifies an instance of course_tag by findig its nearest neighbor.
The matrix factorization is used as it allows to discover latent features underlying the interactions b/w users and assessment_tags. I use SVD for identifying these latent features.


2.For large user sample size, and many more features, a few aspects that woud be considered are 
a. the parallel processing of the data using cloud platform which is suported by mapreduce, so that large matrices can be processed in parallel.
b. Dimensionality reduction and identifying components that capture the variance of the data and then transforming incoming new datasets using these components for all further analysis.
c. Anonymization is a challenge in the security world, so ensuring that the user data is protected, hashed, encrypted, based on needs.
d. Fast data access for further analysis requires quick data lookup, and hence a key-value store that can manage the data. Example hadoop, apache spark, etc.

3. Data I will be interested in more about user geographics, age, language, gender, and incorporate this to understad trends in a given area, by a user age range, education level, friends or recommended users network, and so on. This will help form clusters of users that can form a study-group online (recommendation based on this).

------------------

Notes on steps followed:

CSVs imported to sqlite server.
Took a alook at the database comprising the  4 csv files. Will be using the file named"user_assessment_scores" for identifying different kinds of similarities. The other csv table called "course_tags" is more of an extension table that provides description of course_tags and will not be used for finding various similarities. It is a useful one to get a pointer back to which course exactly the users were assessed on, but I'm not using it at the moment for the purpose of this exercise.

Some simple similarities that could be done are as follows. I've created pandas for some of them (bold), but not all, as they follow similar routine (in pluralsight v-1):
Simple similarity statistics :
-> user_handle similarities by creating groups by "level" of the user (from table user_course_views)
-> user_handle similarities by creating groups by "interest tags", one or more (from table user_interests)
and so on.




