# CPP Newbie Mentoring
Created for an async code review for students

## How to use this repository

Each folder contains only a task description in the main branch. Students guide: 

0. Install git: https://git-scm.com/install/
1. Fork the repository once: https://github.com/Aeomanate/CPPNewbieMentoring/fork
2. Clone your fork locally in the first time:
   ```
   git clone https://github.com/<your_github_username>/CPPNewbieMentoring.git
   ```

   And update your repository with new tasks if necessary:
   - Sync your fork and update main branch:
   - https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork
   - `git checkout main`
   - Update your branch locally: 
   -  ```
      git checkout students/your_name
      git rebase main
      ```
3. Use a specific branch for your solutions: `git checkout -b students/your_name`
   <details>
      <summary>Advanced git usage</summary>
      
      If you want to know git a bit better and you have to make several commits, it's better to manage it as an additional branch from your:
      - `git checkout -b students/your_name`
      - `git checkout -b students/your_name/solution_for_task_x`
   
      It will create this branch graph:
      - `main` <- `students/your_name` <- `students/your_name/solution_for_task_x`
   
      When you've done with the solution and you've commited it, you can do a merge to your branch:
      - `git checkout students/your_name`
      - `git merge students/your_name/solution_for_task_x`
   </details>
   
4. Solve a problem from the main repository locally. Place your solution into an appropriate task folder.
5. Store and publish your work
   ```
   git status # check what files you're about to commit
   
   git add . # only if there are only *.cpp, *.hpp and other code files
   
   git commit -m "Solved problem X" \
              -m "Approach Y was used, tradeoffs Z discussed"

   git push -u origin students/your_name

   # -u sets the upstream branch, so future git push commands work without arguments:
   git push
   ```
> [!WARNING]
> Important!
> - Make sure that your git-ignore file has a correct setup to exclude all non-code files.
> - It's important to commit only code files without any `.dbg`, `.cmake`, `.dll`, `.exe`, etc.
> - If you're working on C++, your commit should contain only `.cpp`, `.h` files (or `.cxx`, `.hpp` and other variations)
>   AND files that required for proper work (`.png` or `.txt`) as an input data

   Make a pull request to the main repository:
   - You're asking for a merge of **your** branch (`your fork -> students/your_name`)
   - **to your branch** here (`CPPNewbieMentoring -> students/your_name`),
   - Do NOT target the main branch!
   
   GitHub guide:
   https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request
   
6. Wait for or ask for a code review (a code-review guide: https://github.com/mawrkus/pull-request-review-guide)

7. After the code review, your changes will be merged into the main repository to **your** branch
   
8. Any new pull request should go to **your** branch again. Therefore, this repository will contain all your accepted solutions under **your** branch.

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
     - Maybe, you decided to change task description, and you didn't notice it.
     - Maybe, you have to change a task description and without it the task should be solved in a different way that the description is supposed to do.
     - It's always a good idea to ask for help in task description understanding. 
