---
title: Cricket-2
date: 2025-01-03
author: Your Name
cell_count: 10
score: 10
---

```python
import random
import asyncio
```


```python
from langchain.llms import Ollama
from langchain.prompts import PromptTemplate
from langchain.chains import LLMChain
```


```python
# Initialize the Ollama LLM with the Mistral model
llm = Ollama(
    model       = "mistral",
    base_url    = "http://localhost:11434"
)
```

    /var/folders/26/1_zstvd1579g9j700z2jnmp40000gn/T/ipykernel_41177/2325888272.py:2: LangChainDeprecationWarning: The class `Ollama` was deprecated in LangChain 0.3.1 and will be removed in 1.0.0. An updated version of the class exists in the :class:`~langchain-ollama package and should be used instead. To use it run `pip install -U :class:`~langchain-ollama` and import as `from :class:`~langchain_ollama import OllamaLLM``.
      llm = Ollama(



```python
# Define a prompt template
template = """
You are a Cricket Commentator who makes one line Cricket Commentary. Please provide one line commentary about the given run.
It's a plain commentary for a ball, don't add batsman's name.
Your commentary should be between 20 to 40 words:

{run}
"""
```


```python

# Define the prompt template and chain
prompt = PromptTemplate(
    input_variables=["run"],
    template=template,
)
```


```python
# Create the chain for generating commentary
llm_chain = LLMChain(
    llm=llm,
    prompt=prompt
)

```

    /var/folders/26/1_zstvd1579g9j700z2jnmp40000gn/T/ipykernel_41177/2298729601.py:2: LangChainDeprecationWarning: The class `LLMChain` was deprecated in LangChain 0.1.17 and will be removed in 1.0. Use :meth:`~RunnableSequence, e.g., `prompt | llm`` instead.
      llm_chain = LLMChain(



```python
# Asynchronous function to simulate the innings and commentary
async def first_innings():
    over_count = 2
    current_over_balls = 6

    # Initialize two batsmen (start with batsman 1)
    batsmen = ["Dhoni", "Kohli"]
    current_batsman_index = 0  # Start with the first batsman

    for current_over in range(over_count):
        log_content = f'\nPlaying: over {current_over + 1}'
        yield f"{log_content}"

        for current_ball in range(current_over_balls):
            current_ball += 1

            # Get the current batsman
            current_batsman = batsmen[current_batsman_index]

            total_score = []
            
            # Generate a random run
            c_run = get_random_run()

            total_score.append(c_run)
            print (f'{total_score}')
            

            # If the run is odd, switch the batsman
            if c_run % 2 != 0:
                current_batsman_index = 1 - current_batsman_index  # Toggle between 0 and 1

            # Get the magic commentary for the run
            magic_commentary = get_magic_commentary(c_run)

            # Format the ball commentary
            ball_commentary = f'[{current_over + 1}.{current_ball}]: {current_batsman} scored: {c_run}   {magic_commentary}'

            # Yield the ball commentary
            yield f"{ball_commentary}"

            # Wait for a short time before the next ball (simulate time delay between balls)
            await asyncio.sleep(0.2)

        # Wait for a short time before the next over (simulate break between overs)
            await asyncio.sleep(0.2)
    print("The first innings is done")
   




```


```python
async def second_innings():
    over_count = 2
    current_over_balls = 6

    # Initialize two batsmen (start with batsman 1)
    batsmen = ["Ben Stokes", "Buttler"]
    current_batsman_index = 0  # Start with the first batsman

    for current_over in range(over_count):
        log_content = f'\nPlaying: over {current_over + 1}'
        yield f"{log_content}"

        for current_ball in range(current_over_balls):
            current_ball += 1

            # Get the current batsman
            current_batsman = batsmen[current_batsman_index]

            # Generate a random run
            c_run = get_random_run()

            # If the run is odd, switch the batsman
            if c_run % 2 != 0:
                current_batsman_index = 1 - current_batsman_index  # Toggle between 0 and 1

            # Get the magic commentary for the run
            magic_commentary = get_magic_commentary(c_run)

            # Format the ball commentary
            ball_commentary = f'[{current_over + 1}.{current_ball}]: {current_batsman} scored: {c_run}   {magic_commentary}'

            # Yield the ball commentary
            yield f"{ball_commentary}"

            # Wait for a short time before the next ball (simulate time delay between balls)
            await asyncio.sleep(0.2)

        # Wait for a short time before the next over (simulate break between overs)
        await asyncio.sleep(0.2)
    print("The second innings is done")  




```


```python
async def main():
    async for result in first_innings():
        print(result)
    async for result in second_innings():
        print(result)

asyncio.run(main())
```


    ---------------------------------------------------------------------------

    RuntimeError                              Traceback (most recent call last)

    Cell In[9], line 7
          4     async for result in second_innings():
          5         print(result)
    ----> 7 asyncio.run(main())


    File /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/asyncio/runners.py:190, in run(main, debug, loop_factory)
        161 """Execute the coroutine and return the result.
        162 
        163 This function runs the passed coroutine, taking care of
       (...)
        186     asyncio.run(main())
        187 """
        188 if events._get_running_loop() is not None:
        189     # fail fast with short traceback
    --> 190     raise RuntimeError(
        191         "asyncio.run() cannot be called from a running event loop")
        193 with Runner(debug=debug, loop_factory=loop_factory) as runner:
        194     return runner.run(main)


    RuntimeError: asyncio.run() cannot be called from a running event loop



```python

```


---
**Score: 10**
