---
title: "React Libraries for 2023"
description: "A comprehensive list of all React libraries used in 2023. If you are new to React, its ecosystem of libraries may be overwhelming. However, all these React libraries offer everything you need to build large scale applications with React ..."
date: "2023-02-21T08:50:46+02:00"
categories: ["React"]
keywords: ["react libraries 2023"]
hashtags: ["#ReactJs"]
banner: "./images/banner.jpg"
contribute: ""
author: ""
---

<Sponsorship />

React has been around for a while. Since then, a well-rounded yet overwhelming ecosystem of libraries evolved around the component driven library. Developers coming from other programming languages or libraries/frameworks often have a hard time figuring out **all the libraries for creating web applications with React**.

At its core, React enables one to create component-driven user interfaces with [function components](/react-function-component/). It comes with a couple of built-in solutions though, for instance, [React Hooks](/react-hooks/) for local state, side-effects, and performance optimizations. But after all, you are only dealing with functions (components and hooks) to create a UI here.

The following article will give you guidance on **how to choose libraries for building a React application**.

# Table of Contents

<TableOfContents {...props} />

# How to create a React project

There is this unknown for every React beginner on how to set up a React project when joining the React world. There are many frameworks to choose from. The most popular choice in the React community is [Vite](https://vitejs.dev/) which allows you to create projects with various library (e.g. React) + opt-in TypeScript combinations. It comes with [incredible performance](https://twitter.com/rwieruch/status/1491093471490412547).

<ReadMore label="Learn why frameworks like React matter" link="/why-frameworks-matter/" />

If you are already familiar with React, you can choose one of its most popular (meta) frameworks as alternative: [Next.js](https://nextjs.org/) which builds up on top of React, hence you should already be familiar with [React's fundamentals](https://www.roadtoreact.com/). Another popular yet newer framework in this arena is [Remix](https://remix.run/).

<ReadMore label="Learn more about websites and web applications" link="/web-applications/" />

While Next.js has been initially used for server-side rendering (web applications), it can also be used for static site generation (e.g. websites). However, if you are looking for a framework with the best performance in mind for static content, you need to check out [Astro](https://astro.build/) which is framework agnostic and therefore can be used with React.

<ReadMore label="How to create a modern JavaScript project" link="/javascript-project-setup-tutorial/" />

If you just want to understand how tools like Vite work under the hood, try to [set up a React project](/minimal-react-webpack-babel-setup/) yourself. You will start with a bare bones HTML with JavaScript project and add React with its supportive tools (e.g. Webpack, Babel) yourself. It's not something you will have to deal with in your day to day work, but it's a great learning experience to get to know the underlying tooling.

**Recommendations:**

* Vite for client-side React applications
* Next.js server-side rendered React applications
* Astro for static-side generated React applications
* optional learning experience: [create a React project](/minimal-react-webpack-babel-setup/)

# Package Manager for React

The default and most widely used package manager in the JavaScript ecosystem (and therefore React) is [npm](https://www.npmjs.com/) (which comes with a Node.js installation). When installing dependencies (read: libraries) in a React application, you will usually use it. However, for the last years [yarn](https://yarnpkg.com/) has been a successful alternative. Last but not least, [pnpm](https://pnpm.io/) is the newest kid on the block which comes with a great performance boost.

<ReadMore label="Installing a Package Manager" link="/mac-setup-web-development/" />

If you happen to create multiple React applications which depend on each other or which share a common set of custom UI components, you may want to check out the concept of a [monorepo](/javascript-monorepos/). All previously mentioned package managers allow you to create monorepos by using their in-house workspaces feature, however, I had the best developer experience using yarn/pnpm. In combination with monorepo pipeline tools such as [Turborepo](https://turborepo.org/) the monorepo experience becomes perfect.

**Recommendations:**

* choose one package manager and stick to it
  * default and most widely used -> npm
* if monorepo, check out Turborepo

# React State Management

React comes with two built-in hooks to manage local state: [useState](/react-usestate-hook) and [useReducer](/react-usereducer-hook/). If state needs to be managed globally, one can opt-in [React's built-in useContext Hook](/react-usecontext-hook/) to tunnel props from top-level components to components below them without using [props](/react-pass-props-to-component/) and therefore avoiding the problem of props drilling.

<ReadMore label="Learn when to use useState and useReducer" link="/react-usereducer-vs-usestate/" />

All three React hooks enable developers to implement powerful state management in React which is either co-located in components by using React's useState/useReducer Hooks or globally managed by combining them with React's useContext Hook.

<ReadMore label="Learn how to combine useState/useReducer with useContext" link="/react-state-usereducer-usestate-usecontext/" />

If you find yourself using React's Context too often for shared/global state, you should definitely check out [Redux](https://redux.js.org/) as the most popular state management library out there. It allows you to manage global application state which can be read and modified by any React component that is connected to its global store.

<ReadMore label="Learn Redux" link="/react-redux-tutorial/" />

If you happen to use Redux, you should definitely check out [Redux Toolkit](https://redux-toolkit.js.org/) as well. It improves the developer experience of using Redux tremendously by being a great API on top of Redux's core.

As alternatives, if you like the general idea of a global store but do not like how Redux approaches it, check out other popular local state management solutions such as [Zustand](https://github.com/pmndrs/zustand), [Recoil](https://github.com/facebookexperimental/Recoil), [XState](https://github.com/statelyai/xstate), or [Jotai](https://github.com/pmndrs/jotai).

**Recommendations:**

* useState/useReducer for co-located or shared state
* opt-in useContext for enabling *little* global state
  * optional learning experience: learn how to combine useState/useReducer with useContext
* Redux (or an alternative) for *lots of* global state

# React Data Fetching

React's built-in hooks are great for UI state, but when it comes to state management of remote data (and therefore data fetching), I would recommend using a dedicated data fetching library such as [TanStack Query](https://tanstack.com/query) (formerly React Query). While TanStack Query itself is not seen as a state management library, because it is primarily used to fetch your remote data from APIs, it takes care of all the state management (e.g. caching, optimistic updates) of this remote data for you.

<ReadMore label="Learn how TanStack Query works under the hood" link="/react-hooks-fetch-data/" />

TanStack Query was designed for consuming [REST APIs](/node-express-server-rest-api/). However, these days it supports [GraphQL](https://www.roadtographql.com/) too. But if you are looking for a dedicated GraphQL library for your React frontend, check out either [Apollo Client](https://www.apollographql.com/docs/react/) (popular), [urql](https://formidable.com/open-source/urql/) (lightweight), or [Relay](https://github.com/facebook/relay) (by Facebook).

<ReadMore label="Everything about State in React for Local and Remote Data" link="/react-state/" />

If you are already using Redux and want to add data fetching with integrated state management in Redux, instead of adding TanStack Query, you may want to check out [RTK Query](https://redux-toolkit.js.org/rtk-query/overview) which integrates data fetching neatly into Redux.

Last but not least, check out [tRPC](https://trpc.io/) for end-to-end type typesafe APIs if you are in control of your TypeScript written backend.

**Recommendations:**

* TanStack Query (REST APIs, GraphQL APIs)
  * with axios as fetching library
* Apollo Client (GraphQL APIs)
* optional learning experience: learn how TanStack Query works under the hood

# Routing with React Router

If you are using a React framework like Next.js, routing is already taken care of for you. However, if you are using React without a framework and only for client-side rendering (e.g. Vite without SSR), the most powerful and popular routing library out there is [React Router](https://reactrouter.com/). A new alternative with full TypeScript support in mind is [TanStack Router](https://tanstack.com/router).

<ReadMore label="Learn to use React Router" link="/react-router/" />

If you are using client-side routing in React with React Router, it's not much work introducing code splitting on a route level. If you happen to introduce this kind of optimization, you could substitute `React.lazy()` with [@loadable/component](https://github.com/gregberge/loadable-components) which gives you a better UX and more options.

<ReadMore label="Learn Lazy Loading with React Router" link="/react-router-lazy-loading/" />

Before you introduce a router in your React project, when you are just about to learn React, you can give [React's conditional rendering](/conditional-rendering-react/) a shot first. It is not a replacement for routing, but in small applications, it is often used to exchange components that way.

**Recommendations:**

* React Router
* fairly new, but check out TanStack Router if you like TypeScript and TanStack Query

# CSS Styling in React

There are many options and even more opinions about styling/CSS in React out there, so putting everything in one section here does not suffice. If you want to get deeper into this topic and get to know all the options, check out the following guide.

<ReadMore label="React CSS Styling" link="/react-css-styling/" />

But let's give you a brief overview. As a React beginner, it is just fine to start with inline styles and bare bones CSS by using a style object in JSX:

```javascript
const Headline = ({ title }) =>
  <h1 style={{ color: 'blue' }}>
    {title}
  </h1>
```

Whereas inline style can be used to add style dynamically with JavaScript in React's JSX, an external CSS file can hold all the remaining style for your React application:

```javascript{1,4}
import './Headline.css';

const Headline = ({ title }) =>
  <h1 className="headline" style={{ color: 'blue' }}>
    {title}
  </h1>
```

Once your application grows, there are many other styling options though. First, I would recommend you to have a look into CSS Modules as one of many *CSS-in-CSS* solutions. CSS Modules are supported by Vite and give you a way to encapsulate your CSS into component scoped modules. This way, it doesn't leak accidentally into the styling of other React components. Whereas some parts of your application can still share style, other parts don't have to get access to it. In React, CSS Modules are most often co-located CSS files to your React component files:

```javascript{1,4}
import styles from './style.module.css';

const Headline = ({ title }) =>
  <h1 className={styles.headline}>
    {title}
  </h1>
```

Second, I want to recommend you so-called Styled Components as one of many *CSS-in-JS* solutions for React. This approach is brought to you by a library called [styled-components](/react-styled-components/) (or alternatives such as [emotion](https://emotion.sh/) which co-locates styling with JavaScript next to your React components in your component's JavaScript file or a co-located file:

```javascript
import styled from 'styled-components';

const BlueHeadline = styled.h1`
  color: blue;
`;

const Headline = ({ title }) =>
  <BlueHeadline>
    {title}
  </BlueHeadline>
```

And third, I want to recommend [Tailwind CSS](https://tailwindcss.com/) as the most popular *Utility-First-CSS* solution. It comes with pre-defined CSS classes that you can use without defining them yourself. This makes you more efficient as a developer and streamlines the design system of your React application, but comes with the tradeoff of getting to know all the classes and verbose inlining of many CSS classes:

```javascript
const Headline = ({ title }) =>
  <h1 className="text-blue-700">
    {title}
  </h1>
```

Whether you choose CSS-in-CSS, CSS-in-JS, or Utility-First-CSS is up to you. All strategies scale well for larger React applications. One last hint: If you want to apply a className conditionally in React, use a utility like [clsx](https://github.com/lukeed/clsx).

**Recommendations:**

* CSS-in-CSS with CSS Modules
* Utility-First-CSS with Tailwind CSS
* CSS-in-JS with Styled Components (most popular)
  * alternatives: Emotion
* optional: clsx for conditional CSS classes

# React UI Libraries

As a beginner, it is a great and recommended learning experience to build reusable components from scratch. Whether it is a [dropdown](/react-dropdown/), a [select](/react-select/), a [radio button](/react-radio-button/), or a [checkbox](/react-checkbox/), you should know how to create these UI components yourself eventually.

However, if you don't have the resources to come up with all the components yourself at your company, you want to use a UI library which gives you access to lots of pre-built components which share the same design system. All of the following UI libraries come with essential components like Buttons, Dropdowns, Dialogs and Lists:

* [Material UI (by MUI)](https://material-ui.com/) (most popular)
* [Mantine UI](https://mantine.dev/) (most recommended)
* [Chakra UI](https://chakra-ui.com/) (most recommended)
* [Radix](https://www.radix-ui.com/) (unstyled design system)
* Tailwind
  * [Headless UI](https://headlessui.com/)
  * [Daisy UI](https://daisyui.com/)
  * [Tailwind UI](https://www.tailwindui.com/) (not free)
* [Ant Design](https://ant.design/)
* [Semantic UI](/react-semantic-ui-tutorial)
* [React Bootstrap](https://react-bootstrap.github.io/)
* [Reactstrap](https://reactstrap.github.io/)
* [NextUI](https://nextui.org/)
* [Primer](https://primer.style/react/)

Even though all of these UI libraries come with lots in-house components, they cannot make each component as powerful as libraries which focus only on one UI component. For example, [react-table-library](https://react-table-library.com/) allows you to create powerful table components in React while also offering you themes (e.g. Material UI) for blending nicely into popular UI component libraries.

# React Animation Libraries

Any animation in a web application starts with CSS. Eventually you will notice that CSS animations aren't enough for your needs. Usually developers check out [React Transition Group](https://reactcommunity.org/react-transition-group/) then, which gives them the possibility to perform animations with React components. Other well known animation libraries for React are:

* [Framer Motion](https://www.framer.com/motion/) (most recommended)
* [react-spring](https://github.com/react-spring/react-spring) (also often recommended)
* [react-motion](https://github.com/chenglou/react-motion)
* [react-move](https://github.com/sghall/react-move)
* [Animated](https://facebook.github.io/react-native/docs/animated) (React Native)

# Visualization and Chart Libraries in React

If you really want to build charts from the ground up yourself, there is no way around [D3](https://d3js.org/). It's a low level visualization library that gives you everything you need to create amazing charts. However, learning D3 is a whole other adventure, thus many developers just pick a React charting library which does everything for them in exchange for flexibility. These are some popular solutions:

* Recommendation: [Recharts](http://recharts.org) (great composability) (comes with customization due to opt-in composability)
* [visx](https://github.com/airbnb/visx) (leaning more towards low-level D3 than high-level abstraction, therefore steeper learning curve)
* off the shelf charts, more difficult to customize
  * [Victory](https://formidable.com/open-source/victory/)
  * [nivo](https://nivo.rocks/)
  * [react-chartjs](https://github.com/reactchartjs/react-chartjs-2)

# Form Libraries in React

The most popular library for [forms in React](/react-form/) is [React Hook Form](https://react-hook-form.com/). It comes with everything needed from validation (most popular integrations is [zod](https://github.com/colinhacks/zod)) over submission to form state management. As alternative there are [Formik](https://github.com/jaredpalmer/)and [React Final Form](https://final-form.org/react). If you are already using a React UI library, you could also check out their built-in form solution.

**Recommendations:**

* React Hook Form
  * with zod integration for validation
* If you use a UI library, check whether built-in form supports all your requirements
  * React Hook Form comes with a clean API for a UI library integration

# React Type Checking

React comes with an in-house type checking called [PropTypes](https://facebook.github.io/react/docs/typechecking-with-proptypes.html). By using PropTypes, you are able to define the props for your React components. Whenever a prop with a wrong type is passed to the component, you will get an error message when running the application:

```javascript
import PropTypes from 'prop-types';

const List = ({ list }) =>
  <div>
    {list.map(item => <div key={item.id}>{item.title}</div>)}
  </div>

List.propTypes = {
  list: PropTypes.array.isRequired,
};
```

However, PropTypes are not included in the React core library anymore. Over the last years, PropTypes got less popular in favor of TypeScript:

```javascript
type Item = {
  id: string;
  title: string;
};

type ListProps = {
  list: Item[];
};

const List: React.FC<ListProps> = ({ list }) =>
  <div>
    {list.map(item => <div key={item.id}>{item.title}</div>)}
  </div>
```

If you truly want to embrace types in React, [TypeScript](https://www.typescriptlang.org/) is the way to go these days. If you want to go beyond TypeScript for typed form validation, API input/output validation and more, check out [Zod](https://github.com/colinhacks/zod).

**Recommendations:**

* If typed JavaScript is wanted, use TypeScript

# React Code Structure: Style and Format

Essentially there are two ways to follow for a common sense for code structure:

If you want to embrace a unified and common sense code style, use [ESLint](https://eslint.org/) in your React project. A linter such as ESLint enforces a particular code style in your React project. For example, you can make it a requirement with ESLint to follow a popular styleguide (e.g. [Airbnb Style Guide](https://www.npmjs.com/package/eslint-config-airbnb)). Afterward, integrate [ESLint with your IDE/editor](/vscode-eslint/) and it will point you to every mistake.

<ReadMore label="React File/Folder Structure" link="/react-folder-structure/" />

If you want to embrace a unified code format, use [Prettier](https://github.com/prettier/prettier) in your React project. It is an opinionated code formatter with only a handful of opt-in configurations. You can [integrate it in your editor or IDE](/how-to-use-prettier-vscode/) so that it formats your code every time you save a file. Prettier doesn't replace ESLint though, but it [integrates nicely](/prettier-eslint/) with it.

**Recommendations:**

* ESLint + Prettier

# React Authentication

In a React application, you may want to introduce authentication with functionalities such as sign up, sign in, and sign out. Other features like password reset and password change features are often needed as well. These features go far beyond React, because a backend application manages these things for you.

<ReadMore label="How to prepare for authentication with React Router" link="/react-router-authentication/" />

The best learning experience would be implementing a backend application with authentication (e.g. [GraphQL backend](/graphql-apollo-server-tutorial/)) yourself. However, since authentication comes with lots of security risks and nitty gritty details not everyone knows about, I advice to use one of many authentication/backend-as-a-service solutions that are out there:

* [Firebase Auth](/complete-firebase-authentication-react-tutorial/)
* [Supabase Auth](https://supabase.com/docs/guides/auth/overview)
* [Auth0](https://auth0.com/)
* [AWS Cognito](https://aws.amazon.com/cognito/)

**Recommendations:**

* choose an authentication service or BaaS (e.g. Firebase/Supabase)
* optional learning experience: Custom Backend

# React Hosting

You can deploy and host a React application like any other web application. If you want to have full control, choose something like [Digital Ocean](https://m.do.co/c/fb27c90322f3). If you want to have someone taking care of everything, [Netlify](https://www.netlify.com/) or [Vercel](https://vercel.com/) (especially for Next.js) are popular solutions. If you are already using a third-party backend as a service like Firebase/Supabase, you can check whether they offer hosting as well. Other popular hosting providers are [Render](https://render.com/), [Fly.io](https://fly.io/), or [Railway](https://railway.app/).

# Testing in React

If you want to get a deep dive about testing in React, read this: [How to test components in React](/react-testing-tutorial/). Here comes the gist: The backbone of testing a React application is a test framework like [Jest](https://github.com/facebook/jest). It gives you test runner, assertion library and spying/mocking/stubbing functionalities. Everything that's needed from a comprehensive test framework. If you are a fan of Vite, you should check out [Vitest](https://vitest.dev/) as viable Jest alternative thoguh.

At the minimum, you can render React components in your testing framework with [react-test-renderer](https://www.npmjs.com/package/react-test-renderer). This is already sufficient to perform so-called [Snapshot Tests with Jest](/react-testing-jest/) or Vitest. A snapshot test works the following way: Once you run your tests, a snapshot of your rendered DOM elements of the React component is created. When you run your tests again at some point in time, another snapshot is created which is used as diff for the previous snapshot. If the diff is not identical, the test framework will complain and you either have to accept the snapshot or change the implementation of your component.

Eventually you will find yourself using the popular [React Testing Library (RTL)](/react-testing-library/) -- which is used within your testing framework's environment -- for a more elaborate testing library for React. RTL makes it possible to render your components and to simulate events on HTML elements. Afterward, your test framework (e.g. Jest/Vitest) is used for the assertions on the DOM nodes.

If you are looking for a testing tool for React end-to-end (E2E) tests, [Playwright](https://playwright.dev/) and [Cypress](/react-testing-cypress/) are the most popular choices.

**Recommendations:**

* Unit/Integration: Jest/Vitest + React Testing Library (most popular)
* Snapshot Tests: Jest/Vitest
* E2E Tests: Playwright or Cypress

# React and Immutable Data Structures

Vanilla JavaScript gives you plenty of built-in tools to handle data structures as if they are immutable. However, if you and your team feel the need to enforce immutable data structures, one of the most popular choices is [Immer](https://github.com/immerjs/immer). Personally I don't use it, because JavaScript can be used for managing immutable data structures, but any time someone asks about immutability in JS, someone will recommend it.

# React Internationalization

When it comes to [internationalization i18n for your React application](/react-internationalization/), you need to think not only about translations, but also about pluralizations, formattings for dates and currencies, and a handful of other things. These are the most popular libraries for dealing with it:

* [FormatJS](https://github.com/formatjs/formatjs)
* [react-i18next](https://github.com/i18next/react-i18next)

# Rich Text Editor in React

When it comes to Rich Text Editors in React, I can only think of the following, because I haven't used any others in React:

* [Draft.js](https://draftjs.org/)
* [Slate.js](https://www.slatejs.org/)
* [ReactQuill](https://github.com/zenoamaro/react-quill)

# Payments in React

Like in any other web application, the most common payment providers are Stripe and PayPal. Both can be neatly integrated into React. This is a [working Stripe Checkout with React integration](https://github.com/rwieruch/react-express-stripe).

* [PayPal](https://developer.paypal.com/docs/checkout/)
* [React Stripe Elements](https://github.com/stripe/react-stripe-js) or [Stripe Checkout](https://stripe.com/docs/payments/checkout)

# Time in React

JavaScript itself got pretty awesome dealing with dates and times over the recent years. So there is no real need to use a library for dealing with them. However, if your React application deals heavily with dates, times, and timezones, you could introduce a library which manages these things for you. These are your options:

* [date-fns](https://github.com/date-fns/date-fns)
* [Day.js](https://github.com/iamkun/dayjs)
* [Luxon](https://github.com/moment/luxon/)

# React Desktop Applications

[Electron](https://www.electronjs.org/) is still the go to framework for cross-platform desktop applications. However, there exist alternatives such as:

* [Tauri](https://github.com/tauri-apps/tauri) (great alternative, very popular)
* [Neutralino.js](https://github.com/neutralinojs/neutralinojs)
* [NW.js](https://nwjs.io/)

# File Upload in React

* [react-dropzone](https://react-dropzone.js.org/)
* [filepond](https://pqina.nl/filepond/)

# Mobile Development with React

The go-to solution for bringing React from the web to mobile is still [React Native](https://facebook.github.io/react-native/). If you want to help a framework for creating React Native applications, check out [Expo](/react-native-expo/).

<ReadMore label="Learn Navigation in React Native" link="/react-native-navigation/" />

# React VR/AR

It's possible to dive into virtual reality or augmented reality with React. To be honest, I haven't used any of these libraries, but they are the ones I know from the top of my head when it comes to AR/VR in React:

* [react-three-fiber](https://github.com/pmndrs/react-three-fiber) (popular 3d library, however, I have seen VR examples too)
* [react-360](https://facebook.github.io/react-360/)
* [aframe-react](https://github.com/supermedium/aframe-react)

# Design Prototyping for React

If you are coming from a UI/UX background, you may want to use a tool for fast prototyping for new React components, layouts, or UI/UX concepts. I used [Sketch](https://www.sketch.com) in the past, but switched to [Figma](https://www.figma.com/). [Zeplin](https://zeplin.io/) is another alternative. For rough yet lightweight sketches, I like to use [Excalidraw](https://excalidraw.com/). If you are looking for interactive UI/UX designs, check out [InVision](https://www.invisionapp.com/).

# React Component Documentation

If you are in charge of writing the documentation for your components, there are various neat React documentation tools out there. I have used [Storybook](https://storybook.js.org/) in many projects and can only recommend, but I have heard good things about these other solutions too:

* [Docusaurus](https://github.com/facebook/docusaurus)
* [Docz](https://github.com/doczjs/docz)
* [Styleguidist](https://github.com/styleguidist/react-styleguidist)

<Divider />

After all, the React ecosystem can be seen as a framework for React, but it stays flexible with React at its core. It is a flexible framework where you can make your own well-informed decisions about which libraries you want to opt-in. You can start small and add only libraries to solve specific problems. In contrast, if React is all you need, you can stay lightweight by using only the library.

