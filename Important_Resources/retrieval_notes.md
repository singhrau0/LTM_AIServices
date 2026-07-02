# Retrieval Notes for Future Agent Bot

These notes describe how to make this repository easy to search with a future Q&A agent.

## Recommended Indexing Units

Index content at these levels:

- One markdown section per topic.
- One notebook markdown cell per concept.
- One notebook code cell per runnable step.
- One dataset file entry with a short description.
- One PDF or DOCX entry with extracted text and source path.

## Suggested Metadata

Attach this metadata to every indexed chunk:

- `day`
- `date`
- `level`
- `topic`
- `resource_type`
- `source_path`
- `tags`
- `prerequisites`
- `related_days`

## Retrieval Strategy

Use `course_map.json` as the source of truth for paths and tags. For notebooks, extract markdown and code cells separately so students can ask both conceptual and implementation questions.

All current course entries are marked as `beginner` level.

Good student questions the bot should answer:

- Which lab should I revise before LSTM?
- Where is the CNN image preprocessing notebook?
- What is the difference between RNN and LSTM?
- Which resources cover model evaluation?
- How do I load the IMDB movie review dataset in Keras?
- Where is the beginner TF-IDF text classification lab?
- Which lab explains attention and transformers?
- Which lab covers summarization, sentiment, and chatbot patterns?

## Maintenance Rule

Whenever a new lab is added:

1. Add the file inside the correct `Day_XX` folder.
2. Update `README.md`.
3. Update `labs_index.md`.
4. Update `course_map.json`.
5. Add clear tags for retrieval.
