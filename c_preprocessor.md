---
title: C Preprocessor
---

### Compiling

    $ cpp -P file > outfile

### Includes

    #include "file"

### Defines

    #define FOO
    #define FOO "hello"
    
    #undef FOO

### If

    #ifdef DEBUG
      console.log('hi');
    #elif defined VERBOSE
      ...
    #else
      ...
    #endif

### Error

    #if VERSION == 2.0
      #error Unsupported
      #warning Not really supported
    #endif

### Macro

    #define DEG(x) ((x) * 57.29)

### Token concat

    #define DST(name) name##_s name##_t
    DST(object);   #=> "object_s object_t;"

### Token stringify

    #define varName(var) #name
    varName(var1);   #=> "var1";

### file and line

    #define LOG(msg) console.log(__FILE__, __LINE__, msg)
    #=> console.log("file.txt", 3, "hey")
