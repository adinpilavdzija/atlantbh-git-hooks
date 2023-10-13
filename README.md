# Task
[Link](https://www.atlantbh.com/git-hooks/)

Imagine a scenario where you work on a collaborative project using git for versioning files. To maintain clarity and organization within the project, you want to enforce a standardized commit message format.

You want to commit messages to be in the format:

    <type>:<description>
and to have a maximum of 50 characters.


As for the commit type, you offer:
- feature (new feature)

- fix (bug fix)

- refactor (refactoring code)

- wip (work in progress – commits to be pushed later)

Solve this using git hooks.

Hint: use `commit-msg` hook.

  

# Solution

Bash script for enforcing a standardized commit message format.

Variable 'regex' declares Regular Expression rule. It is used for comparison with 'commit_msg'.

'commit_msg=$(cat "$1")' line reads the contents of the first argument passed to the script which is commit message. The commit message isn't directly passed as a command-line argument to the commit-msg hook, so we need to retrieve it.

If the commit message does not conform to the defined regex rule, we get a clear error message.

Script needs to be executable.