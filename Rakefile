namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts 'hola de Rake!'
  end
end

desc 'Configure environment'
task :environment do
  require_relative 'config/environment.rb'
end

desc 'Start up pry'
task :console => :environment do
  Pry.start
end

namespace :db do
  'migrate changes into database'
  task :migrate => :environment do
    Student.create_table
  end

  'seed data'
  task :seed do
    require_relative './db/seeds.rb'
  end

end