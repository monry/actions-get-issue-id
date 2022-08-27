# Get Project Id

Get issue ID by issue number

# Usage

```yaml
- uses: monry/actions-get-issue-id@v1
  with:
    # Personal Access Token that with `org:read` are granted.
    github-token: ${{ secrets.PERSONAL_ACCESS_TOKEN }}
    issue-repository: 'monry/awesome-repository'
    issue-number: 1
```

# Inputs

## `github-token`

This action requires Personal Access Token that `repo` is granted.

For security purposes, it is recommended to register Personal Access Token as Secrets.

## `issue-repository`

Repository name of issue with owner name.

## `issue-number`

Number of issue.

# Outputs

## `issue-id`

Obtained value stores into output variable named `issue-id`.

```yaml
- uses: monry/actions-get-issue-id@v1
  id: get-issue-id # requires `id` to refer output values with after steps
  with:
    github-token: ${{ secrets.PERSONAL_ACCESS_TOKEN }}
    issue-repository: 'monry/awesome-repository'
    issue-number: 100
- run: |
    echo '${{ steps.get-project-id.outputs.project-id }}'
```
