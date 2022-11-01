# Usage

Scoring your Kubernetes manifests with GitHub Actions

```yaml
name: kube-score
on: 
  pull_request:
    branches: [ "master" ]
jobs:
  score:
    name: Score
    runs-on: ubuntu-latest
    steps:
    - name: scoring kubernetes manifests
      uses: marcleibold/kube-score-action@v1
      with:
        # The files to your Kubernetes manifests
        files: "*/*.yaml"
```