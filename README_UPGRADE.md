## Version upgrade
- Clone Sanyaku/trino repository to your local machine
  `dev clone trino`
- Add public trino repository as a remote to your local Sanyaku/trino repository
  `git remote add trinodb/trino https://github.com/trinodb/trino.git`
- Get the tag from public trino repository to your local Sanyaku/trino repository
  `git fetch trinodb/trino tag <tag_number>`
- Push the tag to Sankayu/trino origin  
  `git push origin <tag_number>`
- Create a git branch from the tag
  `git checkout -b <tag_number>-patched <tag_number>`

NOTE: If all tags are fetched in your local Sanyaku/trino repository, you can delete them from local using command:
- `git tag -d $(git tag)`

Important: Cherry-pick the changes from previous version to your new branch before uploading the artifact to JFrog.
