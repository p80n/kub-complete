# kub-complete
Command-line completion for Kubernetes

## Installation
For the full git experience:
```shell 
git clone https://github.com/p80n/kub-complete.git ~/.kub-complete
```
Just the file please:
```shell
mkdir ~/.kub-complete && curl -o ~/.kub-complete/kub-complete https://raw.githubusercontent.com/p80n/kub-complete/master/kub-complete 
```
Note: File can be downloaded wherever suits you best - just be sure to update SCRIPT_HOME in the `kub-complete` file.

You'll need to source in the file from above:
```shell
~>source ~/.kub-complete/kub-complete
```
Add the above line to your `~/.bash_profile` or `~/.bashrc` to have this done automatically with every login.


## Usage
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
