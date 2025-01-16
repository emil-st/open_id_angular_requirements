# Angular Test Application: OpenID Connect Integration

## Introduction

The goal of this test is to evaluate the candidate's knowledge of working with modern authentication protocols, specifically **OpenID Connect (OIDC)**, within the context of a web application. This test focuses on implementing the **frontend part** of the OIDC Authorization Code Flow using the provided [demo server](https://demo.duendesoftware.com/).

To successfully complete the task, the candidate is expected to demonstrate an understanding of OIDC concepts or be able to research and learn the necessary information independently. This includes, but is not limited to, working with authorization endpoints, token exchange, securely handling tokens in a web application, and utilizing **Angular Signals**.

### Key Concepts to Explore

Candidates should familiarize themselves with the following topics:
1. **OpenID Connect Overview**:
   - [Introduction to OpenID Connect](https://openid.net/connect/)
   - [Authorization Code Flow with PKCE](https://auth0.com/docs/authenticate/protocols/oauth/oauth-authorization-code-flow)

2. **State Management in Angular**:
   - [NgRx](https://ngrx.io/)
   - [Angular Signals](https://angular.io/guide/signals)

3. **Routing in Angular**:
   - [Angular Router](https://angular.io/guide/router)

4. **HTTP Requests**:
   - [HttpClient](https://angular.io/guide/http)

5. **Secure Token Handling**:
   - [Angular Secure Storage Practices](https://angular.io/guide/security)

---

## Requirements

### Functional Requirements

1. **Authorization via Code Flow**
   - Implement the **Authorization Code Flow with PKCE** to authenticate with the [demo server](https://demo.duendesoftware.com/).
   - Use the provided native client (`interactive.public`) for login.
   - Retrieve and securely store the **access token**, **ID token**, and **refresh token** upon successful authorization.

2. **Protected API Access**
   - Use the **access token** to fetch data from a protected API endpoint (https://demo.duendesoftware.com/api/test).
   - Display the retrieved data (e.g., user profile or demo-provided data) in the app.

3. **Token Refresh**
   - Implement periodic token refresh using the **refresh token**.
   - Automatically refresh the access token before it expires.
   - Display updated tokens in the logs or UI for demonstration purposes.

---

### Additional Functional Requirements

1. **State Management**
   - Use **NgRx** for managing global state.
   - Integrate **Angular Signals** for local or component-level reactive state updates.
   - Manage states such as unauthorized, authenticating, authorized, and token refreshing.

2. **Routing**
   - Use **Angular Router** for navigation.
   - Redirect users to a login page if they are unauthorized.
   - Navigate to the authorized home page after successful login.

3. **HTTP Requests**
   - Use **HttpClient** to handle all API requests.
   - Implement an **HTTP interceptor** to automatically inject the access token into the headers of all authorized requests.

4. **Logout Functionality**
   - Implement a logout feature that:
     - Clears stored tokens and session data.
     - Redirects the user to the login page.

---

## Technical Requirements

1. **Angular Libraries**
   - Use the following libraries:
     - Use any appropriate package for handling OIDC flows.
     - `@ngrx/store` and `@ngrx/effects` for state management.
     - Angular Router for navigation.
     - `HttpClient` for API requests.

2. **Angular Signals**
   - Use Angular Signals to manage reactive state within components or for lightweight state management.
   - Demonstrate an understanding of how signals complement other state management techniques like NgRx.

3. **Secure Token Handling**
   - Store tokens securely, preferably using secure cookies or encrypted storage.
   - Ensure tokens are not exposed in logs or the UI unnecessarily.

4. **Error Handling**
   - Gracefully handle errors during authorization, API requests, and token refresh.
   - Provide user-friendly error messages where appropriate.

5. **UI/UX**
   - Simple and functional UI with:
     - **Login Page**: Includes a login button to start the OIDC flow.
     - **Home Page**: Displays user data fetched from the protected API.
     - **Error Notifications**: Displays errors when applicable.

---

## Deliverables

1. **Angular Project Code**
   - Submit the complete Angular project.
   - Include a `README.md` with setup instructions, including configuration of the redirect URI and running the app.

---

## Evaluation Criteria

1. **Functionality**:
   - Does the app implement the OIDC Authorization Code Flow with PKCE?
   - Are authorized API requests and token refresh handled correctly?

2. **Use of Libraries**:
   - Is NgRx used appropriately for global state management?
   - Are Angular Signals used effectively for reactive state updates?
   - Does Angular Router handle navigation effectively?
   - Is HttpClient used with an interceptor to inject access tokens?

3. **Code Quality**:
   - Is the code clean, modular, and maintainable?
   - Are secure coding practices followed?

4. **User Experience**:
   - Is the UI intuitive and functional?
   - Are errors handled gracefully?

---

By completing this test, candidates can showcase their knowledge of OIDC, state management (NgRx and Signals), routing, and API integration in Angular. Successful implementation will demonstrate problem-solving skills, self-learning capability, and adherence to best practices.
