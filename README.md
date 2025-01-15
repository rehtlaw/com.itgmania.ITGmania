```
git submodule update --init --recursive
```

requires freedesktop sdk v24.08
```
flatpak install --include-debug flathub org.freedesktop.Sdk 24.08
flatpak install flathub org.freedesktop.Platform 24.08
```

build for testing:
```
flatpak-builder --force-clean --user --repo=repo --install builddir com.itgmania.ITGmania.yml
```

also make sure to install the Debug symbols if you want to debug with gdb

it will be in a local repo (mine was called `itgmania-origin`)
```
flatpak install itgmania-origin com.itgmania.ITGmania.Debug
```

```
flatpak run --devel --command=sh com.itgmania.ITGmania
gdb /app/itgmania/itgmania
```
