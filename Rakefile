# http://qubitlogs.com/Workflow/2013/01/22/jekyll-blogging-reference-and-perfect-workflow-guide/

task :deploy do
  # rsync [OPTIONS]                               SOURCE DESTINATION
  # rsync -avz --progress --stats -e ssh --delete _site/ wbzyl@sigma.ug.edu.pl:public_html/blog/
  sh "rsync -avz --progress --stats -e ssh --delete _site/ wbzyl@sigma.ug.edu.pl:public_html/blog/"
end
