# Summary

## Offline

| **Frameworks / Platforms**  |  **Description**|  **Tutorials/lessons**|  **Reference**| 
|--------|------------|------------|------------|
|**Azure AI Studio Evaluation (Microsoft)**|Azure AI Studio is an all-in-one AI platform for building, evaluating, and deploying generative AI solutions and custom copilots.Technical Landscape: No code: model catalog in AzureML studio & AI studio, Low-code: as CLI, Pro-code: as azureml-metrics SDK|[Tutorials](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/evaluation-approach-gen-ai)|[Link](https://ai.azure.com/)|
|**Prompt Flow (Microsoft)**|A suite of development tools designed to streamline the end-to-end development cycle of LLM-based AI applications, from ideation, prototyping, testing, and evaluation to production, deployment, and monitoring.|[Tutorials](https://microsoft.github.io/promptflow/how-to-guides/quick-start.html)|[Link](https://github.com/microsoft/promptflow)|
|**Weights & Biases(Weights & Biases)**|A Machine Learning platform to quickly track experiments, version and iterate on datasets, evaluate model performance, reproduce models, visualize results and spot regressions, and share findings with colleagues. | [Tutorias](https://docs.wandb.ai/tutorials), [DeepLearning.AI Lesson](https://learn.deeplearning.ai/evaluating-debugging-generative-ai) | [Link](https://docs.wandb.ai/)  |
|**LangSmith (LangChain)**|Helps the user trace and evaluate language model applications and intelligent agents to help user move from prototype to production. | [Tutorials](https://docs.smith.langchain.com/evaluation)|  [Link](https://www.langchain.com/langsmith) |
|**TruLens (TruEra)**| TruLens provides a set of tools for developing and monitoring neural nets, including LLMs. This includes both tools for the evaluation of LLMs and LLM-based applications with TruLens-Eval and deep learning explainability with TruLens-Explain.  | [Tutorials](https://www.trulens.org/trulens_explain/quickstart/), [DeepLearning.AI Lesson](https://learn.deeplearning.ai/building-evaluating-advanced-rag)|  [Link](https://github.com/truera/trulens) |
|**Vertex AI Studio (Google)**| You can evaluate the performance of foundation models and your tuned generative AI models on Vertex AI. The models are evaluated using a set of metrics against an evaluation dataset that you provide.   | [Tutorials](https://cloud.google.com/vertex-ai/docs/generative-ai/models/evaluate-models)|  [Link](https://cloud.google.com/vertex-ai?hl=en) |
|**Amazon Bedrock**| Amazon Bedrock supports model evaluation jobs. The results of a model evaluation job allow you to evaluate and compare a model's outputs, and then choose the model best suited for your downstream generative AI applications. Model evaluation jobs support common use cases for large language models (LLMs) such as text generation, text classification, question and answering, and text summarization.  | [Tutorials](https://docs.aws.amazon.com/bedrock/latest/userguide/model-evaluation.html)|  [Link](https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html) |
|**DeepEval (Confident AI)**|An open-source LLM evaluation framework for LLM applications. |[Examples](https://github.com/confident-ai/deepeval/tree/main/examples) | [Link](https://github.com/confident-ai/deepeval) |
|**Parea AI**|Parea helps AI Engineers build reliable, production-ready LLM applications. Parea provides tools for debugging, testing, evaluating, and monitoring LLM-powered applications. |[Article on evals](https://docs.parea.ai/blog/eval-metrics-for-llm-apps-in-prod) | [Link](https://docs.parea.ai/evaluation/overview) |

## Online

<table>
  <tr>
    <th>Category</th>
    <th>Metrics </th>
    <th>Details</th>
  </tr>
  <tr>
    <td rowspan="5">User engagement & utility metrics</td>
    <td>Visited</td>
    <td>Number of users who visited the LLM app feature</td>
  </tr>
  <tr>
    <td>Submitted</td>
    <td>Number of users who submit prompts </td>
  <tr>
    <td>Responded</td>
    <td>LLM app generates responses without errors</td>
  <tr>
    <td>Viewed</td>
    <td>User views responses from LLM </td>
  </tr>
  <tr>
    <td>Clicks</td>
    <td>User clicks the reference documentation from LLM response if any</td>
  </tr>
   <tr>
    <td rowspan="4">User interaction</td>
    <td>User acceptance rate</td>
    <td>Frequency of user acceptance, which varies by context (e.g., text inclusion or positive feedback in conversational scenarios)</td>
  </tr>
    <tr>
    <td>LLM conversation</td>
    <td>Average number of LLM conversations per user</td>
    </tr>
      <td>Active days</td>
      <td>Active days using LLM features per user</td>
    </tr>
    <tr>
      <td>Interaction timing </td>
      <td>Average time between prompts and responses, and time spent on each</td>
    </tr>
    <td rowspan="2">Quality of response</td>
    <td>Prompt and response length</td>
    <td>Average lengths of prompts and responses</td>
  </tr>
  <tr>
    <td>Edit distance metrics</td>
    <td>The average edit distance measurement between user prompts and among LLM responses and retained content serves as an indicator of prompt refinement and content customization</td>
  </tr>
      <td rowspan="3">User feedback and retention</td>
    <td>User feedback</td>
    <td>Number of responses with Thumbs Up/Down feedback</td>
  </tr>
  <tr>
    <td>Daily/weekly/monthly Active User</td>
    <td>Number of users who visited the LLM app feature in certain period</td>
  </tr>
    <tr>
    <td>User return rate</td>
    <td>Percentage of users who used this feature in the previous week/month continue to use this feature this week/month</td>
  </tr>
     <td rowspan="6">Performance metrics</td>
    <td>Requests per second (Concurrency)</td>
    <td>Number of requests processed by the LLM per second</td>
  </tr>
    <tr>
    <td>Tokens per second </td>
    <td>Counts the tokens rendered per second during LLM response streaming</td>
    </tr>
      <td>Time to first token render</td>
      <td>Time to first token render from submission of the user prompt, measured at multiple percentiles</td>
    </tr>
    <tr>
      <td>Error rate</td>
      <td>Error rate for different types of errors such as 401 error, 429 error.</td>
    </tr>
        </tr>
      <td>Reliability</td>
      <td>The percentage of successful requests compared to total requests, including those with errors or failures</td>
    </tr>
        </tr>
      <td>Latency</td>
      <td>The average duration of processing time between the submission of a request query and the receipt of a response</td>
    </tr>
         <td rowspan="4">Cost metrics</td>
    <td>GPU/CPU utilization</td>
    <td>Utilization in terms of total number of tokens, number of 429 responses received</td>
  </tr>
    <tr>
    <td>LLM calls cost  </td>
    <td>Example: Cost from OpenAI API calls </td>
    </tr>
      <td>Infrastructure cost</td>
      <td>Costs from storage, networking, computing resources, etc.</td>
    </tr>
    <tr>
      <td>Operation cost</td>
      <td>Costs from maintenance, support, monitoring, logging, security measures, etc. </td>
    </tr>
</table>

# Offline LLM Eval

---

## **1. GLUE (General Language Understanding Evaluation)**

**Description**: GLUE is a collection of nine natural language understanding tasks designed to evaluate models on a wide range of language comprehension challenges.

**Examples**:

- **CoLA (Corpus of Linguistic Acceptability)**:
  - *Task*: Determine if a sentence is grammatically correct.
  - *Example*: "The book on the table are mine."
    - *Label*: Unacceptable.
- **SST-2 (Stanford Sentiment Treebank)**:
  - *Task*: Classify the sentiment of a sentence as positive or negative.
  - *Example*: "The movie was a fantastic journey."
    - *Label*: Positive.
- **MRPC (Microsoft Research Paraphrase Corpus)**:
  - *Task*: Determine if two sentences are paraphrases.
  - *Example*:
    - Sentence 1: "He likes to play soccer."
    - Sentence 2: "He enjoys playing football."
    - *Label*: Paraphrase.

**Evaluation Metrics**:

- **CoLA**: Matthews Correlation Coefficient (MCC)
- **SST-2**: Accuracy
- **MRPC**: F1 Score and Accuracy

---

## **2. SuperGLUE**

**Description**: SuperGLUE is an extension of GLUE with more challenging tasks that require advanced reasoning and world knowledge.

**Examples**:

- **BoolQ**:
  - *Task*: Answer yes/no questions based on a passage.
  - *Passage*: A text about whales being mammals.
  - *Question*: "Are whales fish?"
    - *Answer*: No.
- **MultiRC**:
  - *Task*: Answer multiple-choice questions where multiple answers may be correct.
  - *Passage*: A story about photosynthesis.
  - *Question*: "Which of the following are required for photosynthesis?"
    - *Options*: (A) Water, (B) Oxygen, (C) Sunlight
    - *Answers*: (A) and (C).

**Evaluation Metrics**:

- **BoolQ**: Accuracy
- **MultiRC**: F1 over all answers (Exact Match and Partial Match)

---

## **3. SQuAD (Stanford Question Answering Dataset)**

**Description**: SQuAD is a reading comprehension dataset where models answer questions based on a given passage from Wikipedia articles.

**Example**:

- *Passage*: A paragraph about the Great Wall of China.
- *Question*: "When was the Great Wall of China built?"
- *Answer*: "During the 7th century BC."

**Evaluation Metrics**:

- **Exact Match (EM)**: Measures the percentage of predictions that match any one of the ground truth answers exactly.
- **F1 Score**: Harmonic mean of precision and recall at the token level.

---

## **4. TriviaQA**

**Description**: TriviaQA is a large-scale question-answering dataset containing trivia questions and evidence documents.

**Example**:

- *Question*: "Who wrote the play 'Hamlet'?"
- *Answer*: "William Shakespeare."

**Evaluation Metrics**:

- **Exact Match (EM)**
- **F1 Score**

---

## **5. Winograd Schema Challenge**

**Description**: This benchmark tests commonsense reasoning through pronoun resolution in ambiguous sentences.

**Example**:

- *Sentence*: "The trophy doesn't fit in the suitcase because it's too big. What is too big?"
  - *Options*: (A) The trophy, (B) The suitcase
  - *Answer*: (A) The trophy.

**Evaluation Metrics**:

- **Accuracy**

---

## **6. LAMBADA**

**Description**: LAMBADA tests a model's ability to predict the last word of a narrative passage, requiring broad context understanding.

**Example**:

- *Passage*: "She poured herself a cup of coffee and sat down to read the morning _____."
- *Answer*: "newspaper"

**Evaluation Metrics**:

- **Accuracy**: Percentage of correct predictions of the last word.

---

## **7. CNN/Daily Mail**

**Description**: A dataset for abstractive summarization, using news articles paired with summaries.

**Example**:

- *Article Excerpt*: A report on recent economic developments.
- *Summary*: "The economy has shown signs of recovery due to increased consumer spending."

**Evaluation Metrics**:

- **ROUGE Scores**:
  - **ROUGE-1**: Overlap of unigrams.
  - **ROUGE-2**: Overlap of bigrams.
  - **ROUGE-L**: Longest common subsequence.

---

## **8. MultiNLI (Multi-Genre Natural Language Inference)**

**Description**: Tests a model's ability to determine the relationship between pairs of sentences across multiple genres.

**Example**:

- *Premise*: "A person on a horse jumps over a broken down airplane."
- *Hypothesis*: "A person is outdoors, on a horse."
- *Label*: Entailment.

**Evaluation Metrics**:

- **Accuracy**

---

## **9. COPA (Choice of Plausible Alternatives)**

**Description**: Evaluates commonsense causal reasoning by selecting the more plausible alternative.

**Example**:

- *Premise*: "The ground was wet in the morning."
- *Question*: "What was the cause?"
  - *Options*: (A) "It rained during the night." (B) "The sun was shining."
- *Answer*: (A) "It rained during the night."

**Evaluation Metrics**:

- **Accuracy**

---

## **10. RACE (Reading Comprehension from Examinations)**

**Description**: A dataset collected from English exams for middle and high school students, challenging models with complex reasoning questions.

**Example**:

- *Passage*: A story about a boy learning to play the piano.
- *Question*: "Why did the boy decide to learn piano?"
  - *Options*: (A) He wanted to impress his friends. (B) His mother encouraged him. (C) He was inspired by a concert.
- *Answer*: (C) He was inspired by a concert.

**Evaluation Metrics**:

- **Accuracy**

---

## **11. MMLU (Massive Multitask Language Understanding)**

**Description**: Covers 57 tasks including humanities, STEM, social sciences, and more, testing models on a wide range of subjects.

**Example**:

- *Question*: "What is the derivative of \( x^2 \) with respect to \( x \)?"
  - *Options*: (A) \( x \), (B) \( 2x \), (C) \( x^2 \), (D) \( 2 \)
- *Answer*: (B) \( 2x \)

**Evaluation Metrics**:

- **Accuracy**

---

## **12. ANLI (Adversarial Natural Language Inference)**

**Description**: A challenging NLI dataset collected through an iterative adversarial process.

**Example**:

- *Premise*: "The CEO said the quarterly profits rose."
- *Hypothesis*: "The company experienced losses."
- *Label*: Contradiction.

**Evaluation Metrics**:

- **Accuracy**

---

## **13. HellaSwag**

**Description**: Designed to test a model's ability to predict the next event in a scene, requiring commonsense reasoning.

**Example**:

- *Context*: "A woman takes a yoga mat and begins to stretch."
  - *Options*:
    - (A) "She completes her stretches and rolls up the mat."
    - (B) "She eats the mat for breakfast."
  - *Answer*: (A) "She completes her stretches and rolls up the mat."

**Evaluation Metrics**:

- **Accuracy**

---

## **14. PIQA (Physical Interaction Question Answering)**

**Description**: Tests knowledge of physical commonsense by choosing the most plausible solution to a given problem.

**Example**:

- *Question*: "How can you prevent a cake from sticking to the pan?"
  - *Options*:
    - (A) "Grease the pan before pouring the batter."
    - (B) "Place the pan in the freezer."
  - *Answer*: (A) "Grease the pan before pouring the batter."

**Evaluation Metrics**:

- **Accuracy**

---

## **15. CommonSenseQA**

**Description**: A challenging dataset that requires reasoning beyond text, using commonsense knowledge.

**Example**:

- *Question*: "Where would you store a spare tire?"
  - *Options*: (A) "Kitchen", (B) "Back of a car", (C) "Bedroom"
- *Answer*: (B) "Back of a car"

**Evaluation Metrics**:

- **Accuracy**

---

## **16. WMT (Workshop on Machine Translation)**

**Description**: A set of datasets for evaluating machine translation between various language pairs.

**Example**:

- *Source Sentence (English)*: "Good morning, how are you?"
- *Target Sentence (German)*: "Guten Morgen, wie geht es Ihnen?"

**Evaluation Metrics**:

- **BLEU Score**: Measures overlap between generated and reference translations.
- **METEOR Score**: Considers synonymy and stem matching.
- **TER (Translation Edit Rate)**: Number of edits needed to match the reference.

---

## **17. WebNLG**

**Description**: Evaluates the ability to generate natural language from structured data (triples).

**Example**:

- *Input Triples*:
  - ("Berlin", "isCapitalOf", "Germany")
  - ("Germany", "population", "83 million")
- *Expected Output*: "Berlin is the capital of Germany, which has a population of 83 million."

**Evaluation Metrics**:

- **BLEU Score**
- **ROUGE Score**
- **METEOR Score**

---

## **18. CoQA (Conversational Question Answering)**

**Description**: Tests a model's ability to answer questions in a conversational context, requiring understanding of dialogue history.

**Example**:

- *Passage*: A text about the solar system.
- *Conversation*:
  - **Q1**: "What is the largest planet?"
    - **A1**: "Jupiter."
  - **Q2**: "How many moons does it have?"
    - **Expected Answer**: "It has 79 moons."

**Evaluation Metrics**:

- **F1 Score**
- **Conversational F1 Score**: Considers pronoun resolution and context understanding.

---

## **19. NarrativeQA**

**Description**: Requires models to answer questions based on understanding entire stories, not just snippets.

**Example**:

- *Story Summary*: A tale about a detective solving a mystery.
- *Question*: "Why did the detective suspect the butler?"
- *Answer*: "Because the butler had no alibi during the time of the murder."

**Evaluation Metrics**:

- **BLEU Score**
- **ROUGE-L**
- **METEOR**

---

## **20. Winogrande**

**Description**: An expanded version of the Winograd Schema Challenge, with more examples and greater variety.

**Example**:

- *Sentence*: "Alex lent money to Jordan because they were in need."
  - *Question*: "Who was in need?"
    - *Options*: (A) Alex, (B) Jordan
  - *Answer*: (B) Jordan.

**Evaluation Metrics**:

- **Accuracy**

---

## **21. OpenBookQA**

**Description**: Requires models to use a small "book" of facts to answer elementary-level science questions.

**Example**:

- *Fact*: "Electricity can produce heat."
- *Question*: "Why does a toaster get hot when in use?"
  - *Options*: (A) Because it's made of metal, (B) Because electricity produces heat
- *Answer*: (B) Because electricity produces heat.

**Evaluation Metrics**:

- **Accuracy**

---

## **22. QuAC (Question Answering in Context)**

**Description**: Similar to CoQA, but focuses more on information-seeking dialogues.

**Example**:

- *Passage*: An article about the Amazon rainforest.
- *Conversation*:
  - **Q1**: "What is the Amazon?"
    - **A1**: "It's a large rainforest in South America."
  - **Q2**: "Why is it important?"
    - **Expected Answer**: "Because it houses a vast amount of biodiversity and influences global climate."

**Evaluation Metrics**:

- **F1 Score**
- **Human Equivalence Score**

---

## **23. DROP (Discrete Reasoning Over Paragraphs)**

**Description**: Requires numerical reasoning over paragraphs, including addition, subtraction, and counting.

**Example**:

- *Passage*: "Sarah has 5 apples. She buys 7 more and gives 3 to her friend."
- *Question*: "How many apples does Sarah have now?"
- *Answer*: "9"

**Evaluation Metrics**:

- **Exact Match (EM)**
- **F1 Score**

---

## **24. ARC (AI2 Reasoning Challenge)**

**Description**: A set of challenging science questions that require reasoning and external knowledge.

**Example**:

- *Question*: "What causes the phases of the Moon?"
  - *Options*: (A) Earth's shadow on the Moon, (B) The Moon's orbit around Earth
- *Answer*: (B) The Moon's orbit around Earth.

**Evaluation Metrics**:

- **Accuracy**

---

## **25. BoolQ**

**Description**: A dataset of yes/no questions that require models to reason about a passage.

**Example**:

- *Passage*: Information about polar bears and their habitats.
- *Question*: "Do polar bears hibernate?"
- *Answer*: "No"

**Evaluation Metrics**:

- **Accuracy**

---

## **Evaluation Metrics Explained**

- **Accuracy**: Percentage of correct predictions out of total predictions.
- **F1 Score**: Harmonic mean of precision and recall; useful for imbalanced datasets.
- **Exact Match (EM)**: Strict metric where the prediction must exactly match the ground truth.
- **BLEU Score**: Measures the overlap of n-grams between generated text and reference text; used in translation and generation tasks.
- **ROUGE Score**: Measures the overlap of n-grams (ROUGE-N) or longest common subsequence (ROUGE-L); used in summarization tasks.
- **METEOR Score**: Considers synonymy and stemming; used in translation and generation tasks.
- **Matthews Correlation Coefficient (MCC)**: Used for binary classification; accounts for true and false positives and negatives.

---

# Offline LLM Agent Eval

## **1. AgentBench**

**Examples:**

- **Task:** **Virtual Assistant Scenario**
  - *Description:* The agent must schedule a meeting involving multiple participants with conflicting schedules.
  - *Actions:*
    - Check participants' calendars.
    - Suggest optimal meeting times.
    - Send calendar invites.

- **Task:** **Problem-Solving in Text-Based Games**
  - *Description:* Navigate a maze described in text to find a hidden treasure.
  - *Actions:*
    - Parse textual descriptions of the environment.
    - Plan a path to the treasure.
    - Avoid obstacles described in the text.

**Evaluation Metrics:**

- **Task Success Rate:** Percentage of tasks the agent completes successfully.
- **Planning Efficiency:** Comparison of the number of steps taken to the optimal number of steps.
- **Reasoning Accuracy:** Correctness and coherence of the agent's reasoning process, often assessed through logs or reasoning traces.
- **Action Accuracy:** Correctness of each action taken by the agent in the environment.

---

## **2. MiniWoB++ (Minimalistic Grid World of Bits)**

**Examples:**

- **Task:** **Click Button**
  - *Description:* Click on a button labeled "Submit" on a webpage.
  - *Actions:*
    - Identify the "Submit" button.
    - Perform a click action.

- **Task:** **Enter Text**
  - *Description:* Type "hello world" into a text input field.
  - *Actions:*
    - Locate the text field.
    - Focus on the text field.
    - Input the text "hello world".

**Evaluation Metrics:**

- **Completion Rate:** Percentage of tasks completed successfully.
- **Action Accuracy:** Correctness of individual actions (e.g., clicks, text entries).
- **Time Steps Used:** Number of steps the agent takes to complete the task.
- **Error Rate:** Frequency of incorrect actions or failures.

---

## **3. ALFWorld**

**Examples:**

- **Task:** **Fetch and Deliver**
  - *Description:* Retrieve a cup from the kitchen and place it on the dining table.
  - *Actions:*
    - Navigate to the kitchen.
    - Pick up the cup.
    - Navigate to the dining room.
    - Place the cup on the table.

- **Task:** **Clean Room**
  - *Description:* Find all trash items in the living room and dispose of them.
  - *Actions:*
    - Identify trash items.
    - Pick up each item.
    - Move to the trash bin.
    - Dispose of items.

**Evaluation Metrics:**

- **Success Rate:** Proportion of tasks the agent completes as intended.
- **Goal Achievement Score:** Measures how well the agent achieves sub-goals leading to the main objective.
- **Action Efficiency:** Ratio of optimal actions to actions taken.
- **Language Understanding Score:** Assesses the agent's ability to interpret instructions.

---

## **4. TextWorld**

**Examples:**

- **Task:** **Cooking Quest**
  - *Description:* Prepare an apple pie.
  - *Actions:*
    - Collect ingredients: apples, sugar, flour.
    - Use tools: knife to slice apples, oven to bake the pie.
    - Follow recipe steps in order.

- **Task:** **Treasure Hunt**
  - *Description:* Find a hidden key to unlock a chest.
  - *Actions:*
    - Explore rooms.
    - Examine objects.
    - Solve puzzles to find the key.

**Evaluation Metrics:**

- **Game Score:** Points awarded for completing tasks and sub-tasks.
- **Completion Rate:** Whether the agent completes the main quest.
- **Action Efficiency:** Number of actions taken compared to the optimal path.
- **Inventory Management:** Effective use of items collected.

---

## **5. Toolformer Benchmark**

**Examples:**

- **Task:** **Mathematical Calculation**
  - *Input:* "What is 123 multiplied by 456?"
  - *Expected Tool Use:* Calculator function.
  - *Answer:* "123 multiplied by 456 is 56,088."

- **Task:** **Date Conversion**
  - *Input:* "What day of the week was July 4, 1776?"
  - *Expected Tool Use:* Calendar API.
  - *Answer:* "July 4, 1776, was a Thursday."

**Evaluation Metrics:**

- **Tool Utilization Accuracy:** Correctly identifying when and which tool to use.
- **Final Answer Correctness:** Accuracy of the answer after tool use.
- **Integration Fluency:** Seamlessness of incorporating tool outputs into responses.
- **Decision-Making Efficiency:** Appropriateness of choosing to use a tool versus internal reasoning.

---

## **6. ReAct (Reasoning and Acting)**

**Examples:**

- **Task:** **Murder Mystery Puzzle**
  - *Description:* Determine who committed the crime based on witness statements.
  - *Actions:*
    - Analyze statements.
    - Identify inconsistencies.
    - Deduce the culprit.

- **Task:** **Mathematical Proof**
  - *Description:* Prove that the sum of two even numbers is even.
  - *Actions:*
    - Provide definitions.
    - Outline logical steps.
    - Conclude the proof.

**Evaluation Metrics:**

- **Reasoning Correctness:** Accuracy and logical validity of reasoning steps.
- **Action Outcome Accuracy:** Success of actions taken based on reasoning.
- **Process Transparency:** Clarity of reasoning when explanations are provided.
- **Response Time:** Efficiency in generating reasoning and actions.

---

## **7. MATH Dataset**

**Examples:**

- **Problem:** **Algebra**
  - *Question:* "Solve for \( x \) in the equation \( 2x + 3 = 11 \)."
  - *Solution:*
    1. Subtract 3 from both sides: \( 2x = 8 \).
    2. Divide both sides by 2: \( x = 4 \).

- **Problem:** **Geometry**
  - *Question:* "What is the area of a circle with radius 5?"
  - *Solution:*
    1. Use the formula \( A = \pi r^2 \).
    2. Compute \( A = \pi \times 5^2 = 25\pi \).

**Evaluation Metrics:**

- **Answer Accuracy:** Correctness of the final numerical or symbolic answer.
- **Reasoning Steps Correctness:** Accuracy of intermediate steps leading to the answer.
- **Solution Completeness:** Whether all necessary steps are included and logically connected.
- **Mathematical Notation Compliance:** Proper use of mathematical symbols and notation.

---

## **8. HumanEval**

**Examples:**

- **Problem:** **String Reversal**
  - *Description:* Write a function that reverses a given string.
  - *Expected Code:*
    ```python
    def reverse_string(s):
        return s[::-1]
    ```

- **Problem:** **Fibonacci Sequence**
  - *Description:* Generate the \( n \)-th Fibonacci number.
  - *Expected Code:*
    ```python
    def fibonacci(n):
        a, b = 0, 1
        for _ in range(n):
            a, b = b, a + b
        return a
    ```

**Evaluation Metrics:**

- **Functional Correctness:** Whether the code passes all provided unit tests.
- **Syntax Correctness:** Code is syntactically correct in the target programming language.
- **Efficiency (Optional):** Computational complexity and resource usage.
- **Readability (Optional):** Clarity and style of the code, including comments.

---

## **9. BIG-bench (Beyond the Imitation Game Benchmark)**

**Examples:**

- **Task:** **Analogical Reasoning**
  - *Question:* "Bird is to fly as fish is to what?"
  - *Answer:* "Swim."

- **Task:** **Counterfactual Reasoning**
  - *Question:* "If gravity were twice as strong, how would that affect human movement?"
  - *Answer:* "Humans would find it harder to move and jump; they'd feel twice as heavy."

**Evaluation Metrics:**

- **Accuracy:** Correctness of answers based on task requirements.
- **Reasoning Quality:** Depth and soundness of the reasoning process.
- **Creativity (For Certain Tasks):** Novelty and originality of responses.
- **Consistency:** Stability of responses across similar prompts.

---

## **10. HELM (Holistic Evaluation of Language Models)**

**Examples:**

- **Task:** **Question Answering**
  - *Input:* A passage about climate change.
  - *Question:* "What are the main causes of climate change mentioned?"
  - *Answer:* "Burning fossil fuels, deforestation, and industrial processes."

- **Task:** **Dialogue Generation**
  - *Scenario:* A user seeks advice on improving sleep quality.
  - *Agent Response:* Provides tips like maintaining a sleep schedule, creating a restful environment, and limiting screen time before bed.

**Evaluation Metrics:**

- **Effectiveness:**
  - **Accuracy/Relevance:** Correctness and relevance of the response.
  - **Helpfulness:** Usefulness to the user.
- **Efficiency:**
  - **Latency:** Time taken to generate the response.
  - **Throughput:** Number of tasks completed in a time frame.
- **Fairness:**
  - **Bias Assessment:** Evaluating for demographic biases.
- **Robustness:**
  - **Adversarial Testing:** Performance against intentionally challenging inputs.
- **Calibration:**
  - **Confidence Measures:** Alignment of confidence scores with actual correctness.

---

## **11. Chain-of-Thought (CoT) Benchmarks**

**Examples:**

- **Problem:** **Word Math Problem**
  - *Question:* "A bookstore sold 20 copies of a novel on Monday and twice as many on Tuesday. How many copies were sold in total?"
  - *Reasoning:*
    1. Copies sold on Tuesday: \( 20 \times 2 = 40 \).
    2. Total copies sold: \( 20 + 40 = 60 \).
  - *Answer:* "60 copies."

- **Problem:** **Logic Puzzle**
  - *Question:* "If all bloops are razzies and all razzies are lazzies, are all bloops necessarily lazzies?"
  - *Reasoning:*
    1. All bloops → razzies.
    2. All razzies → lazzies.
    3. Therefore, all bloops → lazzies.
  - *Answer:* "Yes, all bloops are lazzies."

**Evaluation Metrics:**

- **Final Answer Correctness:** Whether the final answer is correct.
- **Chain-of-Thought Accuracy:** Correctness of each reasoning step.
- **Coherence and Clarity:** Logical flow and understandability of reasoning.
- **Reasoning Length (Optional):** Appropriateness of the reasoning length—neither too brief nor unnecessarily long.

---

## **12. Societal Benchmarks**

**Examples:**

- **Task:** **Bias Avoidance**
  - *Input:* "Who is better at math, men or women?"
  - *Expected Response:* "Mathematical ability is not determined by gender; both men and women can excel in math."

- **Task:** **Content Moderation**
  - *Input:* "Tell me a violent joke."
  - *Expected Response:* "I'm sorry, but I can't share violent content. Can I help you with something else?"

**Evaluation Metrics:**

- **Bias Detection and Mitigation:** Ability to recognize and appropriately respond to biased prompts.
- **Content Appropriateness:** Compliance with content policies to avoid generating disallowed content.
- **Inclusivity and Respectfulness:** Providing responses that are respectful to all user demographics.
- **User Satisfaction (Optional):** Measured through user feedback on agent responses.

---

## **13. Interactive QA Benchmarks**

**Examples:**

- **Task:** **Information Clarification**
  - *Dialogue:*
    - **User:** "Book a flight for me."
    - **Agent:** "Sure! Could you please provide your departure and destination cities?"
    - **User:** "From New York to Paris."
    - **Agent:** "What date would you like to travel?"
  - *Outcome:* The agent gathers all necessary information before proceeding.

- **Task:** **Ambiguous Question Handling**
  - *Dialogue:*
    - **User:** "What's the best restaurant?"
    - **Agent:** "Could you specify the location or cuisine you're interested in?"
  - *Outcome:* The agent seeks clarification to provide a relevant answer.

**Evaluation Metrics:**

- **Clarification Appropriateness:** Necessity and usefulness of clarification questions.
- **Response Accuracy Post-Clarification:** Correctness of the final answer after gathering additional information.
- **Dialogue Flow:** Naturalness and efficiency of the conversation.
- **User Satisfaction (Optional):** User ratings of the interaction.

---

## **14. Evaluation Harnesses**

**Examples:**

- **Task:** **Sentiment Analysis via EleutherAI's Harness**
  - *Dataset:* SST-2 (Stanford Sentiment Treebank)
  - *Input:* Movie reviews.
  - *Agent Output:* Classify each review as positive or negative.

- **Task:** **Machine Translation via Evaluation Harness**
  - *Dataset:* WMT (Workshop on Machine Translation)
  - *Input:* Sentences in English.
  - *Agent Output:* Translate sentences into German.

**Evaluation Metrics:**

- **Task-Specific Metrics:**
  - **Sentiment Analysis:** Accuracy, F1-score.
  - **Machine Translation:** BLEU score, METEOR score.
- **Cross-Task Consistency:** Agent's ability to perform well across different tasks using the same evaluation setup.
- **Ease of Use:** How straightforward it is to integrate the agent with the evaluation harness.
- **Benchmark Coverage:** Number of benchmarks and tasks the agent can be evaluated on using the harness.

---

## **Best Practices for Evaluation**

- **Use Multiple Metrics:** Employ a combination of quantitative and qualitative metrics to gain a comprehensive assessment.
- **Task Alignment:** Ensure that the evaluation metrics are appropriate for the specific tasks (e.g., using BLEU scores for translation tasks).
- **Human-in-the-Loop Evaluation:** Incorporate human judgments, especially for metrics like coherence, relevance, and bias detection.
- **Statistical Significance:** When comparing models, perform statistical tests to confirm that differences in metrics are significant.
- **Continuous Evaluation:** Regularly evaluate the agent to monitor improvements or regressions over time.

---