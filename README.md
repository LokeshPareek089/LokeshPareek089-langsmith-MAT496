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

## Module 2:
 * Lesson-01: Dataset Upload
    * Summary: 
      I learnt how to use LangSmith to create and manage datasets, which are essential for testing and
      evaluating LLM applications. It covers methods for constructing these datasets by either manually
      curating examples or automatically capturing high value traces from your production application
      runs. These structured datasets allow for repeatable, consistent performance testing.
    * Source File: https://github.com/langchain-ai/intro-to-langsmith/blob/661952bca6c5196a8d60c5a3d64448206ca07ba4/notebooks/module_2/dataset_upload.ipynb
    * Changes Made:
      Changed Input Examples to Fundamentals of LLM.
      Added question cells related to the input examples.

 * Lesson-02: Evaluators
    * Summary: 
      We learn the concept of Evaluators in LangSmith as the functions used to score and measure the
      performance of your LLM application outputs. It explains how to define and run different types
      of evaluators—including LLM-as-a-judge and custom code functions—against your datasets to
      quantitatively assess metrics like correctness, relevance, and adherence to specific criteria.
    * Source File: https://github.com/langchain-ai/intro-to-langsmith/blob/661952bca6c5196a8d60c5a3d64448206ca07ba4/notebooks/module_2/evaluators.ipynb
    * Changes Made: 
      Changed the sample run and exaple to check Evaluator's response upon dissimilar outputs.
      Added extra Sample Inputs and outputs to Evaluate my answer.

 * Lesson-03: Experiments
    * Summary:
      I learnt how to use LangSmith to run comparative evaluations on different versions of
      your LLM application against a single dataset. You learn how to systematically test changes (like
      prompt tweaks or model swaps) and use the platform's features to analyze the results from various
      evaluators, allowing you to quickly determine which version performs best.
    * Source File: https://github.com/langchain-ai/intro-to-langsmith/blob/661952bca6c5196a8d60c5a3d64448206ca07ba4/notebooks/module_2/experiments.ipynb
    * Changes Made: 
      Changed Data Set Name in Langsmith.
      Changed Dataset Name to mine in Notebook.
      Tagged the initial version of Dataset in Langsmith.
      Typed Example ids accordingly to the ones displayed in Datasets Upload code.
      Added Crucial Examples split in Dataset.

## Module 3:
 * Lesson 1: Playground Experiments
   * Summary:
      I learnt how to use Playground in Langsmith, to quickly iterate between prompts templates,
      instead of hardcoded promts.
      Easily compare different LLMs using Playground in Langsmith over a dataset.
   * Source File: https://github.com/langchain-ai/intro-to-langsmith/blob/661952bca6c5196a8d60c5a3d64448206ca07ba4/notebooks/module_3/playground_experiments.ipynb
   * Changes Made:
     Changed questions to bit more philosophical ones.
     Changed Dataset name in notebook to Sentience.
     Changed Temperature in Playground Prompt settings to max.
     <img width="3199" height="1851" alt="Screenshot 2025-10-11 170624" src="https://github.com/user-attachments/assets/8a814943-1a90-478b-81ba-ab439135db77" />

 * Lesson 2: Prompt Hub
   * Summary:
     Learnt how to use Langsmith Promt Hub for easy access of versions of Prompts created in Playground.
     Output schema defining the expected structure of a model's response.
   * Source File: https://github.com/langchain-ai/intro-to-langsmith/blob/661952bca6c5196a8d60c5a3d64448206ca07ba4/notebooks/module_3/prompt_hub.ipynb
   * Changes Made:
     Created a Scientist turned Philosopher prompt in Langsmith using Prompt Hub.
     Created another ancient version of it, set in year 1000 AD.
     Changed questions to match the philosophical vibe.

 * Lesson 3: Prompt Engineering Lifecycle
   * Summary:
     I learnt how to apply concepts learnt in Playground and Prompt Hub on a DataSet using RAG
     Application.
   * Source File: https://github.com/langchain-ai/intro-to-langsmith/blob/661952bca6c5196a8d60c5a3d64448206ca07ba4/notebooks/module_3/prompt_engineering_lifecycle.ipynb
   * Changes Made:
     Changed Questions in the Dataset to those similar to Existence, Conciousness & Reality.
     Changed Prompt from Assistant to a Philosopher.
     Updated RAG Application's code from Hardcoded prompt to one that is connected to PrompHub.
      
