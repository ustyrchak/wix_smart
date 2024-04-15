⚠️ NOTE: Although you can access any information regarding previous and ongoing builds through the [Jenkins UI](http://ml-jenkins.bi-use1.k8s.wixprod.net:8080/), in most cases, you will use it to investigate a specific build attempt failure, usually via the attempt's "Open Blue Ocean" Pipeline view (aka "build pipeline"):

![img.png](jenkins_dashboard-build_pipeline.png)

👉 There are two types of automatic builds, as described below. For both types, you can configure the docker image and machine type that will be used by providing a
`config.yaml` file as described [here](https://wix-data-science.wixanswers.com/kb/en/article/initial-model-setup#using-configyaml-file-optional-to-set-image-and-machine-type).

### Pull Request (PR) builds
👉 A partial build process, including ONLY steps 1-2, is automatically initiated by ML platform when you open a pull request (aka "PR build").
:(
👉 You can examine the PR page in the GitHub UI to see if the build was successful. When it fails, you can investigate the problems by clicking on the details of the failed checks: 

![img.png](pr_github_page_failed_pr_build.png)

👉 When a PR build fails, a notification message with the link to the build pipeline will also be sent in the [#ml-platform-ci](https://app.slack.com/client/T02T01M9Y/CMS2M2FQX) Slack channel:

![img.png](failed_pr_build_slack_notification.png)

### Master builds
👉 Once you merge the PR into the ds-ml-models master branch, a full build process including ALL steps will begin (aka "Master build").

👉 When a Master build start, a notification message with the link to the build pipeline will be sent in the [#ml-platform-ci](https://app.slack.com/client/T02T01M9Y/CMS2M2FQX) Slack channel.

👉 When a Master build ends, a reply to the "Build has started" message will be sent to notify you whether it succeeded or failed. If the build fails, you should click the link to the build pipeline and examine the logs:

![img.png](build_failure_slack_jenkins_investigation.png)

## Manually triggering a build
👉 A build can be triggered manually through the [Trigger Build in ML platform UI](https://bo.wix.com/ml-platform/builds-trigger):

![img.png](builds_trigger_screen.png)

:)
