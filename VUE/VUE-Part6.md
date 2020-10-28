# VUE - Part 6
> ## Objectives:
> 
> 1. Improve your coding skills by implementing the Login/Register/Logout mechanism
 
> ## Step 3: [User Story] Register UI setup
>     [User story] Register UI setup
>       ID:  ES-4 
>       Type: Functional     
>       Description:      
>         As a Designer of the site 
>         I want to have a Register page
>         So that the users of the site can create an account
>       Business rules:
>         A Register link will be added in the navigation bar
>         On click on the Register Link, the user will be redirected to the Register page
>         The Register page will be implemented as a component called Register
>         The Register page will follow the base layout of the site
>         The BaseLayout of the site displays 3 sections: header, content and footer
>         The header section will cover 100% of the screen with 
>         The content section will cover 100% of the screen width
>         The footer section will cover 100% of the screen with and 20% of the screen height
>         The three sections will be implemented as components (BaseLayoutHeader, BaseLayoutContent and BaseLayoutFooter). 
>         The Register page will display:
>         - The title of the page in the header section. This title must not be displated
>         - A Register form where the user can enter the following informations: firstName, lastName, email, password, password confirmation.
>         - A button called Register
>         The firstName, lastName, email, password and password confirmation fields are mandatory
>         A error message will be displayed if:
>         - Mandatory fields are not filled
>         - Passwords are not identical
>         On click on the Register button the user profile will be logged on the console  
>       Acceptance tests:  
>         A Register Link is added in the navigation bar
>         On click on the Register Link, the user is redirected to the Register page
>         The Register page follows the base layout of the site
>         The Register form displays the relevant information
>         An error message is displayed if the mandatory fields are not supplied or if password are not identical
>         On click on the Register button the profile is logged to the console.


 > ## Step 4: [User Story] Login UI setup
>     [User story] Login UI setup
>       ID:  ES-4 
>       Type: Functional     
>       Description:      
>         As a Designer of the site 
>         I want to have a Login page
>         So that the users of the site can authenticate
>       Business rules:
>         A Login link will be added in the navigation bar
>         On click on the Login Link, the user will be redirected to the Login page
>         The Login page will be implemented as a component called Login
>         The Login page will follow the base layout of the site
>         The Login page will displays
>         - The title of the page in the header section. This title must not be displayed
>         - A Login form where the user an enter the following informations: email and password.
>         - A button called Login
>         The email and passwords fields are mandatory
>         A error message will be displayed if:
>         - Mandatory fields are not filled
>         On click on the Login button the user will be logged on the console 
>       Acceptance tests:  
>         A Login Link is added in the navigation bar
>         On click on the Login Link, the user is redirected to the Login page
>         The Login page follows the base layout of the site
>         The Login form displays the relevant information
>         An error message is displayed if the mandatory fields are not supplied
>         On click on the Login button the user is logged to the console.

> ## Step 3: Setup the User API
>     [User story] User API
>       ID:  ES-X 
>       Type: Non functional     
>       Description:      
>         As a Designer of the site 
>         I want to consume an API
>         So that easily users can register, login and logout
>       Business rules:
>         The API entrypoint will be api/v0 with the follow endpoints:
>           - api/users/ (POST): Create a user profile
>           - api/users (GET) : List the user profiles
>           - api/users/:id (GET) : Read a user profile
>           - api/users/id/:id (PUT): Update a user profile
>           - api/users/:id (DELETE): Delete a user profile
>       Acceptance tests:  
>         The User API is available when the application starts
>       Notes:
>           For the sake of simplicity, the API will be a fake REST API:
>           - The API will be embedded in the Vue application
>           - The API will be implemented with JSON Server.
>           - The API will be installed in the api directory as a db.json file

## Step 4: [User Story] Register
>     [User story] Register
>       ID:  US-X 
>       Type: Functional     
>       Description:      
>         As a User of the site 
>         I want to create an account 
>         So that I can access to features protected by authentication
>       Business rules:
>         The Register mechanism will rely on the User API
>         The state will be maintained in the centralized store
>         Registration with an already existing email will be forbidden. An error message will be displayed
>         On successfull registration: 
>         - 'Logged as' and Logout sections will be added in the navigation bar
>         - Login and Register links will disappear
>         - A new user profile will be added in the fake database 
>         - The user will be considered as authenticated.
>         - The user will be redirected to the Home page
>       Acceptance tests:  
>         After successfull registration a new profile has been added in the fake database
>         A error message is displayed if the email is already existing
>         The registered user is considered as authenticated
>         'Logged as' and Logout section have been added in the navigation bar
>         Login and Register are no more present
>         The registered user is redirected to the Home page

## Step 5: [User Story] Login
>     [User story] Register
>       ID:  US-X 
>       Type: Functional     
>       Description:      
>         As a User of the site 
>         I want login 
>         So that I can access to features protected by authentication
>       Business rules:
>         The Login mechanism will rely on the User API
>         The state will be maintained in the centralized store
>         On login success: 
>         - 'Logged as' and Logout sections will be added in the navigation bar
>         - The user will be considered as authenticated.
>         - The user will be redirected to the Home page
>         On login failure:
>         - An error message will be displayed
>       Acceptance tests:  
>         A error message is displayed if the credeb
>         The registered user is considered as authenticated
>         A 'Logged as' section has been added in the navigation bar
>         The registered user is redirected to the Home page


> ## Resources
> https://fr.vuejs.org/v2/cookbook/using-axios-to-consume-apis.html
>

