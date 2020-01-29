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

### Day 10: Jan 17, 2020

**Today's Progress**: Add Dockerfile and test application on production database (MongoDB Atlas)

**Thoughts**: Today I tried to deploy the webhook to serverless docker container service (Google Cloud Run), but it requires the docker image to be only on Google Container Registry! To push the image to GCR, it might incur a cost which is opposite of my goal on this project (Deploy only to free service!). After falling from Cloud Run, I took a look on other serverless containers (AWS, Azure), but none of them are free T_T. So, I will find other solution for deploy this webhook to production!

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 11: Jan 18, 2020

**Today's Progress**: Finish first part of second week assignment on Coursera Princeton's Algorithms course.

**Thoughts**: The second week of this course focuses more on the elementary data structure/algorithm which are stack, queue and sorting. So, the assignment might not be exciting as much as the percolation problem from the previous week. But the good thing is that, I've learn a lot about Java from this week (Generic type, Iterator). I like how Java implements very strict type approach of coding which is, in my opinion, a very good way of coding since the code will be more scalable and maintainable (The later developer can know almost every details on the class/method due to the strict type!). I hope I can finish this assignment within tomorrow. So, I can continue the SaveIt project!

**Link to work**: [My Assignments Repo](https://github.com/mekpavit/coursera-princeton-algorithms)

### Day 12: Jan 19, 2020

**Today's Progress**: Finish second week assignment on Coursera Princeton's Algorithms course.

**Thoughts**: Unit test is very powerful! Compare to the first week which does not have the actual unit test, this week assignment passed the auto-grader in much less time! Looking forward to practice my TDD in all the project that is coming!

**Link to work**: [My Assignments Repo](https://github.com/mekpavit/coursera-princeton-algorithms)

### Day 13: Jan 20, 2020

**Today's Progress**: Change shuffle algorithm to be inplaced (Algorithms course). Implement and deploy firebase function to SaveIt.

**Thoughts**: After watching shuffling lesson on Coursera, I started to realize that; Even the simple algorithm like shuffling, it has some mathematic in it that need to be cared! For example, some shuffle algorithm might not result in an uniform shulffling! Very interesting to learn all of these. About the SaveIt project, today I deployed to Firebase which was easy because I can just add one more line to the code and it will be available to be deployed by Firebase CLI. But the lesson learn is that 1. Enviroment variable implementation in Firebase function is suck!!!! I need to use its library just to get the enviroment variable! which make the code coupled to the Firebase platform. It would be better if I can use process.env just like normal deployment. 2. Spark plan on Firebase does not let the application connect to external services!!!! which mean that, I might to use Firebase realtime db instead of Mongodb.

**Link to work**: [My Assignments Repo](https://github.com/mekpavit/coursera-princeton-algorithms) [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 14: Jan 21, 2020

**Today's Progress**: Fix the issue in the Dialogflow-Integration server and [pull request](https://github.com/GoogleCloudPlatform/dialogflow-integrations/pull/5) to the original repo.

**Thoughts**: This in my first time of doing the pull request on the public repository! Very exciting to contribute something back to the community (even it is not merged to the repo, still worth it!). I also read about the Firestore (NoSQL) which I will uses instead of MongoDB because the Spark plan on the Firestore does not allow connecting to the external service. I will make this change and deploy tomorrow!

**Link to work**: [Dialogflow-Integration Server](https://github.com/mekpavit/dialogflow-integrations/tree/fix/query-parameter-payload)

### Day 15: Jan 22, 2020

**Today's Progress**: Read JavaScript Promise. Read how to effectively write the Firebase functions.

**Thoughts**: After deeply studying on Firebase ecosystem, I found that it is the most complete ecosystem I have ever seen! Firebase function provide its own unit testing implementation. The Firestore online testing mode is also provided with the exmaple! Therefore, I think I will dedicate a new Github repo for the saveit-webhook-firebase to learn about Firebase ecosystem and pause the current github repo as it is (Common Express app with Mongodb).
**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 16: Jan 23, 2020

**Today's Progress**: Deploy to Cloud Run.

**Thoughts**: Change plan! I switched from Firebase function to Cloud Run because I feel that it would be part of Firebase platform someday. With Cloud Run, I can write tests like normal app which is very crucial for me because I want to practice more TDD!!! Tomorrow will add image memorizing feature to SaveIt. Also, it seems like the SaveIt cannot process multiple requests in the same time (forward 5+ messages from other chat to SaveIt). I will try to fix it tomorrow!
**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 17: Jan 25, 2020

**Today's Progress**: Complete Coursera Algorithms course's third-week assignment.

**Thoughts**: If you have bad test samples, the code will be properly tested! In this week assignment, I was too lazy to mock a good test sample! The consequence is that, my code passed that bad test but not passed the course test! After creating a better test sample, everything was much easier! So, next time, I will spend time to write a good test sample!
**Link to work**: [My Assignments Repo](https://github.com/mekpavit/coursera-princeton-algorithms)

### Day 18: Jan 26, 2020

**Today's Progress**: Fix bug that the bot could only handle 2 messages from users when they forwarding 2 or more messages to the bot. Test getting the user's image from LINE server (getContent API)

**Thoughts**: When 2 or more messages are sent to the bot in the same time (ex. messages from forwarding), the request body will contain more than one event. At first, I thought that LINE will send each request for each message sent and wrote the code to only handle the first event in the request body! This make the bot unable to handle more than 2 messages. After fixing and testing, now, the bot is working as expected! Next step is finding a way to work with Cloud Storage, so the bot can store the images from users!
**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 19: Jan 27, 2020

**Today's Progress**: Zero progress!

**Thoughts**: Today I researched about how to upload binary file (recieved from LINE getMessageContent API) to Google Cloud Storage. The approach I think I will try is 1. Store binary file in tmp file using [tmp](https://www.npmjs.com/package/tmp) lib (in order to get file path) 2. Use google-cloud@storage lib to upload tmp file using tmp file path 3. When needs to publish the file in the bucket to the user, use getSignedUrl and send the url to the user. After implementing this method, I will start refactor the code using TypeScript!

EDIT: Just found out that the File object of google-cloud@storage is writable object. So, we can use file.createWriteStream or file.save to directly upload binary object to it! [ref](https://github.com/googleapis/google-cloud-node/issues/2334)

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)

### Day 20: Jan 28, 2020

**Today's Progress**: Implement cloud storage.

**Thoughts**: After understanding readable and writable object in fs library, hanlding file in NodeJS is easy! Luckily, I have some knowledge about cloud storage from Python project at work, so, the hard part is only dealing with file. Tomorrow will make the bot able to deal with image file and implement TypeScript!

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)


### Day 21: Jan 29, 2020

**Today's Progress**: Re-write the code using TypeScript, in progress.

**Thoughts**: Now, the POC state is ended. It's time to write a good code! After writing some Java during Algorithms class, the coding style learnt Java somehow make me better at writing the TypeScript. The unit testing concept descibed in the book, "the Art of Unit Testing", like Stub, Mock and perforimg dependency injection, will be used here in SaveIt-Webhook! For SaveItClient, I decided to inject dependencies via constructor because SaveIt-Webhook will need the client to declare the details of its dependencies which will give a flexible for SaveIt-Webhook to use with any platform, database and storage servicec!

**Link to work**: [SaveIt-Webhook](https://github.com/mekpavit/saveit-webhook)
