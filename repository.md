# Co-working with repository

## Branches:
```
├── main    # Main branch with production version of app
├── deploy  # A branch with configured CD
├── dev     # Developement branch
├── feat/<task-name>  # Each task have its own feat/ branch

Merge direction: feat > dev > deploy
                             \
                              > main
```
## Pull Requests:
- Work with tasks in `feat/<task-name>` branch. When task is done then:
```sh
git pull origin dev  # Receive latest version of dev branch
# Resolve possible conflicts
git push --set-upstream origin feat/<task-name>  # Push your task
```
- Do not use `git rebase` with already merged commits.
- Make a PR from `feat/<your-task>` to `dev` branch. Write a description. Example:
```
Task: [Task name](https://github.com/WDL-Team/greet-card/issues/1)
Screenshot: ![](https://private-user-images.githubusercontent.com/51874769.png)

   – [x] The smallest available page width: 320px
   – [±] UI is copied from the template or is even improved
   – [ ] the application works correctly for each of the languages
   ...

Additional info
```

- Pull Request is a place to discuss code. Be cultural, respect each other's time and work.
- PR must be approved by team leader or at least one of your team mates.
- Merge your PR using `squash` to reduce number of commits and each of them will contain its own specific task.
