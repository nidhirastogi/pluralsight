# pluralsight

CSVs imported to sqlite server.
Took a alook at the database comprising the  4 csv files. Will be using the file named"user_assessment_scores" for identifying different kinds of similarities. The other 
The csv table called "course_tags" is more of an extension table that provides description of course_tags and will not be used for finding various similarities. It is a useful one to get a pointer back to which course exactly the users were assessed on, but I'm not using it at the moment for the purpose of this exercise.


Some simple similarities that could be done are as follows. I've created pandas for some of them (bold), but not all, as they follow similar routine:
Simple similarity statistics :
-> user_handle similarities by creating groups by "level" of the user (from table user_course_views)
-> user_handle similarities by creating groups by "interest tags", one or more (from table user_interests)
and so on.

A more fun exercise to find similarities between users is to find one where we find most similar user engagement vectors based on their assessment scores.

Using kNN



