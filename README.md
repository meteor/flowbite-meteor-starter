This is a [Meteor.js](https://meteor.com/) project.

Live demo: [flowbit-meteor-starter.meteorapp.com](https://flowbit-meteor-starter.meteorapp.com/)

It also includes:

- [x] [`flowbite`](https://flowbite.com)
- [x] [`flowbite-react`](https://flowbite-react.com)
- [x] [`react-icons`](https://react-icons.github.io/react-icons)
- [x] [`tailwindcss`](https://tailwindcss.com)
- [x] Quality of life tools, like
  - [x] [`eslint`](https://eslint.org) with some plugins
  - [x] [`prettier`](https://prettier.io)

## Getting started

`Meteor.js` requires [`Node.js`](https://nodejs.org).

If you don't already have `npm` available, make sure you set them up.

Install the dependencies:

```bash
meteor npm install
```

Now you can run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `imports/ui/App.tsx`. The page auto-updates as you edit the file.

## Add `flowbite-react` to `meteor` on your own

Follow these steps to add `flowbite-react` to a `meteor` project without cloning this repo.

### Requirements

- [x] [Node.js](https://nodejs.org/en/)
- [x] [Meteor.js CLI](https://docs.meteor.com/install.html)

### How-to

#### Create a new `meteor` starter project:

```sh
meteor create flowbite-app --tailwind      
cd flowbite-app
```
This will create a new `meteor` project with `tailwindcss` support.

#### Install `flowbite` and `flowbite-react`:

```sh
meteor npm install --save flowbite flowbite-react
```

#### Edit your `tailwind.config.js`:

```js
module.exports = {
  content: [
    "./imports/ui/**/*.{js,jsx,ts,tsx}",
    "./client/*.html",
    "node_modules/flowbite-react/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [require("flowbite/plugin")],
};

```

#### Start using `flowbite-react`!

```js
import { Alert } from "flowbite-react";

export default function MyPage() {
  return <Alert color="info">Alert!</Alert>;
}
```

## Learn more

### About `meteor`

To learn more about Meteor.js, take a look at the following resources:

- [Meteor.js Documentation](https://docs.meteor.com) - learn about Next.js features and API.

You can check out [the Meteor.js GitHub repository](https://github.com/meteor/meteor/) - your feedback and contributions are welcome!

### About `flowbite`

[Flowbite](https://flowbite.com) is an open source collection of UI components built with the utility classes from Tailwind CSS that you can use as a starting point when coding user interfaces and websites.

In this repository, we setup [`flowbite-react`](https://flowbite-react.com) for you with examples of how to use the React components in `pages/index.tsx`.

## Deploy on `meteor-cloud`

The easiest way to deploy your Meteor.js app is to use the [Meteor Cloud Platform](https://meteor.com/cloud) from the creators of Meteor.js.

Check out our [Meteor.js deployment documentation](https://galaxy-guide.meteor.com/deploy-to-galaxy.html) for more details.