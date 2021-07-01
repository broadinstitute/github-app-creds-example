# github-app-creds-example
Example of using GitHub App credentials.

1. ```
   pip install pygithub
   ```

2.  ```python
    from github import Github, GithubIntegration
    
    GITHUB_APP_ID = os.getenv('GITHUB_APP_ID')
    GITHUB_APP_INSTALLATION_ID = os.getenv('GITHUB_APP_INSTALLATION_ID')
    GITHUB_APP_PRIVATE_KEY = os.getenv('GITHUB_APP_PRIVATE_KEY')
    
    ghi = GithubIntegration(GITHUB_APP_ID, GITHUB_APP_PRIVATE_KEY)
    ghi_token = ghi.get_access_token(GITHUB_APP_INSTALLATION_ID).token
    ```
  
