## Page 1

1.
INTRODUCTION & OBJECTIVES 
──────────────────────────────────────────
──────── 
A) Slide 1: Title and Subtitle 
• Title: “Introduction to AI Prompting” 
• Subtitle: “Strategies, Tools, and Real-World Examples for HR, Sales, Marketing, DevOps, 
Data, and More” 
• Presenter Name & Date 
2.
  
B) Slide 2: Why AI Prompting Matters 
   • Key Points: 
     – Effective prompting saves time and improves answer quality 
     – Poorly crafted prompts → vague or unhelpful responses 
     – AI can aid multiple departments (HR, Sales, Marketing, DevOps, Data, etc.) in different tasks    
C) Slide 3: Agenda / Session Overview 
   • Topics: 
     1. Cross-Department Use Cases & Basic Prompting Concepts 
     2. Maintaining a Central “Project Doc” (Requirements & Structure) 
     3. Four Core Prompting Strategies (Q&A, Pros & Cons, Stepwise, Role) 
     4. Additional Prompt Techniques (Few-Shot, Zero-Shot, Chain-of-Thought, RAG) 
     5. Incorporating Function Templates (for Dev focus) 
     6. Tools & Tips (GitHub Copilot, Cursor, Others) 
     7. Correct vs. Incorrect Prompt Examples 
 
2. CROSS-DEPARTMENT USE CASES & BASIC PROMPTING CONCEPTS 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━  
Slide 4: Departmental Relevance 
• HR: 
  – Use Cases: Automating candidate screening, drafting HR policy Q&A, creating onboarding 
processes. 
  – Potential Impact: Saves time for HR teams, standardizes information. 
• Development: 
  – Use Cases: Code generation, debugging, refactoring, project documentation. 
  – Potential Impact: Accelerates development cycles, reduces repetitive coding tasks. 
• Other Departments (Brief Mentions): 
  – Sales (pros & cons of CRM tools, personalized outreach) 
  – Marketing (campaign ideation, refining brand messaging) 
  – DevOps/IT (CI/CD setups, Dockerfiles, server logs analysis) 
  – Data/Analytics (data cleaning, SQL optimization)  
Slide 5: Basic AI Prompting Concepts (Beginner-Friendly) 
• Clarity: Ask direct, unambiguous questions or requests. 
  – Example: “Provide three key metrics to measure our new HR onboarding process success.” 
• Context: Give background details, domain info, or constraints. 
  – Example: “Assume an HR department of 500 employees across two global offices.” 
• Constraints: Specify format, style, word limits, or other neede 
d ranges. 
  – Example: “Respond in under 150 words and use bullet points.” 
• Iteration: Follow up with more prompts to refine or correct. 
  – Example: “Focus only on compliance requirements now.”    



## Page 2

Slide 6: In-Depth Back-and-Forth Example (HR) 
• Example Goal: Automate candidate screening questions. 
• Conversation Flow (Illustrative):    
1.
 Prompt (User): 
"I need to automate candidate screening for a software developer position. Before giving me a 
final list of questions, please ask clarifying questions about our job requirements and any 
constraints we have."    
2.
 AI Response: 
"Could you provide:    
1.
 The technical skills required (languages, frameworks)?   
2.
 Preferred experience level or years of experience?   
1.
 Any focus on cultural fit or soft skills?   
2.
 Number of questions you’d like to ask candidates?" 
1.
  
2.
3.
 Prompt (User): 
"We need a mid-level Java developer with some cloud experience. Emphasis on problem-
solving and communication. We need 5 screening questions in total."    
4.
 AI Response (Refined): 
"Here are 5 screening questions tailored to a mid-level Java developer with cloud experience. 
Each question focuses on problem-solving and communication skills…"    
5.
 Optional Follow-up (User): 
"Can you add an additional question about REST API best practices?"    
6.
 AI Response (Final): 
"Revised list of 6 questions…"  
7.
  
• Teaching Point: Shows how Q&A strategy (the AI asking clarifications first) leads to a more 
targeted final output.  
Slide 7: In-Depth Back-and-Forth Example (Development) 
• Example Goal: Code Generation for a Specific Function. 
• Conversation Flow (Illustrative):    
1.
 Prompt (User): 
"I want to create a function in Python that sorts a list of dictionaries by a ‘timestamp’ key. 
Before you provide the solution, please ask me questions about performance constraints or 
error handling requirements."    
2.
 AI Response: 
"Questions:    
1.
 Maximum size of the list?   
2.
 Do we need to handle missing or invalid timestamp valu 
1.
es?   
2.
 Any preference for sorting library or custom logic?   
3.
 Should we return a new list or modify it in place?" 
1.
  
2.
3.
 Prompt (User): 
"We might have up to 100,000 records. Missing timestamps should default to the current time. 
We prefer using Python’s built-in sorting method, and we want to return a new list to avoid 
side effects."    
4.
 AI Response (Refined): 
"Here’s a function named ‘sort_records(records)’ that uses Python’s built-in ‘sorted’ method 
with a custom key for ‘timestamp.’ It handles missing timestamps by defaulting them to the 
current time. Complexity is O(n log n). Code snippet…"    
5.
 Optional Follow-up (User): 
"Please include docstrings, and add an example usage at the bottom."    



## Page 3

6.
 AI Response (Final): 
"Docstring enhanced function with usage example provided…" 
3. MAINTAINING A CENTRAL “PROJECT DOC” (DEVELOPER FOCUS) 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━  
Slide 8: What Is a “Project Doc” and Why It Matters for Dev Teams 
• Definition: 
  – A living document (e.g., a Confluence page, shared Google Doc, or internal wiki) that stores all 
critical project details, reference materials, and AI prompt guidelines used by developers. 
• Benefits:  
1.
 Code Consistency: Everyone refers to the same style guides and coding standards.   
2.
 Faster Onboarding: New devs can quickly get up to speed on architecture, existing code 
patterns, and AI prompts.   
3.
 Reduced Guesswork: Central place for project constraints (framework versions, memory 
limits, security policies).   
4.
 Collaboration & Transparency: Minimizes confusion by centralizing prompts and best 
practices. 
5.
  
Slide 9: Key Components of the Project Doc (Developer-Oriented)  
1.
 Feature Requirements & Goals 
– Technical user stories (“API must handle 10k requests/minute,” “Service must integrate with 
X library”). 
– Clear acceptance criteria for each feature (e.g., “Unit  
1.
test coverage must be 80% or above”).  
2.
 Project Structures & Constraints 
– Directory layout (e.g., microservices architecture, monolithic structure). 
– Technical constraints (supported language versions, data 
1.
 volume, performance metrics). 
– Security requirements (encryption standards, OWASP top 10 references).  
2.
 Global Instructions & Coding Standards 
– Required frameworks or libraries (e.g., React.js, Express, Spring Boot). 
– Style guidelines (PEP 8 for Python, ESLint rules for JavaScript). 
– Security best practices (password hashing, input sanitization).  
3.
 Prompt Templates & Examples 
– Code generation prompts (“Act as a senior Node.js developer…”). 
– Debugging prompts (“Analyze this error stack trace focusing on concurrency issues…”). 
– Stepwise logic prompts for complex refactoring tasks.  
4.
  
Slide 10: Sample “Project Doc” Layout 
• 1. Title & Intro 
  – “Microservices Migration – Dev Master Doc” or “Refactoring Legacy App – Dev Master Doc” 
• 2. Architecture Overview 
  – Diagrams of modules (e.g., user-service, product-service) or monolithic structure. 
  – Explanation of how services communicate (REST, gRPC). 
• 3. Requirements & Error Handling 
  – “Must handle concurrency for up to 15 microservices,” “Use JWT for authentication,” etc. 
• 4. Constraints & Edge Cases 
  – “Legacy endpoints must be maintained for 3 months,” “Data API calls may fail intermittently,” 
etc. 
• 5. Prompt Templates / Examples 



## Page 4

  – e.g., “For code generation in Node.js: ‘Act as a Node.js expert…’” 
  – e.g., “For Dockerfiles: ‘Create a Dockerfile for Node 14 Alpine…’” 
• 6. Revision History 
  – Track updates to codebase, new prompt guidelines (e.g., new approach to logging, error 
handling).  
Slide 11: Example of Documenting a Prompt Lifecycle 
• Illustrative Flow:  
1.
 Original Prompt: “Write a user login function in Java.” (Insufficient context) 
2.
 Feedback Learned: Missing frameworks, data validations, or security layers. 
3.
 Revised Prompt: “Implement a Spring Boot user login function with MFA. Validate user input 
for SQL injection. Include tests.” 
 
4 
 Final Prompt & Output: 
– Detailed code snippet with test coverage. 
• Value for Devs: 
  – Demonstrates how prompts evolve with clarifications and ensures the final code meets all 
project requirements. 
4. FOUR CORE PROMPTING STRATEGIES (Q&A, PROS & CONS, STEPWISE, ROLE) 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━  
Slide 12: Section Introduction 
• Title: “Four Core Prompting Strategies” 
• Subtitle: “Q&A, Pros & Cons, Stepwise, and Role-Based” 
• Purpose: Provide an overview of each strategy and how it benefits developers.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
A) Q&A PROMPT STRATEGY 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 13: Q&A Prompt Strategy – Overview 
• Concept: 
  – Instead of the AI jumping to a solution, it asks clarifying questi 
ons first. 
  – Ensures the AI “understands” the requirements better. 
• Developer Benefits: 
  – Surfaces important details (frameworks, data structure, performance needs). 
  – Prevents incomplete or misleading answers due to missing context.  
Slide 14: Q&A Prompt Strategy – Developer Example 
• Example Conversation:    
1.
 Prompt (User): 
"I need a function in Python to handle file uploads. Before writing code, ask questions about 
file size limits, validation, and storage approach."   
2.
 AI Response (Questions): 
– "What’s the maximum file size? 
   Are we storing in local filesystem or a cloud service? 
   Any file type restrictions or antivirus checks needed?"   
3.
 Prompt (User): 
"Max size 50MB, storing in AWS S3, only images (jpeg, png), and run a basic scan."   
4.
 AI Response (Solution): 
– “Here’s a Python function using boto3, with checks for file size, extension, and a simple 
virus scan plugin…” 
• Takeaway: By letting the AI ask questions, you eliminate guesswork and get a more accurate 
solution. 



## Page 5

5.
  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
B) PROS & CONS PROMPT STRATEGY 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 15: Pros & Cons Prompt Strategy – Overview 
• Concept: 
  – Request a balanced assessment of multiple options. 
  – Helps developers weigh different frameworks, tools, or design patterns. 
• Developer Benefits: 
  – Avoids biased or one-sided recommendations. 
  – Encourages structured decision-making.  
Slide 16: Pros & Cons Prompt Strategy – Developer Example 
• Example Prompt: 
  "Compare using Redis vs. Memcached for high-speed caching in a Node 
.js application. List advantages and disadvantages of each." 
• Potential AI Response: 
  – Redis Pros: Persistent storage options, built-in data structures. 
    Redis Cons: Slightly more overhead than Memcached, bigger memory footprint. 
  – Memcached Pros: Extremely fast for simple key-value caching, easy setup. 
    Memcached Cons: Limited data structures, no built-in persistence. 
• Takeaway: Developers can choose the best caching solution based on project needs (complex 
data or pure speed).  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
C) STEPWISE (CHAIN-OF-THOUGHT) PROMPT STRATEGY 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 17: Stepwise Prompt Strategy – Overview 
• Concept: 
  – AI solves tasks in discrete steps, waiting for user confirmation before moving on. 
  – Also known as “chain-of-thought” because it outlines each reasoning step. 
• Developer Benefits: 
  – Keeps large refactoring or complex tasks under user control. 
  – Prevents compounding errors by allowing corrections at each step.  
Slide 18: Stepwise Prompt Strategy – Developer Example 
• Example Conversation:    
1.
 Prompt (User): 
"Refactor this Node.js Express middleware code for better error handling. Proceed step by 
step. Stop after each step for my review."   
2.
 AI Response – Step 1: 
– “Identify repeated patterns in error responses… Expl 
1.
anation of approach.” 
– “Type ‘next’ to proceed.”   
2.
 Prompt (User): "next"   
3.
 AI Response – Step 2: 
– “Extract repeated logic into a reusable function… Explanation.” 
– “Type ‘next’ to proceed.”   



## Page 6

4.
 etc. 
• Takeaway: Stepwise approach allows fine-tuning and ensures the final refactor meets all 
requirements. 
5.
  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
D) ROLE PROMPT STRATEGY 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 19: Role Prompt Strategy – Overview 
• Concept: 
  – Ask the AI to act as a specific role (e.g., “senior security engineer,” “database architect,” etc.). 
• Developer Benefits: 
  – Gain domain-specific guidance (e.g., advanced DB optimization or security best practices). 
  – Simulates expertise your team may not have in-house.  
Slide 20: Role Prompt Strategy – Developer Example 
• Example Prompt: 
  "Act as a senior database architect. Optimize our PostgreSQL schema for an e-commerce 
platform with millions of products. Focus on indexing strategy and partitioning." 
• Potential AI Response: 
  – Detailed advice about partial indexes, table partitioning by product category, advanced tuning 
tips (e.g., shared buffers, vacuum settings). 
• Takeaway: The AI’s persona focuses on typical concerns of that role, offering deeper insights.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 
E) WRAP-UP SLIDE FOR THE FOUR STRATEGIES 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 21: Comparing the Four Strategies 
• Quick Recap: 
  – Q&A: AI asks clarifying questions → reduces guesswork. 
  – Pros & Cons: Balanced comparisons → structured decisions. 
  – Stepwise: Iterative problem-solving → better control over final output. 
  – Role-based: Specialized “professional viewpoint” → domain-specific insights. 
• Recommendation: 
  – Combine strategies when needed (e.g., Role + Q&A, Stepwise + Pros & Cons) for more 
nuanced results.  
COMPREHENSIVE AI PROMPTING STRATEGIES & TECHNIQUES 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━  
SLIDE 1: TITLE & OVERVIEW 
• Title: “Comprehensive AI Prompting Strategies & Techniques” 
• Subtitle: “A Unified Look at Structuring Your Prompts for Maximum Effect” 
• Purpose: Present all major prompting methods to developers in one cohesive section without 
repeating concepts.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 



## Page 7

A) ZERO-SHOT & FEW-SHOT PROMPTING 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 2: Zero-Shot Prompting – Overview 
• Definition: The AI receives a direct request with no examples or context. 
• Developer Usage Example: 
  – “Write a function that calculates the factorial of a number in Python.” 
• Pros & Cons: 
  – (+) Quick, straightforward. 
  – (–) May produce generic or incomplete answers if the request lacks detail.  
Slide 3: Few-Shot Prompting – Overview 
• Definition: Providing a few examples of desired input-output before prompting. 
• Developer Usage Example: 
  – Show 1–2 sample code snippets with docstrings, then ask, “Now create a function in the same 
style for reading a CSV file.” 
• Benefits: 
  – Guides the AI toward consistent formatting and approach. 
  – Ideal for setting a “coding style” baseline.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
B) Q&A PROMPTING (CLARIFICATION STRATEGY) 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 4: Why Q&A Prompting? 
• Concept: AI first asks clarifying questions rather than jumping straight to a solution. 
• Advantage to Devs: Surfaces hidden requirements (e.g., performance constraints, security 
needs).  
Slide 5: Q&A Prompting – Developer Example 
• Conversation Sample:    
1.
 “I need a function in Express.js to handle user sign-up. First, ask me all vital details like DB 
preference, password hashing, or email verification.”   
2.
 AI asks clarifications.   
1.
 Developer provides constraints.   
2.
 AI delivers final code snippet, aligned with the clarified requirements. 
3.
  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
C) PROS & CONS PROMPTING 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 6: Pros & Cons Prompting – Overview 
• Definition: Requesting a balanced assessment of multiple options. 
• Developer Usage Example: 
  – “Compare Redis vs. Memcached for caching layers in Node.js.” 
• Outcome: A structured table of tradeoffs, enabling informed decision-making.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
D) STEPWISE (CHAIN-OF-THOUGHT) PROMPTING 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 7: Stepwise Prompting – Also Known as Chain-of-Thought 



## Page 8

• Concept: AI solves tasks in discrete steps, pausing for user confirmation before each step. 
• Developer Example:    
1.
 “Refactor this Java class step by step. Stop after each step and await my ‘next.’”   
2.
 AI provides a partial refactor.   
3.
 Developer approves or adjusts. 
• Benefit: Reduces compounding errors and allows real-time corrections. 
4.
  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
E) ROLE-BASED PROMPTING 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 8: Role-Based Prompting – Overview 
• Definition: Ask the AI to act as a specific expert (e.g., “senior database architect”). 
• Developer Usage Example: 
  – “Act as a senior cybersecurity engineer. Review my new authentication logic for potential 
vulnerabilities.” 
• Advantage: Draws on domain-specific knowledge, surfacing concerns you might overlook.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
F) CHAIN-OF-THOUGHT VS. STEPWISE (OPTIONAL CLARIFICATION) 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 9: Distinguishing Terminology (if needed) 
• Chain-of-Thought: The AI shows its internal reasoning or rationale. 
• Stepwise Approach: The AI breaks down tasks in separate steps. 
• Note: Often used interchangeably. Both aim to provide structured, incremental solutions.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
G) RETRIEVAL-AUGMENTED GENERATION (RAG) 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 10: RAG – Overview 
• Definition: The AI retrieves relevant info from an external source (docs, codebase) and augments 
the response with that context. 
• Developer Example: 
  – “Using our internal wiki on microservices, propose an architecture for a new recommendation 
service.” 
• Benefit: Ensures solutions are grounded in up-to-date, project-specific data instead of purely 
model-based “general knowledge.”  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
H) WRAP-UP & COMPARISON 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 11: Summary Table of Strategies & Techniques 
• Row 1: Zero-Shot → Quick direct answers. 
• Row 2: Few-Shot → Guides style or structure. 
• Row 3: Q&A → AI first clarifies before solving. 
• Row 4: Pros & Cons → Balanced overview of multiple options. 
• Row 5: Stepwise/Chain-of-Thought → Incremental solution steps. 
• Row 6: Role-Based → Domain-specific or expert viewpoint. 
• Row 7: RAG → Leverages external knowledge sources.    



## Page 9

Slide 12: Choosing the Right Approach 
• Key Takeaways:  
1.
 Combine strategies for complex tasks (e.g., Role + Stepwise).   
2.
 Provide clarity and context for better results.   
3.
 Keep an eye on constraints (performance, security) in your prompts. 
4.
  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
USING THIS COMBINED SECTION 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
• This unified approach prevents duplication that might arise from separating “core strategies” and 
“additional techniques.” 
• Each technique has unique benefits; try them in tandem based on your project’s needs. 
• Great for developer-favored tasks: code generation, debugging, tool comparisons, architectural 
planning, etc. 
 
 
 
 
 
6. INCORPORATING FUNCTION TEMPLATES (DEVELOPER FOCUS) 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━  
Slide 1: Section Introduction 
• Title: “Incorporating Function Templates” 
• Subtitle: “Standardizing Signatures & Structures for Code Generation” 
• Purpose: Explain why developers benefit from starting with a function template, then leveraging 
AI to fill in details.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
A) WHY USE FUNCTION TEMPLATES? 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 2: The Concept & Rationale 
• Standardization: 
  – Ensures consistent parameter naming, return types, and docstrings across the codebase. 
• Clarity: 
  – Helps the AI (and developers) understand precisely which inputs and outputs are expected. 
• Team Collaboration: 
  – Multiple devs can agree on a function signature upfront; AI-generated implementations then 
remain consistent.  
Slide 3: Quick Example – Template Before Logic 
• Initial Template (Human-Created): 
  "def process_data(dataset, config) -> dict: 
       ''' 
       Description: 
       Parameters: 
       Returns: 
       ''' 
       pass  # to be implemented" 
• AI Integration: 
  – Prompt: “Fill out the logic for ‘process_data(dataset, config) -> dict’ using Python and follow 
best practices for large datasets.” 
• Outcome: 



## Page 10

  – AI respects the template structure while adding the logic for data processing (error handling, 
transformations, etc.).  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
B) WORKFLOW FOR DEVELOPERS 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 4: Step-by-Step Process    
1.
 Create or Approve Template 
– Agree on parameter names, data types, docstring details.   
2.
 Submit Template to AI 
– Provide relevant constraints (“up to 100k rows,” “missing values handled,” etc.).   
3.
 Review AI-Generated Code 
– Check for consistency with coding standards, security guidelines.   
4.
 Iterative Refinement 
– Prompt AI for improvements if logic or edge cases aren’t fully addressed. 
5.
  
Slide 5: Tips for Writing Effective Templates 
• Include Docstrings: 
  – Clearly specify parameter types, expected return types, and possible exceptions. 
• Use Meaningful Names: 
  – No “foo” or “bar”—use “user_records,” “transaction_data,” etc. 
• Outline Edge Cases: 
  – “# TODO: Handle empty dataset,” or “# TODO: Account for user time zones.” 
• Keep it Minimal: 
  – Enough detail to guide the AI but not so rigid that you stifle creativity (e.g., no over-specifying 
how to implement each line).  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
C) LIVE EXAMPLE & DEMONSTRATION (OPTIONAL) 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 6: Example Prompt with a Given Template 
• Template: 
  "def authenticate_user(username: str, password: str) -> bool: 
       ''' 
       Authenticates a user. 
       Parameters: 
         username: 
         password: 
       Returns: bool - True if authenticated, else False 
       ''' 
       pass" 
• Prompt to AI: 
  "Implement logic in this function. Use bcrypt for password hashing, and consult our user 
database. Return True or False based on authentication. Handle edge cases like missing 
username." 
• AI Response: 
  – Fills in DB query, checks hashed password, returns bool.  
Slide 7: Potential Pitfalls & Workarounds 
• Over-Reliance: 
  – If the template is incomplete, the AI’s output might miss crucial steps. 



## Page 11

• Code Duplication: 
  – Reusing the same template for many functions without re-checking can lead to repeated logic. 
• Security Oversights: 
  – Always manually verify the AI’s code for security concerns (SQL injection, safe handling of 
secrets, etc.).  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
D) KEY TAKEAWAYS 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 8: Summary of Function Template Approach 
• Consistency, Efficiency, & Clarity: 
  – A well-defined template sets the groundwork for accurate AI-generated code. 
• Collaborative Approval: 
  – Team alignment on function signatures avoids rework down the line. 
• Iterative Refinement: 
  – Continue updating templates as the project evolves or new requirements arise. 
 
 
 
 
 
TOOLS & TIPS: VS CODE & CURSOR 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━  
SLIDE 1: SECTION INTRODUCTION 
• Title: “Tools & Tips: VS Code & Cursor” 
• Subtitle: “Practical Pointers for Developer Workflows”    
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
A) USING AI IN VS CODE 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
SLIDE 2: VS CODE – TIPS FOR AI INTEGRATION 
• Install & Enable: 
  – Ensure the AI extension (e.g., GitHub Copilot) is properly installed. 
• Provide Context: 
  – Use descriptive file names and docstrings so the AI sees relevant details. 
• Inline Comments: 
  – Type “// TODO” or “# TODO” plus a short description to guide AI suggestions. 
• Quick Testing: 



## Page 12

￼
 
  – Validate code snippets in a local test environment  
right away—avoid letting partial or unverified AI suggestions linger in production code.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
B) USING CURSOR FOR CHAT-BASED EDIT 
ING 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
SLIDE 3: CURSOR – TIPS FOR FILE-LEVEL CONTEXT 
• Chat Over Specific Lines: 
  – Highlight a range of code and ask: “Refactor these lines for clarity.” 
• Folder Aware: 
  – Let Cursor know if it can reference multiple files so 
 it can see the bigger picture. 
• Request Explanations: 
  – Ask, “Why is this code producing undefined errors?” for quick debugging suggestions. 
• Confirm Changes Incrementally: 
  – Don’t accept large-scale refactors without reviewing them step-by-step.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
C) KEY TAKEAWAYS 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
SLIDE 4: FINAL TIPS & WRAP-UP 
• Keep It Clear: 
  – The AI can’t guess hidden context; specify environment, frameworks, or constraints. 
• Always Validate: 
  – Treat AI suggestions as “drafts”; do your own code reviews or testing. 
• Leverage Iteration: 
  – Ask follow-up prompts to refine partial answers, especially for more complex tasks. 
• Maintain Security: 
  – Never paste credentials or sensitive code openly; use local solutions if privacy is a concern. 



## Page 13

 
 
 
 
CORRECT VS. INCORRECT PROMPT EXAMPLES 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━  
Slide 1: Section Introduction 
• Title: “Correct vs. Incorrect Prompt Examples” 
• Subtitle: “Learning Through Contrast”  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
A) WHY PROMPT QUALITY MATTERS 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 2: Quick Recap & Rationale 
• One poorly-defined prompt can lead to misaligned or incomplete AI outputs. 
• Seeing real examples helps developers understand how specific details improve responses.    
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
B) EXAMPLE 1: CODE GENERATION (PYTHON) 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 3: Incorrect Prompt 
• Prompt: 
  "Write code to sort data." 
• Outcome: 
  – AI returns a minimal snippet (e.g., sorted on a simple list), ignoring edge cases or docstrings.    
Slide 4: Correct Prompt 
• Prompt: 
  "Write a Python function named sort_records(records) that sorts a list of dictionaries by a 
‘timestamp’ key. 
   Requirements:    
1.
 Return a new sorted list (don’t modify in place)   
2.
 Handle missing or null timestamps by skipping the record   
3.
 Include a docstring explaining parameters and return type" 
• Outcome: 
1.
  – AI provides a more complete function with error handling and docstring. 
2.
  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
C) EXAMPLE 2: DEBUGGING & ERROR RESOLUTION (NODE.JS) 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 5: Incorrect Prompt 
• Prompt: 
  "Why won't my Node app work?" 
• Outcome: 
  – AI guesses vaguely, possibly referencing common pitfalls but lacking specifics.    



## Page 14

Slide 6: Correct Prompt 
• Prompt: 
  "I have a Node.js Express server returning ‘TypeError: Cannot read property of undefined.’ 
   Here’s the relevant code snippet from lines 45-60: [paste snippet]. 
   Please identify the root cause and suggest fixes, including how to handle null checks and 
validation." 
• Outcome: 
  – AI zeroes in on the exact snippet, explains the variable or object that’s undefined, and 
suggests relevant solutions.  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
D) EXAMPLE 3: PROJECT SETUP & ARCHITECTURE 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 7: Incorrect Prompt 
• Prompt: 
  "Set up a microservice." 
• Outcome: 
  – Generic instructions, possibly skipping containerization or ignoring your existing environment.    
Slide 8: Correct Prompt 
• Prompt: 
  "Create a Node.js microservice for user authentication. 
   Requirements:    
1.
 Use Docker for containerization   
2.
 Employ JWT-based authentication   
1.
 Expose REST endpoints for login and logout   
2.
 Provide a sample Dockerfile and minimal package.json" 
• Outcome: 
  – AI outlines Docker steps, JWT logic, and endpoint basics in a neat, domain-specific 
solution. 
3.
  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
E) LESSONS LEARNED & WRAP-UP 
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
━━━━━━━━━━━━━━━━━ 
Slide 9: Key Takeaways from Examples 
• Specifics Matter: 
  – Always mention data types, frameworks, and constraints to get targeted results. 
• Rich Context = Better Output: 
  – A short snippet or error log helps AI diagnose issues accurately. 
• Sufficient Detail, but Not Overkill: 
  – Provide must-have requirements without making the prompt unwieldy.    
Slide 10: Conclusion 
• “Crafting better prompts is an iterative process—keep refining based on what the AI returns, and 
document successful prompts in your ‘Project Doc’ for reuse.” 


