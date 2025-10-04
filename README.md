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

  * Lesson-03: Alternative Ways to Trace
    * Summary:This video teaches alternative  methods for tracing in LangSmith beyond setting environment
      variables. It focuses on achieving selective observability by manually passing a LangChainTracer
      as a callback or using the tracing_context manager to trace specific code blocks.
    * Source File: https://github.com/langchain-ai/intro-to-langsmith/blob/main/notebooks/module_1/alternative_tracing_methods.ipynb
    * Changes Made:
      Added a function to check for internet connectivity before making API calls, preventing
      unnecessary errors if offline.
      Provided user-friendly, visually distinct messages for different error types (no internet,
      connection error, HTTP error, unexpected error).
      Used emoji icons (✅, ❌, 🚫, 🌐) to make feedback more engaging and clear.
      Ensured that all exceptions are caught and explained, not just shown as raw tracebacks.
      Clearly separated success and error output, making it easier to understand what happened during
      execution.

  * Lesson-04: Conversational Threads
    * Summary: The video teaches us how to use LangSmith to group sequential agent "runs" into a single
      conversation thread. This is achieved by adding a unique identifier (like a session_id) to the
      metadata of each run. This feature is crucial for debugging, evaluating, and tracking
      conversation memory in multi-turn chatbot applications.
    * Souce File: https://github.com/langchain-ai/intro-to-langsmith/blob/661952bca6c5196a8d60c5a3d64448206ca07ba4/notebooks/module_1/conversational_threads.ipynb
    * Changes Made:
      Random Emoji in System Prompt:
        Each system prompt now includes a randomly selected emoji for a more engaging and playful
        assistant experience.
      Creative and Informative Print Statements:
      Added print statements throughout the retrieval and generation process to provide clear, fun, and
        informative feedback about what the code is doing.
      Creative Question Prompts:
        The questions in the last two code cells were updated to be more imaginative and open-ended,
        encouraging creative responses.
      Emojis in Output Display:
        The answers are printed with relevant emojis (e.g., 📈, 🎨) to make the output visually
        appealing and thematic.
