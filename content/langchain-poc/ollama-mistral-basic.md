---
title: Ollama-Mistral-Basic
date: 2024-12-05
author: Your Name
cell_count: 15
score: 15
---

```python
!python --version
```

    Python 3.12.7



```python
!pip show langchain | grep "Version:"
```

    Version: 0.3.8



```python
import os
os.environ.get("CONDA_DEFAULT_ENV")
```




    'py312'




```python
!pip show langchain-community | grep "Version:"
```

    [33mWARNING: Package(s) not found: langchain-community[0m[33m
    [0m


```python
!pip install langchain-community==0.3.8
```

    Collecting langchain-community==0.3.8
      Downloading langchain_community-0.3.8-py3-none-any.whl.metadata (2.9 kB)
    Requirement already satisfied: PyYAML>=5.3 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-community==0.3.8) (6.0.2)
    Collecting SQLAlchemy<2.0.36,>=1.4 (from langchain-community==0.3.8)
      Downloading SQLAlchemy-2.0.35-cp312-cp312-macosx_11_0_arm64.whl.metadata (9.6 kB)
    Requirement already satisfied: aiohttp<4.0.0,>=3.8.3 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-community==0.3.8) (3.11.7)
    Collecting dataclasses-json<0.7,>=0.5.7 (from langchain-community==0.3.8)
      Downloading dataclasses_json-0.6.7-py3-none-any.whl.metadata (25 kB)
    Collecting httpx-sse<0.5.0,>=0.4.0 (from langchain-community==0.3.8)
      Downloading httpx_sse-0.4.0-py3-none-any.whl.metadata (9.0 kB)
    Requirement already satisfied: langchain<0.4.0,>=0.3.8 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-community==0.3.8) (0.3.8)
    Requirement already satisfied: langchain-core<0.4.0,>=0.3.21 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-community==0.3.8) (0.3.21)
    Requirement already satisfied: langsmith<0.2.0,>=0.1.125 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-community==0.3.8) (0.1.145)
    Requirement already satisfied: numpy<2,>=1.26.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-community==0.3.8) (1.26.4)
    Collecting pydantic-settings<3.0.0,>=2.4.0 (from langchain-community==0.3.8)
      Downloading pydantic_settings-2.6.1-py3-none-any.whl.metadata (3.5 kB)
    Requirement already satisfied: requests<3,>=2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-community==0.3.8) (2.32.3)
    Requirement already satisfied: tenacity!=8.4.0,<10,>=8.1.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-community==0.3.8) (9.0.0)
    Requirement already satisfied: aiohappyeyeballs>=2.3.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from aiohttp<4.0.0,>=3.8.3->langchain-community==0.3.8) (2.4.3)
    Requirement already satisfied: aiosignal>=1.1.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from aiohttp<4.0.0,>=3.8.3->langchain-community==0.3.8) (1.3.1)
    Requirement already satisfied: attrs>=17.3.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from aiohttp<4.0.0,>=3.8.3->langchain-community==0.3.8) (24.2.0)
    Requirement already satisfied: frozenlist>=1.1.1 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from aiohttp<4.0.0,>=3.8.3->langchain-community==0.3.8) (1.5.0)
    Requirement already satisfied: multidict<7.0,>=4.5 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from aiohttp<4.0.0,>=3.8.3->langchain-community==0.3.8) (6.1.0)
    Requirement already satisfied: propcache>=0.2.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from aiohttp<4.0.0,>=3.8.3->langchain-community==0.3.8) (0.2.0)
    Requirement already satisfied: yarl<2.0,>=1.17.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from aiohttp<4.0.0,>=3.8.3->langchain-community==0.3.8) (1.18.0)
    Collecting marshmallow<4.0.0,>=3.18.0 (from dataclasses-json<0.7,>=0.5.7->langchain-community==0.3.8)
      Downloading marshmallow-3.23.1-py3-none-any.whl.metadata (7.5 kB)
    Collecting typing-inspect<1,>=0.4.0 (from dataclasses-json<0.7,>=0.5.7->langchain-community==0.3.8)
      Downloading typing_inspect-0.9.0-py3-none-any.whl.metadata (1.5 kB)
    Requirement already satisfied: langchain-text-splitters<0.4.0,>=0.3.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain<0.4.0,>=0.3.8->langchain-community==0.3.8) (0.3.2)
    Requirement already satisfied: pydantic<3.0.0,>=2.7.4 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain<0.4.0,>=0.3.8->langchain-community==0.3.8) (2.10.0)
    Requirement already satisfied: jsonpatch<2.0,>=1.33 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-core<0.4.0,>=0.3.21->langchain-community==0.3.8) (1.33)
    Requirement already satisfied: packaging<25,>=23.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-core<0.4.0,>=0.3.21->langchain-community==0.3.8) (24.1)
    Requirement already satisfied: typing-extensions>=4.7 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langchain-core<0.4.0,>=0.3.21->langchain-community==0.3.8) (4.12.2)
    Requirement already satisfied: httpx<1,>=0.23.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langsmith<0.2.0,>=0.1.125->langchain-community==0.3.8) (0.27.2)
    Requirement already satisfied: orjson<4.0.0,>=3.9.14 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langsmith<0.2.0,>=0.1.125->langchain-community==0.3.8) (3.10.12)
    Requirement already satisfied: requests-toolbelt<2.0.0,>=1.0.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from langsmith<0.2.0,>=0.1.125->langchain-community==0.3.8) (1.0.0)
    Requirement already satisfied: python-dotenv>=0.21.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from pydantic-settings<3.0.0,>=2.4.0->langchain-community==0.3.8) (0.21.0)
    Requirement already satisfied: charset-normalizer<4,>=2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from requests<3,>=2->langchain-community==0.3.8) (3.4.0)
    Requirement already satisfied: idna<4,>=2.5 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from requests<3,>=2->langchain-community==0.3.8) (3.10)
    Requirement already satisfied: urllib3<3,>=1.21.1 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from requests<3,>=2->langchain-community==0.3.8) (2.2.3)
    Requirement already satisfied: certifi>=2017.4.17 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from requests<3,>=2->langchain-community==0.3.8) (2024.8.30)
    Requirement already satisfied: anyio in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from httpx<1,>=0.23.0->langsmith<0.2.0,>=0.1.125->langchain-community==0.3.8) (4.6.2.post1)
    Requirement already satisfied: httpcore==1.* in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from httpx<1,>=0.23.0->langsmith<0.2.0,>=0.1.125->langchain-community==0.3.8) (1.0.6)
    Requirement already satisfied: sniffio in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from httpx<1,>=0.23.0->langsmith<0.2.0,>=0.1.125->langchain-community==0.3.8) (1.3.1)
    Requirement already satisfied: h11<0.15,>=0.13 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from httpcore==1.*->httpx<1,>=0.23.0->langsmith<0.2.0,>=0.1.125->langchain-community==0.3.8) (0.14.0)
    Requirement already satisfied: jsonpointer>=1.9 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from jsonpatch<2.0,>=1.33->langchain-core<0.4.0,>=0.3.21->langchain-community==0.3.8) (3.0.0)
    Requirement already satisfied: annotated-types>=0.6.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from pydantic<3.0.0,>=2.7.4->langchain<0.4.0,>=0.3.8->langchain-community==0.3.8) (0.7.0)
    Requirement already satisfied: pydantic-core==2.27.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from pydantic<3.0.0,>=2.7.4->langchain<0.4.0,>=0.3.8->langchain-community==0.3.8) (2.27.0)
    Collecting mypy-extensions>=0.3.0 (from typing-inspect<1,>=0.4.0->dataclasses-json<0.7,>=0.5.7->langchain-community==0.3.8)
      Downloading mypy_extensions-1.0.0-py3-none-any.whl.metadata (1.1 kB)
    Downloading langchain_community-0.3.8-py3-none-any.whl (2.4 MB)
    [2K   [38;2;114;156;31m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m2.4/2.4 MB[0m [31m31.4 MB/s[0m eta [36m0:00:00[0m
    [?25hDownloading dataclasses_json-0.6.7-py3-none-any.whl (28 kB)
    Downloading httpx_sse-0.4.0-py3-none-any.whl (7.8 kB)
    Downloading pydantic_settings-2.6.1-py3-none-any.whl (28 kB)
    Downloading SQLAlchemy-2.0.35-cp312-cp312-macosx_11_0_arm64.whl (2.1 MB)
    [2K   [38;2;114;156;31m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m2.1/2.1 MB[0m [31m77.1 MB/s[0m eta [36m0:00:00[0m
    [?25hDownloading marshmallow-3.23.1-py3-none-any.whl (49 kB)
    Downloading typing_inspect-0.9.0-py3-none-any.whl (8.8 kB)
    Downloading mypy_extensions-1.0.0-py3-none-any.whl (4.7 kB)
    Installing collected packages: SQLAlchemy, mypy-extensions, marshmallow, httpx-sse, typing-inspect, pydantic-settings, dataclasses-json, langchain-community
      Attempting uninstall: SQLAlchemy
        Found existing installation: SQLAlchemy 2.0.36
        Uninstalling SQLAlchemy-2.0.36:
          Successfully uninstalled SQLAlchemy-2.0.36
    Successfully installed SQLAlchemy-2.0.35 dataclasses-json-0.6.7 httpx-sse-0.4.0 langchain-community-0.3.8 marshmallow-3.23.1 mypy-extensions-1.0.0 pydantic-settings-2.6.1 typing-inspect-0.9.0



```python
!pip show langchain-community | grep "Version:"
```

    Version: 0.3.8



```python
from langchain.llms import Ollama
from langchain.prompts import PromptTemplate
from langchain.chains import LLMChain
```


```python
llm = Ollama(model="mistral", base_url="http://localhost:11434")
```

    /var/folders/26/1_zstvd1579g9j700z2jnmp40000gn/T/ipykernel_16160/2585788740.py:1: LangChainDeprecationWarning: The class `Ollama` was deprecated in LangChain 0.3.1 and will be removed in 1.0.0. An updated version of the class exists in the :class:`~langchain-ollama package and should be used instead. To use it run `pip install -U :class:`~langchain-ollama` and import as `from :class:`~langchain_ollama import OllamaLLM``.
      llm = Ollama(model="mistral", base_url="http://localhost:11434")



```python
llm
```




    Ollama(model='mistral')




```python
# Define a prompt template
template = """
You are a helpful assistant. Please provide a short explanation of the following topic:

{topic}
"""
```


```python
prompt = PromptTemplate(
    input_variables=["topic"],
    template=template,
)

```


```python
llm_chain = LLMChain(llm=llm, prompt=prompt)
```

    /var/folders/26/1_zstvd1579g9j700z2jnmp40000gn/T/ipykernel_16160/4149722537.py:1: LangChainDeprecationWarning: The class `LLMChain` was deprecated in LangChain 0.1.17 and will be removed in 1.0. Use :meth:`~RunnableSequence, e.g., `prompt | llm`` instead.
      llm_chain = LLMChain(llm=llm, prompt=prompt)



```python
topic = "About brazil forest"
llm_chain.run(topic=topic)
```




    ' The Brazilian Forest, more specifically known as the Amazon Rainforest or Amazonia, is the world\'s largest tropical rainforest, covering most of northwest Brazil and extending into Colombia, Peru, and other South American nations. It spans approximately 6.7 million square kilometers (2.6 million square miles), representing over half of the world\'s remaining rainforests.\n\n   The Amazon Rainforest is often referred to as the "lungs of the Earth" due to its significant role in the global carbon cycle. It produces about 20% of the world\'s oxygen and absorbs an estimated 2.2 billion metric tons of CO2 each year, helping combat climate change.\n\n   The Amazon is home to an immense variety of flora and fauna, with around 400 billion individual trees representing 16,000 species. It is believed that the forest may contain as much as 390 billion individual trees. Furthermore, it is inhabited by thousands of indigenous tribes who have developed a unique and rich culture in harmony with the rainforest.\n\n   However, the Amazon Rainforest faces numerous threats such as deforestation due to logging and agriculture (especially cattle ranching), mining activities, and infrastructure development. These human activities not only endanger the preservation of countless species but also contribute significantly to climate change by releasing stored carbon dioxide into the atmosphere.\n\n   Preservation efforts for the Amazon Rainforest are critical to maintain biodiversity, combat climate change, and support indigenous communities who rely on the forest for their livelihoods. Various initiatives have been established to protect the rainforest through reforestation projects, sustainable agriculture practices, and legal protections of indigenous lands.'




```python
topic = "Amazon forest"
llm_chain.run(topic=topic)
```




    ' The Amazon Forest, also known as the Amazon Rainforest or Amazonia, is the world\'s largest tropical rainforest, spanning over 6.7 million square kilometers (2.6 million square miles) in South America. It is primarily located within Brazil but extends into nine other neighboring countries: Peru, Colombia, Venezuela, Ecuador, Bolivia, Guyana, Suriname, French Guiana (a department of France), and Paraguay.\n\n   This vast forest is home to an extraordinary level of biodiversity. It is estimated that there are more than 400 billion individual trees belonging to over 16,000 species. The Amazon is also known for its rich wildlife; among the many animals living within it are jaguars, anacondas, sloths, various monkeys, and countless bird species. Additionally, there are thought to be millions of insect species residing in the forest.\n\n   The Amazon Forest plays a critical role in regulating Earth\'s climate as it absorbs large amounts of carbon dioxide and releases oxygen through photosynthesis. It is often referred to as the "lungs of the Earth." However, deforestation poses significant threats to the Amazon Rainforest, leading to habitat loss for its rich biodiversity and contributing to climate change due to the release of stored carbon dioxide when trees are cut down.'




```python

```


---
**Score: 15**
