# social_Media_Classification

sEXism Identification in Social neTworks
Task Description
This year the lab comprises nine subtasks in two languages, English and Spanish, which are the same three tasks (sexism identification, source intention detection, and sexism categorization) applied to three different types of data: text (tweets), image (memes) and video (TikToks). This multimedia approach will help identify trends and patterns in sexism across media formats and user interactions, contributing to a deeper understanding of the social dynamics. Also, approaches submitted to all tasks will be evaluated to analyze their capacity to detect sexism in a multimodal source.
SUBTASK 1.1: Sexism Identification in Tweets
The first subtask is a binary classification. The systems must decide whether a given tweet contains sexist expressions or behaviours (i.e., it is sexist itself, describes a sexist situation or criticizes a sexist behaviour), and classify it according to two categories: YES and NO.
SUBTASK 1.2: Source Intention in Tweets
The second subtask is a multi-class classification. For the tweets that have been predicted as YES, the second subtask aims to classify each tweet according to the intention of the person who wrote it. One of the three following categories must be assigned to each tweet:
• DIRECT: The intention is to write a message that is sexist itself
• REPORTED: The intention of the author is to report or describe a sexist situation or event
suffered by a woman or women in first or third person
• JUDGEMENTAL The intention of the author is to be judgemental since the tweet describes sexist situations or behaviors with the aim to condemning them
SUBTASK 1.3: Sexism Categorization in Tweets
The third subtask is a multi-label classification. For the tweets that have been predicted as YES, the third task aims to categorize them according to the type of sexism. We propose a five-class classification task: This is a multi-label task, so that more than one of the following labels may be assigned to each tweet:
• IDEOLOGICAL-INEQUALITY: the text discredits the feminist movement, rejects inequality between men and women, or presents men as victims of gender-based oppression.
• STEREOTYPING-DOMINANCE: the text expresses false ideas about women that suggest they are more suitable to fulfill certain roles, or inappropriate for certain tasks, or claims that men are somehow superior to women.
• OBJECTIFICATION: the text presents women as objects apart from their dignity and personal aspects or assumes or describes certain physical qualities that women must have to fulfill traditional gender roles
 • SEXUAL-VIOLENCE: the text includes or describes sexual suggestions, requests for sexual favors or harassment of a sexual nature
• MISOGYNY-NON-SEXUAL-VIOLENCE: the text expresses hatred and violence towards women, different to that with sexual connotations.
SUBTASK 2.1: Sexism Identification in Memes
This is a binary classification subtask consisting of deciding whether or not a given meme is sexist, contains sexist expressions or behaviours (i.e., it is sexist itself, describes a sexist situation or criticizes a sexist behaviour), and classify it according to two categories: YES and NO
SUBTASK 2.2: Source Intention in Memes
As in subtask 1.2, this subtask aims to categorize the meme according to the intention of the author, which provides insights in the role played by social networks on the emission and dissemination of sexist messages. Due to the characteristics of the memes, the REPORTED label is virtually null, so in this task systems should only classify memes with DIRECT or JUDGEMENTAL labels
SUBTASK 2.3: Sexism Categorization in Memes
This subtask is a multi-label classification. This subtask aims to classify sexist memes according to the categorization provided for subtask 1.3: (i)IDEOLOGICAL AND INEQUALITY, (ii) STEREOTYPING AND DOMINANCE, (iii) OBJECTIFICATION, (iv) SEXUAL VIOLENCE, and (v) MISOGYNY AND NON-SEXUAL VIOLENCE
SUBTASK 3.1: Sexism Identification in Videos
This subtask is the same subtask as subtasks 1.1 and 2.1. Some examples of videos classified as YES or NO
SUBTASK 3.2: Source Intention in Videos
This subtask replicates subtask 2.2 for memes, but it takes as source videos. Some examples of videos classified as Direct or Judgemental
SUBTASK 3.3: Sexism Categorization in Videos
This subtask aims to classify sexist videos according to the categorization provided for Task 1.3: (i) IDEOLOGICAL AND INEQUALITY, (ii) STEREOTYPING AND DOMINANCE, (iii) OBJECTIFICATION, (iv) SEXUAL VIOLENCE and (v) MISOGYNY AND NON-SEXUAL VIOLENCE
Datasets Description
The EXIST 2025 Tweets Dataset will be employed in Task 1 (subtasks 1-3), the EXIST 2025 Memes Dataset will be used in Task 2 (subtasks 1-3), while the EXIST 2025 Videos Dataset will be used in Task 3 (subtasks 1-3). Note that the .zip package includes the annotation guidelines provided to annotators for the Tweet and Memes datasets. For the video dataset, the same guidelines as those for memes were used, but with video-specific examples; therefore, we have not included them.
EXIST 2025 Tweets Dataset
The EXIST 2025 Tweets Dataset contains more than 10,000 labeled tweets, both in English and Spanish. In particular, the training set contains 6,920 tweets, the development set contains 1,038 tweets and the test set contains 2,076 tweets. Distribution between both languages has been balanced.
The data sets are provided in JSON format.

 1. "id_EXIST": a unique identifier for the tweet.
2. "lang": the languages of the text (“en”).
3. "tweet": the text of the tweet.
4. "number_annotators": the number of persons that have annotated the tweet.
5. "annotators": a unique identifier for each of the annotators.
6. "labels_task1_1": a set of labels (one for each of the annotators) that indicate if the tweet contains sexist expressions or refers to sexist behaviours or not. Possible values are: “YES” and “NO”.
7. "labels_task1_2": a set of labels (one for each of the annotators) recording the intention of the person who wrote the tweet. Possible labels are: “DIRECT”, “REPORTED” “JUDGEMENTAL”, “-”, and “UNKNOWN”.
8. "labels_task1_3": a set of arrays of labels (one array for each of the annotators) indicating the type or types of sexism that are found in the tweet. Possible labels are: “IDEOLOGICAL- INEQUALITY”,“STEREOTYPING-DOMINANCE”, “OBJECTIFICATION”, “SEXUAL- VIOLENCE”, “MISOGYNY-NON-SEXUAL-VIOLENCE”, “-”, and “UNKNOWN”.
EXIST 2025 Memes Dataset
The EXIST 2025 Memes Dataset contains more than 5,000 labeled memes, both in English and Spanish. In particular, the training set contains 4,044 memes and the test set contains 1,053 memes. Distribution between both languages has been balanced.
The data sets are provided in JSON format. Each meme is represented as a JSON object with the following attributes:
1. "id_EXIST": a unique identifier for the meme.
2. "lang": the languages of the meme (“en”).
3. "text": the text automatically extracted from the meme.
4. "number_annotators": the number of persons that have annotated the meme.
5. "annotators": a unique identifier for each of the annotators.
6. "labels_ task2_2": a set of labels (one for each of the annotators) recording the intention of the person who created the meme. Possible labels are: “DIRECT”, “JUDGEMENTAL”,
“- ”, and “UNKNOWN”.
7. "labels_ task2_3": a set of arrays of labels (one array for each of the annotators) indicating the type or types of sexism that are found in the meme. Possible labels are: “IDEOLOGICAL-INEQUALITY”,“STEREOTYPING- DOMINANCE”, “OBJECTIFICATION”, “SEXUAL-VIOLENCE”, “MISOGYNY-NON-

EXIST 2025 Videos Dataset
The EXIST 2025 Videos Dataset contains more than 3,000 labeled Tiktok videos, both in English and Spanish. In particular, the training set contains 2,524 videos and the test set contains 674 videos. Distribution between both languages has been balanced.
The data sets are provided in JSON format. Each video is represented as a JSON object with the following attributes:
1. 1. ”id_EXIST": a unique identifier for the video in EXIST evaluation.
2. "lang": the languages of the video (“en”).
3. "text": the text automatically extracted from the video.
4. "annotators": a unique identifier for each of the annotators.
5. "number_annotators": the number of persons that have annotated the video.
6. 11. "labels_task3_1": a set of labels (one for each of the annotators) that indicate if the video
7. contains sexist expressions or refers to sexist behaviours or not. Possible values are: “YES”,
“NO” and “UNKNOWN”.
8. "labels_ task3_2": a set of labels (one for each of the annotators) recording the intention of the person who created the video. Possible labels are: “DIRECT”, “JUDGEMENTAL”, “-”, and “UNKNOWN”.
9. "labels_ task3_3": a set of arrays of labels (one array for each of the annotators) indicating the type or types of sexism that are found in the video. Possible labels are: “IDEOLOGICAL- INEQUALITY”,“STEREOTYPING-DOMINANCE”,“OBJECTIFICATION”, “SEXUAL- VIOLENCE”, “MISOGYNY-NON-SEXUAL-VIOLENCE”, “-”, and “UNKNOWN”.
IMPORTANT: Since labels for subtasks 1.2, 1.3, 2.2, 2.3, 3.2 and 3.3 are only assigned if the tweet/meme/video has been labeled as YES, the label “-” is assigned to not sexist instances in these subtasks. The label “UNKNOWN” is assigned to tweets/memes/videos for which the annotators did not provide a label. Note that “UNKNOWN” is not a target class for classification, and therefore should not be predicted by the systems.
For the test sets, labels for the subtasks are not provided.
