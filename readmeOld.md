

This project aims to build book recommendation system with LLMs. It allows user to specify description of the book 
and based on description model performs semantic (vector) search using RAG to find 10 books with the most similar description.
It also allows user to specify category and emotional tone of the book (description). This approach assumes 
that description characterizes the book well.
This project is heavly inspired by tutorial from freeCodeCamp.org.


picture 1
docs/general.png

picture 2 
docs/general.png


Semantic (vector) search and how to build a vector database (code in the notebook vector-search.ipynb). This allows users to find the most similar books to a natural language query (e.g., "a book about a person seeking revenge").





steps done in order to build this

data preparation - first data was dowloaded from keggle and cleaned see data-exploration
Than with use of zero shot clasification a categories were determined for books with missing categories. It was done with model from hi
ggingface called model="facebook/bart-large-mnli",. for more details see text-clasification. 

Next step was to generate most likely tone of each book based on its description using model="j-hartmann/emotion-english-distilroberta-base" from huggingface
Using sentiment analyses of description there were new features added for each book such as anger", "disqust", "fear", "joy",
which coresponds to how likely from 0 to 1 the book has given sentiment. See sentiment-analyses for more details.
Lastly the web application dashboard using gradio was made. It allows to llok for books based on user description, category and emotional tone.


The tools for this project include OPEN AI, langchain, transformers and other.


In order to run this projet you need open ai api key to generate embeddings.




generating embeddings 
clasification 





I want to add feature so that when person clciks on some button it redirects to google takes name of book appends pdf
in order to find it online for free
