# repo-example_manifest

Example android repo manifest

## License

This project is licensed under the Unlicense and released into the public
domain.  Any contributions submitted by pull request are similarly licensed
under the Unlicense.  Users are free to reuse this work for commercial or other
applications.

## Manifests

The 'Android repo' tool, hereafter called repo, works from manifest files.  The
manifest tells what git projects to track, where to obtain the source, and what
refs to check out.

## Overview / Usage

This manifest project provides a working example of using Android repo.  It was
created during reaper development to provide a suitable development and test
target since other, freely available repo instances are far more complicated
than what was necessary or helpful.

As documented at https://source.android.com/setup/develop and other sources, a
repo project is checked out as follows:

1. Create and change to the project directory:
```bash
mkdir ~/code/repo-example
cd ~/code/repo-example
```

2. Initialize repo using the manifest remote URL:
```bash
repo init -u https://github.com/openology/repo-example_manifest.git # read-only
```
Note: repo init creates a .repo directory and sets up tracking information, but
does not check out the tracked projects.

3. Execute `repo sync`:
```bash
repo sync  # actually clones - or updates - git projects
```

TODO: replicate, adapt, or summarize the CC0 instructions at
https://www.instructables.com/id/Using-Googles-repo-command-in-your-own-projects/