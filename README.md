# My Thought Process for the Library Exercise
Hi! I’m Lucas, and this is my thought process presentation for the library exercise. My approach was to tackle the project requirements in three distinct phases: first, I built the backend, then the frontend, and finally, I addressed the GenAI component.

## Backend
I began by designing the backend's models and selecting the technology stack. I chose **Ruby on Rails** and leveraged its `api-only` mode to capitalize on its speed for rapid application development.

For authentication, I implemented a custom solution to issue and validate a `Bearer Token`. This was a deliberate choice because, while Rails 8's built-in authentication is session-based, a Bearer Token approach is better suited for a stateless, decoupled API interacting with a separate frontend.

I used PostgreSQL as the database. This was an interesting return to relational databases after several years of working primarily with MongoDB, and it provided a valuable refresher on migrations and schema-based design principles.

When implementing the logic, I separated the work into four main areas to ensure a clear and organized structure:
1. Session logic
2. Books logic
3. Borrowings logic
4. Dashboards logic

My approach was to follow a principle of simplicity, relying on Rails's conventions and built-in features to keep the implementation clean and maintainable. I also created fixtures to provide test data for the database and for testing purposes.

## Frontend
For the frontend, I followed the same logical points as the backend to maintain a consistent flow and validate everything as I went. I chose React with TypeScript as it is the tool I am most familiar with. By using TypeScript, I was able to build a more robust and predictable application, catching potential errors early in the development cycle.

To speed up development and ensure a consistent user experience, I adopted Ant Design as the primary design system and a Catppuccin color palette. This allowed me to rapidly build components without needing to create every UI element from scratch.

I adopted a mobile-first development strategy, building and testing features in Chrome's mobile view to ensure optimal performance and layout on smaller screens before adapting the design for desktop displays.

## GenAI
To scaffold the required API, I used a markdown prompt with a Copilot agent. I began by clearly defining the core requirements, including the RESTful API structure, models, associations, and authentication, which helped the agent generate a highly accurate starting point.

Initially, I considered using a tool like Bruno for API testing. However, I decided that including plain curl requests directly in the README.md would provide a zero-dependency solution, making it easier for anyone to test the API endpoints immediately without needing to install additional software.
