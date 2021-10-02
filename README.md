# yum-rt

## About this plugin
`yum-rt` is a plugin for the JFrog CLI that allows it to interact with the yum and dnf package managers.
The purpose is to give individual users the ability to install packages from Artifactory repositories requiring authentication without leaving a plain-text copy of their API key in a world-readable location.

## Installation with JFrog CLI
Installing the latest version:

`$ jfrog plugin install yum-rt

Installing a specific version:

`$ jfrog plugin install yum-rt@version`

Uninstalling a plugin

`$ jfrog plugin uninstall yum-rt`

## Usage
### Commands
#### Commands specific to this plugin
 * add-repo
    - Arguments:
        - name - The name of the person you would like to greet.
        - path - The Artifactory path of the repository
    - Flags:
        - gpgkey - The Artifactory path or system path of the GPG key
        - gpgcheck - default yes if gpgkey provided
        - enabled - default yes
    - Example:
    ```
  $ jfrog yum-rt add-repo epel epel/7/x86_64 --gpgkey epel/RPM-GPG-KEY-EPEL-7
  epel repository added.
  ```
 * rm-repo
    - Arguments:
        - name - The name of the repository to remove
    - Example:
    ```
 $ jfrog yum-rt rm-repo epel
 epel repository removed.
 ```
 * enable-repo
    - Arguments:
        - name - The name of the repository to enable
    - Example:
    ```
 $ jfrog yum-rt enable-repo epel
 epel repository enabled.
 ```
 * disable-repo
    - Arguments:
        - name - The name of the repository to disable
    - Example:
    ```
 $ jfrog yum-rt disable-repo epel
 epel repository disabled.
 ```

#### Commands passed to yum with changes
 * check-update
 * deplist
 * distribution-synchronization
 * downgrade
 * erase
 * groups
 * info
 * install
 * list

#### Commands passed through to yum
 * check
 * check-update
 * clean
 * deplist
 * distribution-synchronization
 * downgrade
 * erase
 * fs
 * fssnapshot
 * groups
 * history
 * info
 * install
 * list
 * load-transaction
 * makecache
 * provides
 * repo-pkgs
 * search
 * shell
 * swap
 * update
 * update-minimal
 * upgrade
 * version

### Environment variables
* JFROG_CLI_BUILD_NAME
* JFROG_CLI_BUILD_NUMBER
* JFROG_CLI_BUILD_PROJECT
* JFROG_CLI_BUILD_URL

## Additional info
None.

## Release Notes
The release notes are available [here](RELEASE.md).
