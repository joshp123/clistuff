Arbritrary sized files:

`mkfile -n 4g ~/Desktop/four_gb_test_file.blah`

also works with b/k/m for bytes/kb/mb etc

Find/replace across a project and correct style errors afterwards, by filename:
```
flake8 >> before; find . -type f -name "*.py" -exec sed -i 's/foo/bar/g' {} + ; flake8 >> after
diff -u before after 
```
Fixing a broken SSH agent in tmux:
```
# First detach from tmux
env | grep ssh    # copy the result of this line
# Reattach to temux 
export  <the line you copied above>    # something like: SSH_AUTH_SOCK=/tmp/ssh-something/agent.12345 
```
