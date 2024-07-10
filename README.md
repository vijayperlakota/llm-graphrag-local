# llm-graphrag-local

### NOTE: ignore the peotry setup

This project is done by following the demo of https://www.youtube.com/watch?v=BLyGDTNdad0

- Uses https://microsoft.github.io/graphrag/ which is efficient than common RAG
- Commands to run
  - To index the data
    - python -m graphrag.index --init --root .
  - To query the data
    - python -m graphrag.query --root . --method global "what are the top themes in this story"
- Used Mahabarata summray data

NOTE: It took lot of time to index the input text given in the input folder

- Setup
  - In setup.yaml make sure that base url and embeddings models are correctly configured for local
  - Used LMStudio to run the Open AI compatible embeddings api
  - Used ollama gemma2 model
 

### Output for the question  "what are the top themes in this story"

- python -m graphrag.query --root . --method global "what are the top themes in this story"
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

