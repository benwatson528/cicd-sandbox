# CICD Sandbox


## Release Process

To release an update of the plugin:

1. Create a `release/x.y.z` branch.
2. Update the `changeNotes` in `build.gradle`.
3. Merge the branch into `master`.
4. Create and push a tag:
    ```
   git tag -a vx.y.z -m "Create release tag vx.y.z"
   git push origin --tags
   ```
5. The "Create Release" GitHub Action will automatically run and do the following:

   - Create a Release in GitHub,
   - Build and upload the plugin zip to both the GitHub Release and GitHub Packages,
   - Increment the version of the project and commit the incremented version to `build.gradle` and `plugin.xml`

The new plugin zip must still be manually uploaded to the IntelliJ marketplace.
