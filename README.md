# EZ:

[Original README](https://github.com/sorin-ionescu/prezto/blob/master/README.md)

### Manual

Prezto will work with any recent release of Zsh, but the minimum required
version is **4.3.11**.

01. Launch Zsh:

    ```console
    zsh
    ```

02. Clone the repository:

    ```console
    git clone --recursive git@github.com:killtheliterate/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"
    ```

03. Link configurations:

    ```console
    setopt EXTENDED_GLOB
    for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
      ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
    done
    ```

    **Note:** If you already have any of the given configuration files, `ln` in
    the above operation will cause an error. In simple cases, you can load
    Prezto by adding the line `source "${ZDOTDIR:-$HOME}/.zprezto/init.zsh"` to
    the bottom of your _`${ZDOTDIR:-$HOME}/.zshrc`_ and keep the rest of your
    Zsh configuration intact. For more complicated setups, we recommend that you
    back up your original configs and replace them with the provided Prezto
    [_`runcoms`_][10].

04. Set Zsh as your default shell:

    ```console
    chsh -s /bin/zsh
    ```

