We are building a hallucination reduction / instruction following ensuring system for small to medium language models that do not require high amounts of compute.

The goal is to create a system that can be deployed at the edge that ensures that small to medium language models used in agentic scenarios can adhere to instructions without the correction system requiring the similarly high compute as the generation system.

The idea is as follows:

The main instructions to the agent are given in the system prompt itself referred to as the positive prompt. Then some negative text i.e text that the agent could generate when it is deviating from the instruction, is stored as embedding in a vector db

eg:
positive: "to create a PDF write the document in latex and convert it using pdflatex"
negative counter parts: "i cannot create PDFs", "let me write the PDF document as markdown"

The modification to the regular agentic loop is as follows:
1. the user sends a message
2. the LLM generates a response 
3. the response is split into sentences and matched against the negative prompt db
4. if something is matched then the corresponding positive prompt of the matched negative prompt is retreived and appended to the user's response as a message from a "guide"
5. the last response from the LLM is discarded and a new response is generated using the modified user message
6. repeat until the LLM response does not have a high match with any of the items in the DB