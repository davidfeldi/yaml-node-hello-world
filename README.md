# yaml-node-hello-world
E2E use cases - YAML

Test case 1
```
Summary:  Build a service with dockerfile and push to dockerhub when “push to docker registry” has been activated
Expected result: Image should be created. Steps build-prj, push-dockerhub should be passed.
```

Test case 2
```
Summary: Build a service with dockerfile and push to dockerhub when “push to docker registry” hasn’t been activated
Expected result: Image should be created. The step push-dockerhub should be failed.
```

Create post request to:  https://g-staging.codefresh.io/api/workflow/codefresh-io/yaml-node-hello-world/file

Header:
```
X-Access-Token: your token
Content-Type: application/json
```

Body:
```json
{
 "revision": "test-case-4",
 "variables":{
  "DOCKERHUB_USER":"username"
 }
}
```
