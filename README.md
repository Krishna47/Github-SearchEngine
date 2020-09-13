# GitHub Search Engine 

GitHub Search Engine is a User Interface that displays all repositories owned by a particular user in GitHub. This UI offers a search bar where search can be done by providing User's name in the box and internally calls GitHub V4 API to retrieve list of repos. 
 

## How to Find it: 

Visit the below URL to access the UI and check for list of repositories.

```bash
URL : https://s3.tezuka.com/search-engine/github-repos
```

## Features:

1. GitHub Search Engine UI is a React based application and offers dark mode for the users. Internally React Hooks were leveraged to apply the themes. 
2. This application uses GraphQL- a query language for connecting to GitHub v4 API by leveraging Query type to pull required data fields like Repository Name, Description and URL,  based on github-user name as login parameter passed to the Query type.

## GraphQL: 

GraphQL can be used in place of REST API calls; Comparing with REST, Query type operates like GET requests, while Mutations type operate like POST/PATCH/DELETE. 

The GraphQL API v4 has a single endpoint:

```bash
https://api.github.com/graphql
```


 In GraphQL,a JSON-encoded body should be provided for performing a query or a mutation, so the HTTP verb is POST.
To query GraphQL using cURL, make a POST request with a JSON payload. The payload must contain a string called query:

```bash
curl -H "Authorization: bearer token" -X POST -d " \
 { \
   \"query\": \"query { viewer { login }}\" \
 } \
" https://api.github.com/graphql
```

GraphQL allows users to pass parameter values dynamically by using variables. 

Variables can make queries more dynamic and powerful, and they can reduce complexity when passing mutation input objects.



## Versions of libraries and softwares used:

Test libraries : Jest Framework for Unit testing

React: 

GraphQL:

ApolloClient


## Running Tests:

We need to add react-test-renderer for rendering snapshots.

```bash
1.  yarn add --dev react-test-renderer
```
2. Run yarn test to run tests with Jest.




## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
