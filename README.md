# **Fossil Locale by Fossil Logic**

**Fossil Locale** is a lightweight, portable internationalization and localization library written in pure C with zero external dependencies. Built for cross-platform applications, Fossil Locale provides developers with tools for managing language translations, locale-aware formatting, and cultural data without the overhead of large frameworks. Its compact, modular design makes it a perfect choice for applications that need to support multiple languages and regions efficiently.  

### Key Features

- **Cross-Platform Support**  
  Works consistently across Windows, macOS, Linux, and embedded systems.  

- **Zero External Dependencies**  
  Fully implemented in clean, portable C for maximum transparency and maintainability.  

- **Locale-Aware Utilities**  
  Provides language translation helpers, number/date/time formatting, and cultural conventions.  

- **Lightweight and Efficient**  
  Designed with a minimal footprint for use in performance- and memory-constrained environments.  

- **Self-Contained & Auditable**  
  Easy-to-read source code enables simple verification and debugging.  

- **Modular Design**  
  Integrate only the components you need—ideal for embedded or custom solutions. 

## ***Prerequisites***

To get started, ensure you have the following installed:

- **Meson Build System**: If you don’t have Meson `1.8.0` or newer installed, follow the installation instructions on the official [Meson website](https://mesonbuild.com/Getting-meson.html).
- **Conan Package Manager**: If you prefer using Conan, ensure it is installed by following the instructions on the official [Conan website](https://docs.conan.io/en/latest/installation.html).

### Adding Dependency

#### Adding via Meson Git Wrap

To add a git-wrap, place a `.wrap` file in `subprojects` with the Git repo URL and revision, then use `dependency('fossil-locale')` in `meson.build` so Meson can fetch and build it automatically.

#### Integrate the Dependency:

Add the `fossil-locale.wrap` file in your `subprojects` directory and include the following content:

```ini
[wrap-git]
url = https://github.com/fossillogic/fossil-locale.git
revision = v0.1.0

[provide]
dependency_names = fossil-locale
```

**Note**: For the best experience, always use the latest releases. Visit the [releases](https://github.com/fossillogic/fossil-locale/releases) page for the latest versions.

## Build Configuration Options

Customize your build with the following Meson options:
	•	Enable Tests
To run the built-in test suite, configure Meson with:

```sh
meson setup builddir -Dwith_test=enabled
```

### Tests Double as Samples

The project is designed so that **test cases serve two purposes**:

- ✅ **Unit Tests** – validate the framework’s correctness.  
- 📖 **Usage Samples** – demonstrate how to use these libraries through test cases.  

This approach keeps the codebase compact and avoids redundant “hello world” style examples.  
Instead, the same code that proves correctness also teaches usage.  

This mirrors the **Meson build system** itself, which tests its own functionality by using Meson to test Meson.  
In the same way, Fossil Logic validates itself by demonstrating real-world usage in its own tests via Fossil Test.  

```bash
meson test -C builddir -v
```

Running the test suite gives you both verification and practical examples you can learn from.

## Contributing and Support

For those interested in contributing, reporting issues, or seeking support, please open an issue on the project repository or visit the [Fossil Logic Docs](https://fossillogic.com/docs) for more information. Your feedback and contributions are always welcome.
