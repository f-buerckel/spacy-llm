## Changed spacy to support vllm api through openai

### Endpoint & Behavior Changes

| Aspect | Change | Modified File |
|--------|-----------|---------------|
| Chat endpoint | `http://localhost:8001/v1/chat/completions` | [`model.py`](spacy_llm/models/rest/openai/model.py) |
| Completions endpoint | `http://localhost:8001/v1/completions` | [`model.py`](spacy_llm/models/rest/openai/model.py) |
| Models healthcheck URL | `http://localhost:8001/v1/models` | [`model.py`](spacy_llm/models/rest/openai/model.py) |
| Additional OSS model | Added registry `gpt-oss-20b` (`openai/gpt-oss-20b`) | [`registry.py`](spacy_llm/models/rest/openai/registry.py) |

### Added example for NER using VLLM and gpt-oss
[Entity Recognition using VLLM and GPT-oss](usage_examples/ner_v3_vllm_gpt-oss/)

### To install with pip or as a dep through setup.py

```
setup(
    name="my-project",
    version="0.1.0",
    packages=find_packages(),
    install_requires=[
        "spacy-llm @ git+https://github.com/f-buerckel/spacy-llm.git@main",
    ],
)
```

Or with Pip:

```
pip install git+https://github.com/f-buerckel/spacy-llm.git@main
```