# commit-msg
Append actual date and time to git commit message

## 1. Enable git templates:
**_git config --global init.templatedir "~/.git-templates"_**
This tells git to copy everything in ~/.git-templates to your per-project .git/ directory when you run git init

## 2. Create a directory to hold the global hooks:
**_mkdir -p ~/.git-templates/hooks_**

## 3. Write your hooks in ~/.git-templates/hooks.
For example, here's a commit-msg hook (located in ~/.git-templates/hooks/commit-msg):
**_cd ~/.git-templates/hooks_**
**_wget --no-check-certificate --content-disposition https://github.com/techpulsetoday/append-actual-date-time-to-git-commit-message/raw/master/commit-msg_**

## 4. Make sure the hook is executable.
**_chmod a+x ~/.git-templates/hooks/commit-msg_**

## 5. Re-initialize git in each existing repo you'd like to use this in:
**_git init_**
NOTE if you already have a hook defined in your local git repo, this will not overwrite it.
