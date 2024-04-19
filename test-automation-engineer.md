# Tech Assessment for Test Automation Engineers

In this test assignment we would like to ask you to create two small test suits: one for a API and one for a web interface.

## 1. The API Test

Your assignment is to write a test suit using **cypress or playwright** to verify our endpoints are working correctly.

You will be testing only 2 endpoints:

### GET /api/learners
Returns a list of all available learners.

Ex: GET /api/learners

Expected: 
- List of learners in the format bellow. 
- HTTP 200 OK
```
{
    "learners": [
        {
            "id": "b108a08f-1663-4755-a545-bd07e5c5074e",
            "name": "Joy Reynolds DVM"
        },
        {
            "id": "47d8eb7d-fafa-4ef5-9fa9-0bb4dc733f86",
            "name": "Olive Daniel IV"
        }
    ]
}
```

### POST /api/learners/
Adds a new learner to the learners list.

Ex: POST /api/learners

Body:
```
{
    "name": "Some name"
}
```
Expected:
- Learner is added to the list
- Http 201 Created

Our developers double-checked that both endpoints are working fine, but if you find any discrepancy between the spec written here and the result of your test, that test should **break the pipeline and stop it.** We don't want faulty APIs to be deployed to production.


**The base URL will be provided to you by your point of contact of Lepaya. If you didn't receive this, please, email us.**

<br/>

## 2. The Web Interface Test

For the web, we will be testing this system: https://react-ts-redux-realworld-example-app.netlify.app/#/

**Use case:** Should like post in the Global Feed List
1. Login to the application
1. Go to the Global Feed Tab
1. Find the Project "Welcome to RealWorld project"
1. Click in the heart box on the right to like the project.
1. The number of likes should increase by 1
 
This is an open application, you can easily create a new user on your own to run your tests.

<br/>

## Task requirements

Feel free to spend as much or as little time on the exercise as you like as long as the requirements have been met. 
However, we understand people have busy lives so feel free to spend no more than 2-3 hours on a submission. 
We also take into consideration the answers to the technical questions file and what you would like to have added if you had more time. You should look at this as the complete solution, it's much quicker to explain what you would like to have done than coding it.

- **You should use Cypress or Playwright as our Test framework/tool**.

- **Create just one project/repository for both tests**.

- Feel free to use whatever frameworks / libraries / packages you like besides that.

- The code is clean and follows modern patterns.

- Commit messages are clear.

- **Write 2 Github Actions for running the tests**, **one for the API** and **another for the Web Interface**. If a test fails, it should break the pipeline.
  - Tip: use the trigger: "[workflow_dispatch]" to be able to manually run the pipelines.

- **Write a README.md** with instructions on how to run your project and your tests.

- Please, **don't overengineer the solution**. Impress us with your clear and elegant code, avoid extra complexity where you don't need it.

- Feel free to ask any questions to clarify the Use Case.

<br/>

## Technical questions

Please answer the following questions in a markdown file called **"Answers to technical questions.md"**. Place this file in the **root of your project** so it is easly found.

1. How long did you spend on this test? What would you add to your solution if you had more time? If you didn't spend much time on the test then use this as an opportunity to explain what you would add.

1. Have you learned something new doing this test? If yes, describe it here.

1. How would you improve this API you just used?

1. What could be improved in the description of the task/use cases so it would be more clear what the requirements are?

1. What are your tools/frameworks of choice when testing each type of test? Why did you choose these tools?

1. Describe yourself using JSON.

<br/>

## How to deliver this test

- Create a **private repository** on Github and push your code to it. Remember, we will be evaluating your commit messages too, so no big bang commit, please.
- Don't forget to add the 2 Github Actions so we can run your tests.
- When you are done, invite the user **lepaya-code-reviewer** as a contributor to the repo and then **notify us**.
- **If you have any questions, send us a message.**
- Good luck!
