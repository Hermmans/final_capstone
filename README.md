# Figma design and Planning

The figma design was designed by Hermmans Orejuela
Down below is a link on how it was supposed to look like. The design was made with mobile first. The idea that you start with your mobile design and expand from there.
https://www.figma.com/file/UfyArGAuZcWvHRkuO2dpol/Prep-%3EMeals-web-app-draft

Below is a little preview on it as well:
https://www.figma.com/proto/UfyArGAuZcWvHRkuO2dpol/Prep-%3EMeals-web-app-draft?node-id=18%3A98&starting-point-node-id=18%3A98

Due to time constraints we couldn't have the project do everything we wish it had, but despite that this project demonstrates collaborative work as well a fully functional full stack application that involves Javascript, React, Redux, html, css for the frontend. For the Backend we have Java, SQL, and Springs. 

Our database design was done using lucid
https://lucid.app/lucidchart/d9bbfd0a-f0a1-4361-b753-196f38877074/edit?invitationId=inv_3ae72632-6cd5-4ab4-8511-345a8242a742&referringApp=slack&page=0_0#

To do this project we used slack and zoom for video and messaging each other, google docs and sheets for planning and presenting, figma for design and proto-typing, and trello for our agile process. 
## Project setup

The first thing you'll need to do is to download any dependencies by running this command:

```
npm install
```


Your React frontend communicates with this API endpoint to authenticate and register users.

The last thing to do is start the back-end application before you work on the front-end application. Start your application with the following command:

```
npm start
```

## Authentication

When you first run the project and visit the base URL, you're taken to a login page. This is because the home route `/` is secured by default. If you look in `/src/Components/Main/Main.js`, you'll see the following code:

```
<Switch>
    <Route path='/login' component={() => <Login/>}/>
    <Route path='/register'component={() => <Register/>}/>
    <Route path='/home' component={this.props.token.token !== undefined ? () => <Home/> : null}/>
    <Redirect to='/login'/>
</Switch>
```

The line that reads `<Redirect to='/login'/>` tells the Router to navigate to the `/login` path by default and the other `<Route/>` tags tell you which components will be loaded depending on the `to`

path variable. If you look at the `<Route/>` component with the path `/home` you'll see the component has a condition `this.props.token.token !== undefined`. This is to ensure that the home component

is only loaded if the user is authorized.

## TO LOGIN 
we have user and admin, 
both have a password set to password.
