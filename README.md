# The Alexa greeter
This Alexa skill will say 'hello' to you and call you by name should you choose to reveal it :)

This repo contains the `voice-interface` directory, which holds the configuration needed to register the Alexa skill with Amazon, and it contains the `src` directory which has the actual source code that will essentially be the API that Alexa will be hitting to her responses.

### Installation
If you want to set this up with Amazon, register and configure your Skill with Amazon using the intents and utterances from the `voice-interface` directory, then add the files from the `src` directory to an AWS Lambda function. Below explains some steps on how to do that.
1. Create an Amazon Developer account here: https://developer.amazon.com.
2. Go to the Alexa tab and chose to get started on the "Alexa Skills Kit".
3. Click "Add a New Skill", and you will begin to be taken through some steps where you will name and configure this new Alexa skill.
4. On part 2 (Interaction Model), you'll paste the contents of `voice-interface/intent-schema.json` into the Intent Schema text area, and the `voice-interface/sample-utterances.txt` in the Sample Utterances text area. Also click "Add Slot Type" to add some random domains as the values, and LIST_OF_DOMAINS as the "Type". (This corresponds to the "type" in the intent schema)
5. Once you get to the "Configuration" step, you'll need to upload `src` files to a lambda function and add it's ARN here.

And that's it! You can now test sending some voice commands to your skill in the Test section.

More detailed information about setting up an Alexa skill can be found here:s https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/overviews/steps-to-build-a-custom-skill
