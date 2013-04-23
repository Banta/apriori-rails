#!/usr/bin/env rake

require File.expand_path('../config/requirements', __FILE__)
require File.expand_path('../config/hoe', __FILE__) # setup Hoe + all gem configuration

class Rake::Task
  def abandon
    prerequisites.clear
    @actions.clear
  end
end

Dir['tasks/**/*.rake'].each { |rake| load rake }

Rake::Task[:default].abandon
task :default => :extension 

