# Tech Assessment

Here at Lepaya we have to integrate with many other HR systems. We get data from them so we can automate a lot of processes but also use this valuable information to provide insights to our customers.

In this assignment, you will experience a bit of the type of problems we face every day with our development teams.

## Coding Test

Your assignment is to connect to one HR System API, combine some information from there and make it available as a new internal endpoint.

## The HR System API

You will be accessing 3 endpoints:

Endpoint | Description
-- | --
/api/trainers | List of all available trainers
/api/trainers/{id} | A single trainer
/api/learners | List of all available learners
/api/learners/{id} | A single learner
/api/courses | List of all available courses
/api/courses/{id} | A single course


Unfortunately, this is a third party API and we can’t change it.

**The base URL will be provided to you by your point of contact of Lepaya. If you didn't receive this, please, email us.**

## Task requirements

Feel free to spend as much or as little time on the exercise as you like as long as the requirements have been met. 
However, we understand people have busy lives so feel free to spend no more than 2-3 hours on a submission. 
We also take into consideration the answers to the technical questions file and what you would like to have added if you had more time. You should look at this as the complete solution, it's much quicker to explain what you would like to have done than code it.

- Your code should run in one step.

- **The API should be a node.js application. Use typescript.**

- Our default framework is nestjs but feel free to use whatever frameworks / libraries / packages you like.

- The code is clean and follows modern patterns.

- Commit messages are clear.

- You must include unit tests. They are really important to us so make sure they are all green and test the code well. Bonus points if you use TDD well.

- Please, **don't overengineer the solution**. Impress us with your clear and elegant code, avoid extra complexity where you don't need it.

## User Story

- Given I am a user running the application.

- When I submit an id (e.g. "ef131a0c-3006-4a38-8cfd-085fa08f8361") to the API.

- Then I want to see the selected course, its trainer and learners.


The API output format should look like this:

**GET /api/lepaya-courses/{id}**

```
{
  "id": "ef131a0c-3006-4a38-8cfd-085fa08f8361",
  "title": "Business-focused bifurcated secured line",
  "date": "2073-01-18T06:57:06.870Z",
  "trainer": {
    "id": "65145028-c761-429d-a16b-fd41662dd793",
    "name": "Willis Schamberger"
  },
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


Feel free to ask any questions to clarify the Use Case.

## Technical questions

Please answer the following questions in a markdown file called **"Answers to technical questions.md"**.

1. How long did you spend on the coding test? What would you add to your solution if you had more time? If you didn't spend much time on the coding test then use this as an opportunity to explain what you would add.

1. Describe your solution in plain english. Point out your design decisions and the reasoning behind them.

1. Have you learned something new doing this test? If yes, describe it here.

1. How would you improve the HR System API you just used?

1. Describe yourself using JSON.

# How to deliver this test

- Create a **private repository** on Github and push your code to it. Remember, we will be evaluating your commit messages too, so no big bang commit, please.
- If you have any questions, send us a message.
- When you are done, invite the user **lepaya-code-reviewer** as a contributor to the repo and then **notify us**.
- Good luck!
