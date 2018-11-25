# commit-msg
Append actual date and time to git commit message

## 1. Enable git templates:
```shell
git config --global init.templatedir "~/.git-templates"
```
This tells git to copy everything in ```~/.git-templates``` to your per-project .git/ directory when you run git init

## 2. Create a directory to hold the global hooks:
```shell
mkdir -p ~/.git-templates/hooks
```

## 3. Write your hooks in ```~/.git-templates/hooks.```
For example, here's a commit-msg hook (located in ~/.git-templates/hooks/commit-msg):  
```shell
cd ~/.git-templates/hooks
```
```shell
wget --no-check-certificate --content-disposition https://github.com/techpulsetoday/append-actual-date-time-to-git-commit-message/raw/master/commit-msg
```

## 4. Make sure the hook is executable.
```shell
chmod a+x ~/.git-templates/hooks/commit-msg
```

## 5. Re-initialize git in each existing repo you'd like to use this in:
```shell
git init
```
NOTE if you already have a hook defined in your local git repo, this will not overwrite it.
