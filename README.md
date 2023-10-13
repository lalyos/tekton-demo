test chart to create a tektotn task which uses a script 

## distribute

ttl.sh is a temporary OCI image repo, whitout authentication
```
helm package .
helm push tekton-demo-0.1.1.tgz oci://ttl.sh/demo
```

## Use

```
helm template delme oci://ttl.sh/demo/tekton-demo
```


## test on k8s
```
kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml

helm upgrade -i delme oci://ttl.sh/demo/tekton-demo
```

```