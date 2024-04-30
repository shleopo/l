**Multiple Choice Questions**

There are 20 questions in total, 4 single-choice questions, and 16 multiple-choice questions, with a total score of 100 points.

**1. The core components of LangChain include?** ABDE
A. Chain
B. Memory
C. Agent
D. Model
E. Database

**2. What is the main difference between Chat models and Text models?** C 
A. Chat models are newer
B. Chat models return data in a different format than Text models
C. Chat models can have role prompts in messages
D. Text models can transmit multiple messages at once

**3. Which steps can be included in the construction of a local document question-answering system?** ABCDE
A. Loading: Document loader loads documents into a format that LangChain can read
B. Splitting: Text splitter divides documents into specified sizes of segments, i.e., "document blocks" or "document pieces"
C. Storage: Store segmented "document blocks" in the form of "embeddings" into a vector database to form individual "embedding pieces"
D. Retrieval: Retrieve segmented documents from storage
E. Synthesis: Pass the question and similar embedding pieces to the language model to generate answers

**4. Which components are included in the Model I/O module of LangChain?**ABCD
A. Model: The core of Model I/O is calling the model
B. Prompt: Pass prompt information into the model through prompt templates and prompt engineering
C. Generation: Generate answers by retrieving local documents
D. Output Parsing: Parse the response content returned by the model into the correct format

**5. Which prompt template should you choose if you want to implement a few-shot prompt?** C
A. PromptTemplate
B. ChatPromptTemplate
C. FewShotPromptTemplate
D. PipelinePromptTemplate

**6. What specific content should be included in the CoT prompt template?**ABC
A. Description of AI's roles and goals
B. Explanation of thought chains
C. Some examples following the thought chain
D. Beam search of multiple thought paths

**7. In LangChain, what are the methods to call open-source models?** ABC
A. LangChain's built-in open-source model interface
B. Through HuggingFace Hub
C. Through HuggingFace Pipeline
D. Through the Base.LLM interface to call custom language models

**8. Scenario: You are building an intelligent writing assistant that can generate an article based on prompts provided by the user. You use GPT-3 as the language model. The output of GPT-3 is a piece of raw text, and you need to convert it into structured JSON format for further processing in your application.**
**Question: In this scenario, which LangChain output parser would you choose?** C
A. PydanticOutputParser
B. XMLOutputParser
C. StructuredOutputParser
D. CommaSeparatedListOutputParser

**9. Which type of memory can remember summaries of conversations from many rounds ago and also remember the raw content of recent conversations?** D
A. ConversationBufferMemory
B. ConversationBufferWindowMemory
C. ConversationSummaryMemory
D. ConversationSummaryBufferMemory

**10. What are the different ways to invoke a chain?** ABCD
A. Direct invocation
B. Through the run method
C. Through the predict method
D. Through the apply method
E. Through the generate method

**11. How to build a question-answering chain that selects relevant prompts based on the question using RouterChain?** ABD
A. Define several prompts and related destinationChains.
B. Build RouterChain, such as LLMRouterChain.
C. Combine destination Chain and RouterChain into MultiPromptChain.
D. RouterChain will select relevant prompts and destination Chains to answer the question based on the problem.

**12. Regarding the ReAct framework for intelligent agents, which of the following statements is correct?** A
A. The inspiration for the ReAct framework comes from the synergy between "action" and "reasoning."
B. ReAct can learn new tasks and make decisions or inferences.
C. ReAct can be considered the most popular frontend development framework currently.
D. The specific steps of ReAct are observe, think, act.

**13. The characteristics of a structured tool dialogue agent include?**B
A. Using ReAct logic.
B. Being able to call multiple tools to complete complex tasks.
C. Only being able to call a single tool to ensure the accuracy of the large model.
D. Managing the conversation process through interaction between two agents.

**14. AgentExecutor is a component in LangChain used to drive agent models and tool chains to complete various tasks. Which of the following descriptions about its working principle are correct?** BC
A. AgentExecutor directly calls LLM to generate responses.
B. AgentExecutor maintains a tool chain and passes it to the agent.
C. AgentExecutor is responsible for parsing the output of the agent.
D. AgentExecutor calls a new agent instance for each task.

**15. What steps does LangChain take when calling tools?** AB
A. Initialize tools.
B. Add tools to the Toolkit object that manages them.
C. Call .run0 on the Toolkit object, passing input.
D. Call .run0 directly on the tool.

**16. Which steps summarize the working principle of RAG?** ABC
A. Retrieval: Retrieve relevant documents or paragraphs from a large document collection using a retrieval system for a given input (question).
B. Context encoding: Encode the relevant documents or paragraphs found with the original input (question).
C. Generation: Generate output (answers) using the encoded context information through a large model.
D. Checking: Check the final information for accuracy through search functionality.

**17. Steps to implement a simple SQLDatabaseChain for retrieving documents from an SQL database include?** ABCDE
A. Initialize SQL database connection.
B. Define SQL query statements to match queries based on the question text.
C. Define database retrieval functions to query the database and return a list of documents.
D. Build SQLDatabaseChain, passing database retrieval functions and LLM.
E. Use the Chain's run method, passing the question and returning result documents.

**18. Where can the Callback mechanism be used in LangChain?** ABCDEF
A. Before LLM execution.
B. After LLM execution.
C. Before Tool execution.
D. After Tool execution.
E. Before Chain execution.
F. After Chain execution.

**19. Which type of agent is considered a simulation agent (role-playing in a simulated environment, attempting to simulate specific scenarios or behaviors)?** D
A. AutoGPT
B. BabyAGI
C. CAMEL
D. HuggingGPT

**20. Which of the following statements is correct?** B
A. AutoGPT can automatically link multiple tasks to achieve large objectives.
B. The characteristic of BabyAGI is the integration of multimodal perception capabilities to handle multiple AI tasks.
C. HuggingGPT selects appropriate expert models from Hugging Face to execute tasks.
D. AutoGPT, BabyAGI, and HuggingGPT are all self-driven (autonomous) agents.

## Practical Questions

**Project**: Internal Employee Knowledge Base Q&A System.

**Project Description**: "Floral" is a large-scale online flower sales platform with its own business processes and standards, as well as Standard Operating Procedure (SOP) manuals for employees. Relevant information is shared during new employee onboarding training. However, this information is scattered across various internal websites and directories of the HR department, making it inconvenient to access at times. Additionally, employees may struggle to find the desired content promptly due to lengthy documents, and sometimes, company policies are updated while employees still have outdated document versions.

To address these needs, we will develop a "Doc-QA" system based on various internal knowledge manuals.

This question-and-answer system will understand employees' inquiries and provide precise answers based on the latest employee manuals.

**Prepared Data:**

Internal data includes various files in PDF, Word, and TXT formats. These have already been provided.
