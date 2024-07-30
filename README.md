# EZ:

[Original README](https://github.com/sorin-ionescu/prezto/blob/master/README.md)

### Manual

Prezto will work with any recent release of Zsh, but the minimum required
version is **4.3.11**.

## launch:

    ```console
    zsh
    ```

### clone:

    ```console
    git clone --recursive git@github.com:killtheliterate/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"
    ```

### symlink:

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

### default:

    ```console
    chsh -s /bin/zsh
    ```

### etc::

* install [pyenv](https://github.com/pyenv/pyenv?tab=readme-ov-file#installation)
* install [chruby](https://github.com/postmodern/chruby?tab=readme-ov-file#install)
* install [ruby-install](https://github.com/postmodern/ruby-install?tab=readme-ov-file#install)
* install [n](https://github.com/tj/n?tab=readme-ov-file#installation)
* install [base16-shell](https://github.com/chriskempson/base16-shell)
