
# Development Guidelines for Node.js Projects

## 1. Project Structure
- Use a clear modular structure:
  ```
  /src
    /controllers
    /services
    /models
    /routes
    /utils
  ```
- Keep configuration files in `/config`.
- Place tests in `/tests` mirroring the source structure.

---

## 2. Language & Framework
- Use **TypeScript** for all new code.
- Target **ES Modules** (`"type": "module"` in `package.json`).
- Prefer `import`/`export` over CommonJS `require`.

---

## 3. Coding Standards
- Follow **Airbnb JavaScript Style Guide** (or ESLint config based on it).
- Use **Prettier** for formatting.
- Enforce strict typing with `tsconfig.json`:
  - `"strict": true`
  - `"noImplicitAny": true`

---

## 4. Error Handling
- Always use `try/catch` for async operations.
- Centralize error handling in middleware:
  ```typescript
  app.use((err, req, res, next) => {
    console.error(err);
    res.status(err.status || 500).json({ message: err.message });
  });
  ```

---

## 5. API Design
- Follow **RESTful conventions**:
  - Use nouns for resources (`/users`, `/orders`).
  - Use proper HTTP verbs (`GET`, `POST`, `PUT`, `DELETE`).
- Validate inputs using **Zod** or **Joi**.
- Return consistent JSON responses:
  ```json
  { "data": {}, "error": null }
  ```

---

## 6. Security
- Never commit secrets; use `.env` and `dotenv`.
- Sanitize user input to prevent XSS/SQL injection.
- Enable **Helmet** for HTTP headers.

---

## 7. Testing
- Use **Jest** for unit tests.
- Use **Supertest** for API endpoint tests.
- Maintain coverage > 80%.

---

## 8. Performance & Logging
- Use **async/await** for non-blocking operations.
- Implement structured logging with **Winston** or **Pino**.
- Avoid synchronous file I/O in production code.

---

## 9. Git & Commits
- Follow **Conventional Commits**:
  - `feat: add new API endpoint`
  - `fix: correct validation logic`
- Commit small, atomic changes.

---

## 10. Documentation
- Document all public functions with JSDoc or TSDoc.
- Maintain an updated `README.md` with setup instructions.

---

## References
- https://github.com/goldbergyoni/nodebestpractices
- https://github.com/airbnb/javascript
