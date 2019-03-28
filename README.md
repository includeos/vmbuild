# vmbuild

Utilities for building IncludeOS VMs

### Configure Settings

```
  conan config install https://github.com/includeos/conan_config.git
```

##### Check Profiles installed

```
  conan profile list
```

**Vmbuild** doesn't require `binutils` to built Thus vmbuild can be built with the **_toolchain_** profiles.

* To build on **macos**:
`apple-clang-10-macos-toolchain`

* To build on **linux** with `clang-6.0`:
`clang-6.0-linux-x86_64-toolchain`

* To build on **linux** with `gcc-7.3.0`:
`gcc-7.3.0-linux-x86_64-toolchain`

* To build on **linux** for `arm` with `gcc-8.2`:
`gcc-8.2.0-linux-aarch64-toolchain`


### Build and run vmbuild

```bash
  mkdir build
  cd build
  conan create .. includeos/stable -pr <toolchain-profile-name>
```
