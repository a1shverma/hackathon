#Foodify

##Demo Video on YouTube



##Objective: 
The goal of our app is to track nutritional content of what you consume with a simple snap of your food item. The app processes the image of a food item, retrieves nutritional content and also suggests recipes based on your daily calorie limit goal.

##Code Organization

We started with a [GitHub Organization] to organize our code. We had separate repositories for our *Backend API* and *Android App*. We have utilized Github efficiently as our VCS by creating branches and set up a webhook to Heroku to automatically deploy new builds whenever new code is pushed.

**Tech Stack**: We used Python (Flask) for our API, Parse for the user database and Android for the mobile app. We have used CloudSight and NutritionX API and Spoonacular API. On the Android app, one of our main goals was to accomplish a low bandwidth connection to our server. Cameras on mobile device these days are capable of reproducing high quality photos measuring up to 6 MB in size. By using a simple Bitmap scaling down mechanism, we were able to reduce the size to around 200 kB, thus allowing users to use our app on low bandwidth connections like 2G. 

**User Flow**:
We built our core API on Flask(Python) and hosted it on Heroku. The image is sent as multipart data from Android App as a POST request to /upload endpoint which calls CloudSIght API to retrieve food item name and then NutritionX API is called to retrieve relevant nutritional data of that item. The daily calorie limit is set at the time of signup, and this is deducted every time a new food item is added. Using Spoonacular API we get a list of recommended recipes which are within bounds of daily calorie limit.

**Documentation**: We have properly documented our API endpoints for reference to other people. It is available [here](https://anypoint.mulesoft.com/apiplatform/rhnvrm/#/portals/organizations/ba699460-af7b-4192-b37f-7e7d635c9a8a/apis/62058/versions/64448)

**Future Work**: Our aim is to integrate social features into this app, provide leaderboards, share healthy food items a user recommends to his/her followers. We will include some data insights on user's food consumption and give him/her suggestions on what to consume to achieve his goal, provide visualizations, build a streak for providing an incentive to the user for eating healthy. We have already built our core API so porting this app to other platforms like iOS, web won't be much difficult. 



2. Build android source code or use the apk provided and run app.

3. Take photo of the food product from the app and wait for it to be processed.

4. Voila.
