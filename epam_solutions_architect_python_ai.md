# Interview Review: Python, AI, and Search Engineering

**Candidate:** Tarun Nagpal\
**Interview date:** 16 October 2026\
**Purpose:** Interview debrief, question bank, feedback, and preparation
notes\
**Source:** Interview transcript shared in this conversation. Some
questions below are lightly normalized for readability; they preserve
the topics and intent of the interview rather than claiming verbatim
transcription.

------------------------------------------------------------------------

## 1. Overall feedback

### Summary

The interview showed solid experience in system architecture, end-to-end
project ownership, and explaining a real search application. The main
concerns were hands-on Python depth, coding/problem-solving execution
under interview conditions, and the ability to explain how an LLM-based
system is evaluated and protected against incorrect results.

### Strengths

-   **Architecture and ownership:** You described an end-to-end
    expertise-search platform, its services and layers, and your role in
    designing it.
-   **System context:** You could explain the major components:
    Python/FastAPI, React, OpenSearch, AWS, Docker/Kubernetes,
    monitoring, and an NLP/transformer component.
-   **Delivery leadership:** You described working with a Product Owner,
    quarterly OKRs, a roadmap, epics/stories, and sprint-based work
    allocation.
-   **Search relevance awareness:** You described a business-specific
    reranking approach using engagement, endorsements, and experience.

### Areas to improve

-   **Python fundamentals:** Your answers showed limited direct
    experience with Python generators and decorators, and you did not
    confidently cover dictionaries, sets, and other core data
    structures.
-   **Coding and problem clarification:** In the book-distribution
    problem, you initially misunderstood the goal and wrote a solution
    that did not produce the expected minimum movement. The key
    improvement is to restate the problem, confirm examples, derive the
    invariant, and test edge cases before coding.
-   **React performance concepts:** You correctly brought up
    memoization, but confused memoized values with browser local
    storage. React memoization normally retains values in memory as part
    of rendering; it is not the same as `localStorage`.
-   **LLM/NLP architecture reasoning:** You had difficulty clearly
    distinguishing traditional search, NLP/entity extraction,
    embeddings/vector retrieval, and generative LLM use cases. Be
    precise about which model or technique does which job.
-   **Evaluation and hallucinations:** This was the most important gap.
    Reranking retrieved records does not prove that the original
    retrieval or the LLM-extracted query terms are correct. A model
    being pretrained or fine-tuned, and a successful proof of concept,
    do not guarantee that outputs are always accurate.
-   **Guardrails:** You described filtering disallowed terms and
    code-quality/security checks. Those are useful, but distinguish
    content/security controls from answer-grounding and
    retrieval-quality controls.

### Hiring outlook (assessment, not a fact)

Based on this interview alone, the assessment was **uncertain, leaning
slightly negative for a highly hands-on Python/AI engineering role**. An
AI solution-architect or technical-lead role may be a better fit when it
emphasizes architecture and delivery, but the Python and AI-evaluation
gaps still need to be addressed. This is not a prediction of the
employer's actual decision.

------------------------------------------------------------------------

## 2. Interview questions

The following is a consolidated preparation list of 67 questions and
question prompts grouped by topic. Some are direct questions from the
transcript; others separate a multi-part interviewer prompt into the
individual skills it tested.

### A. Introduction, projects, architecture, and delivery (1--15)

1.  Are you currently working, and which organization are you working
    for?
2.  How long have you been working at your current organization?
3.  Why is your current designation "Senior Software Engineer" if you
    previously worked as an architect?
4.  Briefly describe the work you are currently doing.
5.  What is the expertise-search application, and who uses it?
6.  Which technologies are used in the expertise-search platform?
7.  Which cloud platform does the application use?
8.  What other technologies are used besides Python and the search
    engine?
9.  What was your role in the project?
10. Can you explain the high-level architecture you designed?
11. What are the different layers or microservices in the application?
12. What is the current stage of the project, and what happens now that
    it is being outsourced?
13. Are you working on any other project, such as an AI operating
    system?
14. What is your role in that second project?
15. How many developers were on the team, and how was work assigned
    across the team?

### B. Python coding and problem-solving (16--26)

16. Given `N` rows with different numbers of books, how would you make
    every row contain the same number?
17. What is the minimum number of books that must be moved to make all
    row counts equal?
18. Can you explain the expected output for a sample input?
19. How do you determine the target number of books per row?
20. How would you calculate the minimum number of moves once the target
    is known?
21. Can you write and run a Python program for this problem?
22. Does your program produce the expected output for the sample?
23. Can you explain how your program produced its current output?
24. How would you debug the result when it differs from the expected
    answer?
25. Which assumptions or edge cases should be checked before finalizing
    the solution?
26. Do you write code day to day?

### C. Python fundamentals and FastAPI (27--33)

27. Have you worked with Python generators?
28. What is a generator, and how does it differ from returning a
    complete list?
29. Have you used Python decorators?
30. What are decorators used for in Python?
31. Which Python data structures have you worked with?
32. When would you use a list, tuple, set, or dictionary?
33. How do you validate incoming request data in FastAPI?

### D. React and JavaScript (34--38)

34. How comfortable are you with React?
35. How would you identify and prevent unnecessary component rerenders?
36. What is memoization, and when would you use `useMemo` or
    `React.memo`?
37. Where is memoized data stored, and does it consume memory?
38. How is memoization different from browser `localStorage`, and what
    limits apply to browser storage?

### E. AI, NLP, LLMs, and search architecture (39--52)

39. Have you worked on AI or LLM-based applications?
40. Can you explain the NLP/transformer component used in your search
    application?
41. What happens when a user submits a natural-language search query?
42. Why do you need an LLM or NLP model in this use case?
43. Could traditional search technology such as Elasticsearch/OpenSearch
    or Apache Solr solve part of this problem without an LLM?
44. How would you remove irrelevant words from a query while preserving
    its meaning?
45. What business rules or context do you provide to the model for query
    cleansing or extraction?
46. Does the system use embeddings or a vector database, and where do
    those fit into the pipeline?
47. Can you walk through the complete request flow from the React search
    box to the final results?
48. What kind of query chunks or extracted entities does the model
    return?
49. Are the extracted chunks always meaningful, and what rules define a
    valid chunk?
50. What is the final output returned by the application?
51. How does your custom reranking algorithm work?
52. What was your individual contribution to the search use case?

### F. LLM evaluation, accuracy, and hallucinations (53--62)

53. How do you evaluate the responses returned by an LLM?
54. How do you measure LLM accuracy?
55. If the system returns ten records, how do you know that those ten
    records are the right ones?
56. Does reranking prove that the retrieved records are correct?
57. What happens if the model extracts the wrong search terms or returns
    irrelevant records?
58. How would you detect and measure hallucinations?
59. Does fine-tuning or training on a large dataset guarantee accurate
    responses?
60. What was the purpose of fine-tuning the NLP model on domain-specific
    terminology?
61. How would you improve results if the current system has no explicit
    accuracy-evaluation process?
62. If there are no expected answers or labelled examples, how would you
    establish a trustworthy evaluation baseline?

### G. Guardrails, code quality, and engineering practices (63--66)

63. What guardrails exist in the application before results are shown to
    users?
64. How do you prevent disallowed or sensitive terms from appearing in
    search or responses?
65. What tools or checks do you use to enforce code quality and prevent
    secrets or inappropriate data from being committed?
66. At what stages do the pre-commit hooks, code-quality checks, and
    secret-scanning controls run?

### H. Closing (67)

67. What questions do you have for the interviewer about the role, team,
    or organization?

------------------------------------------------------------------------

## 3. The most important correction: measuring LLM accuracy

### What went wrong in the interview

When asked how accuracy was measured, the answer focused on the custom
reranker. The interviewer correctly challenged that point: reranking can
reorder the records that have already been retrieved, but it cannot
guarantee that the original query interpretation or retrieved candidate
set is correct.

A model's training data, fine-tuning, or a successful proof of concept
also does not establish that every production answer is correct.
Accuracy needs to be measured against a representative evaluation
dataset and monitored over time.

### Interview-ready answer (about 60 seconds)

> I measure an LLM-powered search system at three levels: retrieval
> quality, answer quality, and safety.
>
> First, for retrieval, I create a labelled test set of representative
> user queries and the employee records that should be returned. I use
> metrics such as Precision@K, Recall@K, and ranking metrics like MRR or
> NDCG to check whether relevant records are retrieved and ranked near
> the top.
>
> Second, I evaluate the model's query extraction and final answer
> against expected outputs verified by domain experts. I check whether
> extracted skills, locations, experience, and other constraints are
> correct, and whether the final response is supported by the retrieved
> data.
>
> Third, I test failure cases such as unsupported claims, missing
> results, irrelevant results, and hallucinations. I combine automated
> evaluation with human review, compare changes against a baseline, and
> run regression tests whenever prompts, models, or retrieval logic
> change. In production, I monitor feedback and failures and add
> representative cases to the evaluation set.

### Metrics to know

  -----------------------------------------------------------------------
  Area                    Example metric or check What it tells you
  ----------------------- ----------------------- -----------------------
  Retrieval               Precision@K             What proportion of the
                                                  top K results are
                                                  relevant?

  Retrieval               Recall@K                What proportion of all
                                                  relevant results appear
                                                  in the top K?

  Ranking                 MRR / NDCG              Are the most relevant
                                                  results near the top,
                                                  with appropriate
                                                  ranking?

  Extraction              Field-level precision,  Did the model extract
                          recall, and exact match the correct skills,
                                                  locations, and
                                                  constraints?

  Generated answer        Correctness against a   Does the response match
                          verified reference      the expected answer?

  Grounding               Faithfulness / support  Are claims supported by
                          by retrieved context    the retrieved records
                                                  or documents?

  Safety                  Hallucination and       How often does the
                          policy-violation rate   system produce
                                                  unsupported or
                                                  disallowed content?

  Operations              Latency, failure rate,  Is the system reliable
                          and user feedback       and useful in
                                                  production?
  -----------------------------------------------------------------------

**Important:** Do not claim that your existing project implemented these
metrics unless it actually did. If it did not, say: "We had a
business-specific reranking algorithm, but we did not have a
sufficiently formal, labelled evaluation framework. I would introduce
one using representative queries, expected records, retrieval metrics,
and human review."

### Example for the expertise-search application

User query: "Find an Indian consultant who knows React and has recent
experience in healthcare."

1.  **Expected output:** Build a reviewed test case identifying which
    employee records match the criteria and why.
2.  **Query extraction:** Check whether the model correctly identifies
    location/nationality, React, healthcare, and recent experience.
3.  **Retrieval:** Check whether OpenSearch returns the expected
    employee records, using Precision@K and Recall@K.
4.  **Reranking:** Check whether the most relevant records are placed
    near the top.
5.  **Final response:** Verify that skills and experience claims are
    supported by indexed employee data and that the system does not
    invent qualifications.
6.  **Regression:** Repeat the test after changing the model, prompts,
    index, or ranking algorithm.

### If the interviewer asks, "What if you have no expected answers?"

> I would first create a representative evaluation set from real queries
> and ask domain experts to label the relevant records or expected
> fields. If labels are limited, I would start with human-reviewed
> samples to establish a baseline, then use automated or LLM-based
> evaluators to scale evaluation. I would validate those evaluators
> against human judgements and continuously add production failures to
> the test set.

------------------------------------------------------------------------

## 4. Technical corrections to prepare

### Python coding: equalizing row counts

For counts such as `[5, 1, 9]`, the total is `15`; with three rows, the
target is `5` each. The second row needs four books and the third row
has four surplus books, so four books must be moved. For a general
input, first check whether the total is divisible by the number of rows.
If it is not divisible, equal integer counts are impossible without
changing the total.

A clear interview approach:

1.  Restate the problem in your own words.
2.  Work through one example and confirm the expected output.
3.  Calculate `target = sum(counts) / len(counts)` after checking
    divisibility.
4.  Sum the positive surpluses above the target; that is the minimum
    number of individual books that must be moved.
5.  Test already-equal counts, one row, uneven totals, and zero counts.

### Python data structures

-   **List:** ordered, mutable collection; allows duplicates.
-   **Tuple:** ordered, immutable collection.
-   **Set:** unique elements; useful for membership and deduplication.
-   **Dictionary:** key-value mapping; efficient lookups by key.
-   **Generator:** yields values lazily, often saving memory for large
    sequences.
-   **Decorator:** wraps or modifies a function or method's behavior,
    commonly for logging, authorization, timing, or reusable
    cross-cutting concerns.
-   **FastAPI validation:** use type annotations and Pydantic models for
    request-body and field validation; add explicit validators and
    business-rule checks where needed.

### React memoization

-   `React.memo` can skip rerendering a component when its props have
    not changed under its comparison rules.
-   `useMemo` caches a computed value between renders while its
    dependencies remain unchanged.
-   `useCallback` caches a function reference between renders while its
    dependencies remain unchanged.
-   Memoization is not `localStorage`; it is an in-memory optimization
    associated with React rendering. Use it when measurement shows it
    helps, not by default everywhere.

### Search and LLM design

Be able to separate these stages clearly:

1.  **Query understanding / extraction:** identify intent, entities,
    skills, locations, and constraints. This may use rules, NER,
    classifiers, an LLM, or a combination.
2.  **Retrieval:** search indexed data using lexical search, filters,
    vectors, or hybrid retrieval.
3.  **Ranking/reranking:** order retrieved candidates by relevance and
    business signals.
4.  **Answer generation:** if a natural-language answer is needed,
    generate it using retrieved evidence and verify grounding.
5.  **Evaluation:** measure extraction, retrieval, ranking, and
    generation separately; end-to-end quality cannot be inferred from
    the reranker alone.

Use an LLM only where its contextual understanding or generation adds
value. Some extraction tasks can be handled more cheaply and predictably
with rules, dictionaries, NER, or classifiers. The right design depends
on ambiguity, domain complexity, quality requirements, latency, and
cost.

### Guardrails

Distinguish these categories rather than presenting them as
interchangeable:

-   **Input and content controls:** validation, disallowed-term
    filtering, prompt-injection handling where relevant.
-   **Retrieval controls:** access permissions, source filtering, and
    retrieval of authorized records.
-   **Grounding and output checks:** validate generated claims against
    retrieved evidence; refuse or qualify answers when evidence is
    insufficient.
-   **Security and engineering controls:** secret scanning, static
    analysis, dependency checks, tests, code review, and pre-commit/CI
    checks.
-   **Monitoring:** logging, auditability, feedback, incident review,
    and regression tests.

------------------------------------------------------------------------

## 5. A better way to handle coding questions

Use this repeatable sequence:

1.  **Clarify:** "Let me confirm the expected input and output."
2.  **Work an example:** calculate the answer manually before coding.
3.  **State the invariant:** explain the property the algorithm relies
    on.
4.  **Choose the simplest algorithm:** avoid sorting or complex logic
    unless necessary.
5.  **Code in small steps:** use descriptive names and avoid editing
    multiple things at once.
6.  **Test:** run the sample, an edge case, and a normal case.
7.  **Explain complexity:** state time and space complexity when
    relevant.

For the book problem, a useful clarification is: "Are we counting
individual books moved, and can any book be moved directly from a
surplus row to a deficit row?" Confirming this avoids solving a
different problem.

------------------------------------------------------------------------

## 6. Suggested preparation priorities

### Priority 1 --- Python fundamentals and coding

Practise lists, dictionaries, sets, tuples, comprehensions, generators,
decorators, exceptions, typing, and common coding problems. Focus on
explaining the approach before coding and validating outputs.

### Priority 2 --- Search relevance and RAG evaluation

Understand Precision@K, Recall@K, MRR, NDCG, labelled evaluation
datasets, human evaluation, faithfulness, answer correctness,
hallucination tests, and regression evaluation.

### Priority 3 --- Explain the search architecture precisely

Prepare a two-minute architecture explanation covering
ingestion/indexing, query understanding, retrieval, reranking, API
orchestration, final response, observability, and failure handling.
Clearly state what is deterministic and what relies on a model.

### Priority 4 --- React performance basics

Review rerenders, props/state, `React.memo`, `useMemo`, `useCallback`,
dependency arrays, and the difference between in-memory memoization and
browser storage.

### Priority 5 --- Guardrails and production readiness

Prepare concrete examples of access control, evidence grounding,
unsafe-output handling, observability, model/version changes, regression
tests, and evaluation datasets.

------------------------------------------------------------------------

## 7. Honest positioning for future interviews

A strong way to present the experience is to emphasize the architecture
and search pipeline you designed, then be transparent about evaluation
maturity:

> I designed the end-to-end expertise-search architecture and
> implemented business-specific reranking using engagement,
> endorsements, and experience signals. One lesson from the project is
> that reranking is not the same as measuring LLM accuracy. For a more
> mature evaluation approach, I would maintain a labelled set of
> representative queries and expected records, measure extraction and
> retrieval separately, track ranking metrics such as Precision@K,
> Recall@K, and NDCG, and use human review to validate answer
> correctness and grounding. I would also run regression tests after
> changes to models, prompts, indexing, or ranking.

This demonstrates learning and sound engineering judgement without
claiming that an evaluation framework was already implemented when it
was not.

------------------------------------------------------------------------

## 8. Final checklist before the next interview

-   [ ] Explain one project architecture clearly in two minutes.
-   [ ] Solve a simple Python problem without coding before confirming
    the example.
-   [ ] Explain generators, decorators, lists, tuples, sets, and
    dictionaries.
-   [ ] Explain FastAPI request validation using Pydantic.
-   [ ] Explain `React.memo`, `useMemo`, and `useCallback` accurately.
-   [ ] Distinguish NER/query extraction, lexical search, vector search,
    reranking, and generation.
-   [ ] Explain how to evaluate retrieval and generated answers
    separately.
-   [ ] Explain why fine-tuning does not guarantee factual correctness.
-   [ ] Describe guardrails for permissions, grounding, content
    filtering, and production monitoring.
-   [ ] Be clear about what the project actually implemented versus what
    you would improve.

------------------------------------------------------------------------

*This document is intended as a personal interview-preparation record.
The question list is normalized from the transcript and consolidated
into 67 prompts; use the original recording/transcript if exact verbatim
wording is important.*
