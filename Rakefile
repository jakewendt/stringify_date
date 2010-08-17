require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

begin
	require 'jeweler'
	Jeweler::Tasks.new do |gem|
		gem.name = "jakewendt-stringify_date"
		gem.summary = %Q{one-line summary of your gem}
		gem.description = %Q{longer description of your gem}
		gem.email = "github@jake.otherinbox.com"
		gem.homepage = "http://github.com/jakewendt/stringify_date"
		gem.authors = ["Jake"]
		# gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings

		# we like to keep our gem slim
		gem.files = FileList['lib/**/*.rb']
		gem.test_files = []
		gem.add_dependency('chronic', '>= 0.2.3')

	end
	Jeweler::GemcutterTasks.new
rescue LoadError
	puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end


desc 'Default: run unit tests.'
task :default => :test

desc 'Test the stringify_date plugin.'
Rake::TestTask.new(:test) do |t|
	t.libs << 'lib'
	t.pattern = 'test/**/*_test.rb'
	t.verbose = true
end

desc 'Generate documentation for the stringify_date plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
	rdoc.rdoc_dir = 'rdoc'
	rdoc.title		= 'StringifyDate'
	rdoc.options << '--line-numbers' << '--inline-source'
	rdoc.rdoc_files.include('README')
	rdoc.rdoc_files.include('lib/**/*.rb')
end
