cmake_minimum_required(VERSION 3.5)

idf_component_register(
    SRC_DIRS
        "ttn-esp32/src"
        "ttn-esp32/src/aes"
        "ttn-esp32/src/hal"
        "ttn-esp32/src/lmic"
    INCLUDE_DIRS "ttn-esp32/include"
    REQUIRES nvs_flash
)
if (IDF_VER STRGREATER_EQUAL "v4.0")
target_compile_options(${COMPONENT_LIB} PRIVATE -Wno-expansion-to-defined)
endif()
