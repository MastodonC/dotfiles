# dotfiles## pre-push and pre-commitTo use:```git clone https://github.com/MastodonC/dotfilescd dotfiles# this will overwrite any prior pre-commit and pre-push hooks, so append if that suits bettercp -R git_template ~/.git_template# this will set the template directory of gitgit config --global init.templatedir '~/.git_template'```Any future created directories will have the hooks included.For any existing Mastodon C directories (!! important !!) do the following: go to the root of the directory, and do```$(git config --path --get init.templatedir)/update.sh```This will sync all the .git_template/hooks with existing .git/hooks *it will also delete any pre-existing git hooks, so if you have them a copying approach might be better*Git hooks were largely copied from Neale Swinnerton's dotfiles (https://github.com/sw1nn/dotfiles/tree/master/git_template)## Mac OS X usersMac OS X seems to have an old grep version by default. to fix this, the homebrew version is a solution:```brew install grep --with-default-names```this will replace grep.  Make sure your PATH has /usr/local/bin preceding /usr/bin or /bin