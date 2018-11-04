My (Marko10_000) flatpak build scripts.

Sources
=======

Original source:

	https://git.marko10-000.de/flatpaks/flatpak

Github-Mirror:

	https://github.com/Marko10-000/flatpaks

Packages
========

Planed:
-------

- Clonk Rage (with popular packs as extension?)
- OpenClonk
- Wine-applications (perhaps using [Winepak](https://github.com/winepak/winepak-sdk-images))

Contains:
---------

- [CodeLite](https://codelite.org/) (org.codelite.CodeLite)
- [Kodi](https://kodi.tv/) (tv.kodi.Kodi)
	- SMB-support (samba) isn't added (will be added in the future)
	- Airplay-support isn't added (will be added in the future)
	- Bluetooth-support isn't added (will be added in the future)
	- Blu-ray-support isn't added (will be added in the future)
	- Remote control-support isn't added (has somebody the hardware for it?)
	- Extension: inputstream libs aren't add (coming soon)

Get a flatpak
=============

Download from my server
-----------------------

Replace **\<app\>** with the wanted app name (e.g. for CodeLite replace it with
*org.codelite.CodeLite*)

```bash
$ flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
$ flatpak remote-add --if-not-exists marko10_000 https://build.marko10-000.de/marko10_000.flatpakrepo
$ flatpak install --assumeyes marko10_000 <app>
```

Build it on your own
--------------------

Replace in the second command **\<build folder\>** and **\<file\>**.
**\<file\>** should be replaced with the wanted *app.yaml*. **\<build folder\>**
should be an empty folder (doesn't have to exists).

```bash
$ flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
$ flatpak-builder --install --user --install-deps-from=flathub <build folder> <file>
```
