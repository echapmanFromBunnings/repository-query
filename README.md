# repository-query actions
Action to query for repositories by topic using a token

Action provides details back in a format that works with a [matrix](https://docs.github.com/en/actions/using-jobs/using-a-matrix-for-your-jobs)
that can work with other processes I've listed [here](https://medium.com/@ericchap/how-to-centralize-your-workflow-management-in-github-4ee49283790c)

```
- uses: echapmanFromBunnings/repository-query@v1.3
  id: get-repos
  with:
    repo-owner: 'echapmanFromBunnings'
    repo-token: ${{ secrets.GITHUB_TOKEN }}
    topic-filter: 'team-a'
- name: Get result
  run: echo "${{steps.get-repos.outputs.repojson}}"
```
