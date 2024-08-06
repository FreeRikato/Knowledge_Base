Tadashi is a toy project that i am planning to build. The main objective of this project is fact checking my thoughts/zettelkastens. This is a Gen-AI project that would review my thoughts from Obsidian Vault especially in Zettelkasten folder and check if i have stated any fact wrong and How grammatically right I am.

## Tentative Plan

- Local storage (Mostly SQLite - Refer [[Choosing the right database]]) that keeps track of untracked files
- Untracked files would be which are newly added - deleted - udpated (basically) and need reviewing like git changes
- The tracked files no need reviewing and untracked files would be listed and reviewed.
- Suggestions would be rendered alongside the notes when clicked with Grammar scores
- Then, the user can do the changes or ignore it. The user will add it to tracked files

> The main challenge would be to check for facts that are more recent, since LLMs have a knowledge cutoff date and wouldn't be aware of the information if the notes is about something that is after the LLM's Knowledge cutoff date

=> To solve this problem, I should think of creating an agent/system that browses and researches about an information that is not sure of (adaptive rag reference).

## Algorithm

Step 1: The LLM would go through a note and checks if it needs to refer the knowledge base
Step 2: If yes, go to step 3 else go to step 6
Step 3: Uses similarity search to list out relevant chunks of information and grades them based on the information that it is not sure of in the first place
Step 4: If there are no graded documents above a set threshold then go to step 5 else go to step 6
Step 5: Research on web to find relevant information
Step 6: Fact check the notes to find places where it sounds wrong
Step 7: Evaluate Grammar scores
Step 8: Render suggestions and grammar scores

Refer below to visualize the agentic workflow, state propagation and architecture diagram, 
[[Tadashi Visualize]]

