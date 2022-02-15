1. Create a new github account with company email

	Ref: https://github.com/signup

2. Check if you have existing ssh key

	`ls -al ~/.ssh`
	
	In either case [generate a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)



	Follow the above guide. When asked for filename path add full filename path.

	E.g. `~/.ssh/work`

3. Add the newly generated key to github as specified in the following [guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

4. Update gitconfig

	Open your git config file generally at `$HOME/.config/git/config`

	And update the following key

	```text
	[user]
		email = <COMPANY-MAIL>

	```

> **Note**: Below steps are advanced and adviced to use if you want more fine grained control. Use this only if
> you want to have multiple git users on your machine. **( Not recommended )**

5. Update gitconfig with following key

	Adding this setting will make sure that whenever you are in `Work` folder your
	gitconfig use the specified gitconfig file to overwrite some settings
	```text

	[includeIf "gitdir/i:~/Work/"]
	  path = gitconfig-work
	```

- create a `gitconfig-work` file in the same directory as config file

	e.g recommended path for gitconfig-work `$HOME/.config/git/gitconfig-work`

- In this file add the following values

```text
[user]
	email = <COMPANY-MAIL>
```

6. Create ssh key config to handle the use case for multiple account ssh keys

```text
# Make default to be used with work
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/work

# Personal account

Host github.com-<personal-username>
  HostName github.com
  User git
  IdentityFile ~/.ssh/<PERSONAL-SSH-KEY>

```

Whenever you use the git clone command make sure to change the git url like
shown below

When you want to clone the repo with personal github account use the command
like following
```
      Note this part
    |---------------|
git@github.com-hmble:MTechZilla/nextjs-starter.git

```
Change the highlighted part with your own preferred SSH `Host` value

Thats it!! Have a good day


References:
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh
- https://stackoverflow.com/a/3860139
- https://code.tutsplus.com/tutorials/quick-tip-how-to-work-with-github-and-multiple-accounts--net-22574



	
