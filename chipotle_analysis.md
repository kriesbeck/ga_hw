# Class 2 Homework:  Command Line Chipotle

1. Look at the head and the tail of chipotle.tsv in the data subdirectory of this repo. Think for a minute about how the data is structured. 
 What do you think each column means? What do you think each row means? Tell me! (If you're unsure, look at more of the file contents.)

 ```
 head chipotle.tsv

 tail chipotle.tsv
 ```

 The data set is tabular with 5 columns and 4623 rows.  The first row contains column headers.  
 The data detail the contents of orders at Chipotle (one row for each separate component of an order).
  * order_id: unique id for the order 
  * quantity: number of items ordered
  * item_name: name of item ordered
  * choice_description: personalization of item ordered
  * item_price: total price of each item
 
2. How many orders do there appear to be?
 
 ```
 sort chipotle.tsv | tail chipotle.tsv
 ```
 
 There are 1834 orders.
 
3. How many lines are in this file?
 
 ```
 wc -l chipotle.tsv
 ```
 
 4623
 
4. Which burrito is more popular, steak or chicken?
 
 ```
 grep -i 'Steak Burrito' chipotle.tsv | wc -l
  
 grep -i 'Chicken Burrito' chipotle.tsv | wc -l
 ```

 There are 368 steak burritos and 553 chicken burritos, so chicken is more popular.

5. Do chicken burritos more often have black beans or pinto beans?

 ```
 grep -i 'Chicken Burrito' chipotle.tsv | grep -i 'Black Beans' | wc -l

 grep -i 'Chicken Burrito' chipotle.tsv | grep -i 'Pinto Beans' | wc -l
 ```
 
 Black beans - there are 282 chicken burritos with black beans and 105 with pinto beans.

6. Make a list of all of the CSV or TSV files in the DAT10 repo (using a single command). 
 Think about how wildcard characters can help you with this task.

 ```
 find . -name *.?sv
 ```
  ./data/airlines.csv
  ./data/bank-additional.csv
  ./data/bikeshare.csv
  ./data/chipotle.tsv
  ./data/drinks.csv
  ./data/hitters.csv
  ./data/imdb_1000.csv
  ./data/sms.tsv
  ./data/titanic.csv
  ./data/ufo.csv
  ./data/vehicles_test.csv
  ./data/vehicles_train.csv
  ./data/yelp.csv

7. Count the approximate number of occurrences of the word "dictionary" 
 (regardless of case) across all files in the DAT10 repo.

 ```
 grep -ir 'dictionary' ./DAT-DC-10 | wc -l
 ```

 There are currently 91 instances of 'dictionary' in the repo.

8. Optional: Use the the command line to discover something "interesting" about the Chipotle data. 
 Try using the commands from the "advanced" section!
