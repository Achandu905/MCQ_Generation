# Automated-MCQS-Generation
Automated MCQ generation is a popular research area. It is important for students to expertise in their field of study. Our project consists of 2 phases (Video Summarization, MCQ Generation). In the fast-growing technology today, we can see that the students are being given video lectures in institutions. Even though it’s effective in learning the concept from scratch using a video, it’s not very helpful as in the end it takes more time for revision. In our attempt to Video Summarization, we look to create a certain degree of synopsis that explains the most informative parts of the video. The most important thing in learning is assessment and the question is crucial for assessment. Online tests are becoming more common at universities, colleges and other educational institutions. The assessment pattern is largely evolving towards objective assessment, i.e.,MCQ based. Even though MCQ’s have many advantages like electronic evalua- tion and less testing time, exam question preparation by hand is a difficult undertaking for educators, when the time is limited. To address this issue in he development of multiple-choice exam questions,this study offers an automated exam question genera- tor. Distractors are created in order to generate options for queries.
#project overview

Exam-style questions are a basic teaching tool that can be used for a variety of objec- tives. Questions have the capacity to influence student learning in addition to serving as an assessment tool. Learning tools are provided, and students can learn from a variety of online sources. The manual questions from the learning materials, on the other hand, are necessary for the learner’s assessment. To our knowledge, no generic assessment approach has been provided in the literature to evaluate learners’ learning gaps from e-reading documents. As a result, automated question production and evaluation methodologies can aid in the assessment system’s automation. Given a video lecture, our framework aims to find an effective way to extract summary out of it and generate MCQ’s.

# Purpose
The purpose of the project is to ease the hectic task of going through minute details of a video in order to generate Multiple Choice Questions (MCQs) for various quizzes.
The primary function of this project is to take in a video and generate high quality MCQs with four options from the provided video with the help of Natural Language Processing.
# Existing System
• Multiple choice question (MCQ) is a very popular form of assessment in which respon- dents are asked to select the best possible answer out of a set of choices.
• Intraditionalmethod,MCQ’sareproducedManuallyandbyusingBruteForceapproach which is a tedious and time consuming task.
• So to generate MCQ’s in simple and timely manner this system is useful.
# Proposed System
• Our proposed idea of producing MCQs with software can help organizations and institu- tions to evaluate in a simple and timely manner.
• Our proposed idea of producing MCQs with software can help organizations and institu- tions to evaluate in a simple and timely manner.
• To make our MCQ’s more tricky and comparable to human made MCQ’s, They should be properly analyzed and accurate and with a well-defined structure.
• Wetrainthemodelsuchthatthemodelisabletoimprovisebyitselfandchangeaccording to the trends and patterns.
The whole methodology can be grouped into 4 parts.
1. The first part is interaction with data which is provided by the user.
2. The second phase is processing, analyzing and extraction of key words from the data provided.
3. The next phase sentences for the keywords are mapped accordingly.
4. And the last phase is where false option is Produced which together creates a stan- dard concise MCQ’s
# REQUIREMENT SPECIFICATIONS

  # Hardware Requirements
Hardware Requirements for the project are::
The functional requirements or the overall description documents include the product
perspective and features, operating system and operating environment, graphics requirements, design constraints and user documentation.
The appropriation of requirements and implementation constraints gives the general overview of the project in regards to what the areas of strength and deficit are and how to tackle them.
• Computer / laptop with minimum 4 GB memory and 128 GB of storage
• Operating System requirements: Preferably Linux flavour. MacOS or Windows can also be used.
• Operating System: Flavour of Linux, preferably Ubuntu. ‘

# Software Requirements:
Minimum hardware requirements are very dependent on the particular software being developed by a given En thought Python . Applications that need to store large arrays/objects in memory will require more RAM, whereas applications that need to perform numerous cal- culations or tasks more quickly will require a faster processor.
1. Python: Python is a high-level, general-purpose programming language.
2. version: Python 3.9 or greater
3. Highly dependent on libraries like nltk, pandas, numpy, sklearn, tensorflow, FFPEG, etc 4. No OS Restrictions
# system Analysis
 We propose an Automated MCQ generation model that generates relevant MCQ’s from the given video lecture.
• The input given is in the form of a video which is then converted to text and gets the summarized text after Pre-processing.
• TheInformativeretrievalalgorithmretrievesthecorecontentofthevideo,andwe’llpass it the MCQ generation models which is the second phase of our project.
• First, we train the model and then test it with the current summary extracted given.
• The performance of the proposed model is calculated based on the diversions in the options generated and an accuracy score is generated.

# Algorithms
# BERT (Bidirectional Encoder Representations from Transformers)
• BERT (Bidirectional Encoder Representations from Transformers) is a neural network- based technique for natural language processing.
• It is a pre-trained open-sourced model from Google. It helps computers to understand the language a bit more as humans do.
• The input text is summarized using the BERTSUM model, which is fine-tuned BERT for extractive summarization.
. In the BERTSUM model, at the start of each sentence, a [CLS] token is added, and between every two sentences, a [SEP] token is added to separate the sentences.
• Here, a [CLS] token is added to collect the preceding sentence context. Now each word of the sentence is tokenized using token embeddings.
• There is also a difference in segment embeddings. In the BERTSUM model, each sen- tence is assigned an embedding of Ea or Eb depending on whether the sentence is even or odd. If the sequence is [s1, s2, s3] then the segment embeddings are [Ea, Eb, Ea].
• This way, all sentences are embedded and sent into further layers. BERTSUM assigns scores to each sentence that represents how much value that sentence adds to the overall document.
# Rapid Automatic Keyword Extraction (RAKE)
Rapid Automatic Keyword Extraction (RAKE) is a well known keyword extraction method that uses a list of stopwords and phrase delimiters to detect the most relevant words or phrases in a piece of text. This algorithm has mainly three components:
Candidate Selection
• In candidate selection, all possible words, phrases and terms from the summarized text get extracted that can potentially be a keyword. Consider the following example where the text is, “Keyword extraction is not that difficult after all. There are many libraries that can help you with keyword extraction. Rapid automatic keyword extraction is one of those.”
• Thefirstthingthismethoddoesissplitthetextintoalistofwordsandremovestopwords from that list. After splitting, two lists are generated as follows:stopwords = [is, not, that, there, are, can, you, with, of, those, after, all, one] delimiters = [“.” , “,”]
• The above list of words cannot be part of the candidate key. Now the remaining words will be considered as candidate words.
• candidate words = [keyword, extraction, difficult, many, libraries, help, rapid, automatic]
Word Co-occurrence Matrix
• After getting the candidate words, the word co-occurrence matrix is built by this method.
• Inthismatrix,eachrowshowsthenumberoftimesthatagivencandidatewordco-occurs with every other candidate word in the candidate phrases.
• For the above-mentioned text example, the matrix looks like this:
Scoring and selecting words
• After creating a word co-occurrence matrix, RAKE calculates the keyword score. This score of candidate word is computed by taking the degree of a word in the matrix (i.e. the sum of the number of co-occurrences the word has with any other content word in the text), as the word frequency (i.e. the number of times the word appears in the text) which is given by,K = deg(t)/freq(t)

# WordNet
• WordNet is a lexical database for the English language, which was created by Princeton, and is part of the NLTK corpus.
• In the WordNet network, the words are connected by linguistic relations.
• These linguistic relations includes hypernym, hyponym, meronym, holonym, etc. Word- Net stores synonyms in the form of synsets (Nouns, verbs, adjectives and adverbs are grouped into sets of cognitive synonyms) where each word in the synset shares the same meaning.
• Basically, each synset is a group of synonyms. Each synset has a definition associated with it. Relations are stored between different synsets. This Lesk algorithm is based on the assumption that words in a given”neighborhood” (section of text) will tend to share a common topic.
• A simplified version of the Lesk algorithm compares the dictionary definition of an am- biguous word with the terms contained in its neighbourhood.
• Now all the possible hypernyms of the key and the corresponding hyponyms for each of the hypernym are found.
• These hyponyms are considered potential distractors. Then, the potential distractors are ranked, and the final distractors are chosen based on their rank.
• The ranks given to the potential distractors are based on whether it occurs in the text extracted from the summarization.
• Thepotentialdistractorsthatexistintheextractedtextandhavingthesamepartofspeech structure as the key have a higher rank than those with a different structure.
# CONCLUSION
Multiple Choice Questions (MCQs) are generated successfully. Efficient questions are pro- duced with good quality distractors. The problem of manually creating questions is solved with the proposed system. The proposed system creates automated questions with the help of NLP that reduces human intervention and it is a cost and time effective system. And the accu- racy of the distractor generated is reasonably high. This system not only helps teachers with E-assessments but also helps students who are preparing for competitive exams. Students can test their ability to solve the questions and can also check their understanding of the concepts. Since our proposed system is based on Google’s BERT Model, the accuracy of the system will increase in the future as the performance of the model is improved and as the research in the field of NLP is trying to reach the human level every day.
