# To compile this package with scram use
scram build -j8
cmsenv

# To compile a standalone executable use (alternative -stdlib=libc++)
clang++ `root-config --cflags --glibs` -std=c++11 -stdlib=libstdc++ bin/lheReader.cpp -o test/lheReader

# Usage:
lheReader -i [input_1.lhe] -i [input_2.lhe] -o [output.root] -r [run] -e [event] -l [lumi] -d [debug mode]

