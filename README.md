
# Installing the Pico C/C++ SDK on Ubuntu

1. Create a directory for your Pico project:

    mkdir pico
    cd pico

    csharp
    Copy code

2. Clone the Pico SDK from GitHub:

    git clone -b master https://github.com/raspberrypi/pico-sdk.git


3. Initialize and update the submodules in the SDK:

    cd pico-sdk
    git submodule update --init
    cd ..


4. Clone the Pico examples repository:

    git clone -b master https://github.com/raspberrypi/pico-examples.git

5. Update the package list and install necessary tools:

    sudo apt update
    sudo apt install cmake gcc-arm-none-eabi build-essential


# Creating Your First Blink Sketch with the Pico C/C++ SDK

6. Create a new project directory:

    mkdir project
    cd project


7. Copy the pico_sdk_import.cmake file from the Pico SDK to your project directory:

    cp ~/pico/pico-sdk/external/pico_sdk_import.cmake .


8. Create a CMakeLists.txt file for building your project:

    sudo nano CMakeLists.txt


9. Create a blink.c file for your code and edit it to blink the LED:

    sudo nano blink.c


10. Create a build directory for your project:

 ```
 mkdir build
 cd build
 ```

11. Export the Pico SDK path to the build directory:

 ```
 export PICO_SDK_PATH=.../.../pico/pico-sdk
 ```
 (Be sure to provide the correct path to your Pico SDK)

12. Start the CMake build process:

 ```
 cmake ..
 ```

13. Build the project to create a UF2 file:

 ```
 make
 ```

These steps will help you set up the Pico C/C++ SDK and create your first blink sketch