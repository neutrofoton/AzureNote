# Azure Container Registry

To login to ACR:
1. Login to azure first
    ```
    az login
    ```
    The detail of Azure login through CLI can be seen in [Login Acccount](login-account.md) part

2. Make sure set to the right subscription profile id.
3. Login to ACR
    ```
    az acr login --name myregistry
    ```
Other login techniques are explained in [Azure Container Registry authentication with service principals](https://learn.microsoft.com/en-us/azure/container-registry/container-registry-auth-service-principal)


# Push Local Image to ACR
1. Login to ACR
2. Build docker image locally for example: <code>pocnetmvc</code>
3. Check makesure we have loged in the ACR
    ```
    cat .docker/config.json
    ```

    The content should be
    ```
    {
        "auths": {
                "myregistry.azurecr.io":{}
        },
        "credsStore": "xxxx"
    }
    ```

4. Tagging the image with the **full repo name** and add a reasonable version to it
    ```
    docker tag pocnetmvc myregistry.azurecr.io/pocnetmvc:v1
    ```
5. Push the image to ACR
    ```
    docker push myregistry.azurecr.io/pocnetmvc:v1
    ```