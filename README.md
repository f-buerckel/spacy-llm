## Changed spacy to support vllm api through openai

### Endpoint & Behavior Changes

| Aspect | Change | Modified File |
|--------|-----------|---------------|
| Chat endpoint | `http://localhost:8001/v1/chat/completions` | [`model.py`](spacy_llm/models/rest/openai/model.py) |
| Completions endpoint | `http://localhost:8001/v1/completions` | [`model.py`](spacy_llm/models/rest/openai/model.py) |
| Models healthcheck URL | `http://localhost:8001/v1/models` | [`model.py`](spacy_llm/models/rest/openai/model.py) |
| Additional OSS model | Added registry `gpt-oss-20b` (`openai/gpt-oss-20b`) | [`registry.py`](spacy_llm/models/rest/openai/registry.py) |
