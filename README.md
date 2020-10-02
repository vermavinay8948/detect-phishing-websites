# Phishing website detection - phishing is a crime..we have to stop it.


This experiment was created using machine learning algorithms with turicreate. 

Data set in this experiment was taken from the 'Machine Learning Repository'.


Machine Learning Repository: https://archive.ics.uci.edu/ml/datasets/Phishing+Websites

turicreate: https://github.com/apple/turicreate

## Accuracy Results  - Machine learning algorithms

1. Boosted Decision Tree = 0.913~  (Lowest)
2. Decision Tree         = 0.926~
3. K Nearest Neighbour   = 0.939~ (Highest)
4. Logistic Regression   = 0.928~ 

## Script

```terminal
  $ python script.py
  
  [1] Boosted decision tree
  [2] Decision tree
  [3] Nearest neighbour
  [4] Logistic regression
  
  Select ML Algorithm: 1
  
  Finished parsing file dataset.csv
  Parsing completed. Parsed 100 lines in 0.041388 secs.
  ------------------------------------------------------
  Inferred types from first 100 line(s) of file as
  column_type_hints=[int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int,int]
  If parsing fails due to incorrect types, you can correct
  the inferred type list above and pass it to read_csv in
  the column_type_hints argument
  ------------------------------------------------------
  Finished parsing file dataset.csv
  Parsing completed. Parsed 11055 lines in 0.035361 secs.
  PROGRESS: Creating a validation set from 5 percent of training data. This may take a while.
            You can set ``validation_set=None`` to disable validation tracking.
  
  Boosted trees classifier:
  --------------------------------------------------------
  Number of examples          : 8365
  Number of classes           : 2
  Number of feature columns   : 30
  Number of unpacked features : 30
  +-----------+--------------+-------------------+---------------------+-------------------+---------------------+
  | Iteration | Elapsed Time | Training-accuracy | Validation-accuracy | Training-log_loss | Validation-log_loss |
  +-----------+--------------+-------------------+---------------------+-------------------+---------------------+
  | 1         | 0.012667     | 0.909265          | 0.892019            | 0.505161          | 0.509974            |
  | 2         | 0.019960     | 0.917753          | 0.908451            | 0.401738          | 0.406688            |
  +-----------+--------------+-------------------+---------------------+-------------------+---------------------+
  
  
  >>> Accuracy         : 0.9165194346289752
```

## Usage

  ```terminal
  $ git clone https://github.com/danrevah/detect-phishing-websites.git
  $ cd detect-phishing-websites
  $ pip install virtualenv
  $ source venv/bin/activate
  $ pip install -r requirements.txt
  $ python script.py
  ``` 
 
## DataSet--Required attributes
Based on the following attributes: 

 * having_IP_Address  { -1,1 } 
 * URL_Length   { 1,0,-1 } 
 * Shortining_Service { 1,-1 } 
 * having_At_Symbol   { 1,-1 } 
 * double_slash_redirecting { -1,1 } 
 * Prefix_Suffix  { -1,1 } 
 * having_Sub_Domain  { -1,0,1 } 
 * SSLfinal_State  { -1,1,0 } 
 * Domain_registeration_length { -1,1 } 
 * Favicon { 1,-1 } 
 * port { 1,-1 } 
 * HTTPS_token { -1,1 } 
 * Request_URL  { 1,-1 } 
 * URL_of_Anchor { -1,0,1 } 
 * Links_in_tags { 1,-1,0 } 
 * SFH  { -1,1,0 } 
 * Submitting_to_email { -1,1 } 
 * Abnormal_URL { -1,1 } 
 * Redirect  { 0,1 } 
 * on_mouseover  { 1,-1 } 
 * RightClick  { 1,-1 } 
 * popUpWidnow  { 1,-1 } 
 * Iframe { 1,-1 } 
 * age_of_domain  { -1,1 } 
 * DNSRecord   { -1,1 } 
 * web_traffic  { -1,0,1 } 
 * Page_Rank { -1,1 } 
 * Google_Index { 1,-1 } 
 * Links_pointing_to_page { 1,0,-1 } 
 * Statistical_report { -1,1 } 
 * Result  { -1,1 }
