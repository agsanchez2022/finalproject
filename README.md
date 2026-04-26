# Module 14 – BREAD Functionality for Calculations (CRUD Operations, Testing & Deployment)
This project focuses on implementing full BREAD (Browse, Read, Edit, Add, Delete) functionality for calculations within a FastAPI application. The backend uses FastAPI, SQLAlchemy, and Pydantic to manage calculation data tied to authenticated users.

Each calculation includes operations (such as addition, subtraction, multiplication, and division) along with operands, and all endpoints are secured so users can only access their own data. The project includes full API support for creating, retrieving, updating, and deleting calculations.

On the frontend side, forms and basic validation were added to allow users to interact with the API. Client-side validation ensures inputs are valid (like checking numeric values and valid operations) before sending requests.

End-to-end testing was expanded using Playwright to cover both positive and negative scenarios, including successful CRUD operations and handling invalid or unauthorized requests. The application is containerized using Docker and integrated with GitHub Actions for automated testing and deployment.

## 🧪 How to Run Tests Locally

1. Activate virtual environment:
```bash
source venv/bin/activate
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Start Docker:
```bash
docker compose up -d
```

4. Run tests:
```bash
pytest
```

---

## 🐳 Docker Hub Repository

https://hub.docker.com/repository/docker/drew2026000000/assignment14/general

---

## 📸 Screenshots

### GitHub Actions
![GitHub Actions](github_actions.png)

### Docker
![Docker](docker.png)

### Application Running in Browser:
![Application](application.png)

---

## 📸 Reflection

This assignment helped me understand how to fully implement CRUD functionality in a real application. Instead of just building endpoints, I had to make sure everything worked together, including authentication, database operations, and frontend interaction.

Working on the BREAD endpoints made it clearer how data flows between the user, API, and database. I also had to make sure that users could only access their own calculations, which reinforced how important proper authorization is.

One of the main challenges I ran into was dealing with environment and dependency issues, especially when running tests locally versus in GitHub Actions. Fixing those issues helped me understand how CI/CD environments work and why dependencies need to be consistent.

The Playwright tests were also useful because they simulate real user behavior instead of just testing individual functions. This made it easier to verify that the full application flow was working correctly.

Overall, this assignment tied together backend development, API design, testing, and deployment. It felt more like building a complete application rather than just individual features.