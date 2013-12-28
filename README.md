# TODO:
- 100% code coverage

# Guard::Codeception [![Build Status](https://travis-ci.org/colby-swandale/guard-codeception.png?branch=master)](https://travis-ci.org/colby-swandale/guard-codeception)

Guard::Codeception is an extension to the [guard gem](http://guardgem.org/) for the [codeception](http://codeception.com/) testing framework 

## Installation

Add this line to your application's Gemfile:

    gem 'guard-codeception'

And then execute:

    $ bundle

## Example Guardfle

```ruby
guard 'codeception' do
	watch(%r{^.*\.php$})
end
```

## Configuration
The following options can be passed to Guard::Codeception

```ruby
# run only specified suites 		default: [:acceptance, :functional, :unit]
:suites			=> [:acceptence, :custom_suite]

# run specific test group 			default: []
:groups			=> [:foo, :bar]

# enable codeception debug mode 	default: false
:debug 			=> false

# run tests when guard starts		default: false
:test_on_start 	=> false

# path to codecept					default 'codecept'
# if codecept is not avaliable via the PATH you can
# define the path to codecept here. ie: installing codeception
# via composer would be :codecept => 'vendor/bin/codecept'
:codecept		=> '/path/to/codecept'

# extra cli you wish to pass to codeceeption
# ie: config, json or xml output
:cli 			=> false
```

## Usage
- Make sure you have codeception installed in your project via [composer](http://getcomposer.org/)
- Create Guardfile, see example above

```bash
$ guard
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Author

[Colby Swandale](https://github.com/colby-swandale)

