# IMPORTANT
Because I added sub-repositories to deploy it to heroku and github
does not display it I created separate repositories:
- front: https://github.com/butterfly-123/fullstack-course-front
- backend: https://github.com/butterfly-123/fullstack-course-backend
- link to page: https://dragon-fullstack-front.herokuapp.com/login

# Deploy to heroku and configuration
**Heroku** - allows developers to quickly and almost painlessly deploy an application on a web server. It also provides a lot of plugins that you can integrate into your application.

1. Create the project.
2. Create a new repository in version control system (GitHub).
3. Link the repository with Heroku.
At this step, we can link the repository from Github to our Heroku application.
* First, create a new application on Heroku.
![image](https://user-images.githubusercontent.com/58802893/112967853-fc83c180-914b-11eb-9e68-e0397b2a301e.png)

* Once the application has been created, a window similar to this should appear.
![image](https://user-images.githubusercontent.com/58802893/112967957-17563600-914c-11eb-85ae-da7c07c3aad8.png)

* Now, if you look at the navigation at the top, you'll see  Overview, Resources, Deploy, Metrics  and so on. Be sure that Deploy is selected. Then on the second row, click on the GitHub icon.
![image](https://user-images.githubusercontent.com/58802893/112968115-410f5d00-914c-11eb-9a1c-168f4aca2f38.png)

Search for the desired application, which is demo-deploy-app-09 in our case. Then click Connect.
* Once the application is successfully connected with your Heroku account, you can click Deploy Branch to deploy your application.
![image](https://user-images.githubusercontent.com/58802893/112969754-d7904e00-914d-11eb-9d88-1d2cfb5dd0a0.png)

If you want, you can also select the option Enable Automatic Deploys which will automatically pull the code from your Github repository every time you make a push to that repository.
* Once the application has been deployed, you can click on View to open your application.
![image](https://user-images.githubusercontent.com/58802893/112969873-f393ef80-914d-11eb-9197-89f1db8d44ad.png)

4. Configure Heroku to properly run the application.
If you open the application at this point, you should see something like this:
![image](https://user-images.githubusercontent.com/58802893/113265434-6cbd4f00-92d4-11eb-9dad-e64a4659621b.png)

To solve this problem, we must create a new file named Procfile with the following content: web: node ./app.js.

To update our application, all we need to do is push a new commit to GitHub. If we have enabled the Automatic Deploys option, then the code will be automatically pulled to Heroku. Otherwise we need to click on Deploy Branch again.

Once the application is rebuilt, we should see it working like so:
![image](https://user-images.githubusercontent.com/58802893/113265617-a5f5bf00-92d4-11eb-8421-6477ce85f3a4.png)

5. How to add an add-on.
Let's see how to add a new resource to your project. First, we'll go to Resources, and from there we'll add a new tool for testing.

Go ahead and click on Find more add-ons and then search for Loadmill.
![image](https://user-images.githubusercontent.com/58802893/113265861-e6edd380-92d4-11eb-9521-359386e7843d.png)

Then choose the application you want to link.
![image](https://user-images.githubusercontent.com/58802893/113266054-156bae80-92d5-11eb-8e45-f57bae8c2bae.png)

Heroku will automatically create a new account for you on the provisioned platform.

On the resources tab, you can see the newly added resource:
![image](https://user-images.githubusercontent.com/58802893/113266170-3af8b800-92d5-11eb-9d99-68a8e6203542.png)

If you go ahead and access this add-on, you should see its dashboard with an intro tutorial and a demo test created for you.
![image](https://user-images.githubusercontent.com/58802893/113266196-464be380-92d5-11eb-903a-26dc6157f5bd.png)

# How to start a project?
 1. You create a folder in the terminal (**mkdir** 'name')
 2. In this folder you create another folder (**mkdir** 'name')
 3. You can adding `README.md` as needed
 4. You install `npm init` in the terminal - this will create a package.json 
 5. Next you install `npm and nodemon@1.17.5 --save-dev`
 6. In package.json, you change calling from
 `"test": "echo \" Error: no test specified \ "&& exit 1"`
 on
 `"start": "node.",
 "dev": "nodemon."`
 7. Now You can run these commands in the terminal: `npm run start` and `npm run dev`

### Node
**Node** - is an environment that runs Javascript code. Meaning _it takes files full of javascript syntax and then executes that code_.

> Our backing is a machine that will be running a server that can supply information this back in is going
> to be implemented in Node.js.

#### Benefit from Node.js
1. We can make the code more consistent and quicker to understand.
2. Vast number of resources relating to node that inhabit the wild world.

> When would you like see, what is in `index.js`, you can in the terminal call the command `node index.js` 

### What that mean `constructor() {}`?
The **constructor** is actually named pretty well in my opinion because in this function we set the properties of an instance of the class.

### What that mean `setTimeout(() => {});`?
The **setTimeout** is placing a given object at a _certain_ time.

### Hints:
* Keep track of the current generation using `this.generation` in the class.
   
* A `newGeneration` method could come in handy. This would make a generation object, setting it to `this.generation`.
   
* Consider using `setTimeout` to schedule calls to `newGeneration` in a timely manner.
   
* Recursion may come in handy (be careful to avoid infinite loops).

### Express
**Express** (framework within Node.js to create a webserver and API) - is designed for building web applications and APIs. It has been called the de facto standard server framework for Node.js.

### Api
* Set of related functions 

Web API is a set of functions that one entity exposes to allow other entities to interact with it over the web.
* Web API exposes interaction from one entity to other
* HTTP (Hypertext Transfer Protocol)
It's the basis of communication over the internet. 

It's the basis of communication over the internet:
1. Get
2. Post
3. Put
4. Delite

#### Relation **Database**
* Database that structures data in _relation_ to other data
* A table stores data about a particular data element
* Tables consist of rows nd columns  

#### **PostgreSQL**
* SQL is a language used to communicate with data 
* is a language, PostgreSQL is the system
* Other relation system: MySQL, SQLite, Oracle DB, and more

#### JavaScript **Promises**
* The guaranteed future of an eventual value
* The completion or failure of an asynchronous operation 
* Enfore order and coordinate asynchronous behavior 
 
1. Function that accept the callback 
2. Wraps around **resolve** (the promise return an err) **reject** functions
3. Handlers:
* **.then** handler, with callback to handle resolve value
* **.catch** handler, with a callback to handle err value

#####Resolve:

Asynchronous functionality has succeeded. Return value. 

#####For exapmle:
```
const examplePromise = new Promise((resolve, reject) => {
    const success = true;

    if (success) {
        resolve({ message: 'woohoo' });      
    } else {
        reject({ message: 'oh no...' });
    }
});
```
```
examplePromise
    .then(({ message }) => console.log('message', message))
    .catch(error => console.log('err', error));
```
> The order in which the arguments are listed is very **important**:
```
app.use((err, req, res, next) => {
    const statusCode = err.statusCode || 500;

    res.status(statusCode).json({
        type: 'error', message: err.message
    })
});
```
> 1. err
> 2. req
> 3. res
> 4. next

### Same-Origin Policy
* Enforces script execution occurs only with the same origin
* Prevents malicious script from different origin

### Redux (A state container for JavaScript applications)
* Store and unidirectional flow
* Actions: object with a unique type and contain data
* Reducers to split up a store and describe updates

#### Store
* Manages the state data of the _entire_ applications
* Single source of truth
* Unidirectional flow for data 

#### Actions 
* Primary act like data types
* Object with a type field that is globally unique
* Contain arbitrary payloads of data

#### Reduces 

* Describe sections of the store
* They respond of different types of actions, and update their specific section of the store as a result  

#### Browser Cookies
* Store key/value pairs on the browser
* Data that exists across connections to an app
* The server sets a 'Set-Cookies' response header to store a cookie on the client's behalf

### Get and Set 
Get - gets a value
Set - assign a value
For example:
```
// Create an object:
var person = {
  firstName: "John",
  lastName : "Doe",
  language : "en",
  get lang() {
    return this.language;
  }
};

var person = {
  firstName: "John",
  lastName : "Doe",
  language : "",
  set lang(lang) {
    this.language = lang;
  }
};

// Set an object property using a setter:
person.lang = "en";
```
```
// The get keyword will bind an object property to a function. When this property is looked up now the getter function is called. The return value of the getter function then determines which property is returned.
var person = {
  firstName: "John",
  lastName : "Doe",
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

var person = {
  firstName: "John",
  lastName : "Doe",
  get fullName() {
    return this.firstName + " " + this.lastName;
  }
};
```

**To create a link to a subpage you can use:**
```
import { Router, Switch, Route } from 'react-router-dom';
import createBrowserHistory from 'history/createBrowserHistory';

const history = createBrowserHistory();

render(
    <Provider store={store}>
        <Router history={history}>
            <Switch>
                <Route exact path='/' component={Root} />
                <Route path='/page' component={Page}/>
            </Switch>
        </Router>
    </Provider>,
    document.getElementById('root')
)
```

### Example
You have:
```
return new Dragon( {...dragon, dragonId, dragonTrait})
```
That mean:
```
 const dragon = {nickname: 1, traits: [2,3]};
 const dragonId = 4;
 const dragonTrait = 'trala';

 const result = {...dragon, dragonId, dragonTrait};
```

 How it will **look** like:
 ```
 const result = {
     nickname: 1, 
     traits: [2,3],
     dragonId: 4,
     dragonTrait: 'trala'
};
```

If you want to install the library you can use two ways:
1. You enter the name of this library in `package.json` and in the terminal you enter `npm i`
2. In the terminal you enter `npm i (and libraryName)` plus `--save`

### How state works  
1. You can make state in Component
```
state = {
    account: 0
}
```
2. Evoke this state
```
<b>STATE IN COMPONENT: {this.state.counter}</b>
```
3. Transfer function that changes state
```
<button
    onClick={this.counterUp.bind(this)}
> + </button>
```
or
```
<button onClick={() => this.counterUp()}> + </button>
```
4. Write a function
```
counterUp() {
    this.setState({counter: this.state.counter + 1})
}
```

### How Redux works
1. You make state in Redux Component
```
const initState = {
    counter: 0
}

const account = (state = initState, action) => {
    switch (action.type) {
        case 'COUNTER_UP':
            return {
                counter: state.counter + 1
            };
        case 'COUNTER_DOWN':
            return {
                counter: state.counter - 1
            };
        default:
            return state;
    }
};

export default account;
```
2. You make action in Redux Component
```
export const counterUp = () => dispatch => {
    dispatch({ type: 'COUNTER_UP' });
}
export const counterUp = () => dispatch => {
    dispatch({ type: 'COUNTER_DOWN' });
}
```
3. Evoke this state
```
<b>STATE IN COMPONENT: {this.props.counter.counter}</b>
```
4. Transfer function that changes Redux state
```
<button onClick={() => this.props.counterUp()}> + </button>
```
or 
```
<button onClick={() => this.props.counterUp()}> + </button>

counterUp() {
    if (this.props.counter.counter) {
        this.props.counter.counterUp()
    }   
}
```
