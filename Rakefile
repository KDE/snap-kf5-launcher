task :'kde-frameworks-5-env_all.tar.xz' do
  name = 'kde-frameworks-5-env_all.tar.xz'
  sh 'ls -lahR kde-frameworks-5-env'
  sh "tar --exclude=._empty -cJf #{name} kde-frameworks-5-env"
  sh "tar -tvf #{name}"
end
task :tar => :'kde-frameworks-5-env_all.tar.xz'
task :default => :tar
