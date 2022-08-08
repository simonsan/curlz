# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased] - 2022-01-01
[Unreleased]: https://github.com/curlz-rs/curlz/compare/v0.1.0-alpha.1...HEAD

### Added
### Changed
### Deprecated 
### Removed
### Fixed
### Security
### Contributors

## [0.1.0-alpha.1] - 2022-08-07
[0.1.0-alpha.1]: https://github.com/curlz-rs/curlz/compare/v0.1.0-alpha.1

### Added
- reading of `.env` files
- reading of `.yaml` env files
- placeholder evaluation, with the [minijinja](https://docs.rs/minijinja/latest/minijinja/) template engine
  - in urls
  - in http headers (`-H | --header` arguments)
  - in every other passed curl parameter
- save request as a bookmark via `--bookmark` or `--bookmark-as`, containing:
  - curl arguments
  - http headers
  - http method
  - placeholders
- pass all arguments after `--` to curl, that makes drop-in-replacement possible
- execute a bookmarked request
- special placeholder variables that would interact with the user
  - prompting for a password as `{{ prompt_password() }}
    ```sh
    curlz -- -u "{{ username }}:{{ prompt_password() }}" https://api.github.com/user
    ```

### Contributors
[@sassman](https://github.com/sassman)