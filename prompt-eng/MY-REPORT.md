![GenI-Banner](https://github.com/genilab-fau/genial-fau.github.io/blob/8f1a2d3523f879e1082918c7bba19553cb6e7212/images/geni-lab-banner.png?raw=true)

# {Exploring Prompting Techniques for Automating Requirement Analysis in Study Companion Bots}

A study on how different prompting techniques impact automated requirement analysis for AI-driven study companion bots.

<!-- WHEN APPLICABLE, REMOVE THE COMMENT MARK AND COMPLETE
This is a response to the Assignment part of the COURSE.
-->

* Authors: [Misbah Khan](misbahkhan2024@fau.edu)
* Academic Supervisor: [Dr. Fernando Koch](http://www.fernandokoch.me)

  
# Research Question 

How can different prompting techniques enhance the automation of requirement analysis for study companion bots?

## Arguments

#### What is already known about this topic

* AI-powered requirement analysis can be automated using GenAI.
* Traditional requirement gathering is manual, time-consuming, and often inconsistent.
* Prompting techniques such as Zero-Shot, Few-Shot, Chain of Thought, Meta, and Self-Consistency influence AI performance in requirement extraction.
* The possibility of optimizing requirement analysis with structured and self-evaluative AI-generated solutions.

#### What this research is exploring

* Self-Consistency prompting is used to compare multiple solution paths and select the most effective one.
* The performance of five prompting techniques is analyzed and compared to determine their impact on AI-driven requirement analysis.
* Exploration of how automation can enhance adaptability, scalability, and efficiency in requirement gathering for educational AI chatbots.

#### Implications for practice

* It will be easier to automate requirement elicitation without extensive human intervention.
* It will optimize the process of requirement validation by comparing multiple solution paths.
* We will better understand how AI reasoning improves requirement accuracy and adaptability.

# Research Method

Five prompting techniques are experimented with (Zero-Shot, Few-Shot, Chain of Thought, Meta, and Self-Consistency) by applying them to the automation of requirement analysis for a Study Companion Bot. Each method was evaluated based on:

- Depth of analysis
- Accuracy of extracted requirements
- Scalability and adaptability
- Feasibility of implementation
- Time taken for execution

The study included AI-generated solutions from each technique, followed by an analysis of their effectiveness in streamlining requirement automation.

Function parameters were changed in order to improve the quality of the model responses. 
 - The context size (num_ctx) was changed to 8192, which was initially limited to 100. This allows the model to understand the context of the prompt better, due to a larger context window size. 
 - The number of tokens the model is allowed to generate (num_predict) was changed to 8192, which was initially limited to 100 by default. This allows the model to generate a detailed answer, as is required by this use case.
 - Temperature was set to 0 to reduce the randomness or creativity in the responses. A preference of stability and consistency in response was considered more preferable for usecase.
      
# Results

### Comparison of Techniques

| **Technique**          | **Depth of Analysis** | **Accuracy** | **Scalability** | **Implementation Feasibility** | **Time Taken** |
|----------------------|-------------------|------------|---------------|--------------------------|------------|
| **Zero-Shot**        | ✦✦✦☆☆ | ✦✦✦☆☆ | ✦✦☆☆☆ | ✦✦☆☆☆ | **28.415s** |
| **Few-Shot**         | ✦✦✦✦☆ | ✦✦✦✦☆ | ✦✦✦✦☆ | ✦✦✦✦☆ | **45.924s** |
| **Chain of Thought** | ✦✦✦✦✦ | ✦✦✦✦☆ | ✦✦✦✦☆ | ✦✦✦✦☆ | **59.986s** |
| **Meta**             | ✦✦✦✦☆ | ✦✦✦✦☆ | ✦✦✦✦☆ | ✦✦✦✦☆ | **60.178s** |
| **Self-Consistency** | ✦✦✦✦✦ | ✦✦✦✦✦ | ✦✦✦✦✦ | ✦✦✦✦✦ | **31.584s** |


### Key Findings

* Zero-Shot: Fastest, but lacks depth and adaptability.
* Few-Shot: More structured than Zero-Shot but lacks multiple reasoning paths.
* Chain of Thought: Strong step-by-step breakdown but slower.
* Meta: Provides structured reasoning but lacks evaluation of multiple paths.
* Self-Consistency (Best Approach): Generates multiple solution paths, evaluates them, and selects the optimal one, making it the most effective.

# Further research

* Integration with real-world AI-based requirement gathering systems to test the practical application of Self-Consistency prompting.
* Exploring hybrid prompting techniques that combine Chain of Thought with Self-Consistency for improved decision-making.
* Assessing AI performance in long-term requirement evolution to ensure adaptability over time.
* Investigating the impact of prompt fine-tuning on automation accuracy and efficiency.
