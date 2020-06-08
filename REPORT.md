# OAuth Comparative Analysis
## OAuth Provider Name : Auth0
### Research Conducted By: 
- Batool Al-Ali
- Anolla Haddad
- Yousef Al-Shen
### Overall Score and Comments
#### Score (Out of 10): 10
#### General Comments
This research provide a full-stack applacation using a mock database. It for learn about  Integrate **Auth0** OAuth into the authentication system to provide a way for users to easily signup and signin to our system.
#### Pros
* Get the required data like Domain, Client ID, Client Secret, etc.
#### Cons
* There is alot of URL like callbackURL, login URI, direct URI, so we got confused what to use.
* Most resourses use Passport and it's not allowed so we it will be better if we used passport.
### Ratings and Reviews
#### Documentation
- We do search in the **Auth0** documentation, first we want to know what is **Auth0**?
  Auth0 is a flexible, drop-in solution to add authentication and authorization services to your applications.
  You can connect any application to Auth0 and define the identity providers you want to use.
  You built an awesome app and you want to add user authentication and authorization. Your users should be able to log in either with username/password or with their social accounts (such as Facebook or Twitter). You want to retrieve the user's profile after the login so you can customize the UI and apply your authorization policies.
- How to Integrate **Auth0** into the authentication system?
    1. First you have to login into the **Auth0** to add your APP and get the required data such as Domain, Client ID, Client Secret, etc.
    2. Then you have to get the authUrl to get the user *code* Example:
    ```javaScript
    {
  "user_code":"WDJB-MJHT",
  }
    }
    ```
    3.  When we get the user code we exchange Code For Token to get access-token by POST this header 
    ```javaScript
    {
    { grant_type: 'authorization_code',
     client_id: 'CLIENT_ID',
     client_secret: 'CLIENT_SECRET',
     code: 'AUTHORIZATION_CODE',
     redirect_uri: 'https://127.0.0.1:3000/authorize' }
    }
    ```
    4. After Getting access-token we use it to get userinfo
#### Systems Requirements 
- .env with CLIENT_ID, PORT, DOMAIN and CLIENT_SECRET.
- npm i base-64 bcryptjs cors debug dotenv express jsonwebtoken morgan superagent
#### Ramp-Up Projections   ///////**************************************/////
How long would/should it take a team of mid-junior developers to become productive?
#### Community Support and Adoption levels ///////**************************************/////
How popular is this framework? What big companies are running on it? How is it "seen" in the general JS community?  Is there an active community of developers supporting and growing it?
### Links and Resources
* [framework](http://xyz.com)   ///////**************************************/////
* [docs](http://xyz.com)        ///////**************************************/////
* [GET/ Redirect uri](https://auth0.com/docs/universal-login)
* [POST/ exchange an Authorization Code for a Token Token](https://auth0.com/docs/api/authentication#authorization-code-flow45)
* [GET /User profile](https://auth0.com/docs/api/authentication#get-user-info)
### Code Demos  ///////**************************************/////
* [live/running application](http://xyz.com)
* [code repository](http://xyz.com)
### Operating Instructions   ///////**************************************/////
* `npm start`
* Endpoint: `/authorize`
  * Returns a atoken
* Endpoint: `/bing/zing/`
  * Returns a JSON object with xyz in it.