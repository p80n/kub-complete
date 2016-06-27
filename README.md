# kub-complete
command-line completion for kubernetes

To use, you'll need to source in the file 'kubcomplete':
```shell
~>source ~/.kub-complete/kub-complete
```

Tab completion is currently supported for the following kubernetes commands:
* get
* describe
* exec
* logs
* rc
* rolling-update
* services

For example:
```shell
~>kubectl exec <tab><tab>
master-pod-13kk3
worker-pod-2941k
worker-pod-12asd

~>kubectl exec worker<tab>
worker-pod-2941k
worker-pod-12asd

~>kubectl exec worker-pod-
```
