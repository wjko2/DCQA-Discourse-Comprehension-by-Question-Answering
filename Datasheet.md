# Why was the dataset created?


Questions that arise as human read through articles (Ko et al., 2020; Westera et al., 2020) may later be answered in the article itself, forming a connection in the discourse. Compared to existing QA datasets, these questions are products of higher-level (semantic and discourse) processing (e.g.,“how” and “why” questions) whose answers are typically in the form of complex linguistic units like whole sentences. Such reader-generated questions are far out of reach from the capabilities of systems trained on current QA datasets, suggesting that human discourse comprehension is still on another level from that of automated systems. We create this dataset to provide training data for this kind of questions, and also help machine understand the discourse structure of articles.

# Who funded the creation of the dataset?
This work was supported by NSF Grant IIS1850153.



# What are the instances?

The dataset contains articles and its corresponding questions. Each question has a specified anchor sentence and an answer sentence, so that the question arises from the anchor sentence and could be answered by the answer sentence. The question describes the discourse relation between the anchor and answer sentence.


# How many questions are there?

We collect 22394 questions over 602 articles. 20942 questions for training,  718 for validation, and 734 for testing.


# What data does each instance consist of? 
"ArticleID" field denotes the article number in the article folder. "Question" field consist of the question. “AnchorSentenceID“ is the sentence ID of the source sentence. "AnswerSentenceID " field consist of the sentence ID of  the answer sentence. 

# Does the data rely on external resources?
We release the WSJ and AP articles. Since Newsela is copyrighted, please obtain permission from newsela (https://newsela.com/data) first, and then send me an email to ask for the articles (wjko@outlook.com).



# Are there recommended data splits or evaluation measures?

We include the recommended train, development, and test sets for our datasets. Each split is constructed such that there are no overlapping annotators nor articles between each set. 
We include two versions of training set, one of them includes all data and in the other we remove articles that overlap with the INQUISITIVE test set. We also provide the the INQUISITIVE test set for external evaluation

# How was the dataset collected?

We collect data using Amazon mechanical turk. To ensure quality, we designed a qualification task consisting of one article. We manually inspected the quality of the responses of each candidate, and only workers who asked satisfactory questions were invited to continue with the task. Throughout the process, we also monitored the responses of the workers and reminded them about specific guidelines when necessary. The workers are paid around $10/hr


# Who was involved in the collection process and what were their roles?
We recruit crowdworkers from Amazon Mechanical Turk to annotate the training set. We let undergrad linguistic students annotate the validation and test set.
 At a high level, data collection consists of two simultaneous tasks: question generation given an answer sentence, and question linking that places the question in a precise anchor point in the document. Annotators start from the beginning of the article. For each new sentence, they write a question that reflects the main purpose of the new sentence and indicates how the new sentence elaborates on prior context. The new sentence is thus the answer to the question. Because the question should arise from one of the previous sentences in the article, the annotator also chooses which earlier sentence most naturally evokes the question (which we refer to as the question’s “anchor” sentence). We instructed annotators to ask open-ended questions that require some explanation as an answer, instead of questions that could be answered simply by a place/person/time or yes/no. They are also told that when writing the question, they should assume that the question could be asked and understood by people only reading the earlier sentences, following the QUD framework. This means avoiding reference to any information first introduced in the new sentence and avoiding copying phrases only used in the new sentence. Reusing phrases from or referencing previous sentences is allowed. 

# Over what time frame was the data collected?
The dataset was collected over a period of May to June 2021.
# Does the dataset contain all possible instances? 



# What preprocessing / cleaning was done?
We use the articles from the INQUISITIVE dataset and did not do further preprocessing, except we used Stanford CoreNLP to parse all articles into sentences .


# Does this dataset collection/preprocessing procedure achieve the initial motivation? 
Our collection process indeed achieves our initial goals of creating a training set for answering QUD style questions, as shown in the experiment results of our paper. Using this data, we are able to achieve better accuracy on INQUISITIVE compared to existing datasets. 



# How is the dataset distributed? 
It is available at https://github.com/wjko2/DCQA-Discourse-Comprehension-by-Question-Answering




# When was it released?
Februrary 2022 

# What license (if any) is it distributed under? 
Our collected questions are distributed under the CC BY- SA 4.0 license.


# Who is supporting and maintaining the dataset? 

The dataset will be maintained by the authors of the paper.


# Were workers told what the dataset would be used for and did they consent?

We explained the goals we want to achieve to crowd workers during data collection. They also consented to have their responses used in this way through the Amazon Mechanical Turk Participation Agreement.

