# bug-reporting

The purpose of this repository is to provide the code necessary to allow the user to submit bug reports when using the Sustain Frontend services. 

## How to Use:

1. Copy BugAlert.js and BugReport into the project. 
2. Create a file called bugSubmitAuth.js and provide it with a github access token (this is standardized for Sustain services, so don't use a personal one). 
    - General form for code inside bugSubmitAuth.js:
      export const auth = 'github_access_token'
        
3. Add bugSubmitAuth.js to .gitignore file. If the access token is found in a commit it will become unusable. 
4. Create the necessary state for setAlert, add imports, and ensure that the request is being sent to the correct github repository (specified in BugReport.js).
5. add: 
   - `<BugReport setAlert={setAlert} />`
   - `<BugAlert alert={alert} setAlert={setAlert} />`
