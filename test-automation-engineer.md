# Tech Assessment for Test Automation Engineers

In this test assignment we would like to ask you to create two small test suits: one for API and one for a web interface.

## 1. The API Test

Your assignment is to write a test suit using cypress to verify our endpoints are working correctly.
## The HR System API

You will be testing only 2 endpoints:

### GET /api/learners
Returns a list of all availabel learners.

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
- Http 201 Created


**The base URL will be provided to you by your point of contact of Lepaya. If you didn't receive this, please, email us.**

<br/><br/>

## 2. The Web Test

For the web, we will be testing this system: https://react-ts-redux-realworld-example-app.netlify.app/#/

**Use case:** Should like post in the Global Feed List
1. Login to the application
1. Go to the Global Feed Tab
1. Find the Project "Welcome to RealWorld project"
1. Click in the heart box on the right to like the project.
1. The number of likes should increase by 1

<br/><br/>

## Task requirements

Feel free to spend as much or as little time on the exercise as you like as long as the requirements have been met. 
However, we understand people have busy lives so feel free to spend no more than 2-3 hours on a submission. 
We also take into consideration the answers to the technical questions file and what you would like to have added if you had more time. You should look at this as the complete solution, it's much quicker to explain what you would like to have done than coding it.

- You should use Cypress as our Test framework/tool. You can create just one project for both tests.

- Your code should run in one step. Ex: cypress run, npx cypress run, etc.

- Feel free to use whatever frameworks / libraries / packages you like besides that.

- The code is clean and follows modern patterns.

- Commit messages are clear.

- Please, **don't overengineer the solution**. Impress us with your clear and elegant code, avoid extra complexity where you don't need it.

Feel free to ask any questions to clarify the Use Case.

<br/><br/>
## Technical questions

Please answer the following questions in a markdown file called **"Answers to technical questions.md"**.

1. How long did you spend on this test? What would you add to your solution if you had more time? If you didn't spend much time on the test then use this as an opportunity to explain what you would add.

1. Have you learned something new doing this test? If yes, describe it here.

1. How would you improve this API you just used?

1. What could be improved in the description of the task/use cases so it would be more clear what to test?

1. Describe yourself using JSON.

<br/><br/>

## How to deliver this test

- Create a **private repository** on your git provider and push your code to it. Remember, we will be evaluating your commit messages too, so no big bang commit, please.
- **If you have any questions, send us a message.**
- When you are done, invite the hiring managers as contributors to the repo. Their emails should have been sent to you already, but if they were not, please send us a message.
- Good luck!