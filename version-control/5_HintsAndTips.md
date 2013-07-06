# Git hints and tips

## `man` page

Like many Unix/Linux commands, `git` has a `man` page,

    $ man git

You can scroll the manual page up and down using the up and down arrows.

You can search for keywords by typing `/` followed by the search term e.g. if interested in help, type `/help` and then hit enter.

To exit the manual page, type `q`.

## Command-line help

Type,

    $ git --help

and Git gives a list of commands it is able to help with, as well
as their descriptions.


    $ git --help
    usage: git [--version] [--exec-path[=<path>]] [--html-path]
               [-p|--paginate|--no-pager] [--no-replace-objects]
               [--bare] [--git-dir=<path>] [--work-tree=<path>]
               [-c name=value] [--help]
               <command> [<args>]

    The most commonly used git commands are:
       add        Add file contents to the index
       bisect     Find by binary search the change that introduced a bug
       branch     List, create, or delete branches
       checkout   Checkout a branch or paths to the working tree
       clone      Clone a repository into a new directory
       commit     Record changes to the repository
       diff       Show changes between commits, commit and working tree, etc
       fetch      Download objects and refs from another repository
       grep       Print lines matching a pattern
       init       Create an empty git repository or reinitialize an existing one
       log        Show commit logs
       merge      Join two or more development histories together
       mv         Move or rename a file, a directory, or a symlink
       pull       Fetch from and merge with another repository or a local branch
       push       Update remote refs along with associated objects
       rebase     Forward-port local commits to the updated upstream head
       reset      Reset current HEAD to the specified state
       rm         Remove files from the working tree and from the index
       show       Show various types of objects
       status     Show the working tree status
       tag        Create, list, delete or verify a tag object signed with GPG

    See 'git help <command>' for more information on a specific command.



You can get more help on a specific command, by providing the command name e.g.

    $ git init --help
    $ git commit --help
    ## git --help : Getting Help


    
    

## Add a repository description

You can edit the file `.git/description` and give your repository a name e.g. "My first repository".

## Ignore scratch, temporary and binary files

You can create a `.gitignore` file which lists the patterns of files you want Git to ignore. It's common practice to not add to a repository any file you can automatically create in some way e.g. C object files (`.o`), Java class (`.class`) files or temporary files e.g. XEmacs scratch files (`~`). Adding these to `.gitignore` means Git won't complain about them being untracked.

Create or edit `gitignore`,

    $ nano .gitignore

Then add patterns for the files you want to ignore, where `*` is a wildcard,

    *~
    *.o
    *.so
    *.dll
    *.exe
    *.class
    *.jar

Then, add `.gitignore` to your repository,

    $ git add .gitignore
    $ git commit -m "Added rules to ignore XEmacs scratch files and binary files"

## Add colour to `diff`

    $ git config --global color.diff auto

Previous: [Conclusions and further information](4_Conclusion.md)
