# Dialogflow Fulfillment: Node.js Weather Sample

## WWO Weather API Setup
 1. Get a WWO Local Weather REST API key from https://developer.worldweatheronline.com/api/
 2. Replace <ENTER_WWO_API_KEY_HERE> with your WWO API key on line 20 of `functions/index.js`
 3. Select **Deploy**.


## Dialogflow and Fulfillment Setup
Select **only one** of three options below.

### Option 1: Add to Dialogflow (recommended)
Select [![Weather Sample](https://storage.googleapis.com/dialogflow-oneclick/deploy.svg "Weather Sample")](https://console.dialogflow.com/api-client/oneclick?templateUrl=https%3A%2F%2Fstorage.googleapis.com%2Fdialogflow-oneclick%2Fweather-agent.zip&agentName=WeatherSample) to create a new agent.

### Option 2: Dialogflow Inline Editor
1. `git clone https://github.com/dialogflow/fulfillment-weather-nodejs.git`
2. Create [Dialogflow Agent](https://console.dialogflow.com/).
3. In Dialogflow console > **Settings** ⚙ > **Restore from Zip** with `weather-agent.zip` in this Github repo.<sup>A.</sup>
4. Under Fulfillment > **Enable Inline Editor**.
5. Change the name of the function in `functions/index.js` from `dialogflowFulfillmentLibAdvancedSample` to `dialogflowFirebaseFulfillment`
6. In the **Inline editor** > copy the contents of `functions/index.js` into `index.js`.
7. Select **Deploy**.
8. In Dialogflow Console > **Settings** ⚙ > select **Google Cloud** link in Project ID section. From Google Cloud Platform > **menu** ☰ > **Enable Billing**.


  <sup>A.</sup>Note: **Restore from Zip** will overwrite any existing agent.

### Option 3: Firebase CLI
1. `git clone https://github.com/dialogflow/fulfillment-weather-nodejs.git`
2. Create [Dialogflow Agent](https://console.dialogflow.com/)
3. In Dialogflow console under **Settings** ⚙ > [Restore from Zip](https://dialogflow.com/docs/agents#export_and_import) using the `weather-agent.zip` in this Github repo<sup>A.</sup>
4. `cd` to the `functions` directory
5. Run `npm install`
6. Install the Firebase CLI with `npm install -g firebase-tools`
7. Login to your Google account with `firebase login`
8. Add your project to the sample with `firebase use [project ID]`
  + In Dialogflow console under **Settings** ⚙ > **General** tab > copy **Project ID**.
9. Run `firebase deploy --only functions:dialogflowFulfillmentLibAdvancedSample`
10. When successfully deployed, visit the **Project Console** link > **Functions** > **Dashboard**
  + Copy the link under the events column. For example: `https://us-central1-<PROJECTID>.cloudfunctions.net/<FUNCTIONNAME>`
11. Back in Dialogflow Console > **Fulfullment** > **Enable** Webhook.
12. Paste the URL from the Firebase Console’s events column into the **URL** field > **Save**.
13. In Dialogflow Console > **Settings** ⚙ > select **Google Cloud** link in Project ID section. From Google Cloud Platform > **menu** ☰ > **Enable Billing**.


## Samples

| Name                                 | Language                         |
| ------------------------------------ |:---------------------------------|
| [Fulfillment Webhook JSON](https://github.com/dialogflow/fulfillment-webhook-json)| JSON |
| [Dialogflow Console Template](https://github.com/dialogflow/fulfillment-webhook-nodejs)| Node.js
| [Bike Shop-Google Calendar API](https://github.com/dialogflow/fulfillment-bike-shop-nodejs)| Node.js|
| [WWO Weather API](https://github.com/dialogflow/fulfillment-weather-nodejs)| Node.js |
| [Alexa Importer](https://github.com/dialogflow/fulfillment-importer-nodejs) | Node.js |
| [Temperature Trivia](https://github.com/dialogflow/fulfillment-temperature-converter-nodejs) | Node.js |
| [Human-Agent](https://github.com/dialogflow/agent-human-handoff-nodejs) | Node.js |
| [Google Translation API](https://github.com/dialogflow/fulfillment-translate-python) | Python |
| [WWO Weather API](https://github.com/dialogflow/fulfillment-weather-python) | Python |

## References & Issues
* Questions? Try [StackOverflow](https://stackoverflow.com/questions/tagged/dialogflow).
* Find a bug? Report it on [GitHub](https://github.com/dialogflow/fulfillment-webhook-json/issues).
* Dialogflow [Documentation](https://dialogflow.com/docs/getting-started/basics).
* For more info on [Cloud Functions for Firebase Inline Editor](https://dialogflow.com/docs/fulfillment#cloud_functions_for_firebase).
* For more info about [billing](https://dialogflow.com/docs/concepts/google-projects-faq).

## How to make contributions?
Please read and follow the steps in the CONTRIBUTING.md.

## License
See LICENSE.md.

## Terms
Your use of this sample is subject to, and by using or downloading the sample files you agree to comply with, the [Google APIs Terms of Service](https://developers.google.com/terms/).
