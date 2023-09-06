# DIR-619L Buffer Overflow

**Vulnerability description**

D-Link DIR-619L B1 2.02 was found to contain a stack overflow in multiple functions. This vulnerability allows attackers to trigger a denial of service (DoS) through web page parameters.

![image](https://github.com/YTrick/vuln/assets/57278844/38ddd2a7-64dd-4c0f-9d6e-54e125a30408)

## 1.formResetStatistic Function

### Vulnerability analysis

The data gets from front-end is processed in the formResetStatistic function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/997e69a1-df58-48ec-9be7-fdd1ba82e839)


![image](https://github.com/YTrick/vuln/assets/57278844/8054a4fe-2f14-46df-a91d-c1944ff05d43)

![image](https://github.com/YTrick/vuln/assets/57278844/9b65fabb-7020-4c85-a0b6-b979cac95f23)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/0b858aea-5442-4784-9412-f1bbc2e4cfe1)

## 2.formSetEnableWizard Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetEnableWizard function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/b76c6dfa-675b-4d92-9285-1563b75b8844)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/33fcc0dd-b541-4047-874f-6249784cf3a7)

## 3.formSetWizard1 Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetWizard1 function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/40435c5a-d64f-41a3-b976-cb2f073a2ed1)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/00c4ceeb-c626-4101-9702-f1bdce3f601e)

## 4.formSetWizard2 Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetWizard2 function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/ddb41ebf-4a94-4d5e-96fa-a3e290222904)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/102889ae-6568-4f41-b7fa-efec78bd2475)

## 5.formSetWizardSelectMode Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetWizardSelectMode function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/36c5a164-ae98-4222-833e-eea652a18843)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/e7519dca-b4c0-49b4-a119-9a4ad0d2f612)

## 6.formLogin Function

### Vulnerability analysis

The data gets from front-end is processed in the formLogin function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/a27c4fa2-bfa3-4e0d-829a-9273285455ac)

![image](https://github.com/YTrick/vuln/assets/57278844/98873804-90b6-4821-8812-dec9a2d4e1b6)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/b5b8cfd3-8d8e-4a9a-8e38-b1cb06013899)

## 7.formSetEmail Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetEmail function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/5f120469-0bfb-4c92-bde7-b11744b66451)

![image](https://github.com/YTrick/vuln/assets/57278844/ca8f90bb-153f-48f9-a4cf-69c0cf9e726b)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/ce3b4f16-594a-419d-b8be-644b47999906)

## 8.formEasySetupWizard Function

### Vulnerability analysis

The data gets from front-end is processed in the formEasySetupWizard function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/114fa313-aea4-4f74-a7a5-fbc605963753)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/a0f9907e-b602-4297-ac1d-ceadd36ff292)

## 9.formSetPassword Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetPassword function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/448490fa-411d-42a2-8979-7a67e6489500)

![image](https://github.com/YTrick/vuln/assets/57278844/0bf1c1b8-25b0-4e2b-b36e-fb82c02c7c3e)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/cac4abb8-1950-4f03-ac21-17586a07de06)

## 10.formSetEasy_Wizard Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetEasy_Wizard function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![image](https://github.com/YTrick/vuln/assets/57278844/7267d429-35ec-4894-ad0a-ee4a17710b08)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/015c0878-23c7-4e15-b375-7f1bfabbde96)
