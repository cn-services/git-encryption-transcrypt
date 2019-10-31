# Git Encryption - Transcrypt

## Install Transcrypt 

MacOS:

        $ brew install transcrypt

Other platforms: https://github.com/elasticdog/transcrypt/blob/master/INSTALL.md

## Designate a File to be Encrypted

        $ cd <path-to-your-repo>/
        $ echo 'sensitive_file  filter=crypt diff=crypt' >> .gitattributes
        $ git add .gitattributes sensitive_file
        $ git commit -m 'Add encrypted version of a sensitive file'

## Listing the Currently Encrypted Files

For convenience, transcrypt also adds a Git alias to allow you to list all of the currently encrypted files in a repository:

        $ git ls-crypt
        sensitive_file

Alternatively, you can use the --list command line option:

        $ transcrypt --list
        sensitive_file

