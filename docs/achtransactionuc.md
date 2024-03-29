# ACH Transaction Architecture
Depending on merchant setup, ACH Transactions can be sent to ConnectPay using Universal Commerce (uCom), Buypass or through PaybyBank Payment through FirstAPI.


>Note: Below is information on PaybyBank Payment through FirstAPI. For uCOM and Buypass, you will need to refer to the respective Implementation guide links below for setup*


[uCOM](?path=docs/documentation/Standard_Implementation_Guide.md)
[Buypass](https://developer.fiserv.com/product/)

## Explanation of Feature
All payments are server-to-server communication between the merchant server and FirstAPI. Transactions can be initiated using `fdAccountId` or, PaybyBank PaymentNumber

## Implementation Steps: ACH Transaction Process
### Create Session Token 

[Create Session Token](?path=./docs/implementationguide.md)
>Note: See section labeled Create Session Token


### Additional Steps
<ol>
  <li>Merchant server makes server to server call to PaybyBank at FirstAPI and sends encrypted ACH Transaction Payload</li>
  <li>ConnectPay at FirstAPI responds back with encrypted response payload</li>
  <li>Merchant server decrypts response payload and takes action accordingly</li>

### Issues with Integration
[Fiserv Implementation Support Team](mailto:DL-GBL-VASDelivery@fiserv.com)
<p>Image on the flow of the activity</p>
<center><img src="https://raw.githubusercontent.com/Fiserv/connect-pay/develop/assets/images/ACH Transaction Arch.png" alt="ACH Transaction Architecture" class="center"></center>