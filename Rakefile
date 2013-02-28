# http://qubitlogs.com/Workflow/2013/01/22/jekyll-blogging-reference-and-perfect-workflow-guide/

task :deploy do
  puts "rsync -avz --progress --stats -e ssh --delete _site/ wbzyl@sigma.ug.edu.pl:public_html/blog/"
  # rsync [OPTIONS] ]SOURCE DESTINATION
  sh "rsync -avz --progress --stats -e ssh --delete _site/ wbzyl@sigma.ug.edu.pl:public_html/blog/"
end
