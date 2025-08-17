# Social Budget Platform

A full-stack web application that simulates a participatory budgeting system, allowing users to collaboratively propose and evaluate how public funds are allocated.

The project was developed independently as part of a university course in Web Programming at Politecnico di Torino. I designed and implemented both the frontend and backend, including user authentication, dynamic phase progression, and real-time interaction features.

## Key Features

- Role-based access: administrators and standard users
- Budget management interface (admin only)
- Proposal creation, editing, and deletion (user)
- Preference scoring system (1–5) for anonymous peer proposals
- Automatic aggregation of preferences and display of approved results
- Phase-based application flow (from proposal to final decision)
- React-based dynamic routing per phase

## Technologies Used

- **Frontend**: React, React Router, Bootstrap
- **Backend**: Node.js, Express
- **Database**: SQLite
- **Authentication**: Session-based login with credentials
- **API**: RESTful APIs for session, user, budget, proposal, and preference management

## Screenshots

### Phase 1 – Proposal Submission (User view)

![Phase 1 - user](image.png)

### Phase 2 – Preference Scoring (Admin view)

![Phase 2 - admin](image-1.png)

## Demo Credentials (Local Testing)

- `mario.rossi@noprofit.it` – password: `marioRossi` (admin)
- `john.smith@noprofit.it` – password: `johnSmith`
- `tony.stark@noprofit.it` – password: `tonyStark`
- `john.lee@noprofit.it` – password: `johnLee`

## Development Notes

This project reflects the complete development cycle of a realistic web platform: from UI design to RESTful API creation, backend logic implementation, and final deployment-ready structure. I was solely responsible for all technical aspects, including route handling, component structure, session logic, and interaction design.

The project demonstrates practical skills in full-stack development, modular code organization, user interface design, and team-use simulation in a single-developer environment.

## Author

Developed by **Chiara Galtieri** as an individual academic project.  
For any questions or details, feel free to contact me via [LinkedIn](https://www.linkedin.com/in/tuo-linkedin) or [email](mailto:tuo@email.com).
