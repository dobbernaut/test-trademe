# Description

This is a template for testing web UI and APIs.

The tests runs on node and is written on Typescript. It uses [axios](https://axios-http.com/) as the http client for testing the services and [webdriverio](https://webdriver.io/) for the website. Both are using [Jasmine](https://jasmine.github.io/) for the test framework.

This is a template using WebdriverIO async mode which means you need to use async/await for page element actions. see further information about [sync and async mode with WebdriverIO](https://webdriver.io/docs/sync-vs-async).

There is a sample test suite branch using this template in this repositry called [async-sample-test-suite](https://github.com/dobbernaut/test-webdriverio/tree/async-sample-test-suite).

If you want to use sync mode, use the [sync branch](https://github.com/dobbernaut/test-webdriverio/tree/sync) as your template instead.

# Prerequisites

You will need to have [Node](https://nodejs.org/en/) installed and able to run npm commands. Run the commands shown here from bash or shell.

Webdriverio uses [selenium-standalone](https://www.npmjs.com/package/selenium-standalone) to run the browser tests, so [Java is required to be available](https://github.com/vvo/selenium-standalone/blob/HEAD/docs/java-versions.md) from your machine.

You can get the [JDK](https://jdk.java.net/archive/) from here, extract and add Java to your machine PATH. These tests were tested on JDK version 11.

![JDK 11](files/jdk11.png)

# Setup

To set up the project, install the npm packages by running

```bash
npm ci
```

# Test

If you need to use passwords or token for your tests, add them as environment variables with the corresponding values **OR** you can can set them on runtime by appending them before the npm run command.

as an example where you require the following variables:

```text
testuser=REPLACEWITHtestusername
testpassword=REPLACEWITHuserpassword
token=REPLACEWITHoauthtoken
tokensecret=REPLACEWITHoauthtokensecret
key=REPLACEWITHconsumerkey
keysecret=REPLACEWITHconsumersecret
```

## Run test

For running the ui tests, use:
```bash
npm run test-ui
```

**to include the required environment variables from the command line:**
```bash
testuser=**REPLACEWITHtestusername** testpassword=**REPLACEWITHuserpassword** token=**REPLACEWITHoauthtoken** tokensecret=**REPLACEWITHoauthtokensecret** key=**REPLACEWITHconsumerkey** keysecret=**REPLACEWITHconsumersecret** npm run test-ui
```

![uiTest](files/uiTest.png)

For running the api tests, use:
```bash
npm run test-api
```

**to include the required environment variables from the command line:**
```bash
testuser=**REPLACEWITHtestusername** testpassword=**REPLACEWITHuserpassword** token=**REPLACEWITHoauthtoken** tokensecret=**REPLACEWITHoauthtokensecret** key=**REPLACEWITHconsumerkey** keysecret=**REPLACEWITHconsumersecret** npm run test-api
```

![apiTest](files/apiTest.png)
