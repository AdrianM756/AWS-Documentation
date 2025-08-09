<img width="684" height="632" alt="image" src="https://github.com/user-attachments/assets/2b49acb5-9999-472c-bb0a-30bb52bde361" /><img width="1672" height="724" alt="image" src="https://github.com/user-attachments/assets/bfb46e80-032a-4bb2-bc92-8912e1e062a1" />## AWS Key Management

[AWS Key Management Service (AWS KMS)](https://docs.aws.amazon.com/kms/latest/developerguide/overview.html) is an AWS managed service that makes it easy for you to create and control the encryption keys that are used to encrypt your data. The AWS KMS keys that you create in AWS KMS are protected by [FIPS 140-3 Security Level 3 validated hardware security modules (HSM)](https://csrc.nist.gov/projects/cryptographic-module-validation-program/certificate/4884). They never leave AWS KMS unencrypted. To use or manage your KMS keys, you interact with AWS KMS.

## Create a KMS Master Key

On the AWS Dashboard, click on the searh bar and type ```Key Management Service``` and select the first thing that appears.
<br>
<img width="947" height="351" alt="image" src="https://github.com/user-attachments/assets/cdf02005-d3ef-4736-a838-72a994455a1c" />
<br>

In the **Key Management Service** section, choose ```Create a key```.
<br>
<img width="1631" height="443" alt="image" src="https://github.com/user-attachments/assets/47226276-8599-4f81-b9e0-5520ff4c6929" />
<br>

On the **Configure key** section, select ```Symmetric``` then click on ```Next```.
<br>
<img width="1698" height="543" alt="image" src="https://github.com/user-attachments/assets/0d4855e9-9281-4aa1-a912-6e79dc3bf911" />
<br>

On the **Add labels** section, type your desired **Allias**. This Allias refers as a friendly name for the encryption key. For the **Description**, It is a good practice to describe what services the encryption key is associated with. Once done, click on ```Next```.
<br>
<img width="1672" height="724" alt="image" src="https://github.com/user-attachments/assets/acc319ed-400c-4c1b-8e3d-ccfba94c9c98" />
<br>

On the ```Define key administrative permissions``` section, select the user or role you’re signed into the Console with. The user is displayed at the top of the page, to the right of the AWS region. Once Done, Click on ```Next```.
<br>
<img width="1373" height="451" alt="image" src="https://github.com/user-attachments/assets/ef29dc56-2b0f-4e46-8181-702f65dc42e4" />
<br>

***NOTE:*** **Key Administrators** are users or roles that manage access to the encryption key.
<br>

On the ```Define key usage permissions``` section, select the user or role you’re signed into the Console with. This is the same user you selected in the previous step. Once done, Click on ```Next```.
<br>
<img width="1373" height="538" alt="image" src="https://github.com/user-attachments/assets/820a8a0e-e6bf-487b-9cde-5666a6d4bcba" />
<br>

***NOTE:*** **Key Users** are the users or roles that use the key to encrypt and decrypt data.
<br>

In the ```Review``` section, take a few moment to review the parameters of the KMS configuration. Once done, click on ```Finish```.
<br>

In the ```Customer managed keys``` section, you can see that the new key that you've created is already listed.
<br>
<img width="1629" height="202" alt="image" src="https://github.com/user-attachments/assets/98656d98-a2f7-4e4b-a276-350ed284900e" />
<br>

## Configure CloudTrail to store logs in a new S3 bucket

In this demo, we will configure CloudTrail to store log files in a new S3 bucket.

On the search bar, type ```Cloudtrail``` and click on the first thing that appears.
<br>
<img width="926" height="344" alt="image" src="https://github.com/user-attachments/assets/2842266c-f52d-47e8-9def-adf39ae74e49" />
<br>

Click on ```Create trail```.
<br>
<img width="1903" height="263" alt="image" src="https://github.com/user-attachments/assets/58be80a1-5e87-4b9f-b465-18ab25057730" />
<br>

In the ```Choose trail attributes``` section, configure:

* Trail name
* Trail log bucket and folder
* De-select ```Enabled``` for ```Log file SSE-KMS encryption```.
<br>

<br>
<img width="684" height="632" alt="image" src="https://github.com/user-attachments/assets/9920bbb5-5ce0-4246-a895-0ddc1c62b6aa" />
<br>

Once done, click on ```Next```.
<br>

On the ```Choose log events``` section, configure:

* Select ```Management events```
* Select ```Data events```
* Select ```Insights events```
<br>

In the ```Data events``` section, choose ```Switch to basic event selectors```, Then choose ```Continue```.
<br>
<img width="1056" height="453" alt="image" src="https://github.com/user-attachments/assets/b428b368-0d2c-42ef-88e4-dd7d5b22102d" />
<br>

In the ```Insights events``` section, select:
* ```API call rate```
* ```API error rate```
<br>
<img width="1093" height="239" alt="image" src="https://github.com/user-attachments/assets/dabc5d80-bbe8-46fb-bee1-26f68235ca92" />
<br>

Once done, click on ```Next```.
<br>

In the ```Review``` section, take a few moment to review the parameters of the KMS configuration. Once done, click on ```Create trail```.
<br>

To be continue....








