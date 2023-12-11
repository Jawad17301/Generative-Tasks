
# Generative AI Tasks Using LangChain 

LangChain uses advanced natural language processing (NLP) techniques to summarize entire PDF books efficiently. By analyzing the content, identifying key themes, and extracting essential information, LangChain condenses the book's core ideas into a concise summary. The platform also facilitates prompt creation through customizable templates, allowing users to generate prompts tailored to specific preferences or requirements. 

Here we have solved two tasks related to Generative AI which are listed below: 




## Summarization of PDF Book:
In order to summarize the entire book, you will need some important libraries to install in your Google Colabs Notebook; 

langchain, openai, pymupdf, fitz, 
and most importantly your openai key. 

Here we have used pymupdf which is basically a high performance Python library for data extraction and manipulation of pdf documents. we loaded our given book "Crime and Punishment" to the function load_my_pdf. Then we utilized text_splitter to split our text into small chunks and required number of book pages that we needed as a summarization. And finally we used  load_summarize_chain() function with the chain_type="map-reduce" parameter. This will Summarize each doc on it’s own in a “map” step and “reduce” the summaries into a final summary using LLM model.

How it works? 

pdf book > (prompt:Summarize theme), LLM > (Summary) >
(prompt:Extract final summary), (LLM > Final Summary)




## Prompt Template (Personalized Study Plans for Students)
To perform this task, we have utilized various approaches inlcuding prompt_template but due to exceeding our current quota in the langchain so we used the random forest classifier to suggest our students personalized study plan. 

we have taken students CGPA, courses grade (programming course, oop, and DS), preferred learning styles, and preferred career path(Data Scinence, AI and ML). 

Each student will enter his/her data and the system will recommed a study plan for the student. 
## Tech Stack

**Programming Language** Python 

**Libraries Used** Langchain, Openai, pymupdf.

**Machine Model** Random Forest Regressor 

