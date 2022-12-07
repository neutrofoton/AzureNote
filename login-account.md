# Login
## Mode 1:
```
az login
```

If the CLI can open your default browser, it will initiate [authorization code flow](https://learn.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-auth-code-flow) and open the default browser to load an Azure sign-in page.

The command will return account information, subscription etc in form of json.

## Mode 2
Sign in with credentials on the command line. This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.
```
az login -u <username> -p <password>
```

Other methods of login can be seen in [Authenticate Azure CLI](https://learn.microsoft.com/en-us/cli/azure/authenticate-azure-cli).

# Account
Show detail account option
```
az account --help
```

Set a subscription to be the current active subscription.
```
az account set --subscription 0f220b16-43e2-4e21-8f39-c8059eb32a38
```
