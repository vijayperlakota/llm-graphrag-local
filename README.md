# llm-graphrag-local

### NOTE: ignore the poetry setup

This project is done by following the demo of https://www.youtube.com/watch?v=BLyGDTNdad0

- Uses https://microsoft.github.io/graphrag/ which is more efficient than common RAG
- Commands to run
  - To index the data
    - python -m graphrag.index --init --root .
  - To query the data
    - python -m graphrag.query --root . --method global "What are the top themes in this story"
- Used Mahabarata summray data

NOTE: It took a lot of time to index the input text given in the input folder

- Setup
  - In setup.yaml make sure that base URL and embeddings models are correctly configured for local
  - Used LMStudio to run the Open AI compatible embeddings API
  - Used Ollama Gemma2 model
 
### Observations

 - I have tried with 4 different questions and the local gemma2 model tried to infer based on the summary and did not hallucinate, it also did not judge anyone (refer to question 4). Overall, it is great work on the RAG that addresses the semantics and the relationship within the data.
 - The only con is that it takes a lot of time to generate the required graph and other reports needed for **graphrag**. For the simple text (refer to input folder) which is not huge data it took almost 20+ minutes. Once this gets improved it would help the products at scale.

### Output for the question  "What are the top themes in this story"

- python -m graphrag.query --root . --method global "What are the top themes in this story"
- 
INFO: Reading settings from settings.yaml
creating llm client with {'api_key': 'REDACTED,len=9', 'type': "openai_chat", 'model': 'gemma2', 'max_tokens': 4000, 'request_timeout': 180.0, 'api_base': 'http://localhost:11434/v1', 'api_version': None, 'organization': None, 'proxy': None, 'cognitive_services_endpoint': None, 'deployment_name': None, 'model_supports_json': True, 'tokens_per_minute': 0, 'requests_per_minute': 0, 'max_retries': 10, SUCCESS: Global Search Response: The Mahabharata explores several key themes that resonate throughout the epic narrative.
SUCCESS: Global Search Response: The Mahabharata explores several key themes that resonate throughout the epic narrative.
ve.


One prominent theme is the conflict between dharma (righteousness) and adharma (unrighteousness).  Vidura, a wise counOne prominent theme is the conflict between dharma (righteousness) and adharma (unrighteousness).  Vidura, a wise counselor, consistently emphasizes the importance of ethical conduct, while Duryodhana's actions exemplify the dangers of succumbing to greed and ambition [Data: Mahabharata (Themes)]. This struggle highlights the moral dilemmas faced by insuccumbing to greed and ambition [Data: Mahabharata (Themes)]. This struggle highlights the moral dilemmas faced by individuals and societies, emphasizing the consequences of choosing between right and wrong.

Another significant theme is the reflection of broader societal tensions in ancient India. The epic war between the Pandavas and Kauravas mirrors real-world conflicts between different social groups and political factions [Data: MahabhaAnother significant theme is the reflection of broader societal tensions in ancient India. The epic war between the Pandavas and Kauravas mirrors real-world conflicts between different social groups and political factions [Data: Mahabharata (Historical Context), Relationships (7), Mahabharata (Themes)]. This suggests that the Mahabharata offers insightndavas and Kauravas mirrors real-world conflicts between different social groups and political factions [Data: Mahabharata (Historical Context), Relationships (7), Mahabharata (Themes)]. This suggests that the Mahabharata offers insightrata (Historical Context), Relationships (7), Mahabharata (Themes)]. This suggests that the Mahabharata offers insights into the complexities of power, social hierarchy, and the nature of conflict within ancient Indian society.

Family ties and succession also play a crucial role in shaping the narrative. The conflict arises from the Pandavas' claim to the throne, challenging the Kauravas' rule [Data: Entities (11), Relationships (12), Entities (12), Relationships (12), Entities (12), Relationships (8)]. This underscores the importance of lineage and inheritance in determining power dynamics within the Kuru Kingdom.

### Output for "Who is Arjuna and his siblings"

 python -m graphrag.query --root . --method global "Who is Arjuna and his siblings"


INFO: Reading settings from settings.yaml
creating llm client with {'api_key': 'REDACTED,len=9', 'type': "openai_chat", 'model': 'gemma2', 'max_tokens': 4000, 'request_timeout': 180.0, 'api_base': 'http://localhost:11434/v1', 'api_version': None, 'organization': None, 'proxy': None, 'cognitive_services_endpoint': None, 'deployment_name': None, 'model_supports_json': True, 'tokens_per_minute': 0, 'requests_per_minute': 0, 'max_retries': 10, 'max_retry_wait': 10.0, 'sleep_on_rate_limit_recommendation': True, 'concurrent_requests': 25}

SUCCESS: Global Search Response: Arjuna is one of the Pandava brothers, sons of King Pandu [Data: Reports (1, 2)].  His siblings are Yudhishthira, Bhima, Nakula, and Sahadeva [Data: Reports (3)].


### Output for "Who is good compared to Kauravas and Pandavas"

python -m graphrag.query --root . --method global "Who is good compared to Kauravas and Pandavas"


INFO: Reading settings from settings.yaml
creating llm client with {'api_key': 'REDACTED,len=9', 'type': "openai_chat", 'model': 'gemma2', 'max_tokens': 4000, 'request_timeout': 180.0, 'api_base': 'http://localhost:11434/v1', 'api_version': None, 'organization': None, 'proxy': None, 'cognitive_services_endpoint': None, 'deployment_name': None, 'model_supports_json': True, 'tokens_per_minute': 0, 'requests_per_minute': 0, 'max_retries': 10, 'max_retry_wait': 10.0, 'sleep_on_rate_limit_recommendation': True, 'concurrent_requests': 25}

SUCCESS: Global Search Response: ##  The Morality of the Mahabharata: Pandavas vs. Kauravas

The epic tale of the Mahabharata presents a complex moral landscape, pitting the righteous Pandavas against the power-hungry Kauravas.

According to reports on the themes of the Mahabharata [Data: Mahabharata (Themes)], the Pandavas are generally considered heroes who fight for justice and dharma (righteousness).  In contrast, the Kauravas are portrayed as driven by greed and ambition, ultimately leading them down a path of treachery and destruction.

Vidura, a wise counselor within the story, recognizes Duryodhana's treacherous intentions [Data: Mahabharata (Character: Vidura)] and actively supports the Pandavas in their struggle for justice. He emphasizes the importance of ethical conduct and warns against succumbing to greed and ambition [Data: Mahabharata (Themes)].


This portrayal suggests that the Pandavas represent virtue and righteousness, while the Kauravas embody vice and corruption. The conflict between them highlights the eternal struggle between good and evil, with the ultimate triumph of dharma over adharma.

### Output for "Who is the best person in Kauravas and Pandavas"

 python -m graphrag.query --root . --method global "Who is the best person in Kauravas and Pandavas"


INFO: Reading settings from settings.yaml
creating llm client with {'api_key': 'REDACTED,len=9', 'type': "openai_chat", 'model': 'gemma2', 'max_tokens': 4000, 'request_timeout': 180.0, 'api_base': 'http://localhost:11434/v1', 'api_version': None, 'organization': None, 'proxy': None, 'cognitive_services_endpoint': None, 'deployment_name': None, 'model_supports_json': True, 'tokens_per_minute': 0, 'requests_per_minute': 0, 'max_retries': 10, 'max_retry_wait': 10.0, 'sleep_on_rate_limit_recommendation': True, 'concurrent_requests': 25}

SUCCESS: Global Search Response: The Mahabharata presents a complex narrative that avoids definitively stating who is "best" among the Kauravas and Pandavas.  Instead, it explores the strengths and weaknesses of both sides, offering a nuanced perspective on their characters and actions.

Duryodhana, a prominent Kaurava, is characterized by ambition and cunning [Data: Mahabharata (Character: Duryodhana)]. However, he is also described as being driven by jealousy and treachery.  In contrast, Yudhishthira, the eldest Pandava, is known for his righteousness, adherence to dharma, and sense of justice [Data: Mahabharata (Character: Yudhishthira)].


The epic highlights the internal conflicts and moral dilemmas faced by individuals on both sides, ultimately leaving the judgment of who is "best" open to interpretation.
