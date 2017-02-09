# aws_hello_alexa

#Simple Hello World Amazon Alexa Skill

Creating an Alexa Hello World skill requires an Amazon Developer Account and An Amazon AWS account.

Next write the functionality of the skill. This is the code you write that will interact with the Alexa service.

In this case, write a simple ```myFunc.js ``` in Sublime Text:

```
exports.handler = function( event, context ) {

    var say = "Hello World";

    var response = {
        outputSpeech: {
            type: "SSML",
            ssml: "<speak>" + say + "</speak>"
        },
        shouldEndSession: true
    };


    context.succeed( { response: response } );

};
```

This func should go to the lambda function in aws.
![alt text](./img/aws_lambda.png "AWS Lambda")
