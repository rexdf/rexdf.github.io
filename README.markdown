# Instal on Cygwin Note
##Make sure	install posix-spawn 0.3.6

	git clone git://github.com/rtomayko/posix-spawn.git
	git reset --hard 2d67c5e6eea5fe50823ca864639b5ae1e25928e3
	gem build posix-spawn.gemspec
	gem install posix-spawn-0.3.6.gem

##0.5.2 will cause error in Chinese
gem uninstall 
gem uninstall pygments.rb --version "=0.5.2"

## change dependency

Gemfile

	source "https://rubygems.org"
	
	group :development do
	  gem 'rake', '~> 0.9'
	  gem 'jekyll', '~> 0.12'
	  gem 'rdiscount', '~> 2.0.7'
	  gem 'pygments.rb', '~> 0.3.4'
	  gem 'RedCloth', '~> 4.2.9'
	  gem 'haml', '~> 3.1.7'
	  gem 'compass', '~> 0.12.2'
	  gem 'sass', '~> 3.2'
	  gem 'sass-globbing', '~> 1.0.0'
	  gem 'rubypants', '~> 0.2.0'
	  gem 'rb-fsevent', '~> 0.9'
	  gem 'stringex', '~> 1.4.0'
	  gem 'liquid', '~> 2.3.0'
	  gem 'json','1.8.1'
	  gem 'kramdown'
	end
	
	gem 'sinatra', '~> 1.4.2'

..

##change _config.yaml

##change source

##rake update note

use `bundle exec rake generate` but not `rake generate`