# Prérequis
## Installer gem
### macOS
```gem``` est présent par défaut
### distro basée sur debian
```bash
sudo apt update
sudo apt install ruby-full build-essential zlib1g-dev
echo '# Install Ruby Gems to ~/.gem' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/.gem"' >> ~/.bashrc
echo 'export PATH="$HOME/.gem/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
## Installer bundle
```bash
gem install bundler
```
# Installation
```bash
bundle install
```
# Exécution
```bash
bundle exec jekyll serve
```