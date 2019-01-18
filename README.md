# KubePloy

[![Join the chat at https://gitter.im/KubePloy/community](https://badges.gitter.im/KubePloy/community.svg)](https://gitter.im/KubePloy/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

CLI tool to update your images on your deployments

## Install
```
npm i -g kubeploy
```

## Help
```
Usage:  [options] [command]

Options:
  -h, --help                              output usage information

Commands:
  deploy <deployment> <registry> <image>  Deploy your image to the deployment in your cluster and update it
  update-image <registry> <image> <path>  Update and push your image to your registry
```

## Example

```
kubeploy update-image gcr.io/test-test server_image . && kubeploy server_app gcr.io/test-test server_image
```

Is the same as

```
kubeploy update-image gcr.io/test-test server_image . -d server_app
```
