# WebAssembly
Harnessing the Speed of C/C++ world in Web

# Requirements

> git clone git clone https://github.com/juj/emsdk.git

> cd emsdk

> ./emsdk install latest

> ./emsdk activate latest

> $ source ./emsdk_env.sh --build=Release

# Write a Sample C++ or C Application

```
#include <iostream>

long gcd(long a, long b){
      if(a == 0){
          return b;
      }else if(b == 0){
          return a;
      }else{
          return gcd(b, a % b);
      }
  }
int main(int argc, const char * argv[]) {
    std::cout << gcd(190, 76);
}
```

# Compilation

emcc main.cpp --emrun -s WASM=1 -o test.html

# Output

Cooy and run test.html on a web server

# References

https://developer.mozilla.org/en-US/docs/WebAssembly/C_to_wasm

0Gohman,%20Wagner,%20Zakai,%20Bastien,%20Holman%20-%20Bringing%20the%20Web%20up%20to%20Speed%20with%20WebAssembly.pdf

https://kripken.github.io/emscripten-site/docs/introducing_emscripten/index.html

http://webassembly.org/getting-started/developers-guide/
