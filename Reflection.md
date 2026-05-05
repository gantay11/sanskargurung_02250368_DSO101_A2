# Reflection
 What I Learned\nI learned how to set up a CI/CD pipeline using Jenkins. I understood how Jenkins can automatically run npm install, build, and test commands whenever code changes. I also learned how to write unit tests using Jest and how to connect Jenkins to a GitHub repository.

 ## Challenges I Faced
 The main challenge was installing Jenkins plugins because my internet connection was unstable. Many plugins failed to download. I also had trouble with the package.json file which had encoding errors that stopped Jest from running.
 
 ## How I Solved Them
 I manually downloaded the plugin files and installed them one by one. I also used Node.js to rewrite the package.json file correctly. For the Git branch issue, I changed the branch from master to main in Jenkins settings.

 ## What I Gained
 This assignment taught me that setting up a CI/CD pipeline requires patience and problem solving. Even when things go wrong, reading the error logs carefully helps find the solution. I now understand why CI/CD is important in real software projects.