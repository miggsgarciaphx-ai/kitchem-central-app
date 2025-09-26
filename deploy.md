# Deploying Your Application to Firebase App Hosting

This guide provides the steps to deploy your Next.js application to Firebase App Hosting, making it accessible to your end-users via a public URL.

## Prerequisites

Before you begin, you need to have the following installed on your local machine:

1.  **Node.js**: [Download and install Node.js](https://nodejs.org/) (which includes npm).
2.  **Firebase CLI**: You will need the Firebase Command Line Interface to deploy your app.

## Step 1: Install the Firebase CLI

If you don't have the Firebase CLI installed, open your terminal or command prompt and run the following command:

```bash
npm install -g firebase-tools
```

## Step 2: Log in to Firebase

In your terminal, log in to your Google account that is associated with your Firebase project:

```bash
firebase login
```

This will open a browser window for you to authenticate.

## Step 3: Set Up Your Project Locally

1.  **Download the Code**: Get the application code from this workspace onto your local machine.
2.  **Navigate to Project Directory**: Open your terminal and change the directory to your project's root folder.

    ```bash
    cd path/to/your/project
    ```

## Step 4: Initialize Firebase in Your Project

From the root directory of your project, run the following command to link your local code to your Firebase project:

```bash
firebase init apphosting
```

You will be prompted to:
- Select the Firebase project you want to use (it should appear in the list).
- Choose the App Hosting backend to link to (it should default to `nextn`).

The CLI will recognize the `apphosting.yaml` file and configure everything accordingly.

## Step 5: Deploy Your Application

After initialization is complete, you can deploy your application with a single command:

```bash
firebase deploy --only apphosting
```

The CLI will build your Next.js application and deploy it to Firebase App Hosting. Once it's finished, it will provide you with a **Live URL** (e.g., `https://<your-app-name>.web.app`).

This URL is what you can share with your end-users!

---

That's it! Your application will be live and running on Google's global infrastructure. If you make further changes to your app, you just need to run `firebase deploy --only apphosting` again to update the live version.
