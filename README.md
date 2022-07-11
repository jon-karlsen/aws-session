# aws-session

Simple shell script to simplify authenticating with the AWS CLI using MFA, as well as switching roles. Usage is simple:

```
$ source <PATH>/aws_session --token="<YOUR_MFA_TOKEN>"
```

Do note that this script requires `~/.aws/credentials` configured as per the following structure:

```
[default]
aws_access_key_id = <YOUR_ACCESS_KEY_ID>
aws_secret_access_key = <YOUR_SECRET_ACCESS_KEY>
mfa_serial = <YOUR_MFA_SERIAL>

[mfa]
role_arn = <ARN_OF_ROLE_TO_WHICH_TO_SWITCH>
role_session_name = <DESIRED_ROLE_SESSION_NAME>
```

