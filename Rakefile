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

desc 'has a console'
task :console do
  require_relative './db/console'
end

namespace :db do
  desc 'migrate changes to database'
  task :environment do
    require_relative './config/environment'
  end

  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds'
  end


  desc 'drop into the Pry console'
  task :console => :environment do 
    Pry.start
  end

end
