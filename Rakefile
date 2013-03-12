# Standard Library
require 'rbconfig'

# Gems
require 'rake'
require 'rack'
require 'rack-rewrite'
require 'thin'

# Static files directory
DIR = "static"

# Port number
PORT = "9292"

# Check OS (for the "open" task)
def darwin?
  RbConfig::CONFIG["host_os"] =~ /darwin/i
end

def windows?
  RbConfig::CONFIG["host_os"] =~ /mswin|mingw|windows/i
end

# Set "rake server" as default
task :default => :server

# rake server
desc "Start the server"
task :server do
  site = Rack::Builder.new do 
    use Rack::Rewrite do
      rewrite "/", "/index.html"
    end
    run Rack::Directory.new(DIR)
  end
  puts ">> Serving: #{DIR}/"
  Rack::Handler::Thin.run(site, :Port => PORT)
end

# rake serve (alias for "server" task)
task :serve do
  Rake::Task[:server].invoke
end

# rake open
desc "Open the default port in a web browser"
task :open do
  if windows?
    system "start http://localhost:#{PORT}/"
  elsif darwin?
    system "open http://localhost:#{PORT}/"
  else
    system "xdg-open http://localhost:#{PORT}/"
  end
end

# rake launch (may require a browser refresh)
desc "Open the default port in a web browser and start the server"
task :launch do
  Rake::Task[:open].invoke
  Rake::Task[:server].invoke
end
