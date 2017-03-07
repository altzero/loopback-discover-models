

<h3>A simple CLI tool to discover and write new model.json and model.js files by using loopback's datasource.discoverSchema API</h3>

<h3>Install</h3>

    $ npm install adamlutz/loopback-discover-models --save

<h3>Usage</h3>
```
./node_modules/.bin/loopback-discover-models -h
Usage:
  loopback-discover-models [OPTIONS] [ARGS]

Options:
      --serverPath [PATH]Path to server.js (relative to CWD). (Default is /server/server.js)
      --modelConfigPath [PATH]Path to model-config.json (relative to CWD). (Default is /server/model-config.json)
      --modelDir [PATH]  Path to models folder (relative to CWD). (Default is /common/models)
      --dataSource [STRING]Name of the data source from data sources.json (required). (Default is db)
      --allNewModels [BOOLEAN]Discover and create all models not in modelDir. (Default is false)
      --modelName STRING Name of a single model/table/collection to create.
      --owner STRING     Name of owner/schema/database for the models.
      --relations [BOOLEAN]Include relations. (Default is false)
      --allOwners [BOOLEAN]Include All Owners. (Default is false)
      --views [BOOLEAN]  Include views. (Default is false)
      --skip STRING      Comma seperate model names to skip when discovering new models.
  -h, --help             Display help and usage details
  ```

<h5>Generate Models for all tables in the database that don't already exist as models.</h5>
```
./node_modules/.bin/loopback-discover-models --allNewModels
```

<h5>generate new models, but skip the tables 'migrations' and 'some_other_table'</h5>
```
./node_modules/.bin/loopback-discover-models --allNewModels --skip migrations,some_other_table
```

<h5>Generate new models and put them in a different folder</h5>
```
./node_modules/.bin/loopback-discover-models --allNewModels --modelDir /server/models
```

<h5>Use prompts instead of cli flags (good for use with npm run).</h5>
```
./node_modules/.bin/loopback-discover-models --prompt
```

<h5>Generate Model for a specific table/collectiom (modelName should be the table/collection name).</h5>
```
./node_modules/.bin/loopback-discover-models --modelName some_table
```

<h5>Generate Model for a specific table/collectiom (modelName should be the table/collection name).</h5>
```
./node_modules/.bin/loopback-discover-models --modelName some_table
```
