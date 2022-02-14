
# DCQA: Discourse Comprehension by Question Answering
During reading comprehension, questions that arise as human read through articles (Ko et al., 2020; Westera et al., 2020) may later be answered in the article itself, forming a connection in the discourse. Compared to existing QA datasets, these questions are products of higher-level (semantic and discourse) processing (e.g.,“how” and “why” questions) whose answers are typically in the form of complex linguistic units like whole sentences. Such reader-generated questions are far out of reach from the capabilities of systems trained on current QA datasets, suggesting that human discourse comprehension is still on another level from that of automated systems. We create this dataset to provide training data for this kind of questions, and also help machine understand the discourse structure of articles.


train.json, val.json, test.json are the DCQA training, validation and test set.
inquisitive.json is the INQUISIIIVE test set. 
Since the articles in INQUISIIIVE test set overlap, we also release train-remove-inq.json which is a version of DCQA training set with overlapping articles removed.
articles.zip are the articles.
Note that this dataset and INQUISITIVE use different sentence segmentation, so the sentence IDs in inquisitive.json refers to the segmentation in  https://github.com/wjko2/INQUISITIVE/blob/master/article.zip instead of the one in this repo.
All sentence IDs start from 1.
More description of the dataset can be found in datasheet.md.

**Citation:**
```
@InProceedings{ko2021dcqa,
  author    = {Ko, Wei-Jen and Dalton,Cutter  and Simmons,Mark and  Fisher,Eliza and Durrett, Greg and Li, Junyi Jessy},
  title     = {Discourse Comprehension: A Question Answering Framework to Represent Sentence Connections},
  booktitle = {arxiv},
  year      = {2021},
}
```




# Article Sources
WSJ: 51\~259, 551\~590, 696\~900, 1446\~1491

Newsela: 1\~50, 260\~550, 901\~1050, 1492\~1500

AP: 591\~695, 1051\~1445


We release the WSJ and AP articles.

Since Newsela is copyrighted, please obtain permission from newsela (<href>https://newsela.com/data</href>) first, and then send me an email to ask for the articles (wjko@outlook.com).


