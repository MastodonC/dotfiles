# dotfiles## pre-push and pre-commitTo use:```git checkout https://github.com/MastodonC/dotfilescd dotfiles# this will overwrite any prior pre-commit and pre-push hooks, so append if that suits bettercp -R git_template ~/.git_template# this will set the template directory of gitgit config --global init.templatedir '~/.git_template'```Any future created directories will have the hooks included.For any existing Mastodon C directories (!! important !!) do the following: go to the root of the directory, and do```$(git config --path --get init.templatedir)/../update.sh```This will sync all the hooks with existing git configuration.