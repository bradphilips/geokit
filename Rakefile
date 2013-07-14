require "bundler/gem_tasks"
require 'rake/testtask'
require 'rake/clean'

CLEAN.include('*.gem')
CLOBBER.include('pkg')

task :default => :build

Rake::TestTask.new do |t|
  t.libs << "test"
  t.test_files = FileList['test/test*.rb']
  t.verbose = true
end

desc "Generate SimpleCov test coverage and open in your browser"
task :coverage do
  ENV['COVERAGE'] = 'true'
  Rake::Task['test'].invoke
end
