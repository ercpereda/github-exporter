# Metrics

Below are an example of the metrics as exposed by this exporter.

```
# HELP github_rate_limit Number of API queries allowed in a 60 minute window
# TYPE github_rate_limit gauge
github_rate_limit{account="myaccount@example.com"} 5000
# HELP github_rate_remaining Number of API queries remaining in the current window
# TYPE github_rate_remaining{account="myaccount@example.com"} gauge
github_rate_remaining 2801
# HELP github_rate_reset The time at which the current rate limit window resets in UTC epoch seconds
# TYPE github_rate_reset{account="myaccount@example.com"} gauge
github_rate_reset 1.527709029e+09
# HELP github_repo_forks Total number of forks for given repository
# TYPE github_repo_forks gauge
github_repo_forks{account="myaccount@example.com",archived="false",fork="false",language="Go",license="mit",private="false",repo="github-exporter",user="infinityworks"} 19
# HELP github_repo_open_issues Total number of open issues for given repository
# TYPE github_repo_open_issues gauge
github_repo_open_issues{account="myaccount@example.com",archived="false",fork="false",language="Go",license="mit",private="false",repo="github-exporter",user="infinityworks"} 7
# HELP github_repo_size_kb Size in KB for given repository
# TYPE github_repo_size_kb gauge
github_repo_size_kb{account="myaccount@example.com",archived="false",fork="false",language="Go",license="mit",private="false",repo="github-exporter",user="infinityworks"} 41
# HELP github_repo_stars Total number of Stars for given repository
# TYPE github_repo_stars gauge
github_repo_stars{account="myaccount@example.com",archived="false",fork="false",language="Go",license="mit",private="false",repo="github-exporter",user="infinityworks"} 64
# HELP github_repo_watchers Total number of watchers/subscribers for given repository
# TYPE github_repo_watchers gauge
github_repo_watchers{account="myaccount@example.com",archived="false",fork="false",language="Go",license="mit",private="false",repo="github-exporter",user="infinityworks"} 10
# TYPE github_repo_release_downloads gauge
github_repo_release_downloads{account="myaccount@example.com",name="release1.0.0",repo="github-exporter",user="infinityworks"} 3500
```

<!--

The above output was generated by running:

```
REPOS=infinityworks/github-exporter GITHUB_ACCOUNT="myaccount@example.com" go run main.go
```

And copying the output of http://localhost:9171/metrics

 -->
