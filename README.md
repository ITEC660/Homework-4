# Homework 4

Run the app that you had created last week (**homework 3)** on the Heroku platform.

1. Sign up on Heroku
    1. [https://signup.heroku.com/](https://signup.heroku.com/)
        1. Check and confirm account creation inside your email
2. Go to the “Getting Started on Heroku” page
    1. [https://devcenter.heroku.com/start](https://devcenter.heroku.com/start)
    2. Click on the Node.js
    3. You should have already installed Node.js and npm in previous weeks
    4. If not, please install them
        1. **Package.json** file should be under the webapp directory to be located at the root of your app, not in a subfolder. (npm init)
3. Click on the button “**I’m ready to start**”
4. Download and install Heroku CLI
    1. Note that it requires Git.
5. Open your terminal (i.e visual studio code) and type “**heroku login**” command
    1. This command will open “**Log in to the Heroku CLI**” and click on “**Log in**”
    2. Click the heroku webpage (dashboard) and go back your terminal
    3. If It ask you to login to your heroku account
    4. Sign in on the browser if it asks
    5. Accept terms below the page and you will be directed to dashboard (https://dashboard.heroku.com/apps)
    6. Now you’re ready to create your first Heroku app. In this step, you will prepare a sample application that’s ready to be deployed to Heroku.
    7. Click on “**Create New App**” on Heroku
6. Check node.js, npm versions, and if git is installed, as instructed in the document
7. We will not use the Heroku sample application, skip that and continue below
8. Update your “**webapp.js**” code with running your node.js terminal such as “**Visual Studio Code**”
    1. Change the line of **app.listen(8002)**; =====> **app.listen(process.env.PORT)**;

//so Heroku can assign any available port

1. Add a new file to your “**webapp**” repository,
    1. Create the file named “**Procfile**” with no extensions in the filename (don't use .txt, .js etc.) and you will see the **heroku** icon in your code console.
    2. Content of the file should have the following one lineweb: node webapp.js
2. Start git commands
    1. git init
        1. Initializes the repository
    2. git add .
        1. Adds all files
    3. git commit -m “first commit”
        1. Adds a comment for the first version
        2. If you received “unable to auto-detect email address”
            1. Search google and apply the solution
    4. git log
        1. Shows changes
3. Run the following command
    1. **heroku create** or Go Heroku web page and create an app
    2. Note your link. It will be something like:
        1. [https://thawing-inlet-61413.herokuapp.com/](https://thawing-inlet-61413.herokuapp.com/)
        2. run **heroku git:remote -a <heroku-app-name>**
4. Run **git push heroku master**
    1. Takes a couple of minutes to be updated.
    2. Viola! You have your app running on the web!!! Go heroku and open your app.
5. If there are any problems check “heroku logs”, that might help.
    1. For example: If you see “npm ERR! missing script: start”
        1. Try: [https://stackoverflow.com/questions/34631300/why-do-i-obtain-this-error-when-deploying-app-to-heroku](https://stackoverflow.com/questions/34631300/why-do-i-obtain-this-error-when-deploying-app-to-heroku)
    2. Write how you have solved problems in your code.
