<h1 align="center">
    <img alt="Proffy" title="Proffy" src="https://github.com/monteiro-alexandre/proffy-mobile/blob/master/.github/assets/logo.svg" width="220px" />
</h1>

<h4 align="center">
  🚀 Next Level Week #02 - Mobile
</h4>

> Proffy is an online study platform that helps people find teachers online. This is the mobile version.

All the resources used by this application comes from its [`API`](https://github.com/monteiro-alexandre/proffy-api).

<div align="left">

[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
</div>

# :pushpin: Table of Contents

* [Screenshots](#camera-screenshots)
* [Installation](#construction_worker-installation)
* [Getting Started](#runner-getting-started)
* [Found a bug? Missing a specific feature?](#bug-issues)
* [Contributing](#tada-contributing)
* [License](#closed_book-license)

# :camera: Screenshots

Click to expand.<br>

<img src="https://github.com/monteiro-alexandre/proffy-mobile/blob/master/.github/assets/landing.jpg" width="32%" />
<img src="https://github.com/monteiro-alexandre/proffy-mobile/blob/master/.github/assets/give-classes.jpg" width="32%" />
<img src="https://github.com/monteiro-alexandre/proffy-mobile/blob/master/.github/assets/search.jpg" width="32%" />
<img src="https://github.com/monteiro-alexandre/proffy-mobile/blob/master/.github/assets/proffys.jpg" width="32%" />
<img src="https://github.com/monteiro-alexandre/proffy-mobile/blob/master/.github/assets/favorites.jpg" width="32%" />

# :construction_worker: Installation

**You need to install [Node.js](https://nodejs.org/en/download/) and [Yarn](https://yarnpkg.com/) first, then in order to clone the project via HTTPS, run this command:**

```
git clone https://github.com/monteiro-alexandre/proffy-mobile.git
```

SSH URLs provide access to a Git repository via SSH, a secure protocol. If you use a SSH key registered in your Github account, clone the project using this command:

```
git clone git@github.com:monteiro-alexandre/proffy-mobile.git
```

**Install dependencies**

```
yarn install
```

Or

```
npm install
```

Create your environment variables based on the examples of ```.env.example```

```
cp environment.example.ts environment.ts
```

After copying the examples, make sure to fill the variables with new values. to run locally you can fill the development environment. if you will use your cell phone for the test, make sure you have point your machine ip address in apiUrl and not use localhost

key|description|example
---|---|---
apiUrl|API's url|`http://your_machine_ip_address:3333/`

```js
import Constants from 'expo-constants';

const ENV = {
	development: {
		apiUrl: 'http://your_machine_ip_address:3333/',
	},
	staging: {
		apiUrl: '',
	},
	production: {
		apiUrl: '',
	},
};

const getEnvVars = (env = Constants.manifest.releaseChannel): any => {
	let environment;
	// What is __DEV__ ?
	// This variable is set to true when react-native is running in Dev mode.
	// __DEV__ is true when run locally, but false when published.
	// eslint-disable-next-line
	if (__DEV__) {
		environment = ENV.development;
	} if (env === 'staging') {
		environment = ENV.staging;
	} if (env === 'production') {
		environment = ENV.production;
	}
	return environment;
};

export default getEnvVars;
```

# :runner: Getting Started

Run the following command to start Expo DevTools:

```yarn start```

Than you can open the app in your cell phone using the Expo client app for IOS and Android, see:

<a href="https://docs.expo.io/get-started/installation/#2-expo-client-app-for-ios-and">Expo Documentation</a>

# :bug: Issues

Feel free to **file a new issue** with a respective title and description on the the [Proffy mobile](https://github.com/monteiro-alexandre/proffy-mobile/issues) repository. If you already found a solution to your problem, **I would love to review your pull request**! Have a look at our [contribution guidelines](https://github.com/monteiro-alexandre/proffy-mobile/blob/master/CONTRIBUTING.md) to find out about the coding standards.

# :tada: Contributing

Check out the [contributing](https://github.com/monteiro-alexandre/proffy-mobile/blob/master/CONTRIBUTING.md) page to see the best places to file issues, start discussions and begin contributing.

# :closed_book: License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.