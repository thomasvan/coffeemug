#!/bin/bash

<<\HOOKS tee ./.git/hooks/pre-commit > /dev/null
#!/usr/bin/env bash

echo "... pre-commit hook start"

echo "... checking author's email"
email_domain=${GIT_AUTHOR_EMAIL#*@}
if [[ $email_domain != 'medialounge.co.uk' ]]; then
    echo "your domain of email must be medialounge.co.uk"
    exit 1
fi
echo "author's email validation: OK"

HOOKS

chmod +x ./.git/hooks/pre-commit 
echo "successfully initialized git hook"