# Use IDT to develop and run your own test suites<a name="idt-custom-tests"></a>

<a name="idt-byotc"></a>Starting in IDT v4\.0\.1, IDT for AWS IoT Greengrass V2 combines a standardized configuration setup and result format with a test suite environment that enables you to develop custom test suites for your devices and device software\. You can add custom tests for your own internal validation or provide them to your customers for device verification\.

Use IDT to develop and run custom test suites, as follows:

**To develop custom test suites**  
+ Create test suites with custom test logic for the Greengrass device that you want to test\.
+ Provide IDT with your custom test suites to test runners\. Include information about specific settings configurations for your test suites\.

**To run custom test suites**  
+ Set up the device that you want to test\.
+ Implement the settings configurations as required by the test suites that you want to use\.
+ Use IDT to run your custom test suites\.
+ View the test results and execution logs for the tests run by IDT\.

## Download the latest version of AWS IoT Device Tester for AWS IoT Greengrass<a name="install-dev-tst-gg"></a>

Download the [latest version](dev-test-versions.md) of IDT and extract the software into a location \(*<device\-tester\-extract\-location>*\) on your file system where you have read/write permissions\. 

**Note**  
<a name="unzip-package-to-local-drive"></a>IDT does not support being run by multiple users from a shared location, such as an NFS directory or a Windows network shared folder\. We recommend that you extract the IDT package to a local drive and run the IDT binary on your local workstation\.  
Windows has a path length limitation of 260 characters\. If you are using Windows, extract IDT to a root directory like `C:\ ` or `D:\` to keep your paths under the 260 character limit\.

## Test suite creation workflow<a name="custom-test-workflow"></a>

Test suites are composed of three types of files:
+ JSON configuration files that provide IDT with information on how to execute the test suite\.
+ Test executable files that IDT uses to run test cases\.
+ Additional files required to run tests\.

Complete the following basic steps to create custom IDT tests:

1. [Create JSON configuration files](idt-json-config.md) for your test suite\.

1. [Create test case executables](create-test-executables.md) that contain the test logic for your test suite\. 

1. Verify and document the [configuration information required for test runners](set-custom-idt-config.md) to run the test suite\.

1. Verify that IDT can run your test suite and produce [test results](run-debug-custom-tests.md) as expected\.

To quickly build a sample custom suite and run it, follow the instructions in [Tutorial: Build and run the sample IDT test suite](build-sample-suite.md)\. 

To get started creating a custom test suite in Python, see [Tutorial: Develop a simple IDT test suite](create-custom-tests.md)\.