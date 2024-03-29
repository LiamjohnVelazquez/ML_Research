# ML Privacy Research

## GOAL: Intel SGX to accomplish some algorithm including deep learning inference and back probagation

### Installation for linux 20.04
Type your cpu name into search bar
[Check for valid intel cpu](https://ark.intel.com/content/www/us/en/ark/products/186604/intel-core-i79700k-processor-12m-cache-up-to-4-90-ghz.html)



[Most up to date installation guide (2/28/2023 version)](https://download.01.org/intel-sgx/latest/linux-latest/docs/Intel_SGX_SW_Installation_Guide_for_Linux.pdf)
- In depth installation guide, useful for information about required drivers, the github below is easier to follow for PSW and SDK installation
- In case of bios with "software-enabled" option in bios and driver not found in dev folder use https://github.com/intel/sgx-software-enable


[Linux sgx github with ReadMe for installing Intel SGX PSW and Intel SGX PSW](https://github.com/intel/linux-sgx)


[Installation of Intel sgx sdk on linux 20.04 walkthrough](https://www.youtube.com/watch?v=X0YzzT4uAY4)
- This video does not cover psw installation, refer to github for that, useful for visual represenation


- Steps to run sample code in simulation mode
  - cd into desired sample code e.g. (/linux-sgx/linux/installer/bin/sgxsdk/SampleCode/[desired sample code]) 
  - create makefile " make SGX_MODE=[desired mode]"
    - e.g. SGX_MODE=SIM
  - cd into bin
  - ls to view "app"
  - "./app" to run code
  - In case sdk isnt working after restarting pc try setting up environment variables again by cd into "/linux-sgx/linux/installer/bin/" and using command "$ source /home/iar/linux-sgx/linux/installer/bin/sgxsdk/environment" replace this line with your specific path
  
source /home/iar/linux-sgx/linux/installer/bin/sgxsdk/environment

-To run in hardware mode make sure intel sgx drivers are installed 
  - Use "make", or refer to developer guide for more specific instructions

###

- [x] Eclipse* Mars 1 with CDT IDE for C/C++ Developpers (version 4.5.1). To
use this version, install Java* Development Kit (JDK) or Java* Runtime
Environment (JRE) version 1.8 or above.

[Install eclipse with c/c++ for Ubuntu](https://www.linuxfordevices.com/tutorials/ubuntu/eclipse-ide-with-cpp#:~:text=Creating%20a%20C%2B%2B%20Program%20in,and%20click%20again%20on%20Next.)

- [x] gcc*/g++ tools
- [x] OpenSSL*
- [x] Intel(R) SGX SDK for Linux* OS

## Deep Learning in C/C++ with Darknet within Intel SGX...
[Deep Learning with Intel SGX by github user landoxy](https://github.com/landoxy/intel-sgx-deep-learning)

## Federated Learning in python with PySyft within Intel SGX
[PYSYFT, PYTORCH AND INTEL SGX: SECURE AGGREGATION ON TRUSTED EXECUTION ENVIRONMENTS](https://blog.openmined.org/pysyft-pytorch-intel-sgx/)
[OpenMined Intel SGX git hub](https://github.com/OpenMined/sgx-experiments)
[Getting Started](https://openmined.github.io/PySyft/)
[Gramine](https://github.com/gramineproject/gramine)
- Gramine (formerly called Graphene) is a lightweight library OS, designed to run a single application with minimal host requirements. Gramine can run applications in an isolated environment with benefits comparable to running a complete OS in a virtual machine -- including guest customization, ease of porting to different OSes, and process migration.

Gramine supports native, unmodified Linux binaries on any platform. Currently, Gramine runs on Linux and Intel SGX enclaves on Linux platforms.


## Learn to use Intel SGX
[The Magic of Intel’s SGX: A Tutorial on Programming a Secure Enclave](https://medium.com/magicofc/the-magic-of-intels-sgx-how-to-hello-it-sec-world-fb0295d6c33b)

[Intel SGX developer guide](https://download.01.org/intel-sgx/sgx-linux/2.8/docs/Intel_SGX_Developer_Guide.pdf)

[Intel(R) Software Guard Extensions SDK Developer Reference for Linux* OS](https://download.01.org/intel-sgx/latest/linux-latest/docs/Intel_SGX_Developer_Reference_Linux_2.19_Open_Source.pdf)

[Sample code "Cxx17SGXDemo" Explained](https://github.com/intel/linux-sgx/tree/master/SampleCode/Cxx17SGXDemo)
- Code begins in app.cpp within the APP folder


## Building blocks of basic Intel SGX Project using SampleCode/Cxx17SGXDemo as reference
- SampleCode/Cxx17SGXDemo is a great template for learning to work with intel sgx but SampleCode/SampleEnclave is great as well
- SampleEnclave has examples for App.cpp, Enclave.cpp, and Enclave.edl files within its Edger8rSyntax files that help understand how to call files from untrusted app.cpp, how to protoype functions within the .edl files, and how to define functions within the Enclave.cpp

## Intel Deep Neural Network
[The project demonstrates Intel(R) Deep Neural Network Library (DNNL) functions inside Intel(R) SGX environment](https://github.com/intel/linux-sgx/tree/master/SampleCode/SampleDNNL)
performed make next step is 
4. Install Intel(R) SGX DNNL library and header files.
   a. Copy Intel(R) SGX DNNL lib to the Intel(R) SGX SDK installation directory.
      $ cp "./sgx_dnnl/lib/libsgx_dnnl.a" "$(SGX_SDK)/lib64"
   b. Copy Intel(R) SGX DNNL header files to the Intel(R) SGX SDK header file directory.
      $ cp "./sgx_dnnl/include/*" "$(SGX_SDK)/include"

- Next step inludes understanding Alexnet which is the CNN architecture that is used in intel's SampleDNNL example in the intel sgx sample code.
[Alexnet implementation solely in C](https://github.com/Dynmi/AlexNet) 



