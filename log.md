# 100 Days Of Code - Log

### Day 1: Jan 7, 2020

**Today's Progress**: Add first unit test for the app

**Thoughts**: Runing unit test on JavaScript is harder than I thought. When using `import` (I think it's babel syntax), there must be a babel/jest configuration before be able to run the test against `import`. Next time, look [here](https://jestjs.io/docs/en/getting-started) at Babel section.

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 2: Jan 8, 2020

**Today's Progress**: Add E2E test but remove it because of misunderstanding of LINE Messaging API -> Zero progress

**Thoughts**: The mechanism of webhook for LINE chatbot is totally different from Dialogflow. For Dialogflow, it sends the HTTP request to the webhook; And the webhook needs to response to that request, in order to answer the user. But for LINE, it sends the HTTP request to the webhook and only hopes for 200 status; but webhook needs to send a a separate HTTP request to LINE endpoint in order to answer the user! This mechanism, somehow, make E2E test much harder. For Dialogflow, we can just send a mock HTTP request to our webhook and assert the response; but for LINE, we cannot simply do this... Tomorrow, I will focus on the unit test instead!


**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)
