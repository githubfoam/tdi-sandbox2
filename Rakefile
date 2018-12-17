require 'rake/testtask'

# run tests
task :default => :test

namespace :test do
  # run inspec check to verify that the profile is properly configured
  task :check do
    dir = File.join(File.dirname(__FILE__))
    sh("bundle exec inspec check #{dir}")
  end
end

begin
  require 'yaml'
end
