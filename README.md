# JSON REST Server Template

A simple JSON REST server template for development using [typicode/json-server](https://github.com/typicode/json-server) to provide a REST API to data stored in a JSON file.

> Note: This template uses Yarn Plug'n'Play feature to get rid of `node_modules`, but you can still use npm if you prefer.

## Getting started

Use [degit](https://github.com/Rich-Harris/degit) to install this template. Instead of cloning whole repositories with all their history, degit allows you to download a specific commit from a repository located on GitHub, GitLab or BitBucket. By default, it will fetch the latest commit from a GitHub repository master branch, but there are options for fetching specific tags and commits. Please see the degit README for more information. Also, contrary to `git clone`, it does not create a `.git` directory. It is especially useful for scaffolding a new app from a template.

_You will need [NodeJs](https://nodejs.org/en/) v8+ to use it._

You can install `degit` globally or use npx to install this template._.

```bash
# if degit is installed globally
degit laplix/json-rest-server-template your-app-name
# or with npx
npx degit laplix/json-rest-server your-app-name
# then install the dependencies
cd your-app-name
yarn
```

Ajust the scrpts dev tag in the package.json file to point to your JSON data file (db.json in this example).

```json
{
  "scripts": {
    "dev": "json-server ./db.json"
  }
}
```

 `json-server` runs on port 3000 by default. If needed, you can specify another port (4000 in this example):

```json
{
  "scripts": {
    "dev": "json-server -p 4000 ./db.json",
  }
}
```

Start your dev server with the `yarn dev` (or `npm run dev`) command in your terminal.

Navigate to [http://localhost:3000](http://localhost:3000). You should be able to query and mutate your data using the REST interface.

> Please note that json-serve runs in memory. This means that if you add, modify or delete data, it will not be written to your JSON data file. You can save a snapshot of your data by typing `s + enter` in your terminal.

## License

json-rest-server-template is licemsed under the [MIT License](LICENCE.md).
