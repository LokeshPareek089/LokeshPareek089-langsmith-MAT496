# LokeshPareek089-langsmith-MAT496
# Module 1:
  * Lesson-01: Tracing Basics
    * Summary: Trace is structured record of the execution of a workflow(in this case, of an LLM Call).
    * Source File: https://github.com/langchain-ai/intro-to-langsmith/blob/661952bca6c5196a8d60c5a3d64448206ca07ba4/notebooks/module_1/tracing_basics.ipynb
    * Changes Made:
      App Versioning: Bumped APP_VERSION to 1.1 and linked it to runtime metadata.
      System Prompt Customization: Changed the system prompt to be teaching-focused with examples.
      Metadata: Added richer metadata (vectordb, environment, app_version, model_name, model_provider,
      temperature).
      Tags: Introduced tags (rag, retrieval, generation, llm, pipeline) for better filtering in LangSmith.
      Debug Logging: Added local debug prints of question/answer for quick inspection.

  * Lesson-02: Types of Runs
    * Summary: LangSmith tracks and visualizes different types of executions (called “runs”) in your
      language model applications. These help you debug, monitor, and improve your system. Types Runs:
      LLM,Retriever, Tool, Prompt, Chain, Praiser.
    * Source File: https://github.com/langchain-ai/intro-to-langsmith/blob/661952bca6c5196a8d60c5a3d64448206ca07ba4/notebooks/module_1/types_of_runs.ipynb
    * Changes Made:
      Added defensive checks in the chat model cell to ensure messages is a list of dicts with required
      keys.
      Avoided mutating the input list by creating a new list when adding the assistant's suggestion.
      Wrapped the chat model call in a try/except block to catch and print errors with clear messages.
      Improved robustness and error handling for Groq API calls in the notebook.
