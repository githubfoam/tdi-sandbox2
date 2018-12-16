require 'rake/testtask'

# run tests
task default: [:lint, 'test:check']

namespace :test do
  # run inspec check to verify that the profile is properly configured
  task :check do
    dir = File.join(File.dirname(__FILE__))
    sh("bundle exec inspec check #{dir}")
  end
end

# Automatically generate a changelog for this project. Only loaded if
# the necessary gem is installed. By default its picking up the version from
# inspec.yml. You can override that behavior with s`rake changelog to=1.2.0`
begin
  require 'yaml'
#  metadata = YAML.load_file('inspec.yml')
#  v = ENV['to'] || metadata['version']
#   puts "Generate changelog for version #{v}"
#   require 'github_changelog_generator/task'
#   GitHubChangelogGenerator::RakeTask.new :changelog do |config|
#     config.future_release = v
#   end
# rescue LoadError
#   puts '>>>>> GitHub Changelog Generator not loaded, omitting tasks'
end
