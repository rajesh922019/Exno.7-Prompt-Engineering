## Exno.7-Prompt-Engineering
# Date:
# Register no.212222033002
# Aim:

To Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

# Algorithm:

1.Identify a personal requirement (e.g., daily task organization).

2.Design simple prompts to collect basic information from the user.

3.Gradually refine prompts to include:

Prioritization of tasks

Time allocation suggestions

Reminders and motivational notes

4.Implement the prompt-based application using ChatGPT.

5.Display outputs showing progression from basic to advanced prompt designs.

6.Evaluate usability and insights provided by the application.

## Python Code:

#Daily Task Organizer Using Chatgpt

import openai

#Set API Key

openai.api_key = "your_openai_api_key"

#Function to query ChatGPT

def ask_chatgpt(prompt):

    try:
    
        response = openai.ChatCompletion.create(
        
            model="gpt-4",
            
            messages=[{"role": "user", "content": prompt}]
            
        )
        
        return response.choices[0].message.content
        
    except Exception as e:
    
        return f"Error: {e}"

#Step 1: Basic Prompt - Simple Task List

prompt1 = "List 5 tasks I should complete today for productivity."

print("=== Basic Prompt ===")

print(ask_chatgpt(prompt1), "\n")

#Step 2: Intermediate Prompt - With Priorities

prompt2 = "Organize my daily tasks into High, Medium, and Low priority categories."

print("=== Intermediate Prompt ===")

print(ask_chatgpt(prompt2), "\n")

#Step 3: Advanced Prompt - With Time Allocation and Motivation

prompt3 = ("Create a structured daily plan for my tasks with estimated time allocations, "
           "short breaks, and a motivational quote at the end.")
           
print("=== Advanced Prompt ===")

print(ask_chatgpt(prompt3))

## Sample Output:

=== Basic Prompt ===
1. Check and reply to important emails  
2. Complete the project report draft  
3. Study one chapter of AI textbook  
4. Exercise for 30 minutes  
5. Plan tomorrow’s agenda  

=== Intermediate Prompt ===
High Priority:  
- Finish project report  
- Study AI textbook  

Medium Priority:  
- Reply to emails  
- Plan tomorrow’s agenda  

Low Priority:  
- Exercise  

=== Advanced Prompt ===
9:00–10:30 AM → Work on project report  
10:30–11:00 AM → Short break  
11:00–12:30 PM → Study AI textbook  
12:30–1:00 PM → Lunch  
1:00–2:00 PM → Reply to emails  
5:30–6:00 PM → Exercise  

"Stay consistent. Small daily progress leads to big results!"  

## Result:

The prompt-based application for organizing daily tasks is developed successfully, demonstrating progression from simple to advanced prompts and showcasing the practical use of LLMs.
