
# Understanding LLMs  

- What does **"understanding"** mean for LLMS ?  
	-> LLMs don't think like humans -> no human-like consciousness.  
	-> They "understand" only in the sense thaty they can generate meaningful, coherent text. 

-  why are LLMs powerful ?  
	-> Built on **Transformer** architecture.  
	-> Trained on huge amounts of text -> learn patterns, context, and meaning.    
	-> LLM = type of neural network that can read, write, reply like a human.

-  Parameters  
	-> Parameters = adjustable values in training  
	-> Used to predict the next word  
	 -> Modern LLMs -> billions of parameters.  
	 GPT-3 has 96 transformer layers & 175 billion parameters.   

-  Applications  
   -> Translation, text generation, chatbots (chatGPT, Gemini).   
   -> Custom LLMs: specialized for domains (e.g. -> bloomberfGPT -> finance, Medical LLMs -> healthcare)  
   -> Benefits fo custom models:  
	   - Better task accuracy  
	   - Improved data privacy  


![[chapter 1 - different fields relationship]]  


##  - Training Process

1. **Pretraining**  
	 -  Trained on row, unlabeled text.   
	 -  Learns general language patterns.  
	 -  Uses self-supervised learning (labels are created from data itself) 

2. **Fine-Tuning**
	-  Further Training for specialization
	-  Types:-
		i) Instruction fine-tuning : Paired prompts & answers. e.g., summarize text. 
		ii) Classification fine-tuning : text labeled into categories. e.g., helpful/not helpful. 


## - Transformer Architecture

- Encoder : Processes Input text into numerical vectors (context representation).    
- Decoder : Generates Output text from vectors.  

		Example: Summarization -> Encoder compresses meaning, 
					Decoder produces summary. 

-  Model Examples:  
	-  BERT : 
		- Bidirectional Encoder Representations from Transformers -> uses Encoder only -> understands context bi-directionally.  
		-  Text Classifications, Sentiment Prediction, Document Categorization.  
	-  GPT :     
		-  Generative Pretrained Transformers -> Uses Decoder only -> autoregressive (predicts next word using previous ones).  
		-  Machine Translations, Text Summarization, Fiction Writing, Writing Computer Code & more.  

-  Training LLMs is extremely expensive.  
- GPT-3 pretraining cost was approx = $ 4.6 million  
  
- The key idea of the transformer architecture is an attention mechanism that gives the LLM selective access to the whole Input sequence when generating the Output one word at a time.  


## - Attention Mechanism  

-  A deep learning technique that allows a neural network to selectively focus on the most relevant parts of its Input data when making a prediction or generating an output, mimicking human cognitive attention.     
-  It does this by assigning varying importance or **"weights"** to different Input elements, effectively creating a "spotlight" on crucial info & diminishing the Impact of Irrelevant data.  
-  This approach enhances a model's capability to understand long sequences, capture dependencies between pieces of Information, and Improve performances across various tasks like Machine Translation and Image Analysis.



![[Pasted image 20250929205556.png]]