### Basic setup

    $ conan install boost/1.69.0@zinnion/stable

### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*

    [requires]
    boost/1.69.0@zinnion/stable

    [generators]
    txt

Complete the installation of requirements for your project running:

    $ mkdir build && cd build && conan install ..

Note: It is recommended that you run conan install from a build directory and not the root of the project directory.  This is because conan generates *conanbuildinfo* files specific to a single build configuration which by default comes from an autodetected default profile located in ~/.conan/profiles/default .  If you pass different build configuration options to conan install, it will generate different *conanbuildinfo* files.  Thus, they should not be added to the root of the project, nor committed to git.


## Build and package

The following command both runs all the steps of the conan file, and publishes the package to the local system cache.  This includes downloading dependencies from "build_requires" and "requires" , and then running the build() method.

    $ conan create . conan/stable


### Available Options
| Option        | Default | Possible Values  |
| ------------- |:----------------- |:------------:|
| shared      | False |  [True, False] |
| header_only      | False |  [True, False] |
| error_code_header_only      | False |  [True, False] |
| system_no_deprecated      | False |  [True, False] |
| asio_no_deprecated      | False |  [True, False] |
| fPIC      | True |  [True, False] |
| skip_lib_rename      | False |  [True, False] |
| magic_autolink      | False |  [True, False] |
| python_executable      | None |  ANY |
| python_version      | None |  ANY |
| namespace      | boost |  ANY |
| namespace_alias      | False |  [True, False] |
| without_math      | False |  [True, False] |
| without_wave      | False |  [True, False] |
| without_container      | False |  [True, False] |
| without_contract      | False |  [True, False] |
| without_exception      | False |  [True, False] |
| without_graph      | False |  [True, False] |
| without_iostreams      | False |  [True, False] |
| without_locale      | False |  [True, False] |
| without_log      | False |  [True, False] |
| without_program_options      | False |  [True, False] |
| without_random      | False |  [True, False] |
| without_regex      | False |  [True, False] |
| without_mpi      | False |  [True, False] |
| without_serialization      | False |  [True, False] |
| without_coroutine      | False |  [True, False] |
| without_fiber      | False |  [True, False] |
| without_context      | False |  [True, False] |
| without_timer      | False |  [True, False] |
| without_thread      | False |  [True, False] |
| without_chrono      | False |  [True, False] |
| without_date_time      | False |  [True, False] |
| without_atomic      | False |  [True, False] |
| without_filesystem      | False |  [True, False] |
| without_system      | False |  [True, False] |
| without_graph_parallel      | False |  [True, False] |
| without_python      | True |  [True, False] |
| without_stacktrace      | False |  [True, False] |
| without_test      | False |  [True, False] |
| without_type_erasure      | False |  [True, False] |
