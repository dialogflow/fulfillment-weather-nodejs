# Dialogflow Fulfillment: Node.js Weather Sample

## Dialogflow and Fulfillment Setup
Select **only one** of the options below.

### Option 1: Add to Dialogflow (Recommended)
To create this agent from our template:

<a href="https://console.dialogflow.com/api-client/oneclick?templateUrl=https://oneclickgithub.appspot.com/dialogflow/fulfillment-weather-nodejs&agentName=WeatherSample" target="blank">
  <img src="https://dialogflow.com/images/deploy.png">
</a>

1. Get a WWO Local Weather REST API key from https://developer.worldweatheronline.com/api/
2. Replace <ENTER_WWO_API_KEY_HERE> with your WWO API key on line 20 of `functions/index.js`
3. Select **Deploy**.
4. In Dialogflow Console > **Settings** ⚙ > select **Google Cloud** link in Project ID section. From Google Cloud Platform > **menu** ☰ > **Enable Billing**.

### Option 2: Firebase CLI
1. Create a [Dialogflow Agent](https://console.dialogflow.com/)
2. `git clone https://github.com/dialogflow/fulfillment-weather-nodejs.git`
3. In Dialogflow console under **Settings** ⚙ > [Restore from Zip](https://dialogflow.com/docs/agents#export_and_import) using the `weather-agent.zip` in this directory.
4. Get a WWO Local Weather REST API key from https://developer.worldweatheronline.com/api/
5. Replace <ENTER_WWO_API_KEY_HERE> with your WWO API key on line 20 of `functions/index.js`
6. `cd` to the `functions` directory
7. Run `npm install`
8. Install the Firebase CLI with `npm install -g firebase-tools`
9. Login to your Google account with `firebase login`
10. Add your project to the sample with `firebase use [project ID]`
      + In Dialogflow console under **Settings** ⚙ > **General** tab > copy **Project ID**.
11. Run `firebase deploy --only functions:dialogflowFulfillmentLibAdvancedSample`
12. When successfully deployed, visit the **Project Console** link > **Functions** > **Dashboard**
      + Copy the link under the events column.
      + For example: `https://us-central1-<PROJECTID>.cloudfunctions.net/<FUNCTIONNAME>`
13. Back in Dialogflow Console > **Fulfullment** > **Enable** Webhook.
14. Paste the URL from the Firebase Console’s events column into the **URL** field > **Save**.
15. In Dialogflow Console > **Settings** ⚙ > select **Google Cloud** link in Project ID section. From Google Cloud Platform > **menu** ☰ > **Enable Billing**.


## Related Samples

| Name       | Language           |
| ------------- |:-------------:|
| [Fulfillment & Regex Validation](https://github.com/dialogflow/fulfillment-regex-nodejs)      | Node.js |
| [Weather: Fulfillment & WWO API](https://github.com/dialogflow/fulfillment-weather-nodejs)     | Node.js      |  
| [Bike Shop: Fulfillment & Google Calendar API](https://github.com/dialogflow/fulfillment-bike-shop-nodejs)| Node.js |
| [Temperature Trivia: Fulfillment & Actions on Google](https://github.com/dialogflow/fulfillment-temperature-converter-nodejs) | Node.js |
| [Fulfillment & Actions on Google](https://github.com/dialogflow/fulfillment-actions-library-nodejs) | Node.js |
| [Fulfillment & Firestore Database](https://github.com/dialogflow/fulfillment-firestore-nodejs) | Node.js |
| [Multi-language/locale](https://github.com/dialogflow/fulfillment-multi-locale-nodejs) | Node.js |
| [Basic Slot Filling](https://github.com/dialogflow/fulfillment-slot-filling-nodejs) | Node.js |
| [Alexa Importer](https://github.com/dialogflow/fulfillment-importer-nodejs) | Node.js |

For Fulfillment Webhook [JSON Requests & Responses](https://github.com/dialogflow/fulfillment-webhook-json).

## References & Issues
+ Questions? Try [StackOverflow](https://stackoverflow.com/questions/tagged/dialogflow) or [Dialogflow Developer Community](https://plus.google.com/communities/103318168784860581977).
+ For bugs, please report an issue on [Github](https://github.com/dialogflow/dialogflow-fulfillment-nodejs/issues).
+ Dialogflow [Documentation](https://docs.dialogflow.com).
+ Dialogflow [Classes Reference Doc](https://github.com/dialogflow/dialogflow-fulfillment-nodejs/tree/master/docs).
+ For more info about [billing](https://dialogflow.com/docs/concepts/google-projects-faq).

## Make Contributions
Please read and follow the steps in the CONTRIBUTING.md.

## License
See LICENSE.md.

## Terms
Your use of this sample is subject to, and by using or downloading the sample files you agree to comply with, the [Google APIs Terms of Service](https://developers.google.com/terms/).
