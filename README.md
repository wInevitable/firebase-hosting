# Firebase-Hosting

A Quickstart Repository for hosting an Application with Firebase

## Setup Firebase Hosting for an existing Application

1. Install [Node.js](https://nodejs.org/) and `npm` on your system. Installing Node will automatically install npm as well.

1. Install the Firebase CLI

```sh
npm install -g firebase-tools
```

1. Login with your Google Account

```sh
firebase login
```

1. Choose the Application you would like to host with Firebase, navigate into the Application directory, and initialize Firebase.

```sh
firebase init
```

This will create a `firebase.json` settings file. The command can also be run later to add new features to your Application.

You may choose from both Database and Hosting options.

You will also have the ability to add the project to an existing Firebase project or create a new one. Note that choosing to create a new Firebase project will require you to visit the [Firebase Console](console.firebase.google.com) in order to create the project. Then add your Application to the Firebase project:

```sh
firebase use --add
```

The `--add` flag will ask you for an alias to add with the new Firebase project. These aliases are listed in your local `.firebaserc` file.

You may import a Firebase project from the console when one is owned by another user. You may set an alias for your project and can associate multiple Firebase projects with one application to allow for multiple environments (production and staging).

Optionally, see available Firebase projects with

```sh
firebase list
```

A Firebase Realtime Database Rules file `database.rules.json` will be created if you select the Realtime Database option. This can be used to restrict changes to your data model.

You will be asked to declare a directory to hold the Hosting assets to be uploaded with `firebase deploy`. The default is `public`.

Finally, you will have the option to set the page as a single-page app to redirect all URLs to index.html.

## Deployment

1. Select the Firebase project you would like to deploy:

```sh
firebase use project_alias_or_id
```

1. Deploy your Firebase project. Your Application will be deployed to the domain `<YOUR-FIREBASE-APP>.firebaseapp.com`. Deploys include Rules for your Firebase Realtime Database and Firebase Storage. They will create new releases for all deployable resources. Any existing security rules are overwritten.

```sh
firebase deploy
```

1. You may specify a project when using the `firebase deploy` command to deploy a project other than the one you care currently using with `firebase use`:

```sh
firebase deploy --project project_alias_or_id
```

## Managing and Rolling Back Deploys

1. From the Hosting Panel in the [Firebase Console](console.firebase.google.com) you can see a full list of previous deploys.

1. Rollback to a previous deploy by hovering over that deploy in the list, clicking the overflow menu icon, and clicking "Rollback."

1. Rules may not be rolled back.

1. Partial deploys are possible by flagging those resources you would like to deploy:

```sh
firebase deploy --only hosting, database, storage
```

## Visit Your Application

1. Navigate to the project URL directly `project_name.firebaseapp.com` or run `firebase open` from the command line.

## Realtime Database

1.

## Update

1. Update the Firebase CLI with the same command as initial installation

```sh
npm install -g firebase-tools
```

## References

[Firebase CLI Reference](https://firebase.google.com/docs/cli/)
[Firebase Hosting Quickstart](https://firebase.google.com/docs/hosting/quickstart)
[Firebase Hosting Documentation](https://firebase.google.com/docs/hosting/)
