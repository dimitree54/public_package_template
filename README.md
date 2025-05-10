# Private Python Package Template

For private packages hosting we use [CloudSmith](https://cloudsmith.com) because of their generous free tier.

## Using This Template for Your Own Package (e.g., "my_package")

To adapt this template for your new package (let's call it "my_package"):

1.  **Copy or Template the Repository:**
    *   Click the "Use this template" button on GitHub to create a new repository from this template.

2.  **Rename the Package Directory:**
    *   Rename the main package directory in src dir

3.  **Update `pyproject.toml`:**
    *   **`[project].name`**: Change from `"private_package_template"` to `"my_package"`.
    *   **`[project].urls`**: Update `Homepage` and `Repository` URLs to point to your new repository.

4.  **Set up bump version:**
	1.	Go to: https://github.com/settings/personal-access-tokens/new?type=beta
    2.	Set permission "Contents" to Read & Write
    3.  Create a repository secret with the name BUMPVERSION_TOKEN
    4.  It is recommended to make the main branch protected as every push/merge/commit to it will trigger a bump version.

5.  **Set up CloudSmith**
    1. Create a new repository (which will store your packages from this GitHub repository), preferable with the name of package (my_name)
       1. If you just created an account, you will create your first repository as part of onboarding
       2. If you already have an account, then go to https://app.cloudsmith.com/dimitree54/repositories
    2. Use this new repo name in the file ci_cd.yml as a CloudSmith repo name
    3. Go to https://app.cloudsmith.com/settings/api-keys, generate the API key 
    4. Create a repository secret with the name CLOUDSMITH_API_KEY

6.  **Once you push anything to master, a new tag will be created, built, and published to cloudsmith


## Installing Your Published Private Package

In the CloudSmith GUI you can get an extra_url and instructions that will help you to install your package
