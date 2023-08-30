# CS2040C RGB Example

This repo provides skeleton code for an example RGB class. You will use this as the basis for implementing operator overloading.

## Installation of CMake

For MacOS, you can install CMake using [brew](https://formulae.brew.sh/formula/cmake).

```bash
brew install cmake
```

## Setup

1. Clone the project.
2. Enter the root directory.
3. Execute CMake to install the necessary dependencies.
4. Execute make to build all the files.
5. Execute `make test` to run the test.

```bash
git clone https://github.com/kshehata/cs2040c-rgb.git
cd CS2040C-RGB
cmake CMakeLists.txt
make
make test
```

## Unit Tests

Unit tests are in the `RGB_test.cpp` file and run automatically with `make test`. To add a new unit test, just add something like:

```C++
TEST(RGBTest, TestName) {
  // write test code here ...
}
```

Note that test names must be unique.

## Mixing Colours

When you mix two colours, you effectively average each of their components. So if you mix bright red RGB(240, 0, 0) and bright blue RGB(0, 0, 220) you would get something like RGB(120, 0, 110).

## Test Driven Development (TDD)

You are to work in pairs and follow TDD, aka "ping-pong programming". One partner writes a test case, and then the other partner writes the simplest code to satisfy the test case. Then the second partner writes the test case and the first writes the implementation. Continue until the tasks below are complete.

## Tasks

1. Add new method to `RGB` to mix the current colour with a given colour and return the new colour, `RGB RGB::mix(const RGB& c)`
2. Implement colour mixing as an overloaded "+" operator. If `c1` and `c2` are colours, then `RGB c3 = c1 + c2;` should result in the mix of `c1` and `c2`.
3. Write a method brighten a colour by a factor given as a real number. A factor of 1.0 means no change, while 2.0 would mean twice as bright (i.e. double each value) or 0.5 would be half as bright (i.e. halve each value).
4. Implement the method above as an overloaded "*" operator.

