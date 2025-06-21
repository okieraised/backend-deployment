## Useful Git Commands

### 1. Rewrite Git Commit
    ```shell
    git reset --soft HEAD~="{{number-of-commits-to-combine}}"
    git commit -m "{{comiit-msg}}"
    git push -f
    ```

### 2. Git submodule
#### 2.1 Add new submodule to repo
    ```shell
    git submodule add
    git submodule update --init --recursive
    git submodule add git@gitlab.com:module_path
    ```
#### 2.2. Remove cached submodule
    ```shell
    git rm --cached module_name
    ```
#### 2.3. remove and readd gitmodule
    ```shell
    git rm mod_name && rm -rf .git/modules/mod_name && \
    git config --remove-section submodule.mod_name && \
    git submodule add mod_name_url mod_name_path
    ```

### 3. Git remote
#### 3.1. View git remote
    ```shell
    git remote -v
    # View existing remotes
    # origin  https://github.com/user/repo.git (fetch)
    # origin  https://github.com/user/repo.git (push)
    ```

#### 3.2. Change remote origin
    ```shell
    git remote set-url origin https://github.com/user/repo2.git
    ```