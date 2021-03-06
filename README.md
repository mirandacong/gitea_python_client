# swagger-client
This documentation describes the Gitea API.

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.1.1
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import swagger_client 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import swagger_client
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: AccessToken
swagger_client.configuration.api_key['access_token'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['access_token'] = 'Bearer'
# Configure API key authorization: AuthorizationHeaderToken
swagger_client.configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['Authorization'] = 'Bearer'
# Configure HTTP basic authorization: BasicAuth
swagger_client.configuration.username = 'YOUR_USERNAME'
swagger_client.configuration.password = 'YOUR_PASSWORD'
# Configure API key authorization: SudoHeader
swagger_client.configuration.api_key['Sudo'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['Sudo'] = 'Bearer'
# Configure API key authorization: SudoParam
swagger_client.configuration.api_key['sudo'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['sudo'] = 'Bearer'
# Configure API key authorization: Token
swagger_client.configuration.api_key['token'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['token'] = 'Bearer'
# create an instance of the API class
api_instance = swagger_client.AdminApi()
username = 'username_example' # str | username of the user that will own the created organization

try:
    # Create an organization
    api_response = api_instance.admin_create_org(username)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AdminApi->admin_create_org: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost{{AppSubUrl}}/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AdminApi* | [**admin_create_org**](docs/AdminApi.md#admin_create_org) | **POST** /admin/users/{username}/orgs | Create an organization
*AdminApi* | [**admin_create_public_key**](docs/AdminApi.md#admin_create_public_key) | **POST** /admin/users/{username}/keys | Add a public key on behalf of a user
*AdminApi* | [**admin_create_repo**](docs/AdminApi.md#admin_create_repo) | **POST** /admin/users/{username}/repos | Create a repository on behalf a user
*AdminApi* | [**admin_create_user**](docs/AdminApi.md#admin_create_user) | **POST** /admin/users | Create a user
*AdminApi* | [**admin_delete_user**](docs/AdminApi.md#admin_delete_user) | **DELETE** /admin/users/{username} | Delete a user
*AdminApi* | [**admin_delete_user_public_key**](docs/AdminApi.md#admin_delete_user_public_key) | **DELETE** /admin/users/{username}/keys/{id} | Delete a user&#39;s public key
*AdminApi* | [**admin_edit_user**](docs/AdminApi.md#admin_edit_user) | **PATCH** /admin/users/{username} | Edit an existing user
*IssueApi* | [**issue_add_label**](docs/IssueApi.md#issue_add_label) | **POST** /repos/{owner}/{repo}/issues/{index}/labels | Add a label to an issue
*IssueApi* | [**issue_add_time**](docs/IssueApi.md#issue_add_time) | **POST** /repos/{owner}/{repo}/issues/{id}/times | Add a tracked time to a issue
*IssueApi* | [**issue_clear_labels**](docs/IssueApi.md#issue_clear_labels) | **DELETE** /repos/{owner}/{repo}/issues/{index}/labels | Remove all labels from an issue
*IssueApi* | [**issue_create_comment**](docs/IssueApi.md#issue_create_comment) | **POST** /repos/{owner}/{repo}/issues/{index}/comments | Add a comment to an issue
*IssueApi* | [**issue_create_issue**](docs/IssueApi.md#issue_create_issue) | **POST** /repos/{owner}/{repo}/issues | Create an issue
*IssueApi* | [**issue_create_label**](docs/IssueApi.md#issue_create_label) | **POST** /repos/{owner}/{repo}/labels | Create a label
*IssueApi* | [**issue_create_milestone**](docs/IssueApi.md#issue_create_milestone) | **POST** /repos/{owner}/{repo}/milestones | Create a milestone
*IssueApi* | [**issue_delete_comment**](docs/IssueApi.md#issue_delete_comment) | **DELETE** /repos/{owner}/{repo}/issues/comments/{id} | Delete a comment
*IssueApi* | [**issue_delete_comment_deprecated**](docs/IssueApi.md#issue_delete_comment_deprecated) | **DELETE** /repos/{owner}/{repo}/issues/{index}/comments/{id} | Delete a comment
*IssueApi* | [**issue_delete_label**](docs/IssueApi.md#issue_delete_label) | **DELETE** /repos/{owner}/{repo}/labels/{id} | Delete a label
*IssueApi* | [**issue_delete_milestone**](docs/IssueApi.md#issue_delete_milestone) | **DELETE** /repos/{owner}/{repo}/milestones/{id} | Delete a milestone
*IssueApi* | [**issue_edit_comment**](docs/IssueApi.md#issue_edit_comment) | **PATCH** /repos/{owner}/{repo}/issues/comments/{id} | Edit a comment
*IssueApi* | [**issue_edit_comment_deprecated**](docs/IssueApi.md#issue_edit_comment_deprecated) | **PATCH** /repos/{owner}/{repo}/issues/{index}/comments/{id} | Edit a comment
*IssueApi* | [**issue_edit_issue**](docs/IssueApi.md#issue_edit_issue) | **PATCH** /repos/{owner}/{repo}/issues/{index} | Edit an issue
*IssueApi* | [**issue_edit_issue_deadline**](docs/IssueApi.md#issue_edit_issue_deadline) | **POST** /repos/{owner}/{repo}/issues/{index}/deadline | Set an issue deadline. If set to null, the deadline is deleted.
*IssueApi* | [**issue_edit_label**](docs/IssueApi.md#issue_edit_label) | **PATCH** /repos/{owner}/{repo}/labels/{id} | Update a label
*IssueApi* | [**issue_edit_milestone**](docs/IssueApi.md#issue_edit_milestone) | **PATCH** /repos/{owner}/{repo}/milestones/{id} | Update a milestone
*IssueApi* | [**issue_get_comments**](docs/IssueApi.md#issue_get_comments) | **GET** /repos/{owner}/{repo}/issues/{index}/comments | List all comments on an issue
*IssueApi* | [**issue_get_issue**](docs/IssueApi.md#issue_get_issue) | **GET** /repos/{owner}/{repo}/issues/{index} | Get an issue
*IssueApi* | [**issue_get_label**](docs/IssueApi.md#issue_get_label) | **GET** /repos/{owner}/{repo}/labels/{id} | Get a single label
*IssueApi* | [**issue_get_labels**](docs/IssueApi.md#issue_get_labels) | **GET** /repos/{owner}/{repo}/issues/{index}/labels | Get an issue&#39;s labels
*IssueApi* | [**issue_get_milestone**](docs/IssueApi.md#issue_get_milestone) | **GET** /repos/{owner}/{repo}/milestones/{id} | Get a milestone
*IssueApi* | [**issue_get_milestones_list**](docs/IssueApi.md#issue_get_milestones_list) | **GET** /repos/{owner}/{repo}/milestones | Get all of a repository&#39;s milestones
*IssueApi* | [**issue_get_repo_comments**](docs/IssueApi.md#issue_get_repo_comments) | **GET** /repos/{owner}/{repo}/issues/comments | List all comments in a repository
*IssueApi* | [**issue_list_issues**](docs/IssueApi.md#issue_list_issues) | **GET** /repos/{owner}/{repo}/issues | List a repository&#39;s issues
*IssueApi* | [**issue_list_labels**](docs/IssueApi.md#issue_list_labels) | **GET** /repos/{owner}/{repo}/labels | Get all of a repository&#39;s labels
*IssueApi* | [**issue_remove_label**](docs/IssueApi.md#issue_remove_label) | **DELETE** /repos/{owner}/{repo}/issues/{index}/labels/{id} | Remove a label from an issue
*IssueApi* | [**issue_replace_labels**](docs/IssueApi.md#issue_replace_labels) | **PUT** /repos/{owner}/{repo}/issues/{index}/labels | Replace an issue&#39;s labels
*IssueApi* | [**issue_tracked_times**](docs/IssueApi.md#issue_tracked_times) | **GET** /repos/{owner}/{repo}/issues/{id}/times | List an issue&#39;s tracked times
*MiscellaneousApi* | [**get_version**](docs/MiscellaneousApi.md#get_version) | **GET** /version | Returns the version of the Gitea application
*MiscellaneousApi* | [**render_markdown**](docs/MiscellaneousApi.md#render_markdown) | **POST** /markdown | Render a markdown document as HTML
*MiscellaneousApi* | [**render_markdown_raw**](docs/MiscellaneousApi.md#render_markdown_raw) | **POST** /markdown/raw | Render raw markdown as HTML
*OrganizationApi* | [**create_org_repo**](docs/OrganizationApi.md#create_org_repo) | **POST** /org/{org}/repos | Create a repository in an organization
*OrganizationApi* | [**org_add_team_member**](docs/OrganizationApi.md#org_add_team_member) | **PUT** /teams/{id}/members/{username} | Add a team member
*OrganizationApi* | [**org_add_team_repository**](docs/OrganizationApi.md#org_add_team_repository) | **PUT** /teams/{id}/repos/{org}/{repo} | Add a repository to a team
*OrganizationApi* | [**org_conceal_member**](docs/OrganizationApi.md#org_conceal_member) | **DELETE** /orgs/{org}/public_members/{username} | Conceal a user&#39;s membership
*OrganizationApi* | [**org_create_hook**](docs/OrganizationApi.md#org_create_hook) | **POST** /orgs/{org}/hooks/ | Create a hook
*OrganizationApi* | [**org_create_team**](docs/OrganizationApi.md#org_create_team) | **POST** /orgs/{org}/teams | Create a team
*OrganizationApi* | [**org_delete_hook**](docs/OrganizationApi.md#org_delete_hook) | **DELETE** /orgs/{org}/hooks/{id} | Delete a hook
*OrganizationApi* | [**org_delete_member**](docs/OrganizationApi.md#org_delete_member) | **DELETE** /orgs/{org}/members/{username} | Remove a member from an organization
*OrganizationApi* | [**org_delete_team**](docs/OrganizationApi.md#org_delete_team) | **DELETE** /teams/{id} | Delete a team
*OrganizationApi* | [**org_edit**](docs/OrganizationApi.md#org_edit) | **PATCH** /orgs/{org} | Edit an organization
*OrganizationApi* | [**org_edit_hook**](docs/OrganizationApi.md#org_edit_hook) | **PATCH** /orgs/{org}/hooks/{id} | Update a hook
*OrganizationApi* | [**org_edit_team**](docs/OrganizationApi.md#org_edit_team) | **PATCH** /teams/{id} | Edit a team
*OrganizationApi* | [**org_get**](docs/OrganizationApi.md#org_get) | **GET** /orgs/{org} | Get an organization
*OrganizationApi* | [**org_get_hook**](docs/OrganizationApi.md#org_get_hook) | **GET** /orgs/{org}/hooks/{id} | Get a hook
*OrganizationApi* | [**org_get_team**](docs/OrganizationApi.md#org_get_team) | **GET** /teams/{id} | Get a team
*OrganizationApi* | [**org_is_member**](docs/OrganizationApi.md#org_is_member) | **GET** /orgs/{org}/members/{username} | Check if a user is a member of an organization
*OrganizationApi* | [**org_is_public_member**](docs/OrganizationApi.md#org_is_public_member) | **GET** /orgs/{org}/public_members/{username} | Check if a user is a public member of an organization
*OrganizationApi* | [**org_list_current_user_orgs**](docs/OrganizationApi.md#org_list_current_user_orgs) | **GET** /user/orgs | List the current user&#39;s organizations
*OrganizationApi* | [**org_list_hooks**](docs/OrganizationApi.md#org_list_hooks) | **GET** /orgs/{org}/hooks | List an organization&#39;s webhooks
*OrganizationApi* | [**org_list_members**](docs/OrganizationApi.md#org_list_members) | **GET** /orgs/{org}/members | List an organization&#39;s members
*OrganizationApi* | [**org_list_public_members**](docs/OrganizationApi.md#org_list_public_members) | **GET** /orgs/{org}/public_members | List an organization&#39;s public members
*OrganizationApi* | [**org_list_repos**](docs/OrganizationApi.md#org_list_repos) | **GET** /orgs/{org}/repos | List an organization&#39;s repos
*OrganizationApi* | [**org_list_team_members**](docs/OrganizationApi.md#org_list_team_members) | **GET** /teams/{id}/members | List a team&#39;s members
*OrganizationApi* | [**org_list_team_repos**](docs/OrganizationApi.md#org_list_team_repos) | **GET** /teams/{id}/repos | List a team&#39;s repos
*OrganizationApi* | [**org_list_teams**](docs/OrganizationApi.md#org_list_teams) | **GET** /orgs/{org}/teams | List an organization&#39;s teams
*OrganizationApi* | [**org_list_user_orgs**](docs/OrganizationApi.md#org_list_user_orgs) | **GET** /user/{username}/orgs | List a user&#39;s organizations
*OrganizationApi* | [**org_publicize_member**](docs/OrganizationApi.md#org_publicize_member) | **PUT** /orgs/{org}/public_members/{username} | Publicize a user&#39;s membership
*OrganizationApi* | [**org_remove_team_member**](docs/OrganizationApi.md#org_remove_team_member) | **DELETE** /teams/{id}/members/{username} | Remove a team member
*OrganizationApi* | [**org_remove_team_repository**](docs/OrganizationApi.md#org_remove_team_repository) | **DELETE** /teams/{id}/repos/{org}/{repo} | Remove a repository from a team
*RepositoryApi* | [**create_current_user_repo**](docs/RepositoryApi.md#create_current_user_repo) | **POST** /user/repos | Create a repository
*RepositoryApi* | [**create_fork**](docs/RepositoryApi.md#create_fork) | **POST** /repos/{owner}/{repo}/forks | Fork a repository
*RepositoryApi* | [**list_forks**](docs/RepositoryApi.md#list_forks) | **GET** /repos/{owner}/{repo}/forks | List a repository&#39;s forks
*RepositoryApi* | [**repo_add_collaborator**](docs/RepositoryApi.md#repo_add_collaborator) | **PUT** /repos/{owner}/{repo}/collaborators/{collaborator} | Add a collaborator to a repository
*RepositoryApi* | [**repo_check_collaborator**](docs/RepositoryApi.md#repo_check_collaborator) | **GET** /repos/{owner}/{repo}/collaborators/{collaborator} | Check if a user is a collaborator of a repository
*RepositoryApi* | [**repo_create_hook**](docs/RepositoryApi.md#repo_create_hook) | **POST** /repos/{owner}/{repo}/hooks | Create a hook
*RepositoryApi* | [**repo_create_key**](docs/RepositoryApi.md#repo_create_key) | **POST** /repos/{owner}/{repo}/keys | Add a key to a repository
*RepositoryApi* | [**repo_create_pull_request**](docs/RepositoryApi.md#repo_create_pull_request) | **POST** /repos/{owner}/{repo}/pulls | Create a pull request
*RepositoryApi* | [**repo_create_release**](docs/RepositoryApi.md#repo_create_release) | **POST** /repos/{owner}/{repo}/releases | Create a release
*RepositoryApi* | [**repo_create_release_attachment**](docs/RepositoryApi.md#repo_create_release_attachment) | **POST** /repos/{owner}/{repo}/releases/{id}/assets | Create a release attachment
*RepositoryApi* | [**repo_create_status**](docs/RepositoryApi.md#repo_create_status) | **POST** /repos/{owner}/{repo}/statuses/{sha} | Create a commit status
*RepositoryApi* | [**repo_delete**](docs/RepositoryApi.md#repo_delete) | **DELETE** /repos/{owner}/{repo} | Delete a repository
*RepositoryApi* | [**repo_delete_collaborator**](docs/RepositoryApi.md#repo_delete_collaborator) | **DELETE** /repos/{owner}/{repo}/collaborators/{collaborator} | Delete a collaborator from a repository
*RepositoryApi* | [**repo_delete_hook**](docs/RepositoryApi.md#repo_delete_hook) | **DELETE** /repos/{owner}/{repo}/hooks/{id} | Delete a hook in a repository
*RepositoryApi* | [**repo_delete_key**](docs/RepositoryApi.md#repo_delete_key) | **DELETE** /repos/{owner}/{repo}/keys/{id} | Delete a key from a repository
*RepositoryApi* | [**repo_delete_release**](docs/RepositoryApi.md#repo_delete_release) | **DELETE** /repos/{owner}/{repo}/releases/{id} | Delete a release
*RepositoryApi* | [**repo_delete_release_attachment**](docs/RepositoryApi.md#repo_delete_release_attachment) | **DELETE** /repos/{owner}/{repo}/releases/{id}/assets/{attachment_id} | Delete a release attachment
*RepositoryApi* | [**repo_edit_hook**](docs/RepositoryApi.md#repo_edit_hook) | **PATCH** /repos/{owner}/{repo}/hooks/{id} | Edit a hook in a repository
*RepositoryApi* | [**repo_edit_pull_request**](docs/RepositoryApi.md#repo_edit_pull_request) | **PATCH** /repos/{owner}/{repo}/pulls/{index} | Update a pull request
*RepositoryApi* | [**repo_edit_release**](docs/RepositoryApi.md#repo_edit_release) | **PATCH** /repos/{owner}/{repo}/releases/{id} | Update a release
*RepositoryApi* | [**repo_edit_release_attachment**](docs/RepositoryApi.md#repo_edit_release_attachment) | **PATCH** /repos/{owner}/{repo}/releases/{id}/assets/{attachment_id} | Edit a release attachment
*RepositoryApi* | [**repo_get**](docs/RepositoryApi.md#repo_get) | **GET** /repos/{owner}/{repo} | Get a repository
*RepositoryApi* | [**repo_get_archive**](docs/RepositoryApi.md#repo_get_archive) | **GET** /repos/{owner}/{repo}/archive/{archive} | Get an archive of a repository
*RepositoryApi* | [**repo_get_branch**](docs/RepositoryApi.md#repo_get_branch) | **GET** /repos/{owner}/{repo}/branches/{branch} | Retrieve a specific branch from a repository
*RepositoryApi* | [**repo_get_by_id**](docs/RepositoryApi.md#repo_get_by_id) | **GET** /repositories/{id} | Get a repository by id
*RepositoryApi* | [**repo_get_combined_status_by_ref**](docs/RepositoryApi.md#repo_get_combined_status_by_ref) | **GET** /repos/{owner}/{repo}/commits/{ref}/statuses | Get a commit&#39;s combined status, by branch/tag/commit reference
*RepositoryApi* | [**repo_get_editor_config**](docs/RepositoryApi.md#repo_get_editor_config) | **GET** /repos/{owner}/{repo}/editorconfig/{filepath} | Get the EditorConfig definitions of a file in a repository
*RepositoryApi* | [**repo_get_hook**](docs/RepositoryApi.md#repo_get_hook) | **GET** /repos/{owner}/{repo}/hooks/{id} | Get a hook
*RepositoryApi* | [**repo_get_key**](docs/RepositoryApi.md#repo_get_key) | **GET** /repos/{owner}/{repo}/keys/{id} | Get a repository&#39;s key by id
*RepositoryApi* | [**repo_get_pull_request**](docs/RepositoryApi.md#repo_get_pull_request) | **GET** /repos/{owner}/{repo}/pulls/{index} | Get a pull request
*RepositoryApi* | [**repo_get_raw_file**](docs/RepositoryApi.md#repo_get_raw_file) | **GET** /repos/{owner}/{repo}/raw/{filepath} | Get a file from a repository
*RepositoryApi* | [**repo_get_release**](docs/RepositoryApi.md#repo_get_release) | **GET** /repos/{owner}/{repo}/releases/{id} | Get a release
*RepositoryApi* | [**repo_get_release_attachment**](docs/RepositoryApi.md#repo_get_release_attachment) | **GET** /repos/{owner}/{repo}/releases/{id}/assets/{attachment_id} | Get a release attachment
*RepositoryApi* | [**repo_list_branches**](docs/RepositoryApi.md#repo_list_branches) | **GET** /repos/{owner}/{repo}/branches | List a repository&#39;s branches
*RepositoryApi* | [**repo_list_collaborators**](docs/RepositoryApi.md#repo_list_collaborators) | **GET** /repos/{owner}/{repo}/collaborators | List a repository&#39;s collaborators
*RepositoryApi* | [**repo_list_hooks**](docs/RepositoryApi.md#repo_list_hooks) | **GET** /repos/{owner}/{repo}/hooks | List the hooks in a repository
*RepositoryApi* | [**repo_list_keys**](docs/RepositoryApi.md#repo_list_keys) | **GET** /repos/{owner}/{repo}/keys | List a repository&#39;s keys
*RepositoryApi* | [**repo_list_pull_requests**](docs/RepositoryApi.md#repo_list_pull_requests) | **GET** /repos/{owner}/{repo}/pulls | List a repo&#39;s pull requests
*RepositoryApi* | [**repo_list_release_attachments**](docs/RepositoryApi.md#repo_list_release_attachments) | **GET** /repos/{owner}/{repo}/releases/{id}/assets | List release&#39;s attachments
*RepositoryApi* | [**repo_list_releases**](docs/RepositoryApi.md#repo_list_releases) | **GET** /repos/{owner}/{repo}/releases | List a repo&#39;s releases
*RepositoryApi* | [**repo_list_stargazers**](docs/RepositoryApi.md#repo_list_stargazers) | **GET** /repos/{owner}/{repo}/stargazers | List a repo&#39;s stargazers
*RepositoryApi* | [**repo_list_statuses**](docs/RepositoryApi.md#repo_list_statuses) | **GET** /repos/{owner}/{repo}/statuses/{sha} | Get a commit&#39;s statuses
*RepositoryApi* | [**repo_list_subscribers**](docs/RepositoryApi.md#repo_list_subscribers) | **GET** /repos/{owner}/{repo}/subscribers | List a repo&#39;s watchers
*RepositoryApi* | [**repo_merge_pull_request**](docs/RepositoryApi.md#repo_merge_pull_request) | **POST** /repos/{owner}/{repo}/pulls/{index}/merge | Merge a pull request
*RepositoryApi* | [**repo_migrate**](docs/RepositoryApi.md#repo_migrate) | **POST** /repos/migrate | Migrate a remote git repository
*RepositoryApi* | [**repo_mirror_sync**](docs/RepositoryApi.md#repo_mirror_sync) | **POST** /repos/{owner}/{repo}/mirror-sync | Sync a mirrored repository
*RepositoryApi* | [**repo_pull_request_is_merged**](docs/RepositoryApi.md#repo_pull_request_is_merged) | **GET** /repos/{owner}/{repo}/pulls/{index}/merge | Check if a pull request has been merged
*RepositoryApi* | [**repo_search**](docs/RepositoryApi.md#repo_search) | **GET** /repos/search | Search for repositories
*RepositoryApi* | [**repo_test_hook**](docs/RepositoryApi.md#repo_test_hook) | **POST** /repos/{owner}/{repo}/hooks/{id}/tests | Test a push webhook
*RepositoryApi* | [**repo_tracked_times**](docs/RepositoryApi.md#repo_tracked_times) | **GET** /repos/{owner}/{repo}/times | List a repo&#39;s tracked times
*RepositoryApi* | [**topic_search**](docs/RepositoryApi.md#topic_search) | **GET** /topics/search | search topics via keyword
*RepositoryApi* | [**user_current_check_subscription**](docs/RepositoryApi.md#user_current_check_subscription) | **GET** /repos/{owner}/{repo}/subscription | Check if the current user is watching a repo
*RepositoryApi* | [**user_current_delete_subscription**](docs/RepositoryApi.md#user_current_delete_subscription) | **DELETE** /repos/{owner}/{repo}/subscription | Unwatch a repo
*RepositoryApi* | [**user_current_put_subscription**](docs/RepositoryApi.md#user_current_put_subscription) | **PUT** /repos/{owner}/{repo}/subscription | Watch a repo
*UserApi* | [**create_current_user_repo**](docs/UserApi.md#create_current_user_repo) | **POST** /user/repos | Create a repository
*UserApi* | [**user_add_email**](docs/UserApi.md#user_add_email) | **POST** /user/emails | Add email addresses
*UserApi* | [**user_check_following**](docs/UserApi.md#user_check_following) | **GET** /users/{follower}/following/{followee} | Check if one user is following another user
*UserApi* | [**user_create_token**](docs/UserApi.md#user_create_token) | **POST** /users/{username}/tokens | Create an access token
*UserApi* | [**user_current_check_following**](docs/UserApi.md#user_current_check_following) | **GET** /user/following/{username} | Check whether a user is followed by the authenticated user
*UserApi* | [**user_current_check_starring**](docs/UserApi.md#user_current_check_starring) | **GET** /user/starred/{owner}/{repo} | Whether the authenticated is starring the repo
*UserApi* | [**user_current_delete_follow**](docs/UserApi.md#user_current_delete_follow) | **DELETE** /user/following/{username} | Unfollow a user
*UserApi* | [**user_current_delete_gpg_key**](docs/UserApi.md#user_current_delete_gpg_key) | **DELETE** /user/gpg_keys/{id} | Remove a GPG key
*UserApi* | [**user_current_delete_key**](docs/UserApi.md#user_current_delete_key) | **DELETE** /user/keys/{id} | Delete a public key
*UserApi* | [**user_current_delete_star**](docs/UserApi.md#user_current_delete_star) | **DELETE** /user/starred/{owner}/{repo} | Unstar the given repo
*UserApi* | [**user_current_get_gpg_key**](docs/UserApi.md#user_current_get_gpg_key) | **GET** /user/gpg_keys/{id} | Get a GPG key
*UserApi* | [**user_current_get_key**](docs/UserApi.md#user_current_get_key) | **GET** /user/keys/{id} | Get a public key
*UserApi* | [**user_current_list_followers**](docs/UserApi.md#user_current_list_followers) | **GET** /user/followers | List the authenticated user&#39;s followers
*UserApi* | [**user_current_list_following**](docs/UserApi.md#user_current_list_following) | **GET** /user/following | List the users that the authenticated user is following
*UserApi* | [**user_current_list_gpg_keys**](docs/UserApi.md#user_current_list_gpg_keys) | **GET** /user/gpg_keys | List the authenticated user&#39;s GPG keys
*UserApi* | [**user_current_list_keys**](docs/UserApi.md#user_current_list_keys) | **GET** /user/keys | List the authenticated user&#39;s public keys
*UserApi* | [**user_current_list_repos**](docs/UserApi.md#user_current_list_repos) | **GET** /user/repos | List the repos that the authenticated user owns or has access to
*UserApi* | [**user_current_list_starred**](docs/UserApi.md#user_current_list_starred) | **GET** /user/starred | The repos that the authenticated user has starred
*UserApi* | [**user_current_list_subscriptions**](docs/UserApi.md#user_current_list_subscriptions) | **GET** /user/subscriptions | List repositories watched by the authenticated user
*UserApi* | [**user_current_post_gpg_key**](docs/UserApi.md#user_current_post_gpg_key) | **POST** /user/gpg_keys | Create a GPG key
*UserApi* | [**user_current_post_key**](docs/UserApi.md#user_current_post_key) | **POST** /user/keys | Create a public key
*UserApi* | [**user_current_put_follow**](docs/UserApi.md#user_current_put_follow) | **PUT** /user/following/{username} | Follow a user
*UserApi* | [**user_current_put_star**](docs/UserApi.md#user_current_put_star) | **PUT** /user/starred/{owner}/{repo} | Star the given repo
*UserApi* | [**user_current_tracked_times**](docs/UserApi.md#user_current_tracked_times) | **GET** /user/times | List the current user&#39;s tracked times
*UserApi* | [**user_delete_access_token**](docs/UserApi.md#user_delete_access_token) | **DELETE** /users/{username}/tokens/{token} | delete an access token
*UserApi* | [**user_delete_email**](docs/UserApi.md#user_delete_email) | **DELETE** /user/emails | Delete email addresses
*UserApi* | [**user_get**](docs/UserApi.md#user_get) | **GET** /users/{username} | Get a user
*UserApi* | [**user_get_current**](docs/UserApi.md#user_get_current) | **GET** /user | Get the authenticated user
*UserApi* | [**user_get_tokens**](docs/UserApi.md#user_get_tokens) | **GET** /users/{username}/tokens | List the authenticated user&#39;s access tokens
*UserApi* | [**user_list_emails**](docs/UserApi.md#user_list_emails) | **GET** /user/emails | List the authenticated user&#39;s email addresses
*UserApi* | [**user_list_followers**](docs/UserApi.md#user_list_followers) | **GET** /users/{username}/followers | List the given user&#39;s followers
*UserApi* | [**user_list_following**](docs/UserApi.md#user_list_following) | **GET** /users/{username}/following | List the users that the given user is following
*UserApi* | [**user_list_gpg_keys**](docs/UserApi.md#user_list_gpg_keys) | **GET** /users/{username}/gpg_keys | List the given user&#39;s GPG keys
*UserApi* | [**user_list_keys**](docs/UserApi.md#user_list_keys) | **GET** /users/{username}/keys | List the given user&#39;s public keys
*UserApi* | [**user_list_repos**](docs/UserApi.md#user_list_repos) | **GET** /users/{username}/repos | List the repos owned by the given user
*UserApi* | [**user_list_starred**](docs/UserApi.md#user_list_starred) | **GET** /users/{username}/starred | The repos that the given user has starred
*UserApi* | [**user_list_subscriptions**](docs/UserApi.md#user_list_subscriptions) | **GET** /users/{username}/subscriptions | List the repositories watched by a user
*UserApi* | [**user_search**](docs/UserApi.md#user_search) | **GET** /users/search | Search for users
*UserApi* | [**user_tracked_times**](docs/UserApi.md#user_tracked_times) | **GET** /repos/{owner}/{repo}/times/{user} | List a user&#39;s tracked times in a repo


## Documentation For Models

 - [AddCollaboratorOption](docs/AddCollaboratorOption.md)
 - [AddTimeOption](docs/AddTimeOption.md)
 - [Attachment](docs/Attachment.md)
 - [Branch](docs/Branch.md)
 - [Comment](docs/Comment.md)
 - [CreateEmailOption](docs/CreateEmailOption.md)
 - [CreateForkOption](docs/CreateForkOption.md)
 - [CreateGPGKeyOption](docs/CreateGPGKeyOption.md)
 - [CreateHookOption](docs/CreateHookOption.md)
 - [CreateIssueCommentOption](docs/CreateIssueCommentOption.md)
 - [CreateIssueOption](docs/CreateIssueOption.md)
 - [CreateKeyOption](docs/CreateKeyOption.md)
 - [CreateLabelOption](docs/CreateLabelOption.md)
 - [CreateMilestoneOption](docs/CreateMilestoneOption.md)
 - [CreateOrgOption](docs/CreateOrgOption.md)
 - [CreatePullRequestOption](docs/CreatePullRequestOption.md)
 - [CreateReleaseOption](docs/CreateReleaseOption.md)
 - [CreateRepoOption](docs/CreateRepoOption.md)
 - [CreateStatusOption](docs/CreateStatusOption.md)
 - [CreateTeamOption](docs/CreateTeamOption.md)
 - [CreateUserOption](docs/CreateUserOption.md)
 - [DeleteEmailOption](docs/DeleteEmailOption.md)
 - [DeployKey](docs/DeployKey.md)
 - [EditAttachmentOptions](docs/EditAttachmentOptions.md)
 - [EditDeadlineOption](docs/EditDeadlineOption.md)
 - [EditHookOption](docs/EditHookOption.md)
 - [EditIssueCommentOption](docs/EditIssueCommentOption.md)
 - [EditIssueOption](docs/EditIssueOption.md)
 - [EditLabelOption](docs/EditLabelOption.md)
 - [EditMilestoneOption](docs/EditMilestoneOption.md)
 - [EditOrgOption](docs/EditOrgOption.md)
 - [EditPullRequestOption](docs/EditPullRequestOption.md)
 - [EditReleaseOption](docs/EditReleaseOption.md)
 - [EditTeamOption](docs/EditTeamOption.md)
 - [EditUserOption](docs/EditUserOption.md)
 - [Email](docs/Email.md)
 - [GPGKey](docs/GPGKey.md)
 - [GPGKeyEmail](docs/GPGKeyEmail.md)
 - [InlineResponse200](docs/InlineResponse200.md)
 - [Issue](docs/Issue.md)
 - [IssueDeadline](docs/IssueDeadline.md)
 - [IssueLabelsOption](docs/IssueLabelsOption.md)
 - [Label](docs/Label.md)
 - [MarkdownOption](docs/MarkdownOption.md)
 - [MigrateRepoForm](docs/MigrateRepoForm.md)
 - [Milestone](docs/Milestone.md)
 - [Organization](docs/Organization.md)
 - [PRBranchInfo](docs/PRBranchInfo.md)
 - [PayloadCommit](docs/PayloadCommit.md)
 - [PayloadCommitVerification](docs/PayloadCommitVerification.md)
 - [PayloadUser](docs/PayloadUser.md)
 - [Permission](docs/Permission.md)
 - [PublicKey](docs/PublicKey.md)
 - [PullRequest](docs/PullRequest.md)
 - [PullRequestMeta](docs/PullRequestMeta.md)
 - [Release](docs/Release.md)
 - [Repository](docs/Repository.md)
 - [SearchResults](docs/SearchResults.md)
 - [ServerVersion](docs/ServerVersion.md)
 - [StateType](docs/StateType.md)
 - [Status](docs/Status.md)
 - [StatusState](docs/StatusState.md)
 - [Team](docs/Team.md)
 - [TrackedTime](docs/TrackedTime.md)
 - [User](docs/User.md)
 - [WatchInfo](docs/WatchInfo.md)


## Documentation For Authorization


## AccessToken

- **Type**: API key
- **API key parameter name**: access_token
- **Location**: URL query string

## AuthorizationHeaderToken

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header

## BasicAuth

- **Type**: HTTP basic authentication

## SudoHeader

- **Type**: API key
- **API key parameter name**: Sudo
- **Location**: HTTP header

## SudoParam

- **Type**: API key
- **API key parameter name**: sudo
- **Location**: URL query string

## Token

- **Type**: API key
- **API key parameter name**: token
- **Location**: URL query string


## Author



