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
