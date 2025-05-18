# nix-single-user-mac
Instructions installing nix single user on Mac - hack

First run ./create-darwin-volume.sh. This is patched version of the nix github pages darwin volume creator.
I checked all sudo usages, looks clean. 

From here on out no more sudo

```
curl -L https://nixos.org/nix/install > nixinstall
```

Modify nixinstall to not run the script, jsut echo
Make cleanup a no-op


Get the temp install script and delete the guards around darwin
```sudo chown -R $(whoami) /nix``` <- real last sudo, take ownership of volume
rerun the install script with flag ' --no-daemon'



