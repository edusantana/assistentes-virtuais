require 'rake/clean'

directory 'tmp'

desc "Cria a página html"
task :html => ['tmp']do
  sh "claat export -o tmp/ -prefix '/assistentes-virtuais/' secitec-2018.md"

  puts "Criando conteúdo em tmp/"
end

task :default => [:html]

desc 'Serve localmente arquivo gerado'
task 'serve' do
  Dir.chdir('tmp') do
    sh "claat serve"
  end
end

desc 'Gera documentação em docs'
task :docs => ['tmp/secitec-2018/index.html'] do
  FileUtils.cp_r 'tmp/.', 'docs'
end
