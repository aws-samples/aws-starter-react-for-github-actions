# AWS CloudFormation Action for GitHub Actions React Starter

This starter template contains a bootstrapped [Create React App](https://github.com/facebook/create-react-app) with a GitHub Workflow that deploys the app to the [AWS Amplify Console](https://aws.amazon.com/amplify/console/) using the [AWS CloudFormation Action for GitHub Actions](https://github.com/marketplace/actions/aws-cloudformation-deploy-cloudformation-stack-action-for-github-actions).

## Create a new repository from this template

Click the **Use this template** button above to create a new repository from this template.

> This repository uses the new [template feature](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-template-repository) of GitHub.

You need your own AWS account to deploy the app to the [AWS Amplify Console](https://aws.amazon.com/amplify/console/). Follow these [steps](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/) if you do not have an account.

The AWS CloudFormation stack is deployed via [AWS CloudFormation "Deploy CloudFormation Stack" Action for GitHub Actions](https://github.com/marketplace/actions/aws-cloudformation-deploy-cloudformation-stack-action-for-github-actions).

When you create a new repository from the template, the GitHub Workflow is not setup. To setup the workflow, you need to follow these steps.

1. Create a [new personal token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line) with **full control of private repositories** store it as [encrypted secret](https://help.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets) `AMPLIFY_TOKEN` in the new repository.
2. Create a [new IAM user in your AWS account](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html) with **Programmatic Access** and store the access key ID as `AWS_ACCESS_KEY_ID` and secret access key as `AWS_SECRET_ACCESS_KEY` as secrets in your new repository.
3. (Optional) Configure a [custom domain](https://docs.aws.amazon.com/amplify/latest/userguide/custom-domains.html) for your app by setting the `AMPLIFY_DOMAIN` secret.

If you are ready, either make a new change an push it, or *re-run* the [failed GitHub Workflow](https://help.github.com/en/actions/configuring-and-managing-workflows/managing-a-workflow-run).

Because the first time the app gets deployed to the AWS Amplify Console it is not fully configured, you need to trigger a first manual build. Go to the [AWS Amplify Console](https://console.aws.amazon.com/amplify) and select your app from the list of all apps. 

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it. In the frontend environments is should show no builds. Click on **Run Build** to initialize the app.

> The stack is deployed to `us-east-1` by default. Please change the region in the `.github/workflows/deploy.yaml` if you want to use a different one.

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

## License

This library and the stack file are licensed under the MIT-0 License. See the LICENSE file.
