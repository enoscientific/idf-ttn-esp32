# esp-idf ttn-esp32

**ttn-esp32** componentized library.

https://github.com/manuelbl/ttn-esp32 organized as a ESP-IDF component.

To use, git clone/submodule to `components` directory.

Or add to `CmakeLists.txt` file:

```
# Adds a new cmake function
include(FetchContent)
# Add remote libraries, which will be pulled down when this project is first built, and cached.


FetchContent_Declare(
  ttn-esp32
  GIT_REPOSITORY https://github.com/enoscientific/idf-ttn-esp32.git
)

FetchContent_MakeAvailable(ttn-esp32)
set(EXTRA_COMPONENT_DIRS ${ttn-esp32_SOURCE_DIR}/components)

```
