# DIR-619L Buffer Overflow

**Vulnerability description**

D-Link DIR-619L B1 2.02 was found to contain a stack overflow in multiple functions. This vulnerability allows attackers to trigger a denial of service (DoS) through web page parameters.

![image-20230919165535424](DIR-619L Buffer Overflow_2/image-20230919165535424.png)

## 1.formSetLog Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608509363528.png)

### POC

![img](DIR-619L Buffer Overflow_2/170608511820431.png)

## 2.formTcpipSetup Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608514994134.png)

### POC

![img](DIR-619L Buffer Overflow_2/170608515748337.png)

## 3.formAutoDetecWAN_wizard4 Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608517708140.png)

![img](DIR-619L Buffer Overflow_2/170608519175543.png)

### POC

![image-20240124165630365](DIR-619L Buffer Overflow_2/image-20240124165630365.png)

## 4.formEasySetPassword Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608531815246.png)

### POC

![img](DIR-619L Buffer Overflow_2/170608532470049.png)

## 5.formEasySetTimezone Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608534311152.png)

### POC

![img](DIR-619L Buffer Overflow_2/170608535345755.png)

## 6.formSetWANType_Wizard5 Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608536998758.png)

![img](DIR-619L Buffer Overflow_2/170608537479261.png)

### POC

![img](DIR-619L Buffer Overflow_2/170608540750364.png)

## 7.formEasySetupWWConfig Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608543911567.png)

![img](DIR-619L Buffer Overflow_2/170608544518670.png)

### POC

![img](DIR-619L Buffer Overflow_2/170608545303373.png)

## 8.formSetWanNonLogin Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608546669876.png)

![img](DIR-619L Buffer Overflow_2/170608547292279.png)

### POC

![image-20240124165728525](DIR-619L Buffer Overflow_2/image-20240124165728525.png)

## 9.formSetWAN_Wizard51  Function

### Vulnerability analysis

The websGetVar function obtains the curtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608556458882.png)

![img](DIR-619L Buffer Overflow_2/170608557001485.png)

### POC

![image-20240124165740710](DIR-619L Buffer Overflow_2/image-20240124165740710.png)

## 10.formSetWAN_Wizard52 Function

### Vulnerability analysis

The websGetVar function obtains the currtime parameter from the front-end and stores the data on the stack through the sprintf function. However, due to the lack of data length restrictions, a buffer overflow vulnerability is created.

![img](DIR-619L Buffer Overflow_2/170608558375488.png)

![img](DIR-619L Buffer Overflow_2/170608559144691.png)

### POC

![image-20240124165751075](DIR-619L Buffer Overflow_2/image-20240124165751075.png)



