# DEPLOYING APP USING "HEROKU"

#### Some important points before deploying:    
1.  **package.json** should have all dependencies (Heroku will install all the packages as soon as we connect to their server)     
2.  Setup up your Heroku first    
3.  Initialize a "Start Script"     
   -> Open package.json    
   -> Inside "scripts"  Type **"start" : "node app.js"**        
4. In app.js change the listening port 3000 to the listening port of heroku    
**Listening port of heroku:**    
const PORT = process.env.PORT || 3000;    
app.listen(PORT, () => {    
console.log("Server has started");
 });

## Setting up HEROKU
###### Steps for terminal (GoormIDE here):
1. Make sure you are in the right directory    
2. Heroku is already pre installed in GoormIDE (If not using GoormIDE or Cloud9 download the correct version from heroku docs)    
3. #**heroku login -i**  and give your details    
It should display an "**Authentication Successful**" message 

## DEPLOYING
1. Login into heroku using    
#**heroku login -i**   
2. Open the correct directory    
#**git init**   
#**git add app.js** (Also add other files like this or directly use **git add .** to add all files)    
#**git commit -m "Initial Commit"**    
3. #**heroku create**    
4. #**git remote -v** (This will check whether the git remote has been add to heroku servers or not)    
5. #**git push heroku master** will push each and every code we added on git
--------------------
-> To view errors use #**heroku logs**    
-> You can always visit https://www.heroku.com/ to change domain name, add some add-ons, temporarily pause or delete the website

# Adding custom domain

