#require 'puppetlabs_spec_helper/rake_tasks'

#require 'puppet-lint'

#PuppetLint.configuration.ignore_paths = ["pkg/**/*.pp", "spec/fixtures/**/*.pp"]
#PuppetLint.configuration.send('disable_class_parameter_defaults')
#PuppetLint.configuration.send('disable_80chars')
#PuppetLint.configuration.send('disable_quoted_booleans')
#PuppetLint.configuration.send('disable_documentation')
#PuppetLint.configuration.send('disable_class_inherits_from_params_class')


desc 'run static analysis with rubocop'
task(:rubocop) do
  if RUBY_VERSION =~ /^2\.[0-9]\.[0-9]/
    require 'rubocop'
    cli = RuboCop::CLI.new
    exit cli.run(%w(-D -f s))
  else
    puts "Rubocop is disabled in ruby < 2.0.0"
  end
end
