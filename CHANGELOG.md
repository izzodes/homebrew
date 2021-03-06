homebrew Cookbook CHANGELOG
===========================
This file is used to list changes made in each version of the homebrew cookbook.

v1.12.0 (2015-01-29)
--------------------

- #67 Add attribute and recipe for installing homebrew taps

v1.11.0 (2015-01-12)
--------------------

- #59 Update Homebrew Cask if auto-update attribute is true
- #52 Manage Homebrew Cask's install directories
- #56 Fix check for existing casks
- #61 Fix owner class for Chef 12
- Depend on build-essential cookbook 2.1.2+ to support OS X 10.10
- #64, #66 add and fix ChefSpec tests for default recipe

v1.10.0 (2014-12-09)
--------------------

- #55 This cookbook no longer sets its `homebrew_package` as the
   `package` provider for OS X when running under Chef 12
- List CHEF as the maintainer instead of Chef.

v1.9.2 (2014-10-09)
-------------------

Bug Fixes:

- #57 Update url per homebrew error: Upstream, the homebrew project
   has changed the URL for the installation script. All users of this
   cookbook are advised to update to this version.

v1.9.0 (2014-07-29)
-------------------

Improvements:

- #35 Modernize the cask provider (use why run mode, inline resources)
- #43 Use `brew cask list` to determine if casks are installed
- #45 Add `default_action` and print warning messages on earlier
   versions of Chef (10.10)

New Features:

- #44 Add `:install` and `:uninstall` actions and alias previous `:cask`,
  `:uncask` actions to them

Bug Fixes:

- #27 Fix name for taps adding the `/homebrew` prefix
- #28 Set `RUBYOPT` to `nil` so Chef can execute in a bundle (bundler
   sets `RUBYOPT` and this can cause issues when running the
   underlying `brew` commands)
- #40 Fix regex for cask to match current homebrew conventions
- #42 Fix attribute for list of formulas to match the README and
   maintain backward compat for 6 day old version

v1.8.0 (2014-07-23)
-------------------
- Add recipes to install an array of formulas/casks

v1.7.2 (2014-06-26)
-------------------
- Implement attribute to control auto-update


v1.7.0 (2014-06-26)
-------------------
#38 - Add homebrew::cask recipe


v1.6.6 (2014-05-29)
-------------------
- [COOK-3283] Use homebrew_owner for cask and tap
- [COOK-4670] homebrew_tap provider is not idempotent
- [COOK-4671] Syntax Error in README


v1.6.4 (2014-05-08)
-------------------
- Fixing cask provider correctly this time. "brew cask list"


v1.6.2 (2014-05-08)
-------------------
- Fixing typo in cask provider: 's/brew brew/brew/'


v1.6.0 (2014-04-23)
-------------------
- [COOK-3960] Added LWRP for brew cask
- [COOK-4508] Add ChefSpec matchers for homebrew_tap
- [COOK-4566] Guard against "HEAD only" formulae


v1.5.4
------
- [COOK-4023] Fix installer script's URL.
- Fixing up style for rubocop


v1.5.2
------
- [COOK-3825] setting $HOME on homebrew_package


v1.5.0
------
### Bug
- **[COOK-3589](https://tickets.chef.io/browse/COOK-3589)** - Add homebrew as the default package manager on OS X Server

v1.4.0
------
### Bug
- **[COOK-3283](https://tickets.chef.io/browse/COOK-3283)** - Support running homebrew cookbook as root user, with sudo, or a non-privileged user

v1.3.2
------
- [COOK-1793] - use homebrew "go" script to install homebrew
- [COOK-1821] - Discovered version using Homebrew Formula factory fails check that verifies that version is a String
- [COOK-1843] - Homebrew README.md contains non-ASCII characters, triggering same issue as COOK-522

v1.3.0
------
- [COOK-1425] - use new json output format for formula
- [COOK-1578] - Use shell_out! instead of popen4

v1.2.0
------
Chef Software has taken maintenance of this cookbook as the original author has other commitments. This is the initial release with Chef Software as maintainer.

Changes in this release:

- [pull/2] - support for option passing to brew
- [pull/3] - add brew upgrade and control return value from command
- [pull/9] - added LWRP for "brew tap"
- README is now markdown, not rdoc.
