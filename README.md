<!-- # How I installed the Pico C/C++ SDK in Ubuntu
--mkdir pico
cd pico
git clone -b master https://github.com/raspberrypi/pico-sdk.git
cd pico-sdk
git submodule update --init
cd ..
git clone -b master https://github.com/raspberrypi/pico-examples.git
sudo apt update
sudo apt install cmake gcc-arm-none-eabi build-essential




# How I created my first blink sketch using th C/C++ SDK for the pico

created a new directory <mkdir project>
opened the directory    <cd project>
copied pico_sdk_import.c from the pico-sdk folder <cp ~/pico/pico-sdk/external/pico_sdk_import.cmake .>
Created a CMakefile <sudo nano CMakeLists.txt> which helps build the code.
Created the blink.c file <sudo nano blink.c> and in the file edit the code to blink the led.
Create a build directory <mkdir build>
Open the build directory <cd build>
 Export the pico sdk to the build directory so as the compiler knows where to find the sdk <export PICO_SDK_PATH=.../.../pico/pico-sdk> <!--be sure to add your correct path here. -->

<!-- <cmake ..> start the build chain using the above stated CMakeLists file
<make> to have create uf2 file that will be copied to the Raspberry pi Pico  -->


markdown
Copy code
# Installing the Pico C/C++ SDK on Ubuntu

1. Create a directory for your Pico project:

mkdir pico
cd pico

csharp
Copy code

2. Clone the Pico SDK from GitHub:

git clone -b master https://github.com/raspberrypi/pico-sdk.git

markdown
Copy code

3. Initialize and update the submodules in the SDK:

cd pico-sdk
git submodule update --init
cd ..

markdown
Copy code

4. Clone the Pico examples repository:

git clone -b master https://github.com/raspberrypi/pico-examples.git

go
Copy code

5. Update the package list and install necessary tools:

sudo apt update
sudo apt install cmake gcc-arm-none-eabi build-essential

php
Copy code

# Creating Your First Blink Sketch with the Pico C/C++ SDK

6. Create a new project directory:

mkdir project
cd project

css
Copy code

7. Copy the pico_sdk_import.cmake file from the Pico SDK to your project directory:

cp ~/pico/pico-sdk/external/pico_sdk_import.cmake .

css
Copy code

8. Create a CMakeLists.txt file for building your project:

sudo nano CMakeLists.txt

css
Copy code

9. Create a blink.c file for your code and edit it to blink the LED:

sudo nano blink.c

go
Copy code

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