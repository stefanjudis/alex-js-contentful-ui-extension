# alex-js-contentful-ui-extension
A UI extension to check for insensitive writing

A validation mechanism for insensitive language as [Contentful UI Extension](https://www.contentful.com/developers/docs/concepts/uiextensions/) using [Alex.js](http://alexjs.com/).

![figure](https://raw.githubusercontent.com/stefanjudis/alex-js-contentful-ui-extension/master/screenshot.png "Alex.js Contentful UI Extension demo")

**Important:** Unfortunately there is no Alex.js script available publicly. This is why this UI-extension uses my hosted version of it.

```html
<script src="https://www.stefanjudis.com/alex.min.js"></script>
```

I don't mind anybody else using this version but relying on me here, means that I could break you UI-extension. **You might consider hosting your own version.**

## How it works

The UI-extension is available for `Boolean` types.

![figure](https://raw.githubusercontent.com/stefanjudis/alex-js-contentful-ui-extension/master/setup.jpg "Alex.js Contentful UI Extension demo")

When installed the UI-extension will evaluate all fields of the entry it is included in with the type `Symbol` (short text) and `Text` (long text). Short text will be evaluated with `alex.text` and long text as it's mostly markdown in my case with `alex.markdown`.

I decided to not block publishing with this UI-extension because sometimes there are false-positives.

## Installation

```sh
git clone git@github.com:contentful-developer-relations/alex-js-contentful-ui-extension.git
cd alex-js-contentful-ui-extension
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

Copyright &copy; Stefan Judis

Licensed under the [MIT license](https://github.com/contentful/developer-relations/ui-country-select/blob/master/LICENSE).