# Store System

A Store System built with Electron, React, Material-UI, Redux, Redux-Saga, MySQL and Sequelize.


## Some Screens


![Login](https://github.com/steniowagner/store-system/blob/master/img/login.png)

![Cashier-Closed](https://github.com/steniowagner/store-system/blob/master/img/cashier-closed.png)

![Cashier](https://github.com/steniowagner/store-system/blob/master/img/cashier-open.png)

![Alerts](https://github.com/steniowagner/store-system/blob/master/img/alerts.png)

![Products](https://github.com/steniowagner/store-system/blob/master/img/products.png)

![Sale](https://github.com/steniowagner/store-system/blob/master/img/sale.png)

![Discount](https://github.com/steniowagner/store-system/blob/master/img/discount.png)

![Payment](https://github.com/steniowagner/store-system/blob/master/img/payment.png)

![Backup](https://github.com/steniowagner/store-system/blob/master/img/backup.png)

## About this Project


This project is part of my personal portfolio, so, I'll be happy if you could provide me any feedback about the project, code, structure or anything that you can report that could make me a better developer!




Also, you can use this Project as you wish, be for study, be for make improvements or earn money with it!



It's free!


## Functionalities


This Project supports the following operations:

- Login/Logout

- Backup (use .json format!)

- Print Receipt

- Alerts about: Customers in debit, Budgets out of date and Products with low stock.



Management of :



- Cashier

- Sales

- Products

- Stock

- Budgets

- Customers

- Providers

- Users



## Getting Started



### Prerequisites



To run this project, be either in development or production, you'll only need to have the [npm](https://www.npmjs.com/) installed and, to run the Database, you'll need the [Docker](https://www.docker.com/) installed (there's a docker-compose file in the root of the project), or the MySQL itself (if you don't want a Database, the data in the App won't be persisted).



### Installing

Cloning the Repository



**In all the followings instructions, I'll be using the yarn, but you can also use npm.**



Installing dependencies

```
$ yarn
```



### Running in Development



**Running the Database**



To start the Database as a Docker container, just perform the following command (from inside the project root directory):

```
$ docker-compose up -d
```

After to initialize the Database, run the migrations by performing the following command:



```
node_modules/.bin/sequelize db:migrate
```




**Running the App**



**OBS**: If you're using a Windows OS, make sure to edit the script "start" at package.json file to:

```
set BROWSER=nul && react-scripts start
```
And then
```
$ yarn run dev
```

## Making Changes



The Project are, basically, divided in two parts: Back-end and Front-end.



The Front-end consists of the React Components. If you need to make some changes here, just access the files inside /src folder, and all the changes will be reflected immediately in the UI.



If you want to make some change inside the Back-end, all the files are inside the /public/back-end folder. After the change, you'll need to finish the process that was started on the past section, and start it again with the news changes.



If you want create a new Table inside the Database, run the following command:



```
node_modules/.bin/sequelize migration:create --name=create-<X>
```



Where X is the Name of the new Table (might be in plural and lower case).



After, just perform the migration:



```
node_modules/.bin/sequelize db:migrate
```



If you just want to edit something inside an existing Table, run the past command after the change.



## Build



The Build consists of two steps:



First, we need to perform the build of the React:

```
$ yarn build
```



Now, we'll execute the electron build, that will point to the build folder that we made in the previous step.



```
$ yarn dist
```

This command will produce a folder called dist in the root of the project, that will have the files needed to install the App.



**OBS:** The files produced by the second command will depend on the OS that you're currently running, for example, if you're using a MAC OS, the files generated will generate a .dmg file inside the dist folder.



## Built With



* [Electron](https://electronjs.org/) - Used to build the native App

* [React](https://reactjs.org/) - Front-end Framework

* [React-Router](https://reacttraining.com/react-router/) - Router

* [Redux](https://redux.js.org/) - React State Manager

* [Redux-Saga](https://redux-saga.js.org/) - Side-Effect model for Redux

* [Material-UI](https://material-ui.com/) - CSS Framework

* [MySQL](https://www.mysql.com/) - Database

* [Sequelize](http://docs.sequelizejs.com/) - ORM





Thank you!
