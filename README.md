# A Starter project for SDL3

## Clone
1. Create a repository using the "Use this template button"
2. Clone the repository locally including submodules. 

Using ssh: ```git clone --recurse git@github.com:TheRealDelep/sdl-template```

Using https: ```git clone --recurse https://github.com/TheRealDelep/sdl-template```

## Build
1. cd to your repository root
2. run ```cmake -B build .```

The first time you build the project (or if you delete the CMakeCache.txt) you may want to specify another generator and compiler than your os default.

You can specify another generator with the -G option. ```cmake -G --help``` to see the list of available generators.

You can specify the compiler to use using ```-DCMAKE_C_COMPILER=<compiler>``` and ```-DCMAKE_CXX_COMPILER=<compiler>```

Example of a command generating a Makefile using clang and clang++ 

```cmake -DCMAKE_C_COMPILER=clang -DCMAKE_CXX_COMPILER=clang++ -G "Unix Makefiles" -B build .```

3. cd ./build/
4. make

You should be up and running
