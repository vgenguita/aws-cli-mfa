If your AWS account has "must MFA" access then typically you can't do
much from the CLI until you get temporary credentials.

`install-scripts.sh` - Copy aws- scripts to your user home folder under ./local/bin (folder must exist and env PATH also)
```shell
./install-scripts.sh
```

`aws_get_creds` - This is the main script that will talk to the endpoints,
discover your account, what MFA token is assigned, request the credentials
and allow them to be exported.  Typically you would do something like
```shell
aws_get_creds myprofile
```

`aws_get_creds-yubikey` - This is the main script that will talk to the endpoints,
discover your account, request the credentials using ykman and allow them to be exported.  
Typically you would do something like

```shell
aws-get-creds-yubikey
```
`aws-assume-role` - This script allows you to assume a predefined role in your account
Typically you would do something like
```shell
aws-assume-role roleName
```

`aws-clear-envs` - Just unsets the main AWS variables
```shell
aws-clear-envs
```