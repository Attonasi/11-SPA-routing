![CF](https://i.imgur.com/7v5ASc8.png)  Lab 11 SPA Routing
=======
[Code of Conduct](https://github.com/codefellows/code-of-conduct)

At the heart of every web app is the Web Request-Response Cycle. Pay close attention to how your app is creating and responding to requests. With client-side routing and the History API, we can add a layer of abstraction on top of traditional routing.

**Ensure you run the blog with `node server.js` or `nodemon` from the `starter-code` directory, not the `live-server` command.  You may also run our blog app with the `nodemon` package which is available through npm. `npm install -g nodemon`. This will also enable reloading pages after changes occur in our code.**

The URLs that your app can respond to maps to your apps capabilities. Consider what public routes your app should have. Use page.js to expose those as navigatable URLs. Then setup controllers to handle those URLs, all on the client side.

We are now building a true Single-Page App, so clicking links within the app should no longer trigger a brand new request to the web server. Work through these user stories to convert the blog to SPA-style.

## TODOs: User Stories: MVP
 1. As a developer, I want an articleController, so that I can group together actions related to the article resource.
  - Let's add in a reference to the newest library in our code - page.js!
	- We have some Controller files! Let's add references to those as well.
  - When the `/` route is requested, only the #articles section should be displayed to the user.
	- When the '/about' route is requested, only the #about section should be displayed to the user.
 1. As a developer, I want a routing file, so that I have a central place to define what URLs my app can handle.
  - Look for the TODO items in `routes.js`. Use the `page.js` features to tell your app how to handle the `/` route and the `/about` routes.
 1. As a reader, I want to view the article index, so that I can read all the articles.
  - Ensure that visiting the `/` route triggers the behavior of loading all the articles and rendering the index page view.
 1. As a reader, I want to view '/about', so that I can learn more about the brilliant developer who created this site.
  - Fill in the contents of `aboutController.js`, so the `#about` section is revealed when the about index action is triggered.
  - Ensure the function is linked to a route, so visitors to `/about` see your info, and not the blog posts.

## Stretch goals (not required):
 1. As an admin, I want the url for my stats page to be part of my SPA, so that it works like the other "pages" of my app.
  - Where should the admin content go? You probably need to move a section out of admin.html into index.html.
  - How should we now navigate to '/admin'?
  - Add a controller and a route so that `/admin` triggers the proper rendering of the stats section.
	- Since we have eliminated another request to the server, we may need to rethink how Article.fetchAll behaves.


## Technical Requirements and Grading Rubric
 - Ensure your code passes ESLint.
 - Create a single place where your app's URLs are connected to actions to handle the URLs.
 - Encapsulate each behavior of your app within an appropriate layer of MVC abstraction.
