<!-- # Arabic-Offensive-Multi-Platform-SocialMedia-Comment-Dataset-->

# Arabic Offensive Comments dataset from Multiple Social Media Platforms.

This release includes annotated social media comment dataset with (not)offensive (OFF vs NOT_OFF) language tags for Arabic social media comments collected from three different online platforms: Twitter, Facebook and YouTube. The dataset is referred as Multi Platforms Offensive Language Dataset **(MPOLD)**.
In addition to the offensive comments, the contents are manually annotated to analyse the distribution of hate speech (HS) and vulgar (but not hate) (V) content.

<!--The distribution of the dataset is presented below:
![Platform wise distribution of offensive and not offensive labels](link-to-image)-->


## Annotation Guidelines and Procedure
The annotation of the collected dataset is obtained using Amazon Mechanical Turk (AMT). To ensure the quality of the annotation and language proficiency, we utilised two different evaluation criteria of the annotator. For more details, check the below paper:

The guideline is available in the `annotation_guideline` folder and can also be cited using the below paper.

<!-- Will be available in the proceedings of LREC2020: -->

```
@inproceedings{chowdhury2020offensive,
  title={A Multi-Platform Arabic News Comment Dataset for Offensive Language Detection},
  author={Chowdhury, Shammur Absar  and Mubarak, Hamdy and Abdelali, Ahmed and Jung, Soon-gyo and Jansen, Bernard J and Salminen, Joni},
  booktitle={Proceedings of the International Conference on Language Resources and Evaluation (LREC'20)},
  year={2020}
}
```


## Data Format
The input file contains have the following fields (separated by tabs), including
`<Id>\t<Platform>\t<Comment>\t<Majority_Label>\t<Agreement>\t<NumOfJudgementUsed>\t<Total_Judgement>\t<Vulgar:V/HateSpeech:HS/None:->`

where
`Id` is the comment id (series)

`Platform` indicates the origin of the social media comment. Values includes: Twitter, Facebook, YouTube

`Comment` raw comments (anonymised for UserID and some urls)

`Majority_Label` include binary labels: Non-Offensive or Offensive. The label is the final label agreed by at least 2 (out of 3) annotators

`Agreement` field include values showing if there was 100% agreement between the annotator or the label was assigned by majority voting (2/3 annotator agreed).

`NumOfJudgementUsed` the number indicates how many annotator's judgement was used for the majority consensus.

`Total_Judgement` total number of judgement obtained from MTurk (this number also includes the rejected assignments).

`Vulgar:V/HateSpeech:HS/None:-` includes the further classification (by expert) of the offensive comments, mentioning if the comment is either hate speech (HS), vulgar (V) or just offensive (-).

Please note the HS can be vulgar but comments which contain vulgar language but not a hate speech is indicated by V.


## Other Resources
In addition to the dataset mentioned in the above paper, we also studied the use of this dataset individually or in combination with other freely available dataset available for offensive study in Arabic language.

The resources used in the study are:
* For out-of-domain evaluation

[Egyptian Arabic dialect data](http://alt.qcri.org/~hmubarak/offensive/TweetClassification-Summary.xlsx)
```
Mubarak, H., Darwish, K., and Magdy, W. (2017). Abusive language detection on Arabic social media. In Proceedings of the First Workshop on Abusive Language Online,
pages 52–56.
```

[Levantine Hate Speech and Abusive (L-HSAB) dataset](https://github.com/Hala-Mulki/L-HSAB-First-Arabic-Levantine-HateSpeech-Dataset)
```
Mulki, H., Haddad, H., Ali, C. B., and Alshabani, H. (2019). L-hsab: A levantine twitter dataset for hate speech and abusive language. In Proceedings of the Third Workshop on Abusive Language Online, pages 111–118
```

* For additional cross-platform evaluation

[Deleted Comments Dataset](http://alt.qcri.org/~hmubarak/offensive/AJCommentsClassification-CF.xlsx)
```
Mubarak, H., Darwish, K., and Magdy, W. (2017). Abusive language detection on Arabic social media. In Proceedings of the First Workshop on Abusive Language Online,
pages 52–56.
```

<!-- ## Fields present in the dataset -->

While using the dataset, cite:


```
@inproceedings{chowdhury2020offensive,
  title={A Multi-Platform Arabic News Comment Dataset for Offensive Language Detection},
  author={Chowdhury, Shammur Absar  and Mubarak, Hamdy and Abdelali, Ahmed and Jung, Soon-gyo and Jansen, Bernard J and Salminen, Joni},
  booktitle={Proceedings of the International Conference on Language Resources and Evaluation (LREC'20)},
  year={2020}
}
```


