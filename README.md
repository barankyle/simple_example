# Simple example of integration to GitHub, Stripe, and Twilio

## How to use:
1. Create a BitScoop account and add these GitHub, Stripe, and Twilio API Maps.

These example maps are stripped down to simplify their functionality and have test API keys already added to them.

GitHub Quick Add:

[![Add to BitScoop](https://assets.bitscoop.com/github/AddBitScoopXSmall.png)](https://bitscoop.com/maps/create?source=https://raw.githubusercontent.com/bitscooplabs/simple_example/master/maps/github.json)

Twilio Quick Add:

[![Add to BitScoop](https://assets.bitscoop.com/github/AddBitScoopXSmall.png)](https://bitscoop.com/maps/create?source=https://raw.githubusercontent.com/bitscooplabs/simple_example/master/maps/twilio.json)

Stripe Quick Add:

[![Add to BitScoop](https://assets.bitscoop.com/github/AddBitScoopXSmall.png)](https://bitscoop.com/maps/create?source=https://raw.githubusercontent.com/bitscooplabs/simple_example/master/maps/stripe.json)

2. Create a BitScoop API Key in and add the key string to the project to the config file.

3. Create a connection to the GitHub API on behalf of a user to get their data.

Call this endpoint to create a connection. Insert the API map ID into the URL. This is found in the BitScoop web interface.

~~~
curl -X POST \
  https://api.bitscoop.com/{{insert_bitscoop_api_map_id}}/connections \
  -H 'authorization: Bearer {{insert_bitscoop_api_key}}' \
  -H 'content-type: application/json'
~~~

Go to the URL in the response and authorize access on behalf of a user.

Paste the ID of the Connection into the project config file.

This is to simulate a 3-legged connection. More info here: https://bitscoop.com/learn/connections

4. Run the app.
~~~
yarn install
node app.js
~~~
