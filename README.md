requires freedesktop sdk v24.08
```
flatpak install flathub org.freedesktop.Sdk 24.08
```

build for testing:
```
flatpak-builder --force-clean --user --repo=repo --install builddir com.itgmania.ITGmania.yml
```

