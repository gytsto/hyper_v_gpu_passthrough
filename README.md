# hyper_v_gpu_passthrough
Passthrough gpu support to hyper-v virtual machine.
## how to run
```
powershell .\gpu_passthrough.ps1 vm_name
```

## dll migration
On your host machine, go to `C:\Windows\System32\DriverStore\FileRepository\`
and copy the `nv_dispi.inf_amd64` folder to `C:\Windows\System32\HostDriverStore\FileRepository\` on your VM (This folder will not exist, so make sure to create it)
Next you will need to copy `C:\Windows\System32\nvapi64.dll` file from your host to `C:\Windows\System32\` on your VM
And once that is done, you can restart the VM.

## if failed to run script, try running
```
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
ir this
```
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

# reference
https://www.reddit.com/r/sysadmin/comments/jym8xz/gpu_partitioning_is_finally_possible_in_hyperv/
