# Dialogflow Fulfillment Weather Sample Node.js

## Setup: WWO Weather API
 1. Get a WWO API key, by going to https://developer.worldweatheronline.com/api/ and following the instructions to get an API key that includes forecasts 14 days into the future
 1. Paste your API key for the value of the `wwoApiKey`varible on line 20 of `functions/index.js`

## Setup: Dialogflow and fulfillment
Choose one of the three options listed below for setup.  You only need to complete one of the three options below to setup this sample.

### Option 1: Add to Dialogflow (recommended)
Click on the **Add to Dialogflow** button below and follow the prompts to create a new agent:

[![Weather Sample](https://storage.googleapis.com/dialogflow-oneclick/deploy.svg "Weather Sample")](https://console.dialogflow.com/api-client/oneclick?templateUrl=https%3A%2F%2Fstorage.googleapis.com%2Fdialogflow-oneclick%2Fweather-agent.zip&agentName=WeatherSample)

### Option 2: Dialogflow Inline Editor
1. Create a Dialogflow agent
1. Go to your agent's settings and [Restore from zip](https://dialogflow.com/docs/agents#export_and_import) using the `weather-agent.zip` in this directory (Note: this will overwrite your existing agent)
1. [Sign up for or sign into Dialogflow](https://console.dialogflow.com/api-client/#/login)
1. [Enable the Cloud Function for Firebase inline editor](https://dialogflow.com/docs/fulfillment#cloud_functions_for_firebase)
1. Change the name of the function in `functions/index.js` from `dialogflowFulfillmentLibAdvancedSample` to `dialogflowFirebaseFulfillment`
1. Copy the code in `functions/index.js` to the `index.js` file in the Dialogflow Cloud Function for Firebase inline editor.
1. Copy the code in `functions/package.json` to the `package.json` file in the Dialogflow Cloud Function for Firebase inline editor.
1. Click `Deploy`

### Option 3: Firebase CLI
1. Create a Dialogflow agent
1. Go to your agent's settings and [Restore from zip](https://dialogflow.com/docs/agents#export_and_import) using the `weather-agent.zip` in this directory (Note: this will overwrite your existing agent)
1. `cd` to the `functions` directory
1. Run `npm install`
1. Install the Firebase CLI by running `npm install -g firebase-tools`
1. Login to your Google account with `firebase login`
1. Add your project to the sample with `firebase use [project ID]` [find your project ID here](https://dialogflow.com/docs/agents#settings)
1. Run `firebase deploy --only functions:dialogflowFulfillmentLibAdvancedSample`
1. Paste the URL into your Dialogflow agent's fulfillment

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
