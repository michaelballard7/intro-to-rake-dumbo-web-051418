
task :environment do
  require_relative './config/environment'
end


# a namespace for greeting:

namespace :greeting do

  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'output hola to the terminal'
  task :hola do
    puts 'hola de Rake'
  end

end


# a namespace for database automation

namespace :db do

  desc 'migrate changes to my database'
    task :migrate => :environment do
      Student.create_table
    end

    desc 'seed the database with some dummy data'
    task :seed do
      require_relative './db/seeds.rb'
    end
  end

  # a task for a pry console:

  desc 'drop into the Pry console'
  task :console => :environment do
    Pry.start
  end
