<h1 align="center">A simplified Jira clone built with React and Node</h1>

<div align="center">Auto formatted with Prettier, tested with Cypress 🎗</div>

<h3 align="center">
  <a href="https://jira.ivorreic.com/">Visit the live app</a> |
  <a href="https://github.com/oldboyxx/jira_clone/tree/master/client">View client</a> |
  <a href="https://github.com/oldboyxx/jira_clone/tree/master/api">View API</a>
</h3>

![Tech logos](https://i.ibb.co/DVFj8PL/tech-icons.jpg)

![App screenshot](https://i.ibb.co/W3qVvCn/jira-optimized.jpg)

## What is this and who is it for 🤷‍♀️

I do React consulting and this is a showcase product I've built in my spare time. It's a very good example of modern, real-world React codebase.

There are many showcase/example React projects out there but most of them are way too simple. I like to think that this codebase contains enough complexity to offer valuable insights to React developers of all skill levels while still being _relatively_ easy to understand.

### Novelty of Idea

Our Jira clone stands out by addressing the common pain points users face with existing project management tools, such as complexity, lack of customization, and high costs. While Jira is a well-established tool, it often presents a steep learning curve and can be overly complex for smaller teams or those without specialized needs. Our platform aims to bridge this gap by providing an intuitive, highly customizable, and affordable alternative that maintains robust functionality without the associated complexity.

### Current Market Offerings

The current market for project management tools is saturated with options like Jira, Trello, Asana, and Monday.com. These tools vary widely in terms of features, pricing, and user experience. Jira is known for its powerful issue tracking and project management capabilities but is often seen as too complex for smaller teams. Trello offers simplicity and ease of use but lacks the depth of features needed for more complex projects. Asana and Monday.com provide a balance of usability and functionality but can be cost-prohibitive for smaller organizations or freelancers. Our Jira clone aims to combine the best aspects of these tools: the comprehensive features of Jira with the simplicity and affordability of Trello.

### Market Size

The project management software market is vast and growing, valued at approximately $4 billion in 2020 and projected to reach $10.67 billion by 2025. This growth is driven by the increasing adoption of remote work, the need for collaborative tools, and the rise of project-based work across various industries. Our target market includes software development teams, product management teams, IT operations teams, project management teams, freelancers, and small businesses. This broad target audience ensures a significant market size and ample growth opportunities.

### Difficulty in Building the Business

Building a business around a new project management tool involves several challenges:

1. *Development Complexity*: Creating a feature-rich, user-friendly, and scalable platform requires significant technical expertise and resources.
2. *Market Penetration*: Competing with established players like Jira, Trello, and Asana will require strategic marketing and a compelling value proposition.
3. *User Acquisition*: Attracting and retaining users in a competitive market demands continuous improvement, excellent customer support, and competitive pricing.
4. *Customization and Integration*: Ensuring our platform integrates seamlessly with other tools and offers extensive customization options can be technically challenging but is crucial for user adoption.

### Conceptual Application
Our Jira clone is designed to serve a diverse range of users:

- **Software Development Teams**: Track issues, manage sprints, and collaborate on code.
- **Product Management Teams**: Plan product roadmaps, prioritize features, and gather user feedback.
- **IT Operations Teams**: Monitor system performance, track incidents, and manage infrastructure projects.
- **Project Management Teams**: Oversee project timelines, allocate resources, and track milestones.
- **Freelancers and Small Businesses**: Manage client projects, collaborate with team members, and streamline workflows.

### Real-World Demonstrations
To demonstrate the real-world application of our Jira clone, we will:

1. **Pilot Programs**: Launch pilot programs with select teams across various industries to gather feedback and showcase success stories.
2. **Case Studies**: Develop detailed case studies highlighting how different teams have successfully implemented our tool to improve productivity and project outcomes.
3. **Live Demonstrations**: Conduct live demonstrations and webinars to showcase the platform’s features, usability, and customization options.
4. **User Testimonials**: Collect and publish testimonials from early adopters to build credibility and attract new users.
5. **Industry Partnerships**: Partner with industry-specific organizations to tailor our tool to their unique needs and gain industry-specific insights.

By focusing on these areas, we aim to establish our Jira clone as a competitive and attractive option in the project management software market.

## Features

- Proven, scalable, and easy to understand project structure
- Written in modern React, only functional components with hooks
- A variety of custom light-weight UI components such as datepicker, modal, various form elements etc
- Simple local React state management, without redux, mobx, or similar
- Custom webpack setup, without create-react-app or similar
- Client written in Babel powered JavaScript
- API written in TypeScript and using TypeORM

## Setting up development environment 🛠

- Install [postgreSQL](https://www.postgresql.org/) if you don't have it already and create a database named `jira_development`.
- `git clone https://github.com/oldboyxx/jira_clone.git`
- Create an empty `.env` file in `/api`, copy `/api/.env.example` contents into it, and fill in your database username and password.
- `npm run install-dependencies`
- `cd api && npm start`
- `cd client && npm start` in another terminal tab
- App should now be running on `http://localhost:8080/`

## Running cypress end-to-end tests 🚥

- Set up development environment
- Create a database named `jira_test` and start the api with `cd api && npm run start:test`
- `cd client && npm run test:cypress`

## What's missing?

There are features missing from this showcase product which should exist in a real product:

### Migrations 🗄

We're currently using TypeORM's `synchronize` feature which auto creates the database schema on every application launch. It's fine to do this in a showcase product or during early development while the product is not used by anyone, but before going live with a real product, we should [introduce migrations](https://github.com/typeorm/typeorm/blob/master/docs/migrations.md).

### Proper authentication system 🔐

We currently auto create an auth token and seed a project with issues and users for anyone who visits the API without valid credentials. In a real product we'd want to implement a proper [email and password authentication system](https://www.google.com/search?q=email+and+password+authentication+node+js&oq=email+and+password+authentication+node+js).

### Accessibility ♿

Not all components have properly defined [aria attributes](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA), visual focus indicators etc. Most early stage companies tend to ignore this aspect of their product but in many cases they shouldn't, especially once their userbase starts growing.

### Unit/Integration tests 🧪

Both Client and API are currently tested through [end-to-end Cypress tests](https://github.com/oldboyxx/jira_clone/tree/master/client/cypress/integration). That's good enough for a relatively simple application such as this, even if it was a real product. However, as the app grows in complexity, it might be wise to start writing additional unit/integration tests.

## Contributing

I will not be accepting PR's on this repository. Feel free to fork and maintain your own version.

## License

[MIT](https://opensource.org/licenses/MIT)

<hr>

<h3>
  <a href="https://jira.ivorreic.com/">Visit the live app</a> |
  <a href="https://github.com/oldboyxx/jira_clone/tree/master/client">View client</a> |
  <a href="https://github.com/oldboyxx/jira_clone/tree/master/api">View API</a>
</h3>
