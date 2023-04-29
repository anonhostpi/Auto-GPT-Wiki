Vision goes here. We crystallize it into a roadmap.

TODO:  
    fix memory  
    stateless + async  
    multiagent  

🎯 Auto-GPT - Key Development Focus Areas 🎯

The followindddg are key areas for improvement for AutoGPT.
Making these improvements will go a long way to ensuring better results, and preventing agents from getting 'confused'.



------------------------------------------------------------------
🔧 1. The Supervisor - Keep AutoGPT On-track (Easy) 🔧

Problem: The main agent requires supervision to stay on task, especially when powered by GPT-3.

Solution:

Turns out, LLMS are way better at criticism than they are at generation. We can use this to our advantage.

- Implement a "Supervisor" that observes the agent's actions through 0-shot GPT-3 calls of the last n commands and the initial goals.
- LLMs excel at accurate criticism and can easily identify issues such as an agent being stuck in a loop or using commands incorrectly.
- The supervisor's feedback could be inserted into the "Human Feedback" section.
------------------------------------------------------------------
🔧 2. Knowledge Obtaining / Command Selection System (Medium) 🔧

Problem: AutoGPT frequently searches for information that gpt3 already knows, or asks another agent running the same model to provide information. LLMs do not recognize their own strengths.

Solution (Needs Work):

- Instead of running a command like Google "What is the big bang", create an "Obtain Knowledge" command that first asks GPT-3 and assesses the answer's confidence/accuracy.
- Then, it decides whether to use Google or another command, such as searching the file system, to gain the knowledge.


This idea requires further discussion and development.
------------------------------------------------------------------
🔧 3. Memory That Makes Sense 🔧

Problem:  The purpose of Memory is to overcome the token limit of LLM, our current implementation is misguided. The original implementation allowed the agent to “take notes”, which was pretty effective at this.

The current vector database search uses the previous 5 messages as a search term, and dumps the results in the context window, but this doesn’t really make sense or solve the original problem. 

Solution options:


Simple but very effective: Simply summarise the trimmed message history (actions until this point). This works really well and fits the original purpose of memory.
https://arxiv.org/abs/2304.13343 
Use a 0-shot llm to create a relevant question to poll a vector database (this is flawed as you would need to know what’s relevant for the next step)
------------------------------------------------------------------
🔧 4. Improved Programming Capabilities (Medium) 🔧

Problem:  AutoGPT is currently limited in programming capabilities. GPT-4 excels at programming when prompted correctly and when assisted by a human who has the entire codebase in their head. However, AutoGPT does not have this bigger picture, and GPT-4 has token limitations.

Solution (Needs Work):
I have a fork that does this 80-90% effectively - when we get this done it will change everything.

- Condense a codebase down to its core components and provide this information to individual 0-shot GPT-4 instances tasked with writing a single file. Each GPT-4 instance must know EVERYTHING that can be referenced from another file (e.g., class names, constructors, functions, params, and return types).  (I've developed a schema for this, but it can be much improved)
- Improve coding commands that take in file names and output to file, rather than requiring code as params and return types.
- Develop the ability to search a file for relevant or specific lines of code, then view and edit them based on line numbers (not the entire file).

This idea requires further discussion and development.
------------------------------------------------------------------
🔧 5. Toggleable Commands (Easy) 🔧

Problem: If someone wants to create an agent to write a book for them, currently they're forced to run an agent with irrelevant commands such as the ability to write and execute code.

Solution:
- Toggle-able commands on agent creation
------------------------------------------------------------------
