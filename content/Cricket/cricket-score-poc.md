---
title: Cricket-Score-Poc
date: 2024-11-27
author: Your Name
cell_count: 42
score: 40
---

```python
import random
import time

def get_random_number(minimum = 0, maximum = 6):
    return random.randint(minimum, maximum)

```


```python
def get_random_run():
    r_run = get_random_number(0, 6)

    if r_run == 5:
        return 4

    return r_run
```


```python
#First over
current_over_balls  = 6


```


```python
for current_ball in range(current_over_balls):

    current_batsman = "Dhoni"

    c_run = get_random_run()

    ball_commentary = f'[{current_ball+1}]: {current_batsman} scored: {c_run}'

    print(f"{ball_commentary}")
    time.sleep(0.2)
```

    [1]: Dhoni scored: 1
    [2]: Dhoni scored: 2
    [3]: Dhoni scored: 4
    [4]: Dhoni scored: 4
    [5]: Dhoni scored: 6
    [6]: Dhoni scored: 1



```python
current_over_balls  = 6
over_count          = 2


```


```python
for current_over in range(over_count):

    for current_ball in range(current_over_balls):

        current_batsman = "Dhoni"

        c_run = get_random_run()

        ball_commentary = f'[{current_ball+1}]: {current_batsman} scored: {c_run}'
        print(f"{ball_commentary}")
        time.sleep(0.2)
    print(f"{current_over+1} over is completed")
        
    
```

    [1]: Dhoni scored: 1
    [2]: Dhoni scored: 3
    [3]: Dhoni scored: 0
    [4]: Dhoni scored: 6
    [5]: Dhoni scored: 0
    [6]: Dhoni scored: 3
    1 over is completed
    [1]: Dhoni scored: 1
    [2]: Dhoni scored: 2
    [3]: Dhoni scored: 1
    [4]: Dhoni scored: 4
    [5]: Dhoni scored: 2
    [6]: Dhoni scored: 0
    2 over is completed



```python
current_over_balls  = 6
over_count          = 2


```


```python
for current_over in range(over_count):

    print(f'\nplaying : over {current_over+1}')
    print('-'*20)
    print('')

    for current_ball in range(current_over_balls):

        current_batsman = "Dhoni"

        c_run = get_random_run()
        ball_commentary = f'[{current_ball+1}]: {current_batsman} scored: {c_run}'

        print(f"{ball_commentary}")
        time.sleep(0.2)
```

    
    playing : over 1
    --------------------
    
    [1]: Dhoni scored: 6
    [2]: Dhoni scored: 3
    [3]: Dhoni scored: 0
    [4]: Dhoni scored: 0
    [5]: Dhoni scored: 4
    [6]: Dhoni scored: 1
    
    playing : over 2
    --------------------
    
    [1]: Dhoni scored: 6
    [2]: Dhoni scored: 6
    [3]: Dhoni scored: 4
    [4]: Dhoni scored: 1
    [5]: Dhoni scored: 0
    [6]: Dhoni scored: 1



```python

```


```python

```


```python

```


```python
import random
import time


```


```python
def get_random_number(minimum = 0, maximum = 6):
    return random.randint(minimum, maximum)


```


```python
def get_random_run():
    r_run = get_random_number(0, 6)

    if r_run == 5:
        return 4

    return r_run



```


```python
def play_inninings():

    current_over_balls  = 6
    over_count          = 2

    for current_over in range(over_count):

        print(f'\nplaying : over {current_over+1}')
        print('-'*20)
        print('')

        for current_ball in range(current_over_balls):
            current_batsman = "Dhoni"

            c_run = get_random_run()

            ball_commentary = f'[{current_ball}]: {current_batsman} scored: {c_run}'

            print(f"{ball_commentary}")
            time.sleep(0.2)


play_inninings()
```

    
    playing : over 1
    --------------------
    
    [0]: Dhoni scored: 2
    [1]: Dhoni scored: 4
    [2]: Dhoni scored: 2
    [3]: Dhoni scored: 3
    [4]: Dhoni scored: 2
    [5]: Dhoni scored: 0
    
    playing : over 2
    --------------------
    
    [0]: Dhoni scored: 4
    [1]: Dhoni scored: 4
    [2]: Dhoni scored: 4
    [3]: Dhoni scored: 2
    [4]: Dhoni scored: 6
    [5]: Dhoni scored: 4



```python
!pip show langchain
```

    Name: langchain
    Version: 0.3.8
    Summary: Building applications with LLMs through composability
    Home-page: https://github.com/langchain-ai/langchain
    Author: 
    Author-email: 
    License: MIT
    Location: /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages
    Requires: aiohttp, langchain-core, langchain-text-splitters, langsmith, numpy, pydantic, PyYAML, requests, SQLAlchemy, tenacity
    Required-by: langchain-community



```python

```


```python

```


```python
import random
import asyncio

from langchain.llms import Ollama
from langchain.prompts import PromptTemplate
from langchain.chains import LLMChain
```


```python
llm = Ollama(
    model       = "mistral",
    base_url    = "http://localhost:11434"
)
```

    /var/folders/26/1_zstvd1579g9j700z2jnmp40000gn/T/ipykernel_21328/1983929500.py:1: LangChainDeprecationWarning: The class `Ollama` was deprecated in LangChain 0.3.1 and will be removed in 1.0.0. An updated version of the class exists in the :class:`~langchain-ollama package and should be used instead. To use it run `pip install -U :class:`~langchain-ollama` and import as `from :class:`~langchain_ollama import OllamaLLM``.
      llm = Ollama(



```python
template = """
You are a Cricket Commentator who makes one line Criket Commentary. Please provide one line commentary about the given run.
Your commentary shoud be between 20 to 40 words:

{run}
"""
```


```python
prompt = PromptTemplate(
    input_variables = ["run"],
    template        = template,
)

```


```python
llm_chain = LLMChain(
    llm     = llm,
    prompt  = prompt
)
```

    /var/folders/26/1_zstvd1579g9j700z2jnmp40000gn/T/ipykernel_21328/1737174222.py:1: LangChainDeprecationWarning: The class `LLMChain` was deprecated in LangChain 0.1.17 and will be removed in 1.0. Use :meth:`~RunnableSequence, e.g., `prompt | llm`` instead.
      llm_chain = LLMChain(



```python
def get_magic_commentary(score):
    return llm_chain.run(score = score)
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

# Define a prompt template
template = """
You are a Cricket Commentator who makes one line Criket Commentary. Please provide one line commentary about the given run.
Its a plain commentary for a ball, dont add batsmen name.
You commentary shoud be between 20 to 40 words:

{run}
"""

prompt = PromptTemplate(
    input_variables = ["run"],
    template        = template,
)

# Create a chain
llm_chain = LLMChain(
    llm     = llm,
    prompt  = prompt
)

def q(run):
    return llm_chain.run(run = run)

def get_magic_commentary(run):
    return llm_chain.run(run = run)

print(get_magic_commentary(6))

```

     A towering six over midwicket! Boundary brings momentum swinging back in favor of the batsman.



```python
from langchain.llms import Ollama
from langchain.prompts import PromptTemplate
from langchain.chains import LLMChain
import asyncio


async def play_inninings():

    over_count          = 2
    current_over_balls  = 6

    for current_over in range(over_count):

        log_content = f'\nplaying : over {current_over + 1}'
        yield f"{log_content}"

        for current_ball in range(current_over_balls):
            current_ball += 1

            current_batsman = "Sachin"

            c_run = get_random_run()

            magic_commentary = get_magic_commentary(c_run)
            ball_commentary = f'[{current_over}.{current_ball}]: {current_batsman} scored: {c_run}   {magic_commentary}'

            yield f"{ball_commentary}"
            await asyncio.sleep(0.2)

        await asyncio.sleep(0.2)


```


```python
import nest_asyncio
nest_asyncio.apply()
```


```python
async def main():
    async for result in play_inninings():
        print(result)

asyncio.run(main())
```

    
    playing : over 1
    [0.1]: Sachin scored: 3    Three runs, beautifully orchestrated with a delicate touch and accurate placement, reminiscent of an artist painting with precision.
    [0.2]: Sachin scored: 4    Four! Cleanly dispatched over mid-wicket, no chance for the fielder.
    [0.3]: Sachin scored: 1    Single converted through delicate wrists, neatly placed for easy pickings.
    [0.4]: Sachin scored: 4    Four! Cleanly dispatched over the ropes, no chance for the fielders there.
    [0.5]: Sachin scored: 3    Three runs off a well-timed drive and a swift scamper by the batsmen. Fine execution under pressure.
    [0.6]: Sachin scored: 0    Dot ball! Batsman looking to break free, but bowler maintains tight lines.
    
    playing : over 2
    [1.1]: Sachin scored: 3    Three runs scampered through a mix-up, no direct hit from the deep.
    [1.2]: Sachin scored: 3    Three runs scampered through tight fielding as batsman made full use of the gap.
    [1.3]: Sachin scored: 6    Six! Cleanly dispatched over the ropes as the crowd erupts in delight. Superb shot!
    [1.4]: Sachin scored: 0    Run missed as the delivery slides past the batsman's attempted drive, narrowly avoiding the stumps.
    [1.5]: Sachin scored: 3    Three runs scampered through a mix-up, narrowly avoiding an incoming fielder's grab.
    [1.6]: Sachin scored: 2    Two runs scampered through a mix-up, close call at the non-striker's end.



```python

```


```python
#!pip install nest_asyncio
```


```python
import random
import asyncio

from langchain.llms import Ollama
from langchain.prompts import PromptTemplate
from langchain.chains import LLMChain

# Initialize the Ollama LLM with the Mistral model
llm = Ollama(
    model       = "mistral",
    base_url    = "http://localhost:11434"
)

# Define a prompt template
template = """
You are a Cricket Commentator who makes one line Criket Commentary. Please provide one line commentary about the given run.
Its a plain commentary for a ball, dont add batsmen name.
You commentary shoud be between 20 to 40 words:

{run}
"""

prompt = PromptTemplate(
    input_variables = ["run"],
    template        = template,
)

# Create a chain
llm_chain = LLMChain(
    llm     = llm,
    prompt  = prompt
)

def q(run):
    return llm_chain.run(run = run)

def get_magic_commentary(run):
    return llm_chain.run(run = run)

def get_random_number(minimum = 0, maximum = 6):
    return random.randint(minimum, maximum)

def get_random_run():
    r_run = get_random_number(0, 6)

    if r_run == 5:
        return 4

    return r_run

async def play_inninings():

    over_count          = 2
    current_over_balls  = 6

    for current_over in range(over_count):

        log_content = f'\nplaying : over {current_over + 1}'
        yield f"{log_content}"

        for current_ball in range(current_over_balls):
            current_ball += 1

            current_batsman = "Dhoni"

            c_run = get_random_run()

            magic_commentary = get_magic_commentary(c_run)
            ball_commentary = f'[{current_over}.{current_ball}]: {current_batsman} scored: {c_run}   {magic_commentary}'

            yield f"{ball_commentary}"
            await asyncio.sleep(0.2)

        await asyncio.sleep(0.2)


async def main():
    async for result in play_inninings():
        print(result)

asyncio.run(main())
```

    
    playing : over 1
    [0.1]: Dhoni scored: 4    Four! Beautifully timed, finds the gap between third man and deep backward point.
    [0.2]: Dhoni scored: 1    Single secured with a well-timed push towards cover, no need for a dash this time.
    [0.3]: Dhoni scored: 4    Four! Majestic drive finds the boundary, cleanly timed. Great shot!
    [0.4]: Dhoni scored: 4    A well-timed drive finds the gap as the batsman races to four runs!
    [0.5]: Dhoni scored: 4    Four! Beautifully dispatched, that's raced away to the boundary!
    [0.6]: Dhoni scored: 4    Four! Cleanly dispatched over the rope for another boundary. Timing perfect from the batsman.
    
    playing : over 2
    [1.1]: Dhoni scored: 6    Six! Clean hit over long-on, crowd goes wild!
    [1.2]: Dhoni scored: 4    Four! Boundary off the edges, perfect placement from the batsman.
    [1.3]: Dhoni scored: 2    Fluent drive, perfectly timed, pair adds another twosome to the tally.
    [1.4]: Dhoni scored: 6    Six! Powerful hit clears the ropes for another maximum. Spectacular shot!
    [1.5]: Dhoni scored: 4    Four! Superbly timed drive finds the gap, clean as a whistle.
    [1.6]: Dhoni scored: 1    Single converted, fielders' concentration wanes under pressure.



```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python
import random
import asyncio

from langchain.llms import Ollama
from langchain.prompts import PromptTemplate
from langchain.chains import LLMChain

# Initialize the Ollama LLM with the Mistral model
llm = Ollama(
    model       = "mistral",
    base_url    = "http://localhost:11434"
)

# Define a prompt template
template = """
You are a Cricket Commentator who makes one line Cricket Commentary. Please provide one line commentary about the given run.
It's a plain commentary for a ball, don't add batsman's name.
Your commentary should be between 20 to 40 words:

{run}
"""

# Define the prompt template and chain
prompt = PromptTemplate(
    input_variables=["run"],
    template=template,
)

# Create the chain for generating commentary
llm_chain = LLMChain(
    llm=llm,
    prompt=prompt
)

# Function to get magic commentary for a given run
def get_magic_commentary(run):
    return llm_chain.run(run=run)

# Function to generate a random number (0-6) for the run
def get_random_number(minimum=0, maximum=6):
    return random.randint(minimum, maximum)

# Function to get a random run (with special case for 5)
def get_random_run():
    r_run = get_random_number(0, 6)
    if r_run == 5:
        return 4  # Special case for 5; treating it as 4
    return r_run

# Asynchronous function to simulate the innings and commentary
async def play_innings():
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

# Main function to run the simulation
async def main():
    async for result in play_innings():
        print(result)

# Run the main function asynchronously
asyncio.run(main())

```

    
    Playing: over 1
    [1.1]: Dhoni scored: 6    Six! Cleanly dispatched over the ropes for another maximum.
    [1.2]: Dhoni scored: 3    Three runs scampered through a mix-up as the throw found the striker short of his ground. Tense moments in the outfield!
    [1.3]: Kohli scored: 3    Three runs scampered through a mix-up, fielder's throw narrowly missing the stumps!
    [1.4]: Dhoni scored: 6    Six! Cleanly dispatched over the boundary rope, no chance for the fielders. Spectacular strike!
    [1.5]: Dhoni scored: 1    Single down to long-on, deftly worked by the middle order.
    [1.6]: Kohli scored: 4    Four! Beautifully timed, finding the gap through point.
    
    Playing: over 2
    [2.1]: Kohli scored: 4    A well-timed drive finds the gap, another boundary for the team.
    [2.2]: Kohli scored: 4    Four! Seamer strays on the pads, batsman makes room and flicks it fine for four.
    [2.3]: Kohli scored: 0    Nothing much to write home about, just a dot ball.
    [2.4]: Kohli scored: 4    Another boundary off the free hit, no need for a second invitation!
    [2.5]: Kohli scored: 3    Three runs scampered through a mix-up, no-one's bat in sight. Splendid fielding keeps them on their toes.
    [2.6]: Dhoni scored: 6    Six over deep mid-wicket, cleanly dispatched!



```python

```


---
**Score: 40**
