\# My Git Mastery Challenge Journey



\## Student Information

\- \*\*Name:\*\* Sai Divya  

\- \*\*Student ID:\*\* 23A91A05C4  

\- \*\*Repository:\*\* https://github.com/sai-divya/git-solved-23A91A05C4  

\- \*\*Date Started:\*\* 20th October 2025  

\- \*\*Date Completed:\*\* 28th October 2025  



---



\## Task Summary

I cloned the instructor’s repository that contained pre-built merge conflicts and successfully resolved all of them across multiple branches using correct Git workflows and commands.  

Throughout this challenge, I practiced various Git operations like branching, merging, rebasing, tagging, and documentation.



---



\## Commands Used



| Command | Times Used | Purpose |

|----------|-------------|----------|

| git clone | 1 | Clone instructor's repository |

| git checkout | 20+ | Switch between branches |

| git branch | 10+ | Create and view branches |

| git merge | 2 | Merge dev and conflict-simulator into main |

| git add | 30+ | Stage resolved files |

| git commit | 15+ | Commit resolved changes |

| git push | 10+ | Push commits to my repository |

| git fetch | 2 | Fetch latest updates from remote |

| git pull | 1 | Pull updates from main branch |

| git stash | 2 | Save temporary work |

| git cherry-pick | 1 | Apply specific commit from another branch |

| git rebase | 1 | Rebase feature branch to main |

| git reset | 3 | Undo commits (soft/mixed/hard) |

| git revert | 1 | Safely undo a commit |

| git tag | 2 | Create release tags |

| git status | 50+ | Check current repository state |

| git log | 30+ | View commit history |

| git diff | 20+ | Compare changes before committing |



---



\## Conflicts Resolved



\### 🧩 Merge 1: main + dev (6 files)



\#### Conflict 1: config/app-config.yaml  

\- \*\*Issue:\*\* Different port numbers (8080 vs 3000)  

\- \*\*Resolution:\*\* Added environment-based configuration for both ports  

\- \*\*Difficulty:\*\* Medium  

\- \*\*Time:\*\* 15 minutes  



\#### Conflict 2: config/database-config.json  

\- \*\*Issue:\*\* Different database hosts and SSL settings  

\- \*\*Resolution:\*\* Created separate JSON profiles for production and development  

\- \*\*Difficulty:\*\* Medium  

\- \*\*Time:\*\* 10 minutes  



\#### Conflict 3: scripts/deploy.sh  

\- \*\*Issue:\*\* Different deployment strategies (production vs docker-compose)  

\- \*\*Resolution:\*\* Used environment variable `DEPLOY\_ENV` to handle both cases  

\- \*\*Difficulty:\*\* Hard  

\- \*\*Time:\*\* 20 minutes  



\#### Conflict 4: scripts/monitor.js  

\- \*\*Issue:\*\* Different monitoring intervals and log styles  

\- \*\*Resolution:\*\* Used `process.env.NODE\_ENV` to set interval dynamically  

\- \*\*Difficulty:\*\* Medium  

\- \*\*Time:\*\* 15 minutes  



\#### Conflict 5: docs/architecture.md  

\- \*\*Issue:\*\* Conflicting architectural descriptions  

\- \*\*Resolution:\*\* Merged both into a complete, detailed version  

\- \*\*Difficulty:\*\* Easy  

\- \*\*Time:\*\* 10 minutes  



\#### Conflict 6: README.md  

\- \*\*Issue:\*\* Different feature lists and version numbers  

\- \*\*Resolution:\*\* Combined both with environment labels (Prod / Dev)  

\- \*\*Difficulty:\*\* Easy  

\- \*\*Time:\*\* 10 minutes  



---



\### 🧩 Merge 2: main + conflict-simulator (6 files)

\- \*\*Files:\*\* same as above (rechecked and merged changes carefully)  

\- \*\*Strategy:\*\* Compared all changes side by side and tested merged results  

\- \*\*Outcome:\*\* All conflicts resolved successfully without breaking workflow.  



---



\## Most Challenging Parts



1\. \*\*Reading Conflict Markers:\*\*  

&nbsp;  Initially, I was confused by `<<<<<<<`, `=======`, and `>>>>>>>`, but later understood that they represent “current vs incoming” changes.



2\. \*\*Merging deploy.sh:\*\*  

&nbsp;  This file had two different deployment logics, so I took time to merge both intelligently.



3\. \*\*Understanding Cherry-pick and Rebase:\*\*  

&nbsp;  It was new to me, but I learned how to use `cherry-pick` for specific commits and `rebase` to clean history.



4\. \*\*Testing After Merge:\*\*  

&nbsp;  After resolving each conflict, I verified that all files worked correctly before committing.



---



\## Key Learnings



\### 💻 Technical Skills

\- Mastered merge conflict resolution  

\- Understood how rebase and cherry-pick work  

\- Learned to use `git diff`, `git log`, and `git status` efficiently  

\- Gained hands-on practice with all major Git commands  



\### 🧠 Best Practices

\- Always read both sides before resolving a conflict  

\- Test code before committing  

\- Write clear and meaningful commit messages  

\- Use small, frequent commits for better history tracking  

\- Keep calm while handling conflicts — they’re part of teamwork  



\### 🔁 Git Workflow Insights

\- Conflicts are common and help improve collaboration.  

\- It’s important to document how conflicts were solved.  

\- Git is powerful when used with discipline and understanding.  



---



\## Reflection

This challenge improved my Git confidence a lot. I no longer see merge conflicts as errors but as opportunities to learn how code evolves between branches.  

I now feel ready to handle real-world Git workflows with branching, merging, rebasing, and tagging.  



The experience taught me that `git reflog` is a true lifesaver, and proper documentation is key to professional version control.  

Overall, this Git Mastery Challenge gave me real, hands-on Git knowledge that I can apply in all my future projects.



---



\## 📦 Final Artifacts



```bash

\# Generate git graph

git log --graph --oneline --all --decorate > git-graph.txt



\# List branches

git branch -a > branches.txt



\# List tags

git tag -l > tags.txt



\# List remotes

git remote -v > remotes.txt



\# Commit all

git add git-graph.txt branches.txt tags.txt remotes.txt

git commit -m "docs: Add final project artifacts"

git push origin main



