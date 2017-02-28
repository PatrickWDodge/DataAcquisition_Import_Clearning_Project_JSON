# Springboard_5.3json
Springboard project 5.3 json

Questions and response:

(1) Find the 10 countries with most projects

This is a simple matter of finding the top 10 country names that appear the most; it can be accomplished by using the value_counts() method on the 'countryname' column, then using the head() method to choose the first 10. 

(2) Find the top 10 major project themes (using column 'mjtheme_namecode')

This was accomplished by creating a new dataframe which contains the project codes and their associated name (this dataframe will also be used in question 3). By attributing each row in the ''mjtheme_namecode' columnn, we can use the method json_normalize() to flatten each entry and then use pandas append() method to add the row to the new dataframe. Finally, the top 10 most common themes is found by using the same methodology as demonstrated in the response to question 1. 

(3) In 2. above you will notice that some entries have only the code and the name is missing. Create a dataframe with the missing names filled in.

First, a dictionary of the key, value pairs was created (with the codes representing the keys, and the project names representing the values). Then, using that dictionary, we iterate over the dataframe created in question 2, and any names that are empty strings are filled by using the dictionary. Finally, I demonstrate that the values have been filled by calling the top 11 values (the 122 previously missing values are no longer present). 
