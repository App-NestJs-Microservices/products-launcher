Dev

    Clone the reporsitory
    Create an .env file based on .env.template
    Run the following command  docker compose up --build

### Steps to create Git Submodules

1. Create a new repository on GitHub
2. Clone the repository to the local machine
3. Add the submodule, where 'reposityory_url' is the URL of repository and 'directory_name' is the name of the folder where you want the submodule to be stored (it should not already exist in the project).
```
git submodule add <repository_url> <directory_name>
```
4. Add the changes to the repository (git add, git commit, git push)
Example:
```
git add .
git commit -m "Add submodule"
git push
```
5. Initialize and update submodules, where someone clone the repository for the first time, they should run the following command to initialize and update the submodules
```
git submodule update --init --recursive
```
6.  To update the references of the submodules
```
git submodule update --remote
```


## Important
If you are working in the repository that has the submodules, **first update and push in the submodule** and then in the main repository

If done reverse, the references of the submodules in the main repository will be lost and conflicts will need to be resolved