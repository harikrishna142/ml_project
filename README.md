
## Environment & Installation Steps
Python 3.8 & Pytorch 1.12
```
pip install -r requirements.txt
```
## Run
Execute the following steps in the same environment:
```
python main.py
```
## Dataset Format
Processed dataset format should be a DataFrame as a .pkl file having the following columns:
1. cur_bp_y : Bipolar symptom labels 0~7 
2. fu_30_su_y : suicidality levels 0~3
3. sb_1024 : list of lists consisting of 1024-dimensional encoding for each reddit post.
4. created_utc : list containing the datetime objects corresponding to each reddit post.

## Annotation Process
To label the collected Reddit dataset, we recruited four researchers, who are knowledgeable in psychology and fluent in English, as annotators. With the supervision of a psychiatrist, the four trained annotators labeled 818 users and their 7,592 anonymized Reddit posts using the open-source text annotation tool Doccano. During annotations, we mainly consider two different label categories: (i) BD symptoms (e.g., manic, anxiety) and (ii) suicidality levels (e.g., ideation, attempt). We further annotate the diagnosed BD type (e.g., BD-I, BD-II) for data analysis. If there is any conflict in the annotated labels across the annotators, all the annotators discuss and reach to an agreement under the supervision of the psychiatrists. 

<img src = "img/dataset.png" width="400">
