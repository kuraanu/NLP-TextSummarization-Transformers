# NLP-TextSummarization-Transformers
Traditional Natural Language Processing (NLP) models struggle to distinguish between essential and redundant information when analyzing large volumes of text. However, the advent of transformer-based models has marked a significant breakthrough in NLP. These models allow for simultaneous processing of entire sequences of text, resulting in more efficient and accurate language understanding.

One prominent application of transformer-based models is in text summarization, where the goal is to condense text while retaining key information. This process offers several advantages, including efficient information comprehension, time-saving for readers, and the facilitation of aggregating news, blog posts, or research papers. Summarization enables individuals to stay informed without the need for extensive reading.

Text summarization techniques can be categorized into two main approaches: extractive and abstractive summarization. Extractive summarization involves selecting and presenting important sentences or passages from the original text, while abstractive summarization involves generating new sentences that capture the essence of the text in a condensed form.

Regarding the dataset used for this study, it was obtained from Kaggle and comprises articles from CNN and the DailyMail. The dataset includes over 300,000 news articles written by journalists, with CNN articles spanning from April 2007 to 2015 and Daily Mail articles from June 2010 to April 2015.

Model Architecture

The prospective models used in this project will include baseline models without machine learning, zero-shot learning model, and fine-tuned pre-trained transformer models.
Two Baseline Models :
TF-IDF based summarization and TextRank based summarization

Zero-Shot Model
To enhance text summarization for news articles, a zero-shot learning approach is implemented using the T5 (Text-to-Text Transfer Transformer) model. The T5 model is fine-tuned specifically for summarization without explicit training on the dataset. T5 is a transformer-based architecture that handles all NLP tasks as text-to-text problems, which allows it to adapt to various domains. This zero-shot learning approach enables the model to generalize its summarization capabilities to news articles, capitalizing on the pre-existing knowledge encoded during pre-training.

Fine Tuning Pre-Trained Seq2seq Model 
For the task of extractive summarization, the model undergoes fine-tuning through a two-step process involving tokenization and training. The tokenization process is carried out using the AutoTokenizer from the Hugging Face transformers library. Each article undergoes tokenization with the addition of a prefix, "summarize:," guiding the model in comprehending the summarization task

Transformers
Furthermore, one neural network model is implemented to advance the models for text summarization.  Specifically, model architecture with BART is utilized because of its capacity to capture contextual information and create coherent summaries.  BART combines some characteristics from both BERT and GPT, it uses an encoder-encoder (seq2seq) model with a bidirectional (BERT-like) encoder and an autoregressive (GPT-like) decoder. BART undergoes pre-training by (1) introducing random noise to the text through an arbitrary noising function and (2) training a model to reconstruct the original text. BART demonstrates notable effectiveness, especially when fine-tuned for tasks such as text generation, including summarization and translation.


