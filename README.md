# go-library-template
A template repository for go libraries. Layout should follow the layout standard https://github.com/golang-standards/project-layout.

Includes settings, codeowners, pull request, and release workflows.

## Usage
1. Change the module name in go.mod
2. Delete pkg/example.go
3. Add your own code in pkg/

Release strategy:
1. Branch from main
2. Create a PR following conventional commits. The PR workflow ensures this. Release version is dictated by what the PR name is prefixed with:
   1. `fix:` - patch version
   2. `feat:` - minor version
   3. `fix!:` or `feat!:` - major version, this indicates a breaking change.
3. On merge, the version is bumped appropriately, a tag and release are created, and the changelog is updated. The first version will be `1.0.0`
