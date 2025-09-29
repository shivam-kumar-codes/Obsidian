
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


## Training Process

1. **Pretraining**  
	 -  Trained on row, unlabeled text.   
	 -  Learns general language patterns.  
	 -  Uses self-supervised learning (labels are created from data itself) 

2. **Fine-Tuning**
	-  Further Training for specialization
	-  Types:-
		i) Instruction fine-tuning : Paired prompts & answers. e.g., summarize text. 
		ii) Classification fine-tuning : text labeled into categories. e.g., helpful/not helpful. 

	