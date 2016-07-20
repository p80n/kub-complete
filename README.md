# kub-complete
Command-line completion for Kubernetes

## Installation
For the full git experience:
```shell 
git clone https://github.com/p80n/kub-complete.git ~/.kub-complete
```
Or just the file:
```shell
mkdir ~/.kub-complete && curl -o ~/.kub-complete/kub-complete https://raw.githubusercontent.com/p80n/kub-complete/master/kub-complete 
```
Note: The file can be downloaded wherever suits you best - just be sure to update `SCRIPT_HOME` in the `kub-complete` file appropriately if you don't go with the default. The script does create a directory for caching under $SCRIPT_HOME/cache - so you'll want some place "out of the way" to avoid cruftiness.

You'll need to source in the file from above:
```shell
~>source ~/.kub-complete/kub-complete
```
This will add a new command (technically a function) to your shell: `kub`. This lets you easily switch back to an unadulterated `kubectl` by just using the full `kubectl` command, should `kub` somehow interfere with default functionality. 

Note: If you want to use this command in other commands/scripts, you'll need to `export -f kub` (I believe that is a bash-only feature).

Add the above line to your `~/.bash_profile` or `~/.bashrc` to make the command available with every login.


## Usage
### Configuration
The `kub` function will automatically try to utilize kubectl configuration files if available. It will first check for the existence of a `kubeconfig` file in the current working directory. If no file is found, it will fall back to `~/.kube/config` (the same as the default location for the `kubectl` command). This is intended to just save some typing, and you can always override this behavior by supplying the `--kubeconfig=/path/to/config` argument to `kub`.

### Tab Completion
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

