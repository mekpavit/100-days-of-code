# 100 Days Of Code - Log

### Day 1: Jan 7, 2020

**Today's Progress**: Add first unit test for the app

**Thoughts**: Runing unit test on JavaScript is harder than I thought. When using `import` (I think it's babel syntax), there must be a babel/jest configuration before be able to run the test against `import`. Next time, look [here](https://jestjs.io/docs/en/getting-started) at Babel section.

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 2: Jan 8, 2020

**Today's Progress**: Add E2E test but remove it because of misunderstanding of LINE Messaging API -> Zero progress

**Thoughts**: The mechanism of webhook for LINE chatbot is totally different from Dialogflow. For Dialogflow, it sends the HTTP request to the webhook; And the webhook needs to response to that request, in order to answer the user. But for LINE, it sends the HTTP request to the webhook and only hopes for 200 status; but webhook needs to send a a separate HTTP request to LINE endpoint in order to answer the user! This mechanism, somehow, make E2E test much harder. For Dialogflow, we can just send a mock HTTP request to our webhook and assert the response; but for LINE, we cannot simply do this... Tomorrow, I will focus on the unit test instead!

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 3: Jan 9, 2020

**Today's Progress**: Start using TypeScript. Finally add first E2E test! Add some magic babel plugins got from StackOverflow that fixes bug and help starting up the test

**Thoughts**: TypeScript is very interesting. It introduces type strict which I really like in Python to JavaScript world. It should help writing JavaScript to be much cleaner. Somehow, I still struggle with TypeScript, Babel and plain JavaScript. I've just could not understand why we need to do so many things just to use TypeScript. Today, I've add 3 Babel preset/plugins without knowing what they do (But somehow, it solves the problem, which is very annoying!!!!). So, I will read more about TypeScript and Babel! Another thing, the way I did the E2E testing was still very tricky and untidy. Hoping that I could find a better way by reading the Art of Unit Testing!

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 4: Jan 11, 2020

**Today's Progress**: Use jest.mock to mock LINE lib dependency. Rewrite and add E2E test for all features.

**Thoughts**: Refering to what I said yesterday about the new way to perform E2E testing, finally, I found the way to do the E2E testing for this app. Instead of using an abstact class, I used mock feature in Jest which is very powerful. From now, I will always use Jest when writing JavaScript app! For the next days, I will try to pass all E2E tests first before refactoring the code; Because in the previous project, I had to delete and write many unit tests because I over-designed the app before writing the code, and had to change the design because the previous one was not working. BTW, today I had a satisified progress! Can't wait for tomorrow.

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 5: Jan 12, 2020

**Today's Progress**: Finish 1st week of Princeton's Algorithms course on Coursera!

**Thoughts**: Today I switched from doing the project to doing the assignment from Algorithms course! This assignment is about Dynamic Connectivity problem which is solved by Union and Find operation. The assignment is very interesting! I have to write a Monte Carlo simulation to solve the percolation problem. This is my first time writing Java application after my freshman at the university. It was a bit hard to switch from very easy language like Python and JavaScript but I finally did it! The only thing I feel a bit annoying is that; It is very hard to set up Test Suite for Java! I'd tried to set it up for about 1 hour and then gave up. So, I hope I can write the Java unit test using JUnit before I finish the course!

**Link to work**: [My Assignments Repo](https://github.com/mekpavit/coursera-princeton-algorithms)

### Day 6: Jan 13, 2020

**Today's Progress**: Add mongodb to the app but it's still incomplete.

**Thoughts**: Trying to use jest-mongodb might be the worst thing for the beginner. Tomorrow I will use the normal mongodb first to test whether or not everything is working and then moving to jest-mongodb for test. Typescript + JavaScript + Babel is so confuse!!!!

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 7: Jan 14, 2020

**Today's Progress**: Try to fix mongodb, did not work.

**Thoughts**: This time, I switched from in-mermory mongo to the real one. The problem seems to be the wrong usage of async and await things. So, I changed from async-await to normal callback. Everything seemed to work as expected, except one thing... The result in mongodb was inconsistant! Sometimes it's worked, sometimes it's not. Hope to find out why this happened tomorrow.

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 8: Jan 15, 2020

**Today's Progress**: Finally fixed all async part! Passed all tests!

**Thoughts**: Simple is the best! After trying on async/await which I don't fully understand how it works, this time, I was focusing on simple plain callback instead! Although the callback is very ugly (callback hell), but it is very simple and easy to understand! Next time after I master the callback approach, I will come back for async/await. My plan for tomorrow is to test the app with real LINE account; And if it works, I will try to write unit test and refactor those database-calling method into ORM-like object.

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 9: Jan 16, 2020

**Today's Progress**: Cleared unnecessary files and packages. Tested with LINE application and it worked!

**Thoughts**: Removing all babel and typescript to make the code clean as much as I can is a good thing to do. Now, the code contains only thing that I fully understand! Tomorrow will set up production Mongodb and deploy the code to Google Cloud Run. If I have time, I plan to add CI/CD to the github repository as well; But let's see first. Lastly, I will add image memorizing and recalling feature and that will be the end of SaveIt project!

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)
