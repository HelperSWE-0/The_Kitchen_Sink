<h1>7 Reliable Steps to Follow Before You Raise the Perfect Pull Request</h1>

You have built the feature and you are ready to raise a pull request (PR) / merge request. But you want to make sure that your code is of the highest standards and you do not get a ton of review comments.

This post covers key areas you can look at so that you do not get a barrage of review comments. These checks are not exhaustive, but it covers the most scenarios and your team will appreciate your code.

It will seem daunting when you try for the first time. But it becomes easier the more you do. I have also provided questions to help you review the code. This will also help you develop a keen eye to spot issues in other people’s code.

## Fulfils Requirements
Your code should meet all the requirements. Ensure you meet the bare minimum specific requirements. To go one step further, identify the impact of your code. Questions to ask –

## Does it meet all the acceptance criteria?
Is there any code which can affect the existing functionality?
Are there any hidden assumptions in the requirement specification that you are missing?
Negative Scenarios / Error Handling
You need to think about the failure scenarios. Review your code at each point where an unexpected error can happen. Common scenarios are reading / writing from a file, or receiving response from an API and the network goes down. The key questions to ask:

## Will your code break if something unexpected happens?
Have you checked all the error scenarios that can happen to your code?
Logging
You need to have sufficient logging in your code so that you can troubleshoot an issue in production. This is a tricky bit, as too much logging can affect your application performance. So you should take care to log key information that will allow you to debug a production incident.

## One example is orderId for a shopping cart application. Logging the orderId at various stages helps in seeing the order journey and thus helps in finding the exact source of failure. Key question to ask yourself:

## Will you be able to identify an issue based on the logs only?
One way to answer this question is to go through the logs and understand how the statements are appearing without looking at the code. If it is easier to understand the flow of the code through logs, then you have added enough logs.

## Clean Code
While writing code, sometimes you write just to get the code working. This can lead to unwanted comments, ambiguous variable names, or redundant code. Some IDEs give this feature out of the box and help you identify. But it still makes sense to go through it through your own eyes. Few things to watch out for:

## Are all variables have clear names?
Are there any unused variables lying around?
Can you reuse some of the code from other parts of the project, or library, saving you the effort of writing a new code?
Clean Code: A Handbook of Agile Software Craftsmanship is a must read for anyone to improve their code. It introduces you to key concepts you can use in your code every day.

##  Required Test Cases
Ensure you are writing sufficient unit test cases to cover all the scenarios. Checking the code coverage and trying to make it 100% coverage uncovers bugs.

There are some teams which do not believe in test coverage and think it is a waste of time. As application matures, these tests become the foundation on which future changes can be done.

A good test coverage with proper test names can make the code self-documenting. Good tests tell future developers the expected behaviour of the application.

It gives the future developers freedom to refactor the code without worrying about unknown conditions. Key questions to ask:

## Have you covered all the branches in your code?
Have you identified all the likely scenarios and have tests for those scenarios?
Patterns
If you have followed so far, you have your test cases available. So now you refactor your own code and make it better.

This is where patterns come in. Patterns are reusable logic that you can leverage from other people’s code. You can refer to patterns used in the team or from the ones used in external libraries.

## The advantage of using patterns is it simplifies the code and removes the probabilities of bugs in the code. Key question to ask:

- Can you replace some of your code with a pattern? For example, if there is a switch statement, can you replace is with Command pattern? What will be the benefits of doing it?
- Can you create smaller functions to make the code readable? Doing this also helps in uncovering bugs or branches that get hidden in a complex function.
-Are you following the SOLID principles?
- Have you contributed any duplicate code?

## Testing
Once you have done everything, you can to improve your code. The next step is to take a break and come back to test it. You become your code’s enemy and try to break it in every way possible. 

##Two approaches 

## Test on your own computer
Test in an integration environment with other code
Sometimes all the unit tests do not avoid an application failing to start in an integrated environment or worse, even on your laptop.

## Deploying the application in an integration environment helps you validate how the code works with all the complexities of integration.

Conclusion
## The key steps you can follow before raising your PR are:

- Check if the code fulfils requirements and meets acceptance criteria
- Check if your code handles any unknown error scenarios
- Check if there is sufficient logging so you can pinpoint any failure point without looking at the code
- Check if you have followed clean code principles.
- Check if you have written sufficient test cases to document the behaviour of your code
- Check if you can replace a piece of code with a design pattern or a library or another function already created in the codebase
- Check if you have deployed your code in an integration environment (if possible) or at least on your laptop
- The above approach would ensure your code is robust, clean and with minimal bugs possible. It would also help you become a better developer as your attention to detail will become better with practice.
