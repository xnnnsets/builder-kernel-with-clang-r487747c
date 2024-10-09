***
* available toolchain/clang/host/linux-x86/clang-r487747c
* available toolchain/gcc/linux-x86/arm/arm-linux-androideabi-4.9
* available toolchain/gcc/linux-x86/aarch64/aarch64-buildroot-linux-android-4.9

***
***
* tested in source kernel [A34X-ARM64](https://github.com/xnnnsets/android_kernel_samsung_a34x)
* tested in source kernel [A01CORE-ARM](https://github.com/xnnnsets/android_kernel_samsung_a01core)
* tested in source kernel [A10S-ARM64](https://github.com/xnnnsets/android_kernel_samsung_a10s)
****

# Use Github Action to compile Kernel Samsung

- Support A34X, A01CORE, A10S

---

tested in source kernel [A34X-ARM64](https://github.com/xnnnsets/android_kernel_samsung_a34x)
tested in source kernel [A01CORE-ARM](https://github.com/xnnnsets/android_kernel_samsung_a01core)
tested in source kernel [A10S-ARM64](https://github.com/xnnnsets/android_kernel_samsung_a10s)

## Thanks to
- All contributors

---

## Parameter Description

| Name | Description | Example |
| ------------ | -------------------- | ------------ |
| `DEVICE_TREE_URL` | Kernel Source | [https://github.com/xnnnsets/android_kernel_samsung_a34x] |
| `DEVICE_TREE_BRANCH` | Kernel branch | muach |
| `NAME_FOLDER` | Name Folder | kernel_a34x |
| `DEVICE_NAME` | Device Name | samsung_a34x |
| `LINK_ANY_KERNEL` | Link Zip Anykernel3 | https://github.com/xnnnsets/AnyKernel3 |
| `Architecture` | Architecture | ARM64 |
-----

## How to use
```
HOW TO USE
```
#### 1. Click 'Fork' in the upper right corner of this repository
![image](https://user-images.githubusercontent.com/37921907/177914706-c92476c5-7e14-4fb3-be94-0c8a11dae874.png)
#### 2. After waiting for the automatic redirection, you will see your own username
![image](https://user-images.githubusercontent.com/37921907/177915106-5bde6fc9-303c-479e-b290-22b48efd1e4e.png)
#### 3. Change the [username and email](https://github.com/CaptainThrowback/Action-Recovery-Builder/blob/main/.github/workflows/Recovery%20Build.yml#L100-L101) in the workflow to reflect your Github credentials (optional)
## Setting up SSH Keys (optional)
#### 4. Go to Settings, then select Deploy keys and select "Add deploy key" button.

#### 5. On your Android device, install [Termux](https://github.com/termux/termux-app/releases)

#### 6. Install openssh in Termux and generate ssh keys. (Do not use passphrase for keys)
NOTE: When creating the deploy key for a repository like git@github.com:owner/repo.git or https://github.com/owner/repo, put that URL into the key comment. (Hint: Try ssh-keygen ... -C "git@github.com:owner/repo.git".)
owner = your Github username
```
pkg install openssh
ssh-keygen -t ed25519 -C "git@github.com:owner/Action-Recovery-Builder.git"
```
#### 7. Add the keys to your repo. In Termux, use the following commands:
```
cd /data/data/com.termux/files/usr/etc/ssh
cat ssh_host_ed25519_key.pub
```
  Select and copy the key then paste in the box for Key.
  You can name it whatever you choose for the title.

#### 8. Now to add your private ssh key. Back in Termux:
```
cat ssh_host_ed25519_key
```
   Copy the output from Termux.

   In your browser, select *Secrets* under the Security tab.
   Select Actions
   Select New repository secret
   For the New secret name, it should be SSH_PRIVATE_KEY
   Paste the output from ssh_host_ed25519_key into the Value box.
   Then select Add secret.

## Building the Recovery
#### 9. Click 'Actions-Recovery Build'
![image](https://user-images.githubusercontent.com/37921907/177915304-8731ed80-1d49-48c9-9848-70d0ac8f2720.png)
#### 10. Click 'Run workflow' and fill in according to the above 'parameter description'
![image](https://user-images.githubusercontent.com/37921907/177915346-71c29149-78fb-4a00-996f-5d84ffc9eb8c.png)
#### 11. After filling in, click 'Run workflow' to start running

-----

## Compilation results
Can be downloaded at [Release](../../releases)

-----
## Remark

#### TeamWin Recovery Project: https://github.com/minimal-manifest-twrp
#### SKYHAWK Recovery Project: https://github.com/SHRP/manifest
