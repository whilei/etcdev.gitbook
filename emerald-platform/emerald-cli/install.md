# Install

## Installing Emerald CLI

### Download stable binary {#_download_stable_binary}

Binaries for all platforms are currently published at [https://github.com/ETCDEVTeam/emerald-cli/releases](https://github.com/ETCDEVTeam/emerald-cli/releases)

### Install with Homebrew \(OSX only\) {#_install_with_homebrew_osx_only}

Installs latest stable binary.

```text
$ brew install ethereumproject/classic/emerald-cli
```

### Download development build {#_download_development_build}

| Warning | Development builds are usually unstable and may contain critical issues that can lead to loss of funds. Use it on your risk |
| :--- | :--- |


ETCDEV has a dedicated website for all build artifacts, which are published on each new commit into `master` branch. To download a latest development build, please open [https://builds.etcdevteam.com](https://builds.etcdevteam.com/)and choose _Emerald CLI_ tab

### Build from sources {#_build_from_sources}

#### Requirements {#_requirements}

Install Rust from [https://www.rust-lang.org/en-US/install.html](https://www.rust-lang.org/en-US/install.html)

Unix one-liner:

```text
$ curl https://sh.rustup.rs -sSf | sh
```

| Note | On Windows, Rust additionally requires the C build tools for Visual Studio 2013 or later. The easiest way to acquire the build tools is by installing Microsoft Visual C Build Tools 2017 which provides just the Visual C++ build tools. |
| :--- | :--- |


#### Compile {#_compile}

**Step 1**

Clone the repository

```text
$ git clone https://github.com/etcdevteam/emerald-cli.git
$ cd emerald-cli
```

**Step 2**

Compile with cargo

```text
$ cargo build --release
```

**Step 3**

Run `emerald`

```text
$ ./target/release/emerald --help
```

