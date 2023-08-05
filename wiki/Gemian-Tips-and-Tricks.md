# Gemian: Tips & Tricks

## Fixes

### Gemian: 'Stretch' repository fix

Gemian, the version of Debian for the Gemini PDA and Cosmo Communicator is (at the the time of writing, July 2023) based on Debian stretch (i.e. Debian version 9). Since this is old and now unsupported, the official .deb repositories have been moved off the main Debian server. This means that users of Gemian stretch will no longer be able to install software with apt.

To fix this, edit the `/etc/apt/sources.list.d/multistrap-debian.list` file (make a backup first!) and change `http.debian.net` to `archive.debian.org`. The new file should look something like:

    deb [arch=arm64] http://archive.debian.org/debian stretch main contrib non-free
    deb-src http://archive.debian.org/debian stretch main contrib non-free

(There may be differences if you added other repositories.)
