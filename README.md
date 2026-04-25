# CPP Newbie Mentoring
Created for an async code review for students

## How to use this repository

Each folder contains only a task description in the main branch. Students guide: 

0. Install git: https://git-scm.com/install/
1. Fork the repository once: (fork guide)[https://github.com/Aeomanate/CPPNewbieMentoring/fork]
2. Clone your fork locally in the first time
   <details>
      <summary>Clone guide</summary>
      
      ```bash
      git clone https://github.com/<your_github_username>/CPPNewbieMentoring.git
      ```
   
      And update your repository with new tasks. You do it, when my __**main**__ branch updates:
      - Sync your fork and update main branch: (sync fork guide)[https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork]
        
      - Make the main branch as current branch
        ```bash
        git checkout main
        git pull
        ```
      - Update your branch locally: 
         ```bash
         git checkout students/your_name
         git rebase main
         ```
         Here may occur merge conflicts. You have to decide how to merge my changes and your changes.
         - Details here: (merge guide)[https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line]
         - Also, for merging you may prefer some GUI utilites, like (tortoise git)[https://tortoisegit.org/].
           
           It's a great tool for fast merging, but you have to adapt to raw git commands, it's always better in any case, (trust me)[https://softwareengineering.stackexchange.com/a/173318]. 
   </details>
   
4. Use a specific branch for your solutions: `git checkout -b students/your_name`
   <details>
      <summary>Advanced git usage</summary>

      Use it if:
      - You want to know git a bit better
      - You have to make several commits in one task
   
      It's better to manage solutions as an additional branch originated from your general branch:
      - ```bash
        git checkout -b students/your_name
        git checkout -b students/your_name/solution_for_task_x
        ```
   
      It will create this branch graph:
      - `main` <- `students/your_name` <- `students/your_name/solution_for_task_x`
   
      When you've done with the solution and you've commited it, you can do a merge to your branch:
      - ```bash
         git checkout students/your_name
         git merge students/your_name/solution_for_task_x
        ```
  
      Such flow allows you to organize branches in more proper way.
      Therefore, for each task you'll have a separated branch, and you won't create a mess in your general branch (`students/your_name`)
   </details>
   
6. Solve a problem from the main repository locally. Place your solution into an appropriate task folder.
   
7. Modify README.md file in the root of the solution.
   - Append `Solution` section, explain what you've done here and why.
   - Append a sub-section `Solution output example` - you may attach a light, small jpg only if necessary.
   - It's better to write just plain text (just copy it from your terminal).
     > Keep in mind, GitHub have a limited free space for each repository, so don't blow up the repository size, commit only text data.
     
8. Store and publish your work
   <details>
      <summary>Publishing guide</summary>
      First, execute these commands:
      
      ```bash
      # Check what files you're about to commit.
      git status 
      
      # Add necessary files to preparing area (stage). Do it only if status showed *.cpp, *.hpp and other code files.
      git add . 

      # Commiting is a operation for saving your changes in a local git database
      git commit -m "Solved problem X" \
                 -m "Approach Y was used, tradeoffs Z discussed"

      # Pushing is a network operation. You're updating your remote fork with fresh local changes.
      git push -u origin students/your_name
   
      # The flag -u sets the upstream branch, so future git push commands work without arguments:
      git push
      ```
      
      > Important!
      > - Make sure that your git-ignore file has a correct setup to exclude all non-code files.
      > - It's important to commit only code files without any `.dbg`, `.cmake`, `.dll`, `.exe`, etc.
      > - If you're working on C++, your commit should contain only `.cpp`, `.h` files (or `.cxx`, `.hpp` and other variations)
      >   AND files that required for proper work (`.png` or `.txt`) as an input data
   
      Make a pull request to the main repository:
      - You're asking for a merge of __**your**__ branch (`your fork -> students/your_name`)
      - __**to your branch**__ here (`CPPNewbieMentoring -> students/your_name`),
      - Do NOT target the main branch!
      
      (GitHub pull request guide)[https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request]
   </details>

6. Wait for or ask for a code review (a code-review guide: https://github.com/mawrkus/pull-request-review-guide)

7. After the code review, your changes will be merged into the main repository to __**your**__ branch
   
8. Any new pull request should go to __**your**__ branch again. Therefore, this repository will contain all your accepted solutions under __**your**__ branch.

## I don't know git / I don't know how to solve a task!
That's completely fine for today.  
1. You can use AI to ask for help with any git operation,
   because it's only an additional tool for working with other people, you don't need to go deep into it right now.
   - You don't have to use AI only while you're working on your solution. Why?
   
     It's usually not helpful to rely entirely on AI while you're working on your first beginner solutions.
     You're learning new things through mistakes and dozens of attempts.
     You don't have to simplify your path for now, until you know how to create a complex program by yourself of at least 500 lines of code.
     Before this point, AI will only give you solutions, but not knowledge.
2. If you want, you can find any git handbook or video. For basic concepts, it's a pretty simple thing.
3. You're allowed to google, find some forum solution pieces, read documentation and try different approaches.
   - Sometimes, a task could get 1 week of your time. Sometimes you can solve it just having a glance at the description.
   - Every task have a dozen variations of solution - it's up to you what to choose.
   - If you can't find any solution, you can ask for help, advice, tip, or direct guide.
     - Maybe, you decided to change a task description, and you didn't notice it.
       Therefore, you can't find a solution to a very broad and, actually, another task. It's a usual case when a task description wasn't interpreted correctly.
     - Maybe, you have to change a task description, and without it the task can't be solved. Mistakes occur - offer your variations. 
     - It's always a good idea to ask for help in task description understanding. 
