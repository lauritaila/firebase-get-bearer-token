# Firebase Bearer Token Generator

[Official Firebase Documentation](https://firebase.google.com/docs/cloud-messaging/auth-server)

## Description

This is a simple Express server that generates a Firebase bearer token. This token can be used to authorize requests to Firebase services.

## Prerequisites

- Node.js (version 16 or higher recommended)
- npm (or yarn)
- Your Firebase Admin SDK private key file (usually named `firebase-admin.json`)

## Installation

1. **Clone the repository** (if you have one):
   ```bash
   git clone https://github.com/lauritaila/firebase-get-bearer-token.git
   cd firebase-get-bearer-token
2. **Install dependencies**:
   ```bash
   npm install
   # or
   yarn install
   ```
3. **Place your Firebase Admin SDK configuration file**:  
Ensure your `firebase-admin.json` file is located in the root directory of your project (or configure the path accordingly in your application).

## Usage

1. **Start the server**:

   ```bash
   node app.js
   # or
   yarn start
   # or
   npm start
   ```
2. **Make a request to generate a token**:

Send a POST request to the / endpoint of your server.

You can use tools like curl, Postman, or a web browser's developer console to make the request.  

**Example using curl:**
   ```bash
curl -X POST http://localhost:3000/
```

3. **Receive the bearer token**:  
The server will respond with a String containing the generated bearer token:

```json
"<generated_token>"
```
You can then use this token in the `Authorization` header of your requests to Firebase services:

`Authorization: Bearer YOUR_GENERATED_BEARER_TOKEN`

## Project Structure

```
firebase-token-generator/
├── app.js             # Main application file
├── package.json       # Project dependencies and scripts
└── firebase-admin.json  # Your Firebase Admin SDK configuration (should be kept secure)
```

## Important Security Note
Ensure your `firebase-admin.json` file is kept private and secure. Do not expose it in your client-side code or version control repositories.

## Contributing
Contributions are welcome! If you have suggestions for improvements or find any issues, please feel free to open an issue or submit a pull request.

This README provides a clear and concise guide for setting up and using your Firebase bearer token generation server. It follows a similar structure to your Flutter app README but focuses on the essentials for a server application. Let me know if you'd like any adjustments or further details added!


