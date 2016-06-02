# kub-complete
command-line completion for kubernetes

To use, you'll need to source in the file 'kubcomplete':
```shell
~>source kub-complete/kubcomplete```

Then when running *describe* or *exec* commands, you'll be able to tab complete to fill the pod ID you want to use.

```shell
~>kubectl exec <tab><tab>
master-pod-13kk3
~>kubectl exec worker<tab>
worker-pod-2941k
worker-pod-12asd
~>kubectl exec worker-pod-```
