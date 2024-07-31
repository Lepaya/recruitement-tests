# Lepaya Flutter Assignment

## Intro

Welcome! This is the Flutter assignment for engineering positions at Lepaya.

---
Please read the task carefully and use **Dart** and **Flutter** to create a solution by building the following deliverables:

1. A Flutter application.
2. Answers to some technical questions.

Each deliverable will be explained further in this document.

Please provide them by cloning this repository, creating a new repository on your git provider, and when ready, invite `lepaya-code-reviewer` as a collaborator on the new repo.

---
Feel free to use any publicly available libraries that you are comfortable with and try to use software development best practices as you would in any professional project.

Also, don't stress; the assignment is tested by humans, so it won't fail automatically due to a minor issue and will be a starting point for a conversation where you can explain your decisions and get feedback on your solution.

Good luck, and have fun!

## The Task

Your task is to create an app that requests and displays the `hot`, `new`, and `rising` lists of the `/r/FlutterDev` subreddit.

You can find the Reddit API documentation [here](https://www.reddit.com/dev/api/) and the expected design [here](https://www.figma.com/file/I24HNkA9NfRVjObQxMVYMi/Flutter-assignment-v2?node-id=0%3A1).

## Deliverables

### 1. Flutter application

The application must run on `web`, `iOS`, and `Android`.

It should be well tested, with a choice of `unit` tests, `widget` tests, `integration` tests, or all of them.

#### 1.1. Data handling

- Implement the logic to request and store the data from Reddit's API.
- Ensure you include a way to request the next page of results, as this will be needed for the next task.
- If you opt to use or not use a state management library, please provide your reasoning.
- Refer to the [Reddit API documentation](https://www.reddit.com/dev/api/) and make sure you are calling the correct API for the `/r/FlutterDev` subreddit.

When you are happy with the result, open a PR just like you would when working normally.

#### 1.2. UI implementation

- Implement the UI for the app, ensuring it matches the provided designs.
- The list on the screen should support infinite scrolling, loading more items as the user scrolls.
- Clicking on a card should open the URL of the post in a web browser.
- Pay close attention to sizes, colors, and spacings as specified in the Figma file.

Please follow our [Figma File](https://www.figma.com/file/I24HNkA9NfRVjObQxMVYMi/Flutter-assignment-v2?node-id=0%3A1) for the specific spacings, colors, and fonts that you should use.

When you are happy with the UI, create another PR that targets PR #1.1.

### 2. Answers to technical questions

Please answer the following questions in a markdown file called **"ANSWERS.md"**.

1. How long did you spend on the coding test?
2. What would you add to your solution if you had more time? If you didn't spend much time on the coding test, then use this as an opportunity to explain what you would add.
3. Describe your final solution in plain english. Point out your design decisions and the reasoning behind them.
4. Have you learned something new doing this test? If yes, describe it here.
5. Describe yourself using JSON.

When ready, create another PR that targets PR #1.2.

## Instructions

1. Clone this repo. *Please do not fork it.*
2. Create a new Flutter application from scratch that targets `web`, `iOS`, and `Android`.
3. Create a private repository on your git provider and push the newly created Flutter app as it is.
4. Create a PR for each subtask (#1.1, #1.2 and #2). Ensure each subsequent PR targets the previous one to maintain a clean diff.
5. If you want, feel free to add extra features, but separate them into different PRs.
6. Provide a concise one or two-line command to start your project. If any explanation is necessary, create a `HOWTO.md` file and explain how to run your solution.
7. When you are finished, add `lepaya-code-reviewer` as a reviewer for each PR.
8. Send an email to your HR contact informing them that you have completed your assessment.

## Final Tips

- Feel free to ask for clarification if something is unclear in the task.
- Ensure your code is clear, maintainable, and adheres to modern coding standards.
- Aim to develop an application that is not only functional but also feels smooth and fluid.
- Try not to over-engineer. "Everything should be made as simple as possible, but not simpler."
