# Ollama on an Local GPU

```sh
ollama list
```

```
NAME            	ID          	SIZE  	MODIFIED    
phi3:latest     	4f2222927938	2.2 GB	2 hours ago	
llama3.1:latest 	91ab477bec9d	4.7 GB	8 days ago 	
codellama:latest	8fdf8f752f6e	3.8 GB	8 days ago 	
phi3:mini       	4f2222927938	2.2 GB	8 days ago 
```

## Sample Python Code

```python
from langchain_core.prompts import ChatPromptTemplate
from langchain_ollama.llms import OllamaLLM
import torch

# clean up any models in RAM
torch.cuda.empty_cache() 

template = """
Why does LLM infernce take up so much GPU RAM?
"""

prompt = ChatPromptTemplate.from_template(template)
model = OllamaLLM(model="phi3:mini")
chain = prompt | model

chain.invoke({"question": "What is LangChain?"})
```