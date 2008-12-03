# -*- ruby -*-

require 'rubygems'
require 'hoe'
require './lib/commander.rb'

Hoe.new('commander', Commander::VERSION::STRING) do |p|
  p.developer('TJ Holowaychuk', 'tj@vision-media.ca')
  p.extra_deps << ['highline', '>= 1.5.0']
end

desc 'Build and install gem.'
task :build => [:remove, :install_gem] do
  sh "clear"
end

desc 'Remove build data.'
task :remove => [:clean] do
  sh "clear"
end

desc 'Build and open docs in safari for viewing'
task :read_docs => [:docs] do
  sh "open -a safari doc/index.html"
end

desc 'Run rspec suite.'
task :spec do
  sh "clear"
  sh "spec ./spec/all_spec.rb"
end

desc 'Run rspec suite with specdoc format.'
task :specd do
  sh "clear"
  sh "spec ./spec/all_spec.rb --format specdoc"
end

# vim: syntax=Ruby
