desc "SSH into a service. Defaults to 'web'."
task :ssh, [:service] do |_t, args|
  args.with_defaults(service: 'web')
  sh "docker-compose exec #{args[:service]} bash"
end

desc "Launch IRB"
task :irb do
  sh "docker exec web irb"
end

desc "Launch Rails Console"
task :console do
  sh "docker exec web rails console"
end
