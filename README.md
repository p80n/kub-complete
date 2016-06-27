# kub-complete
Command-line completion for Kubernetes

## Installation
For the full git experience:
```shell 
git clone https://github.com/p80n/kub-complete.git ~/.kub-complete
```
Else, no cruft, just the file please:
```shell
mkdir ~/.kub-complete && curl -o ~/.kub-complete/kub-complete https://raw.githubusercontent.com/p80n/kub-complete/master/kub-complete 
```
Note: The file can be downloaded wherever suits you best - just be sure to update `SCRIPT_HOME` in the `kub-complete` file appropriately if you don't go with the default. The script does create a directory for caching under $SCRIPT_HOME/cache - so you'll want some place "out of the way" to avoid cruftiness.

You'll need to source in the file from above:
```shell
~>source ~/.kub-complete/kub-complete
```
This will add a new command (technically a function) to your shell: `kub`. This lets you easily switch back to an unadulterated `kubectl` by just using the full `kubectl` command, should `kub` somehow interfere with default functionality. 

Add the above line to your `~/.bash_profile` or `~/.bashrc` to make the command available with every login.


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
~>kub exec <tab><tab>
master-pod-13kk3
worker-pod-2941k
worker-pod-12asd

~>kub exec worker<tab>
worker-pod-2941k
worker-pod-12asd

~>kub exec worker-pod-
```



