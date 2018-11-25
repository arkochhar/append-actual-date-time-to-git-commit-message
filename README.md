# commit-msg
Append actual date and time to git commit message

# Table of Contents
1. [Enable git templates](#enable-git-templates)
2. [Create a directory to hold the global hooks](#global-hooks)
3. [Write your hooks in ```~/.git-templates/hooks.```](#write-your-hooks)
4. [Make sure the hook is executable](#executable)
5. [Re-initialize git in each existing repo](#re-initialize)

## Enable git templates: <a name="enable-git-templates"></a>
```shell
git config --global init.templatedir "~/.git-templates"
```
This tells git to copy everything in ```~/.git-templates``` to your per-project .git/ directory when you run git init

## Create a directory to hold the global hooks: <a name="global-hooks"></a>
```shell
mkdir -p ~/.git-templates/hooks
```

## Write your hooks in ```~/.git-templates/hooks```: <a name="write-your-hooks"></a>
For example, here's a commit-msg hook (located in ~/.git-templates/hooks/commit-msg):  
```shell
cd ~/.git-templates/hooks
```
```shell
wget --no-check-certificate --content-disposition https://github.com/techpulsetoday/append-actual-date-time-to-git-commit-message/raw/master/commit-msg
```

## Make sure the hook is executable: <a name="executable"></a>
```shell
chmod a+x ~/.git-templates/hooks/commit-msg
```

## Re-initialize git in each existing repo you'd like to use this in: <a name="re-initialize"></a>
```shell
git init
```
NOTE if you already have a hook defined in your local git repo, this will not overwrite it.
