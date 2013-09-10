Bundle Extension
==============

The tool to sign and bundle several Adobe Extensions (zxp file) to a special bundle Adobe Extension (zxp file). The Adobe Extensions (zxp file) to be bundled must be a Adobe CEP extension.

How to use this tool:

1. In the BundleExtension folder, create a folder in which the zxp files to be bundled will be placed, such as "SampleBundle".
2. Copy the Adobe Extensions (zxp files) to be bundled into the folder created in step 1.
3. Copy the file "com.example.id.bundle.mxi" into the folder created in step 1. You can rename this file to any file name as long as the extension of file is ".mxi".
Open the mxi file with a text editor, input your name, description and license agreement in the place holder.
Under "<files>" element, input the "<file>" element referring to a zxp file to be bundled. For example, the below "<file>" element refers to "C.zxp". Make sure all the zxp files to be bundled are referred in this mxi file, and keep both zxp files and mxi file in the folder created in step 1. 
<file destination="" file-type="CSXS" products="" source="C.zxp"/>

4. With command line tool, switch the working directory to "BundleExtension", and use run.bat to create the extension. The first argument is the path to the certificate, the second password is the password of the certificate, and the third argument is the name of folder created in step 1. 

Example:

Suppose there is a certificate "cert.p12" in the directory "SampleBundle", the password of the certificate is "password", the command to sign and package SampleBundle would be:

run.bat ./cert.p12 password SampleBundle

(The certificate "cert.p12" is a sample certificate, you can use your own certificate.)