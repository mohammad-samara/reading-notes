# Gatsby, next.js, etc

## CRA, Next.js, and Gatsby

- Once you've finished creating your "creat react app", you may have started to hear about "Next.js" and "Gatsby". From many aspects, they may look similar, but each has a purpose, and their own pros and cons. One won't fit for all.

- Create React App is plain, simple, and it generates HTML code needed to render on the client side. So, when you look at the source code before rendering, you can see it's basically a few js files and an empty div. These js files inject content into the div in the browser (Client-side rendering). All the heavy lifting is done in the browser.

- Next.js a somewhat similar to Create React App, but supports server-side rendering. What it essentially means is that necessary HTML code is generated from the server itself, based on the URL. So your browser is receiving pre-rendered HTML code, not an empty ‘div’.

- While CRA offers client-side rendering and Next.js offers server-side rending, Gatsby is something called “Static Site Generator”. If you’re new to static site generators, those are generators which build “HTML” code during the “build”, by fetching data from some APIs, markdown files or anything. Note that everything is done in the “build” process. Similar to Next.js browser receives pre-rendered HTML code.

## Gatsby vs Next, which is better

- Lately Gatsby and Next have gotten lots of attention. At first glance, they both seem very similar.

- They both:

  - Generate very performant websites.

  - Create SPAs (Single Page Apps) out of the box.

  - Create good SEO (Search Engine Optimization) out of the box.

  - Have an awesome developer experience.

- Also, neither of them are boilerplates, but toolkits, which makes it difficult to choose which one to use.

- Although they have many similarities, they are fundamentally different.

## Static site generator vs. server side rendered pages

- A static site generator generates static HTML on build time. It doesn’t use a server.

- With server-side rendering, it dynamically generates the HTML every time a new request comes in. It uses a server for this.

- Gatsby is a static site generator tool.

- Next is mainly a tool for server-side rendered pages (although it also supports static exports).

- Of course, both can call APIs client side. The difference is Next requires a server to be able to run. Gatsby can function without any server at all.

- Gatsby just generates pure HTML/CSS/JS. This means you can host it at S3, Netlify or other static hosting services. This makes it extremely scalable to high traffic loads.

- Next creates HTML on runtime. So each time a new request comes in, it creates a new HTML page from the server.

## Gatsby Handles Your Data

- Another big difference between the two toolkits is how they handle data:

  - Gatsby dictates how you should handle data in your app.

  - Next does not dictate how you should handle your data. How you do it is entirely up to you.

- So how does Gatsby handle data? All data for your whole apps go into GraphQL. Let’s say you fetch data from an API. Then you first have to tell Gatsby to import the data into a GraphQL database.

- Your React components fetches the data from the GraphQL endpoint.

- Gatsby also has lots of plugins for various data sources which (in theory) makes it easy to integrate against many data sources. Some examples of data sources plugins are contentful, Wordpress, MongoDB and GraphQL

- When building for production, GraphQL is no longer used, but the data is persisted into JSON files instead.

- With Next on the other hand, how you manage your data is up to you. You have to decide on your own architecture how to manage data. You have to make a decision if you want to use GraphQL, Redux, pure React.

## Top 10 javascript frameworks

 1. AngularJS : It's a popular open source front-end development framework which is mainly used for developing single page apps.
 2. React : It's preferred as a choice for a high performing enterprise application needs to be delivered to its users.
 3. Ember.js : It lets developers create single page applications and large web applications, it's a very flexible framework.
 4. Vue.js : It's the fastest growing framework, it has a template style similar to Angular.
 5. Backbone.js
 6. Mithril.js
 7. Polymer.js
 8. Node.js : It's used to execute JS code outside of a browser, it's built on Google Chrome's V8 Engine.
 9. Meteor.js
 10. Aurelia

## Top 10 php frameworks

 1. Laravel
 2. Symfony
 3. Zend Framework
 4. CodeIgniter
 5. CakePHP
 6. FuelPHP
 7. Yii 2
 8. Phalcon
 9. Slim
 10. PHPixie
