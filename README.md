# alex-js-contentful-ui-extension
A UI extension to check for insensitive writing

A validation mechanism for insensitive language as [Contentful UI Extension](https://www.contentful.com/developers/docs/concepts/uiextensions/) using [Alex.js](http://alexjs.com/).

![figure](https://raw.githubusercontent.com/stefanjudis/alex-js-contentful-ui-extension/master/demo.jpg "Alex.js Contentful UI Extension demo")

## Installation

```sh
git clone git@github.com:contentful-developer-relations/ui-country-select.git
cd ui-country-select
npm install
```

### Configure

Create a configuration file with your credentials for Contentful.

```sh
cp env.example .env
```

Open `.env` in a editor of your liking and add your Contentful space ID, and management token. [Learn how to obtain a token](https://www.contentful.com/developers/docs/references/authentication/#getting-an-oauth-token).

Load environment variables

```sh
source .env
```

### Create

```sh
npm run create
```

Create task will register the extension in your space on Contentful.

### Update

```sh
npm run update
```

Update task will upload the extension to your space on Contentful.

## License

Copyright &copy; Contentful Developer Relations

Licensed under the [MIT license](https://github.com/contentful/developer-relations/ui-country-select/blob/master/LICENSE).