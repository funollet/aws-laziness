# aws-laziness

With `ec2ssh` and `ecsssh` tools you can connect to EC2 instances in a fast and easy way from the command line.

## Prerequisites

You need to have configured the awscli tool with all the roles you will use. For that, you can use the `awssso` script.

> 👉 Before executing the script, change the variable [LANDING_ROLE_NAME](./awssso#L4) to the role you want to use.
```shell
chmod +x awssso
mv awssso /usr/local/bin/
awssso
```

With that, you will be logged to aws, the credentials will be stored at `~/.aws/credentials` and the configured profiles at `~/.aws/config`.

## Installation

Give execution permission to scripts and move them to your binary path

```shell
chmod +x ec2ssh ecsssh
mv ec2ssh ecsssh /usr/local/bin/
```

## Usage

> 👉 Remember to be connected to the proper VPN: beta, devel or prod depending on the instances you want to connect to

### EC2SSH
To login into an EC2, you only need to type `ec2ssh [ENV]` where `[ENV]` can be `devel`, `beta`, `prod` or `security`:

![](ec2ssh.gif)

### ECSSSH
To login into an EC2 containing ECS services, you only need to type `ecsssh [ENV]` where `[ENV]` can be `devel`, `beta`, `prod` or `security`:

![](ecsssh.gif)
