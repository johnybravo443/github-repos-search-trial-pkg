# github-repos-search

Get a list of Github repositories of specified username sorted by numbers of stars in descending order and last updated time

## Installation

```js
# using npm
npm github-repos-search-trial-pkg

# using yarn
yarn add github-repos-search-trial-pkg
```

## Usage

```js
# using require
const { getRepos } = require('github-repos-search-trial-pkg');

# using import
import { getRepos } from 'github-repos-search-trial-pkg';
```

## Example

### Using promises:

```js
getRepos({
  username: 'gaearon', // provide GitHub username here
  page: 1, // optional property: default value is 1
  per_page: 50 // optional property: default value is 30
}).then((repositories) => console.log(repositories));
```

### Using async/await:

```js
const getRepositories = async function () {
  const repositories = await getRepos({
    username: 'gaearon', // provide GitHub username here
    page: 1, // optional property: default value is 1
    per_page: 50 // optional property: default value is 30
  });
  console.log(repositories);
};

getRepositories();
```
