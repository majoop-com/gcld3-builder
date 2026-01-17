# gcld3-builder

This project automates the building and releasing of gcld3 Python wheels for macOS.

## Purpose

The gcld3 package (Compact Language Detector 3) is a language detection library. 
Official wheels may not be available for all platforms or Python versions. 
This repository provides a GitHub Actions workflow to build compatible wheels for macOS x86_64 with Python 3.14.

## Workflow

The workflow (`build-gcld3-macos-py314.yml`) performs the following steps:

1. Downloads the gcld3 source distribution (sdist) for the specified version.
2. Patches the setup to use C++17 standard.
3. Builds the wheel using cibuildwheel with Bazel and other tools.
4. Uploads the built wheel as an artifact.
5. Creates a draft GitHub release with the wheel attached.

## Usage

To build a wheel for a specific gcld3 version:

1. Go to the [Actions](https://github.com/your-repo/actions) tab in this repository.
2. Select the "Build gcld3 macOS (Intel) wheel for Python 3.14" workflow.
3. Click "Run workflow" and enter the desired `gcld3_version` (e.g., "3.0.13").
4. Once the workflow completes, a draft release will be created with the wheel file.

## License

See LICENSE file.
