## Installation Instructions

- Clone the repository from GitHub
- Open a terminal in the repository directory and type `docker-compose up`
- The docker container with Gravitee installed should now be running

## Testing Instructions

- Open a browser and enter `localhost:8084` - this should open the Gravitee Management dashboard
- On the left-hand side navigate to APIs, click + Add Api, and then Continue in the wizard
- Create a name, version and description for your API (these can be anything) and then add a path of `/test` in Context-path. Click next after this is complete
- In the Backend field, enter `https://api.gravitee.io/echo` and click Next
- In this section add a Name and Description, and for Security Type use Keyless (public), click Next, and then click Skip in the next section
- Click CREATE AND START THE API, and then in the next section click PUBLISH THE API, then PUBLISH
- The API should now be live. Open a new tab in your browser and type `localhost:8082/test`
- You should be able to visualise returned JSON data from `https://api.gravitee.io/echo` - this indicates that the route is running correctly
