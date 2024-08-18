**Goal: Begin to push portfolio projects to GitHub via the command line to demonstrate knowledge of Git (version control) and understanding of the command line.**

### Key Terms:

**Shell** - a shell is like a bridge or interface between the user and the computer's operating system. It's a program that takes commands and translates them into instructions that the operating system can understand and execute.

**Command Line** - also known as a command-line interface (CLI), a command line a text-based interface that allows users to interact with a computer's operating system and execute commands by typing them as text strings. 

**Git** - Git is an open source distributed version control system (VCS) used for tracking changes in files and coordinating work on projects among multiple people. 

**MacOS Terminal** - a command-line interface (CLI) application that allows users to interact with the MacOS operating system using text-based commands.

Steps

1. I changed the shell on my MacOS from Zsh to Bash. Zsh is a more customizable shell and has more customization, however, in doing research I learned that Bash is still the default shell on many Unix-based systems, including Linux distributions. I’m also more familiar with Bash so I decided to stick with it.

Changed the shell on my MacOS machine from Zsh to Bash using the command line.

```bash
echo $SHELL
```

```bash
chsh -s /bin/bash
```

- **`chsh`**: This stands for "change shell" and is a command-line utility that allows me to change my default login shell.
- **`s /bin/bash`**: This part of the command specifies the new shell that you want to set as the default. In this case, **`/bin/bash`** refers to the Bash shell, which is a popular Unix shell and command language.

2. Homebrew  - Homebrew is a package manager for macOS and Linux that simplifies the installation and management of software packages and libraries. It provides a command-line interface (CLI) for managing software installations, updates, and dependencies. Homebrew also allows for the installation of software not packaged for Linux the home directory without requiring ‘sudo’. I installed Homebrew via the command line.

Install Homebrew:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

1. **`/bin/bash`**: This specifies the shell to be used to execute the rest of the command. In this case, it's using the Bash shell (**`/bin/bash`**).
2. **`c`**: This option tells Bash to execute the following string as a command.
3. **`"$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`**: This part of the command uses **`curl`** to download the Homebrew installation script (**`install.sh`**) from the specified URL.
4. Here's what each component does:
    - **`curl`**: This is a command-line tool for transferring data from or to a server using various protocols (in this case, HTTP).
    - **`fsSL`**: These options for **`curl`**:
        - **`f`**: Fail silently on server errors (i.e., don't show error messages).
        - **`s`**: Silent mode (i.e., don't show progress or download information).
        - **`S`**: Show error messages if there are any.
        - **`L`**: Follow redirects (if the URL redirects to another location).

1. I double-checked to make sure I now had the latest version of Homebrew installed. I then used Homebrew to update Git, and then checked to make sure I had the latest version.

```bash
brew update
brew upgrade git
git --version
```
