# k8s-yaml
編輯 `metadata.annotations.command` 的內容，即可將指定的命令 Run 在 Kubernetes 的每一台 Node 上

```
  annotations:
    command: &cmd sudo podman load < image.tar.gz
```

> `&cmd` 不要刪掉，在 `template.spec.initContainers.command`:`bash -c *cmd` 會用到
