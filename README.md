# WebDSL Docker for grading WPL assignments

## Setup

Copy the source code of the WebDSL application to `webdsl/`. This contains the main app file, the *.app file that starts with `application`.

Copy the source code of the React application to `react/`. This assumes `react/package.json` includes `"proxy":"http://localhost:8080"`. If there is no `react/` folder, only the WebDSL application is deployed.

## Running the app

```bash
./run.sh <name-of-main-app-file>
# Example for webdsl/mytodolist.app: ./run.sh mytodolist
```

After the Docker image is built and the container has started, the WebDSL app should be available at `http://localhost:8080/<name-of-main-app-file>`, and the React app at `http://localhost:3000`. Emails that are sent from the WebDSL application can be viewed at `http://localhost:8025`.
