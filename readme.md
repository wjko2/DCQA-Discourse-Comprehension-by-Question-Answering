
# DCQA: Discourse Comprehension by Question Answering
During reading comprehension, questions that arise as human read through articles (Ko et al., 2020; Westera et al., 2020) may later be answered in the article itself, forming a connection in the discourse. Compared to existing QA datasets, these questions are products of higher-level (semantic and discourse) processing (e.g.,“how” and “why” questions) whose answers are typically in the form of complex linguistic units like whole sentences. Such reader-generated questions are far out of reach from the capabilities of systems trained on current QA datasets, suggesting that human discourse comprehension is still on another level from that of automated systems. We create this dataset to provide training data for this kind of questions, and also help machine understand the discourse structure of articles.


# Data
train.json, val.json, test.json are the DCQA training, validation and test set.

inquisitive.json is the INQUISITIVE test set. 

Since the articles in INQUISITIVE test set overlap, we also release train-remove-inq.json which is a version of DCQA training set with overlapping articles removed.


All sentence IDs start from 1.

More description of the dataset can be found in Datasheet.md.


**Citation:**
```
@InProceedings{ko2022dcqa,
  author    = {Ko, Wei-Jen and Dalton,Cutter  and Simmons,Mark and  Fisher,Eliza and Durrett, Greg and Li, Junyi Jessy},
  title     = {Discourse Comprehension: A Question Answering Framework to Represent Sentence Connections},
  booktitle = {Proceedings of the 2022 Conference on Empirical Methods in Natural Language Processing},
  year      = {2022},
}
```




# Article Sources
WSJ: 51\~259, 551\~590, 696\~900, 1446\~1491

Newsela: 1\~50, 260\~550, 901\~1050, 1492\~1500

AP: 591\~695, 1051\~1445



Since the articles are copyrighted, please send us an email to ask for the articles (wjko@outlook.com, jessy@utexas.edu).  For Newsela please obtain permission from newsela (<href>https://newsela.com/data</href>) first before emailing us.


