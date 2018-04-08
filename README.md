# how to build a custom skill for amazon echo dot
[This](https://developer.amazon.com/de/alexa-skills-kit/alexa-skill-quick-start-tutorial) tutorial explains it is however outdated.

## Build the backend using python AWS LAMBDA
Login to [aws](https://eu-west-1.console.aws.amazon.com/lambda/home?region=eu-west-1#/functions/myColorSkill?tab=graph) using account number: xxxxxxx and user: xxxxx.

Then under AWS services search for `lambda`. 
1. Choose location `ireland` (since skills in Europe can only be hosted here). 
2. Choose create function and choose `blueprints` and look for `alexa` and the following `alexa-skills-kit-color-expert-python ` pops-up in the search results. Choose it. 
3. Enter the Name as `myColorSkill`.
4. disable authentification. 
4. Then create custom role. IAM console open and click on allow. Which populates the role as lambda_basic_execution.
5. Copy the arn from [here](https://eu-west-1.console.aws.amazon.com/lambda/home?region=eu-west-1#/functions/myColorSkill?tab=graph) for later use in the skills definition


## Build the language model
Next login to <https://developer.amazon.com/>. Go to <https://developer.amazon.com/alexa/console/ask> and `create skill`.  

Follow the instructions above, use a lower case `color picker`, but use the `nlu.json` instead.
Do not forget to enter the ARN from the first section under endpoint.
At the very end do not forget to `SAVE MODEL` and `BUILD MODEL`.


## The alexa app frontend
The new skill should now appear under <https://alexa.amazon.de/spa/index.html#skills/?ref-suffix=nav_nav>.