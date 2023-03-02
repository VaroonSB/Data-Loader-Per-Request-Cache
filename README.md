# Data-Loader-Per-Request-Cache
Data Loader used in graphql to avoid n+1 problem. Cache won't be persisted across the queries as new instance of data loader is created for each request.

## Steps: 
- Clone the repo.
- Install packages -> `npm i`
- Start the application -> `npm run start`

### Sample query:
```
query Jobs {
  jobs {
    id
    title
    company {
      id
      jobs {
        id
        description
      }
    }
  }
}
```
