test chart to create a tektotn task which uses a script 

## distribute

ttl.sh is a temporary OCI image repo, whitout authentication
```
helm package .
helm push tekton-demo-0.1.0.tgz oci://ttl.sh/demo
```

## Use

```
helm template delme oci://ttl.sh/demo/tekton-demo
```