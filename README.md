# der-cursor-ai-tasks

this repository contains a definition of roles and tasks to pre-add to your prompts to give the ai certain roles and do certain tasks.

## Usage

Below youll find a view code examples which can be copied and pasted before your prompt. The Idea is that you use those steps to generate a project description, component list and implementaion guid that the cursor-ai-agend then can follow to generate your full project.

All Roles are described in the [roles.md].

(It is a good Idea to create a new chat or composer anytime you do a new step.)

## Steps

### Step 1. Project Description / Concept

Copy the following code infront of your prompt and tell the ai what your project is about, to generate a Concept.md file which will contain you project description. Answer questions that the ai asks to create a better description if your project. Repeat this projcess with the code below and your Concept.md as context in your prompt untill you have a satisfying project concept description.

```
https://raw.githubusercontent.com/derDere/der-cursor-ai-tasks/refs/heads/main/roles.md

Role: ProjectDescriper


```

### Step 2. Component List and Description

Copy the following code infont of your prompt and include the Concept.md file as context into your prompt to generate a list of conponents which your desired application should consist of. Comment and Improve this component structure until you jave a satisfying list of component for your application.

```
https://raw.githubusercontent.com/derDere/der-cursor-ai-tasks/refs/heads/main/roles.md

Role: ComponendDescriber


```

### Step 3. Implementation Steps

Copy the following code infont of your prompt and include the Concept.md and Components.md as context to your prompt to generate a list of implementation steps. Those steps should target to create a fully functionaly version 1 of your application. It is no good idea to try to create deployment/build/release or improvements steps within this first integration list. Try to only define all steps nessesary to create the code of a first running version of your application.

```
https://raw.githubusercontent.com/derDere/der-cursor-ai-tasks/refs/heads/main/roles.md

Role: ImplementationManager


```

### Step 4. Agent Actions

Now try and let your composer run in agend mode and finish each step by step of the implementation guid. Check between each check if the result was created according to your plan. If the AI is going in wrong direktions, try to create a new chat.

## Last Note
Don't forget to include the concept and components file and the link to the role definition for each prompt to hinder the ai from generating false results. Also while folowing the implementation Steps include documentation from used libaries and apis into your promps.
