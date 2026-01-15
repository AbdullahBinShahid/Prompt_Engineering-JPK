# **Which is the best LLM?**

See how leading models stack up across text, image, vision, and beyond. This page gives you a snapshot of each Arena:

https://lmarena.ai/leaderboard
 
 
 
 ## **What is Prompt Engineering?**

Prompt engineering is the art and science of crafting instructions that guide AI language models to produce desired outputs. Think of it as learning to communicate effectively with AI systems to achieve specific goals.

## **Why is it important?**

You don't need to be a programmer to use AI effectively
Good prompts can dramatically improve AI performance
It's an iterative skill that improves with practice
It's becoming essential for productivity in many fields


## **Table of Contents**

•	What is Prompt Engineering?

•	Understanding Large Language Models

•	Essential Configuration Settings

•	Fundamental Prompting Techniques

•	Advanced Prompting Strategies

•	Best Practices for Effective Prompts

•	Common Pitfalls and How to Avoid Them

•	Hands-On Examples

•	Testing and Iteration

•	Resources and Next Steps

•	Mixture-of-Experts (MoE) and Prompt Engineering

•	The 6-Part Prompting Framework

## **Prompt engineering vs. context engineering**.

Prompt engineering = crafting the instruction you give the model. 

Context engineering = curating the information the model can see when following that instruction.

## **Understanding Large Language Models.**

Large Language Models are prediction engines that:

•	Take text input (your prompt)

•	Predict the next most likely word/token

•	Continue this process to generate complete responses

•	Base predictions on patterns learned from training data


# **Fundamental Prompting Techniques:**

	Zero-Shot Prompting.

	 One-Shot Prompting.

	 Few-Shot Prompting.

	System Prompting.

	Role Prompting.

	Contextual Prompting.


## **Advanced Prompting Strategies:**

	Step-Back Prompting.

	ReAct (Reasoning + Acting).

	Tree of Thoughts (ToT).

## 1. **Zero-Shot Prompting:**			

	The simplest approach—just ask directly without examples.

Example:

                 Translate this sentence into English:
                         "Main school ja raha hoon."

 ## 2.**One-Shot Prompting:**

	Provide a single example to guide the response format.
Example:

    Translate English to French:

    English: "Hello, how are you?"

    French: "Bonjour, comment allez-vous?"

    English: "Where is the library?"

## 3.**Few-Shot Prompting:**

Few-shot prompting means teaching the AI by showing a few examples first, instead of just giving instructions.

**Example:**

    Sentence: I love this mobile phone.

    Sentiment: Positive

    Sentence: This movie was very boring.

    Sentiment: Negative

    Sentence: The food tastes amazing.

    Sentiment:	

**What happened here?**

•	You gave a few examples

•	The AI learned the pattern

•	Then it answered the new input correctly

## 4.**System Prompting:**

	Set overall context and behavior guidelines.

Example:

    You are a helpful travel guide. Provide practical, accurate information about destinations. Always include:

- Key attractions

- Local customs to be aware of

- Budget considerations

- Best time to visit

User: Tell me about visiting Tokyo.

## 5.**Role Prompting:**

Assign a specific character or expertise to the AI.

Example:

     Act as a technical interviewer. Ask me 5 beginner-level Python questions

Effective roles:

•	Subject matter expert (doctor, lawyer, teacher)

•	Creative roles (writer, designer, poet)

•	Analytical roles (data analyst, consultant)

•	Communication styles (friendly tutor, formal advisor)
 
## 6.**Contextual Prompting:**

Provide specific background information relevant to the task.

Example:

            Context: You're writing for a tech blog aimed at beginners who have never coded before.

    Write a 200-word explanation of what an API is, using simple language and practical examples.
……………………………………………….

Example #02:

         Write a polite and professional email to my instructor asking for a 2-day extension.
         I am a university student. I missed my assignment deadline because I was sick.
Contextual prompting means giving the AI background information or situation (context) before asking your main question, so the response matches the situation correctly.


# **Advanced Prompting Strategies**

 ## **Chain of Thought (CoT) Prompting**:

Encourage step-by-step reasoning for complex problems.

**EXAMPLE**
          
          Solve this step by step:
          If I was 6 when my sister was half my age, how old is my sister when I'm 40
          Let me think through this step by step:

## When to use:

Math problems
Logical reasoning
Complex analysis
Multi-step processes
Best practices:

Use "Let's think step by step" or similar phrases
Set temperature to 0 for consistent reasoning
Extract final answers separately from reasoning


## Self-Consistency:

Generate multiple reasoning paths and select the most common answer.

Process:

1.Ask the same question multiple times with different phrasings
2.Compare the answers
3.Choose the most frequently occurring result

**Example:**

    You want to know the best time to study.

    You ask the same question to 4 people:
    

Explanation of Concept: Self-Consistency involves generating multiple answers to the same question using varied reasoning approaches to ensure reliability. By comparing the results, you select the most frequent or consistent outcome, reducing the chance of errors from a single flawed reasoning path

## **Step-Back Prompting**:
Ask a more general question first, then use that context for the specific question.

**EXAMPLE**
        
               PROMPT:  What factors make a vacation enjoyable?”
               RESPONSE: Weather
                         Budget
                         Activities you enjoy
                         Travel time
                         Safety


                 Now you ask:

                “Considering these factors, which vacation spot suits me best?”

Explanation of Concept: Step-Back Prompting involves first asking a broader, foundational question to establish key principles or context before tackling the specific task. This approach ensures the model grounds its response in general knowledge. before applying it to the specific problem. By breaking the task into two steps, the model produces more informed and structured recommendations, reducing the risk of overlooking critical factors.                


## **ReAct (Reasoning + Acting)**

Combine reasoning with tool use or actions.

**EXAMPLE**
       
         Step 1 – Reason:

         “I want a restaurant nearby. I like Italian food, and it should have good reviews.”

          Step 2 – Act:

          “Search Google Maps for Italian restaurants within 5 km and sort by rating.”

           Step 3 – Reason:

           “The top-rated one has great reviews but is expensive. I want something affordable too.”

             Step 4 – Act:

              “Check menu prices online and pick the one within my budget.”
              
ReAct is a way of solving problems step by step by mixing thinking and doing.

First, you think about what to do next.
Then, you take an action, like searching for information or using a tool.
After that, you look at the result and decide your next step.
This process repeats until the problem is solved.


**Best Practices for Effective Prompts**

## 1. Be Specific and Clear

Bad:

    Write about dogs.
good:

    Write a 300-word informative article about the health benefits of owning a dog, focusing on mental health, physical activity, and social connections. Use a friendly, accessible tone for general readers.

 ## 2. Use Action Verbs

 Be explicit about what you want the AI to do:

Create, Analyze, Describe, Evaluate, Compare
Generate, Extract, Rank, Summarize, List
Explain, Translate, Classify, Write

## 3. Provide Examples When Possible

Examples are the most powerful way to communicate your expectations

## 4. Structure Your Prompts

Use clear formatting:

    Task: [What you want done]
    Context: [Background information]
    Format: [How you want the output structured]
    Example: [Sample of desired output]

## 5. Use Instructions Over Constraints

 Better:

    Write a professional email summarizing the key points from our meeting.

  bad:

      Write an email but don't make it too long or too informal or too detailed.

#  Common Pitfalls and How to Avoid Them

      
## 1. Ambiguous Instructions:
Problem: Vague requests lead to unpredictable outputs 
Solution: Be specific about what you want

## 2. Contradictory Instructions:
Problem: Conflicting requirements confuse the model 
Solution: Review prompts for internal consistency

## 3. Too Many Constraints:
Problem: Over-constraining limits model creativity 
Solution: Focus on positive instructions rather than long lists of don'ts

## 4. Ignoring Token Limits:
Problem: Responses get cut off mid-sentence 
Solution: Set appropriate limits and structure accordingly

## 5. Not Testing Variations:
Problem: Assuming first attempt is optimal 
Solution: Test different phrasings, examples, and approaches
