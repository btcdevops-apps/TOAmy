message "Thanks @#{github.pr_author}!"

if github.pr_body.length == 0
    fail "Please provide a summary in the Pull Request Description."
end

if git.lines_of_code > 500
    warn "Please consider breaking up this pull request."
end

if github.pr_labels.empty?
    warn "Please add label(s) to this PR."
end

if git.deletions > git.additions
    message "Code Cleanup!"
end

if !git.modified_files.include?("README.md")
    warn "Your changes has not been documented in the README.md file"
end