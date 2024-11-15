Steps To run/host this server on your machine:-

Install these dependecies on your pc:-
  npm install axios cors dotenv
  npm install @octokit/rest
  npm install session-file-store --save server side

To Host this server create a render account, click on new->web service and connect this github repo to the render acc. 
In the server settings change the Build command to "npm install" and the start command to "node server.js"

In the Environemental Tab set the following environmental variables:-

CLIENT_URL= your vercel app url (ex:-https://job-ui-six.vercel.app)
GITHUB_ACCESS_TOKEN = your github access token (To generate your personal access token in github head to settings --> developer settings --> Personal Acess Token --> Tokens(classic) --> and create a new token by providing a name and giving full access to read and write into the repo)
GITHUB_CALLBACK_URL = your_vercel_app_url/auth/github/callback (ex:- https://job-ui-six.vercel.app/auth/github/callback)
GITHUB_CLIENT_ID = your github client id (To generate your client id in github head to settings --> developer settings --> OAuth Apps  --> create a new app with a app name --> for the homepage url provide your vercel app url {ex:- https://job-ui-six.vercel.app/ } and set the callback url as your_vercel_app_url/auth/github/callback {ex:- https://job-ui-six.vercel.app/auth/github/callback } )
GITHUB_CLIENT_SECRET = your client secrete (To generate your client id in github head to settings --> developer settings --> OAuth Apps --> select the app you created and click on generate client secrete )
GITHUB_REPO_NAME = your github repo name
GITHUB_REPO_OWNER = your github account name
JWT_SECRET = (you can generate your jwt secrete locally on your pc by running this command:- node -e "console.log(require('crypto').randomBytes(64).toString('hex'))" . Copy the generate secrete code)
NODE_ENV = production
PORT = 3001
SESSION_SECRET = (you can generate your session secrete locally on your pc by running this command:- node -e "console.log(require('crypto').randomBytes(64).toString('hex'))" . Copy the generate secrete code)
Now you can deploy the server.

Note:- copy the server url after deploying the server. You can find the url of your server right below the name of your server. Here is an sample url on how your server url would be :- https://job-ui-server.onrender.com
