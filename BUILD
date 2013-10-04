[
  { "cmake": {
    "name": "dlib_make",
    "cmake_dir": "dlib",
    "make_target": "dlib",
    "outs": [ "build/libdlib.a" ]
  } },
  { "cc_library": {
    "name": "dlib_headers",
    "cc_headers": [ "dlib/*.h",
                    "dlib/*/*.h",
                    "dlib/*/*/*.h"
    ],
    "header_compile_args": [ "-I$SRC_DIR" ]
  } },
  { "cc_library": {
    "name": "dlib",
    "cc_objects": [ "$GEN_DIR/build/libdlib.a" ],
    "strict_file_mode": false,
    "dependencies": [ ":dlib_make", ":dlib_headers" ]
  } },

  // An example binary.
  { "cc_binary": {
      "name": "svm_rank_example",
      "cc_sources": [ "examples/svm_rank_ex.cpp" ],
      "dependencies" : [ ":dlib" ]
  } }
]

