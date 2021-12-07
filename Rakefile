task :deploy do
  sh "cd _site; git init; git remote add origin https://github.com/AnabelCP/AnabelCP.github.io; touch .nojekyll; git add .; git commit -am new-deploy; git push -u --force origin master"
  end