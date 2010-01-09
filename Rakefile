$:.unshift('lib')
 
require 'rake/testtask'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |s|
    s.name               = 'aunderwo-roo'
    s.platform           = Gem::Platform::RUBY
    s.email              = 'email2ants@gmail.com' 
    s.homepage           = "http://github.com/aunderwo/roo"
    s.summary            = "based on roo"
    s.description        = "roo can access the contents of OpenOffice-, Excel- or Google-Spreadsheets"
    s.authors            = ['Anthony Underwood','Hugh McGowan','Thomas Preymesser']
    s.files              =  FileList[ "{lib,test}/**/*"]
    s.has_rdoc = true
    s.extra_rdoc_files = ["README.markdown", "History.txt"]
    s.rdoc_options = ["--main","README.markdown"]
    s.add_dependency "spreadsheet", [">= 0.6.4"]
    s.add_dependency "rubyzip", [">= 0.9.1"]
    s.add_dependency "hpricot", [">= 0.6"]
    s.add_dependency "GData", [">= 0.0.4"]
    s.add_dependency "libxml-ruby", [">= 1.1.3"]
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
