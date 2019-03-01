desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end


namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end


# desc 'open Pry console'
task :console do
  # Pry.start
end


desc 'load ./config/environment'
task :environment do
  require_relative './config/environment'
end


namespace :db do
  desc 'invokes the :environment task'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'create table with test data'
  task :seed do
    require_relative './db/seeds'
  end
end
