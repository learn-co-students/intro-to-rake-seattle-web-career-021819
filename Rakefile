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

task :environment do
  require_relative './config/environment'
end


namespace :db do
  #we make :migrate depend on our :environment command w/ =>
  #and then this  will run our create_table fn from the student.rb file
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  #this actually runs the seeds.rb file which runs our create fn to seed our databse
  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end  

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end

