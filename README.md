# IMPORTANT
Because I added sub-repositories to deploy it to heroku and github
does not display it I created separate repositories:
- front: https://github.com/butterfly-123/fullstack-course-front
- backend: https://github.com/butterfly-123/fullstack-course-backend
- link to page: https://www.bbc.co.uk/learningenglish/english/features/6-minute-english/ep-210325

# Deploy to heroku and configuration



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
