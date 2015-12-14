# IPA Auto Distribute
A auto distribute ipa shell script based on Shenzhen repo

###Install

The shell script based on [shenzhen](https://github.com/nomad/shenzhen). So must install shenzhen first:

```gem install shenzhen```

and then run the shell on your workspace:

```ruby -e "$(curl -fsSL https://raw.githubusercontent.com/candyan/ipa-auto-distribute/master/install)" your_app_id```

For example: 

```ruby -e "$(curl -fsSL https://raw.githubusercontent.com/candyan/ipa-auto-distribute/master/install)" 944841879```

> TIPS: Shenzhen will load credentials from the environment variables `ITUNES_CONNECT_ACCOUNT` and `ITUNES_CONNECT_PASSWORD`.
>
> add some lines in .zshrc or .bash_profile like:
> 
> `export ITUNES_CONNECT_ACCOUNT="xxx@itunesconnect.com"`
> 
> `export ITUNES_CONNECT_PASSWORD="yourpassword"`


###Usage

```
$ ./distribute.sh

Auto distribte ipa

  Options:
    -c        the configuration you want to distribute. default Release config
    -s        the scheme you want to distribute.
    -w        the workspace which your project located. default current path.

```

For example:

- you are in the project workspace and want to distribute release config: `./distribute.sh`
- you are in the project workspace and want to distribute TestFlight config: `./distribute.sh -c TestFlight`