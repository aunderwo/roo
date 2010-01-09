$:.unshift('lib')
 
require 'rake/testtask'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name               = 'aunderwo-roo'
    gem.platform           = Gem::Platform::RUBY
    gem.email              = 'email2ants@gmail.com' 
    gem.homepage           = "http://github.com/aunderwo/roo"
    gem.summary            = "based on roo"
    gem.description        = "roo can access the contents of OpenOffice-, Excel- or Google-Spreadsheets"
    gem.authors            = ['Anthony Underwood','Hugh McGowan','Thomas Preymesser']
    gem.files              =  FileList[ "{lib,test}/**/*"]

    gem.add_dependency "spreadsheet", [">= 0.6.4"]
    gem.add_dependency "rubyzip", [">= 0.9.1"]
    gem.add_dependency "hpricot", [">= 0.6"]
    gem.add_dependency "GData", [">= 0.0.4"]
    gem.add_dependency "libxml-ruby", [">= 1.1.3"]
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler not available. Install it with: sudo gem install technicalpickles-jeweler -s http://gems.github.com"
end

Rake::TestTask.new do |t|
  t.libs << "test"
  t.test_files = FileList['test/test_roo.rb']
  t.verbose = true
end


task :default => :test
