# Dialogflow Fulfillment Weather Sample Node.js

## Setup: WWO Weather API
 1. Get a WWO API key, by going to https://developer.worldweatheronline.com/api/ and following the instructions to get an API key that includes forecasts 14 days into the future
 1. Paste your API key for the value of the `wwoApiKey`varible on line 20 of `functions/index.js`

## Setup: Dialogflow Agent
 1. Create an account on Dialogflow
 1. Create a new Dialogflow agent
 1. Restore the `dialogflow-agent.zip` ZIP file in the root of this repo
   1. Go to your agent's settings and then the *Export and Import* tab
   1. Click the *Restore from ZIP* button
   1. Select the `dialogflow-agent.zip` ZIP file in the root of this repo
   1. Type *RESTORE* and and click the *Restore* button

## Setup: Fulfillment

Choose between using Dialogflow's inline editor (recommended) or Firebase's CLI to setup fulfillment for you Dialogflow agent.  Do only one of the following:

### Option 1: Dialogflow Inline Editor (recommended)

1. [Sign up for or sign into Dialogflow](https://console.dialogflow.com/api-client/#/login)
1. Create a Dialogflow agent
1. [Enable the Cloud Function for Firebase inline editor](https://dialogflow.com/docs/fulfillment#cloud_functions_for_firebase)
1. Copy this code in `functions/index.js` the `index.js` file in the Dialogflow Cloud Function for Firebase inline editor.
1. Click `Deploy`

### Option 2: Firebase CLI

1. Create a Dialogflow agent
1. Go to your agent's settings and [Restore from zip](https://dialogflow.com/docs/agents#export_and_import) using the `advancedAgent.zip` in this directory (Note: this will overwrite your existing agent)
1. `cd` to the `functions` directory
1. Run `npm install`
1. Install the Firebase CLI by running `npm install -g firebase-tools`
1. Login to your Google account with `firebase login`
1. Add your project to the sample with `firebase use [project ID]` [find your project ID here](https://dialogflow.com/docs/agents#settings)
1. Run `firebase deploy --only functions:dialogflowFirebaseFulfillment` and make a note of the URL printed in the console upon deploy.
 1. Set the fulfillment URL in Dialogflow to your Cloud Function for Firebase URL
   1. Go to your [agent's fulfillment page](https://console.dialogflow.com/api-client/#/agent//fulfillment)
   1. Click the switch to enable webhook for your agent
   1. Enter you Cloud Function for Firebase URL (e.g. `https://central-project.cloudfunctions.net/dialogflowFirebaseFulfillment`) to the URL field
   1. Click *Save* at the bottom of the page

## References and How to report bugs
* Dialogflow documentation: [https://docs.dialogflow.com](https://docs.dialogflow.com).
* If you find any issues, please open a bug on [GitHub](https://github.com/dialogflow/dialogflow-fulfillment-nodejs/issues).
* Questions are answered on [StackOverflow](https://stackoverflow.com/questions/tagged/dialogflow).

## How to make contributions?
Please read and follow the steps in the CONTRIBUTING.md.

## License
See LICENSE.md.

## Terms
Your use of this sample is subject to, and by using or downloading the sample files you agree to comply with, the [Google APIs Terms of Service](https://developers.google.com/terms/).