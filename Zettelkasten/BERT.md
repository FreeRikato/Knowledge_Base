## Introduction to BERT

1. **What is BERT?**
   - [x] What does BERT stand for?
      - Bidirectional Encoder Representation from Transformers.

     => Bidirectional - understand context from both left and right of a word.
     => Encoder - uses the encoder part of the Transformer architecture.
     => Representation - creates contextual representation of words.
     => Transformers - based on the Transformer architecture

   - [x] Who developed BERT and when was it introduced?
      - BERT is a language model introduced by researchers at Google AI in 2018.
      - The original authors were Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova.

   - [x] What are the key innovations of BERT compared to previous models?
      - Bidirectional Contextual Understanding
      - Masked Language Model
      - Next Sentence Prediction
      - Contextual embeddings
      - Transfer Learning

2. **Why is BERT significant in NLP?**
   - [x] How does BERT improve language understanding?

      => Bidirectional Contextual Understanding
          - Unlike previous models that read text either left-to-right or right-to-left, BERT considers context from both directional simultaneously
          - This allows it to develop a much richer understanding of language context and meaning

      => Pre-training on Massive Datasets
          - Large corpora of unlabeled text 
          - entire Wikipedia (2500 million words) and BookCorpus (800 million words)

      => Masked Language Model
          - Randomly masks out 15% of the words in a sentence and then tries to predict those masked words
          - This forces the model to use context from both directions to make predictions

      => Next Sentence Prediction
          - Learns to predict whether two sentences naturally follow each other or not
          - This helps the model understand relationships between sentences

      => Contextual Embeddings
          - Conventional models use Fixed word embeddings
          - BERT creates Contextual embeddings that can change based on the surrounding words
          - This allows for more nuanced understanding of word meanings in different contexts

      => Transformer Architecture
          - self-attention mechanism, which allows it to weigh the importance of different words in a sentence relative to each other
          - Enabling BERT to capture dependencies and relationships within the text, improving its ability to model language intricacies.


   - [x] What are some applications of BERT in NLP tasks?

      - Question answering
      - Sentiment analysis
      - Named entity recognition
      - Text classification
      - Language translation and summarization

## Understanding Transformer Architecture

1. **What is the Transformer architecture?**

   - [ ] How do Transformers work in general?
   - [ ] What are the main components of a Transformer model?
   - [ ] How does the attention mechanism work in Transformers?
   - [ ] How did Transformers improve over RNNs and LSTMs?
   - [ ] How are the encoder and decoder blocks structured?
   - [ ] What is the role of multi-head attention in BERT?
   - [ ] How does BERT use position embeddings?

2. **How does BERT utilise the Transformer architecture?**
   - [ ] What is the role of bidirectionality in BERT?
   - [ ] How does BERT differ from the original Transformer model?

## Pre-training and Fine-tuning

1. **How is BERT pre-trained?**
   - [ ] What are the two main tasks used in BERT's pre-training?
   - [ ] Why is masked language modeling (MLM) important?

2. **What is fine-tuning in BERT?**
   - [ ] How is BERT fine-tuned for specific NLP tasks?
   - [ ] What are some examples of tasks BERT can be fine-tuned for?
## Applications and Use Cases

1. **What are the common applications of BERT?**
   - [ ] How is BERT used in question answering systems?
   - [ ] What role does BERT play in sentiment analysis and named entity recognition?

2. **How is BERT being adapted for specific domains?**
   - [ ] What are some domain-specific adaptations of BERT (e.g., BioBERT, SciBERT)?
   - [ ] How do these adaptations improve performance in specialized tasks?

## Challenges and Limitations

1. **What are the limitations of BERT?**
   - [ ] How does BERT handle tasks requiring commonsense reasoning?
   - [ ] What are the challenges associated with BERT's computational demands?

2. **How is the community addressing BERT's limitations?**
   - [ ] What are some strategies for optimizing BERT for efficiency?
   - [ ] How do smaller models like DistilBERT and TinyBERT address these challenges?

## Future Directions

1. **What are the future trends in BERT research?**
   - [ ] How might BERT evolve to handle multimodal inputs?
   - [ ] What advancements are expected in pre-training objectives?

2. **How can BERT be made more accessible and efficient?**
   - [ ] What are the ongoing efforts to improve BERT's interpretability?
   - [ ] How can BERT be adapted for low-resource languages?
