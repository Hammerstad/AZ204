This folder contains the first azure function i ever made!
I'm following https://docs.microsoft.com/en-us/learn/modules/create-serverless-logic-with-azure-functions/4-creating-and-executing-an-azure-function

It's a http trigger.

Push this by executing the following command

```
func azure functionapp publish totallyunique
```

Where totallyunique is my totally unique global name for my azure functions app.

Call the app:

`http://totallyunique.azurewebsites.net/api/myhttptrigger?code=vCwv5ID7pghZc8GgiXqipY9zl7dUjaiCLl4LgS4Xifh5jUn6pEiPfw==&name=Eirik!`

The webpage should say "Hello Eirik!"
\o/