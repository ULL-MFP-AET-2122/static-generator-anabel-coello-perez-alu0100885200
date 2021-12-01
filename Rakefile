desc "Remember to set my login in guthub"
task :remember do
  puts "Remember to set the environment variable 'login' in your shell before start!\nWrite this command:\n\teval $(gp env -e login=<your login at github>)"
end

desc "Build and serve your website in folder _site. Use: rake server[<portnumber>] otherwise a random port will be chosen"
task :serve, [:port] do |t, args|
  sh "bundle exec jekyll serve --port #{ args[:port] or Integer(1000+9000*rand())}"
end 

desc "Build your website in folder _site"
task :build do
  sh "bundle exec jekyll build"
end

desc "Watch changes and rebuild web site each time some change occurs"
task :bw do
  sh "bundle exec jekyll build --watch"
end 

desc "Makes the folder '_site' a repo. Use: rake setup[aluXXXX]"
task :setup => [:clean_site, :build] do |t, args|
  sh "cd _site && git init . && git config --global init.defaultBranch master && git add -f . && git remote add origin https://github.com/#{ENV["login"]}/#{ENV["login"]}.github.io"
end

desc "Removes everything inside the folder _site"
task :clean_site do 
  sh "rm -fR _site"
end

task :clean => [:clean_site]

desc "Deploy all the files inside _site to GitHub. Assumes _site is already a repo"
task :deploy => [:setup] do 
  sh "cd _site && git add -f . && git commit -am new-deploy && git push -fu origin master"
end
 
desc "Deploy your web site to github and push the changes in the root repo"
task :default => :deploy do
  sh "git add .; git commit -am new-version; git push -u origin master"
end