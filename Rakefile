desc "SSH into a service. Defaults to 'web'."
task :ssh do
  service = ENV.fetch('SERVICE', 'web')
  sh "docker-compose exec #{service} bash"
end

desc "Launch IRB"
task :irb do
  sh "docker-compose exec web irb"
end

desc "Run a Rails command, e.g. rake rails CMD=version"
task :rails do
  cmd = ENV.fetch('CMD', 'version')
  sh "docker-compose exec web rails #{cmd}"
end
