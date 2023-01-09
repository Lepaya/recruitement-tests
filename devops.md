# Cloud DevOps Engineer Assignment

Please carefully read the following observations, and complete the assignments listed at the bottom. If you find the provided information unclear, or lacking details, try to make assumptions, and note them with your answer.
If you are completely blocked, you can email your questions to sabrina.kreitz@lepaya.com. 

Best of luck!

## The Task

- Create a CSV file in a S3 bucket with some random emails.
- Create a script that reads this file and synchronizes it with a database. So when the file changes, the changes are reflected in the database. 
- Assume the data is highly sensitive.
- The script should run as a cron job or as a lambda function every hour.
- You have to use Terraform, but feel free to choose any AWS service, programming language, and database you want.
- Create a pipeline to run your terraform code.
- Assume at least 2 environments: stating and production.

## Acceptance Criteria
- The solution works as expected.
- Your design is clean and simple.
- Documentation is easy to understand by someone unfamiliar with this challenge.
- Your solution is secure.

## Bonuses
Using GitHub Actions for CI/CD pipeline is a Plus.

## How to deliver this test

- Create a private repository on Github and push your code to it. Remember, we will be evaluating your commit messages too, so no big bang commit, please.
- If you have any questions, send us a message.
- When you are done, invite the user **lepaya-code-reviewer** as a contributor to the repo and then notify us.

Good luck!
