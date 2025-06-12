

https://github.com/user-attachments/assets/83384959-f40a-42cf-90a0-642a717a1251


#samsung-88
L&amp;t

Skip to main content
GitHub Docs
REST API/Repositories/Repositories
The REST API is now versioned. For more information, see "About API versioning."
REST API endpoints for repositories
Use the REST API to manage repositories on GitHub.

List organization repositories
Lists repositories for the specified organization.

Note

In order to see the block for a repository you must have admin permissions for the repository or be an owner or security manager for the organization that owns the repository. For more information, see "Managing security managers in your organization."security_and_analysis

Fine-grained access tokens for "List organization repositories"
This endpoint works with the following fine-grained token types:

GitHub App user access tokens
GitHub App installation access tokens
Fine-grained personal access tokens
The fine-grained token must have the following permission set:

"Metadata" repository permissions (read)
This endpoint can be used without authentication or the aforementioned permissions if only public resources are requested.

Parameters for "List organization repositories"
Headers
Name, Type, Description
accept string
Setting to is recommended.application/vnd.github+json

Path parameters
Name, Type, Description
org string Required
The organization name. The name is not case sensitive.

Query parameters
Name, Type, Description
type string
Specifies the types of repositories you want returned.

Default: all

Can be one of: all, public, private, forks, sources, member

sort string
The property to sort the results by.

Default: created

Can be one of: created, updated, pushed, full_name

direction string
The order to sort by. Default: when using , otherwise .ascfull_namedesc

Can be one of: asc, desc

per_page integer
The number of results per page (max 100). For more information, see "Using pagination in the REST API."

Default: 30

page integer
The page number of the results to fetch. For more information, see "Using pagination in the REST API."

Default: 1

HTTP response status codes for "List organization repositories"
Status code	Description
200	
OK

Code samples for "List organization repositories"
Request example
get
/orgs/{org}/repos
cURL
JavaScript
GitHub CLI
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer <YOUR-TOKEN>" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/orgs/ORG/repos
Response

Example response
Response schema
Status: 200
[
  {
    "id": 1296269,
    "node_id": "MDEwOlJlcG9zaXRvcnkxMjk2MjY5",
    "name": "Hello-World",
    "full_name": "octocat/Hello-World",
    "owner": {
      "login": "octocat",
      "id": 1,
      "node_id": "MDQ6VXNlcjE=",
      "avatar_url": "https://github.com/images/error/octocat_happy.gif",
      "gravatar_id": "",
      "url": "https://api.github.com/users/octocat",
      "html_url": "https://github.com/octocat",
      "followers_url": "https://api.github.com/users/octocat/followers",
      "following_url": "https://api.github.com/users/octocat/following{/other_user}",
      "gists_url": "https://api.github.com/users/octocat/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/octocat/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/octocat/subscriptions",
      "organizations_url": "https://api.github.com/users/octocat/orgs",
      "repos_url": "https://api.github.com/users/octocat/repos",
      "events_url": "https://api.github.com/users/octocat/events{/privacy}",
      "received_events_url": "https://api.github.com/users/octocat/received_events",
      "type": "User",
      "site_admin": false
    },
    "private": false,
    "html_url": "https://github.com/octocat/Hello-World",
    "description": "This your first repo!",
    "fork": false,
    "url": "https://api.github.com/repos/octocat/Hello-World",
    "archive_url": "https://api.github.com/repos/octocat/Hello-World/{archive_format}{/ref}",
    "assignees_url": "https://api.github.com/repos/octocat/Hello-World/assignees{/user}",
    "blobs_url": "https://api.github.com/repos/octocat/Hello-World/git/blobs{/sha}",
    "branches_url": "https://api.github.com/repos/octocat/Hello-World/branches{/branch}",
    "collaborators_url": "https://api.github.com/repos/octocat/Hello-World/collaborators{/collaborator}",
    "comments_url": "https://api.github.com/repos/octocat/Hello-World/comments{/number}",
    "commits_url": "https://api.github.com/repos/octocat/Hello-World/commits{/sha}",
    "compare_url": "https://api.github.com/repos/octocat/Hello-World/compare/{base}...{head}",
    "contents_url": "https://api.github.com/repos/octocat/Hello-World/contents/{+path}",
    "contributors_url": "https://api.github.com/repos/octocat/Hello-World/contributors",
    "deployments_url": "https://api.github.com/repos/octocat/Hello-World/deployments",
    "downloads_url": "https://api.github.com/repos/octocat/Hello-World/downloads",
    "events_url": "https://api.github.com/repos/octocat/Hello-World/ev
