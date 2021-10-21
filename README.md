# hyper_v_gpu_passthrough
Passthrough gpu support to hyper-v virtual machine.
## how to run
```
powershell .\gpu_passthrough.ps1 vm_name
```

## if failed to run script, try running
```
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

# reference
https://www.reddit.com/r/sysadmin/comments/jym8xz/gpu_partitioning_is_finally_possible_in_hyperv/