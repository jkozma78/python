# python
if a pyhon code edit a file, extensions like "txt" or "csv"
you need to add, commit and push it to the specified folder with github actions in the workflow yml file.

- name: Commit files
      run: |
        git config --local user.email "jkozma@freestart.hu"
        git config --local user.name "jkozma78"
        git add .
        git commit -m "Add changes" -a
    - name: Push changes
      uses: ad-m/github-push-action@master
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        branch: ${{ github.ref }}
