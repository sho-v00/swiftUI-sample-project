
# Make it more obvious that a PR is a work in progress and shouldn't be merged yet
warn("PR is classed as Work in Progress") if github.pr_title.include? "WIP"


# Many changes, make less them or divide pr.
warn("Too match changes. Please divide PR.") if git.lines_of_code > 500

# Merge commits are found
if git.commits.any? { |c| c.message =~ /^Merge branch 'master'/ }
  warn 'Please rebase to get rid of the merge commits in this PR'
end
