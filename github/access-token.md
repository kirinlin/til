# Access Token

Go `Settings > Developer settings > Personal access tokens`

> Personal access tokens function like ordinary OAuth access tokens. They can be used instead of a password for Git over HTTPS, or can be used to [authenticate to the API over Basic Authentication](https://docs.github.com/en/rest/overview/other-authentication-methods#basic-authentication). 

```console
$ curl -u username:token https://api.github.com/user
docker build -t $IMAGE_TAG https://<token>:x-oauth-basic@github.com/userORorg/myapp.git 
```
