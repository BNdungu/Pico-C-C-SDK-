# How I installed the Pico C/C++ SDK in Ubuntu
mkdir pico
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

<cmake ..> start the build chain using the above stated CMakeLists file
<make> to have create uf2 file that will be copied to the Raspberry pi Pico