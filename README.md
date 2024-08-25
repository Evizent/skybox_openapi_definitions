docker run --rm -v "${PWD}:/local" openapitools/openapi-generator-cli generate -i /local/skybox-openapi-v3.0.1.json -g python -o /local/out --git-host github.com --git-repo-id skybox_openapi_client --git-user-id Evizent -p packageName=skybox_openapi_client -p projectName=skybox_openapi_client -p packageVersion=1.0.1

using a local image `test_openapi_gen` that combines a few PRs that fix the current version. In a few weeks, the official images shouldbe updated. I may continue to use it: 

docker run --rm -v "${PWD}:/local" test_openapi_gen generate -i /local/skybox-openapi-v3.0.1.json -g python -o /local/out --git-host github.com --git-repo-id skybox_openapi_client --git-user-id Evizent -p packageName=skybox_openapi_client -p projectName=skybox_openapi_client -p packageVersion=1.0.1
