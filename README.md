# AI Engineering &mdash; LLM Engineering, RAG, OLoRA, Agents

- This repository contains details related to AI Engineering pertaining to Large Language Models (Proprietary & Open Source), RAGs, OLoRA, and Agentic AI.

## Table of Contents

- [Getting Started](#getting-started)

## Getting Started

- Download Ollama from <https://ollama.com>
- And explore models which have a Context <= 128K (or if you've more memory, go for models which are larger)
  - Check the models at <https://ollama.com/search>
    - Smaller models:
      1. `gemma3:270m` &mdash; `Context: 32K` | `Size >= 290MB`
    - Slightly larger models:
      1. `phi3:latest` &mdash; `Context: 128K` | `Size >= 2.2GB`
    - Large model:
      1. `gpt-oss:latest` &mdash; `Context: 128K` | `Size >= 14GB`
- Demo of using `ollama` via terminal:

  <details>
    <summary><strong>1. <code>gemma3:270m</code></strong></summary>
    <pre><code>
      ~:(0m|git@main) $ ollama serve
      Error: listen tcp 127.0.0.1:11434: bind: address already in use
      ~:(0m|git@main) $ ollama run gemma3:270m
      pulling manifest
      pulling 735af2139dc6: 100% █████████████████████████████████████████████████████████████████████████████████████████ 291 MB
      pulling 4b19ac7dd2fb: 100% █████████████████████████████████████████████████████████████████████████████████████████ 476 B
      pulling 3e2c24001f9e: 100% █████████████████████████████████████████████████████████████████████████████████████████ 8.4 KB
      pulling 339e884a40f6: 100% █████████████████████████████████████████████████████████████████████████████████████████▏61 B
      pulling 74156d92caf6: 100% █████████████████████████████████████████████████████████████████████████████████████████▏490 B
      verifying sha256 digest
      writing manifest
      success
      >>> Hi there, I'm Sriram
      Hi Sriram! How can I help you today?

      >>> Tell me a fun fact?
      Did you know that the smallest animal on Earth is a pocket crab? 

      >>> Another one?
      Okay, another fun fact! 

      >>> Go ahead?
      Yes! 

      >>> Where's the fun fact?
      That's a great question! 😊

      >>> OK
      Okay! 

      >>> /?
      Available Commands:
        /set            Set session variables
        /show           Show model information
        /load &lt;model>   Load a session or model
        /save &lt;model>   Save your current session
        /clear          Clear session context
        /bye            Exit
        /?, /help       Help for a command
        /? shortcuts    Help for keyboard shortcuts

      Use """ to begin a multi-line message.

      >>> /show
      Available Commands:
        /show info         Show details for this model
        /show license      Show model license
        /show modelfile    Show Modelfile for this model
        /show parameters   Show parameters for this model
        /show system       Show system message
        /show template     Show prompt template

      >>> /show info
        Model
          architecture        gemma3     
          parameters          268.10M    
          context length      32768      
          embedding length    640        
          quantization        Q8_0       

        Capabilities
          completion    

        Parameters
          stop     "&lt;end_of_turn>"    
          top_k    64                 
          top_p    0.95               

        License
          Gemma Terms of Use                  
          Last modified: February 21, 2024    
          ...
      </code></pre>
  </details>

  <details>
    <summary><strong>2. <code>phi3:latest</code></strong></summary>
    <pre><code>
      ~:(0m|git@main) $ ollama run phi3:latest
      pulling manifest
      pulling 633fc5be925f: 100% ████████████████████████████████████████████████████████████████████████████████████████▏ 2.2 GB
      pulling fa8235e5b48f: 100% ████████████████████████████████████████████████████████████████████████████████████████▏ 1.1 KB
      pulling 542b217f179c: 100% ████████████████████████████████████████████████████████████████████████████████████████▏  148 B
      pulling 8dde1baf1db0: 100% ████████████████████████████████████████████████████████████████████████████████████████▏   78 B
      pulling 23291dc44752: 100% ████████████████████████████████████████████████████████████████████████████████████████▏  483 B
      verifying sha256 digest
      writing manifest
      success
      >>> Hi, I'm Sriram
      Hello! How can I assist you today?

      >>> Tell me what's the weather like in Australia in an yearly basis?
      As of my latest update, here is a general outline for Australian climate throughout different seasons:
      - Spring (September to November): Generally mild with warm days and cool nights. The southern parts tend to be warmer while the northern regions experience more rainfall due to convective thunderstorm 
      activity known as "monsoon season." This can lead to flooding in some areas, especially along the eastern coast where it's heavily populated.
      - Summer (December to February): Warm and dry weather dominates except for occasional tropical storms impacting Northern Australia. It’s also a time of significant bushfires risk due to strong wind 
      conditions during this season which can extend into late spring in the south, sometimes referred to as "fire seasons."
      - Autumn (March to May): Cooler temperatures return; it's still relatively dry except for occasional thunderstorm activity. This is also peak tourist season with attractions like wine tasting and orchard 
      picking in warmer areas, such as the Hunter Valley region near Sydney or Yarra Valley close to Melbourne.
      - Winter (June to August): The coldest temperatures of the year are experienced; snow can fall at higher altitudes but is rare along coastal regions except for Tasmania and parts like Kangaroo Island 
      which regularly receives significant winter snowfall in late spring, leading occasionally into summer months as well.

      This gives a rough idea based on historical weather patterns, climate data over the past decades suggest that temperatures have been rising with an increased frequency of heatwaves and drought conditions 
      especially during summers affecting agriculture (notably grain crops) in some areas along the east coast like Queensland.
      </code></pre>
  </details>
