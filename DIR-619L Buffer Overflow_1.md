# DIR-619L Buffer Overflow

**Vulnerability description**

D-Link DIR-619L B1 2.02 was found to contain a stack overflow in multiple functions. This vulnerability allows attackers to trigger a denial of service (DoS) through web page parameters.

![image](https://github.com/YTrick/vuln/assets/57278844/56525b82-fc9d-454c-8ed6-db0c44513cf8)


## 1.formSetWAN_Wizard534 Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/29142d71-caf9-4df6-bf57-cbed92fa38b8)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/ec53fd61-5ed5-4c80-8f0c-846f36967a61)

## 2.formSetWAN_Wizard55 Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/3ded85f2-f0ba-4699-a2cb-31279555aa3c)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/be34139a-8148-4167-95d5-68808071f4e2)

## 3.formSetWAN_Wizard56 Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/4833e3c3-61f4-4180-882d-b2223c9eaffe)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/45dd2c19-793a-42a9-ab6b-01fab2170336)

## 4.formSetWAN_Wizard7 Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/971cb899-67bd-460c-b750-aabacfacae50)

![image](https://github.com/YTrick/vuln/assets/57278844/e9fc8cdd-9748-4b0b-84d4-593f6739de55)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/1a489083-4f74-4151-b5ca-aea92eddebcd)

## 5.formSetWanDhcpplus Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/bdfe9f02-a798-4880-b99f-7ba3f79091ba)

![image](https://github.com/YTrick/vuln/assets/57278844/be251492-8b0c-4d05-83dc-d7ff66224b99)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/cd47566c-db66-4ec7-b2a9-46aa3095c4f6)

## 6.formSetWanNonLogin Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/c7f42a4a-5572-44e5-9410-0dcc2010b9e2)

![image](https://github.com/YTrick/vuln/assets/57278844/df527077-c31a-40c1-9bd4-c4b535d11eab)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/a186719d-377e-44a8-9bad-76e45978a64c)

## 7.formSetWanPPPoE Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/13a7ae0d-bd71-46f8-bea3-858d9a9609b4)

![image](https://github.com/YTrick/vuln/assets/57278844/5dd89b8a-d9d3-4922-aef2-3887521f7095)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/e7a5fce1-aa65-4a32-869b-3f049b35c534)

## 8.formSetWanPPTP Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/cc2f0cfd-23b2-4cda-9863-3d827e4f41d5)

![image](https://github.com/YTrick/vuln/assets/57278844/42866e8c-ee17-4fff-815c-30fed8a71d82)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/f59b9415-5a47-4f02-9dde-9fbb210b9270)

## 9.formSetWanL2TP Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/db9b77fe-71f5-4d28-9ebf-a17160124eba)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/e8b5e71b-9602-4839-b898-b7f27253839e)

## 10.formLanguageChange Function

### Vulnerability analysis

The websGetVar function obtains the currtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![image](https://github.com/YTrick/vuln/assets/57278844/3fc309e9-5133-4fd5-9dc9-abd65e3d4084)

### POC

![image](https://github.com/YTrick/vuln/assets/57278844/00157baf-b87f-4964-88cf-1b02ecf5e5fc)


