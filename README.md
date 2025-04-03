# GitHub Stats

A simple package to fetch GitHub user stats without needing to open a browser. Use this in your Node.js applications to retrieve public GitHub user information such as followers, public repositories, and more!

## Installation

You can install the package via npm or yarn:

```bash
npm install githubstats
```

```bash
yarn add githubstats
```
## Usage
You can use `githubstats` with CommonJS or ES Modules.

### CommonJS (Classic Node.js)
```js
const { GithubStats } = require("githubstates");
const dotenv = require("dotenv");
dotenv.config();
const token = process.env.token;

const stats = new GithubStats(token);
async function getStats(username) {
  try {
    const Stats = await stats.getUserStats(username);
    console.log(Stats);
  } catch (error) {
    console.error("Error fetching stats:", error);
  }
}
getStats("MrKhelil");
```
### ES Modules (ESM)
```js
import { GithubStats } from "githubstates";
import dotenv from "dotenv";
dotenv.config();
const token = process.env.token;

const stats = new GithubStats(token);
async function getStats(username) {
  try {
    const Stats = await stats.getUserStats(username);
    console.log(Stats);
  } catch (error) {
    console.error("Error fetching stats:", error);
  }
}
getStats("MrKhelil");
```
## Example Output
```js
{
  login: 'MrKhelil',
  id: 144062404,
  node_id: 'U_kgDOCJY3xA',
  avatar_url: 'https://avatars.githubusercontent.com/u/144062404?v=4',
  gravatar_id: '',
  url: 'https://api.github.com/users/MrKhelil',
  html_url: 'https://github.com/MrKhelil',
  followers_url: 'https://api.github.com/users/MrKhelil/followers',
  following_url: 'https://api.github.com/users/MrKhelil/following{/other_user}',
  gists_url: 'https://api.github.com/users/MrKhelil/gists{/gist_id}',
  starred_url: 'https://api.github.com/users/MrKhelil/starred{/owner}{/repo}',
  subscriptions_url: 'https://api.github.com/users/MrKhelil/subscriptions',
  organizations_url: 'https://api.github.com/users/MrKhelil/orgs',
  repos_url: 'https://api.github.com/users/MrKhelil/repos',
  events_url: 'https://api.github.com/users/MrKhelil/events{/privacy}',
  received_events_url: 'https://api.github.com/users/MrKhelil/received_events',
  type: 'User',
  user_view_type: 'public',
  site_admin: false,
  name: 'Khelil Badro',
  company: 'Source',
  blog: '',
  location: null,
  email: null,
  hireable: true,
  bio: 'Full-Stack Dev',
  twitter_username: null,
  public_repos: 1,
  public_gists: 0,
  followers: 1,
  following: 1,
  created_at: '2023-09-04T19:49:26Z',
  updated_at: '2025-04-03T05:07:38Z'
}
```
## Methods
`getUserStats(username : string)` 
Fetches the public GitHub stats for the given `username`.
* **Args** `username` (String) — The GitHub username of the user whose stats you want to fetch.
* **Retruns** A Promise with the user stats as a JSON object (like followers, public repos, etc.).

## Authentication
To fetch GitHub user stats, you need a GitHub personal access token. You can generate one by following these instructions:

- Go to GitHub: https://github.com/settings/tokens

- Generate a new token with the appropriate scopes (usually repo, user).

Once you have the token, use it as shown in the examples.

## Contributing
If you have suggestions or improvements, feel free to open issues or pull requests. We welcome contributions!

## Bugs and Issues

If you encounter any bugs or issues, please open an issue on the [GitHub repository](https://github.com/MrKhelil/githubStates).


Created with ❤️ by [MrKhelil](https://github.com/MrKhelil/)