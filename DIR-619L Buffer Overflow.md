# DIR-619L Buffer Overflow

**Vulnerability description**

D-Link DIR-619L B1 2.02 was found to contain a stack overflow in multiple functions. This vulnerability allows attackers to trigger a denial of service (DoS) through web page parameters.

![image](https://github.com/YTrick/vuln/assets/57278844/38ddd2a7-64dd-4c0f-9d6e-54e125a30408)

## 1.formResetStatistic Function

### Vulnerability analysis

The data gets from front-end is processed in the formResetStatistic function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=MGViMWJhNjg3ZTA4N2QwYjI5N2RiMjAwZmRiMjk2NTVfaGVFSndMbjJHN1pEWFVhakxkWVJrakxJMmFpa0g5b3BfVG9rZW46SG9COGJnZWI4b0ptVVZ4ek16aWNaRHRUbmtnXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=N2ViZGRjNmYxZDVlYjBhM2U3MDI0NGU3ZjY3NzU5YzNfdmdlTEt0SUJINXU3NWdRWG1qOE93ejhnWVluVHg2R0ZfVG9rZW46THRCUmJ1TElVb0I2c3J4RTA2UmNKOTFlbm9MXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=NDQwNTJlNWJmNjYyNjc1NWFkMTg1MmRkNDYzNTY2MTdfS0hXQUpOeXBJMzkxOVdyYXVUcDc0VmlVb05GZWNFcGpfVG9rZW46SHlLYWJjQjc0b0xlTEN4WFhhaGNycGxlbnVjXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=MmIyZDdjMzBiMjVlZWYzMTFkNjIxOTk0ZDMwMTgzMTRfYTk0c1RlVkJyUk10OXJMNHd3dExlQlU5aVoyVnZyNHVfVG9rZW46QkxuNmI1TklSb09lVVV4cHFTaWNrMm9kbmdnXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

## 2.formSetEnableWizard Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetEnableWizard function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=MmE2YjM3NTMwMjA5YTI4YjM3ZWU5YzE2MTk4MjJkMmVfNDhIYnFOME85N2E3UzVuSUhHNUlEVGQyeTdNZ1hQUnJfVG9rZW46UE9OY2JSaklBb29rQnJ4SXhVeWNCN01rbnVmXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=Y2Q5NGI1NTU1NWE3ZTUzMzFjOTU2YjlmZGY4OGZkNWZfMHE2T1hjaUxBaU4wNnROOURSODROV1FNSnc3aldDalVfVG9rZW46RDRiUWJNRk9Rb0czUTl4OEVHdmNndm1FbjZkXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

## 3.formSetWizard1 Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetWizard1 function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=ZGQ5OTJkNDY1NmVkYzZmMzM4ZGI2MmEzZGFhYTBhZTJfRVpCTEliOUJTY0lFUFgzdWtJelZobEN0eTFYTWF6T0hfVG9rZW46V1A3MGJJTTVlb0R4ZnJ4OVFlZ2NKajlIbnJkXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=MmIyNjk1NDQ1MWMwNWYxOTY5MWZkNjVjY2NlODE1MTVfazB5QUtEUldyM0JTOERIOE9hOWg0d1RjYUltMFE4U3dfVG9rZW46R2V4c2I2Smtab0VNZEl4QnhBRWNBY1BWblNjXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

## 4.formSetWizard2 Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetWizard2 function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=Y2JhMWY4ODFkODU3ZDA2ZDY0ZWJiOTg5ZTFjOTRhY2RfSGNKRGV5aDZiY1VpazhvVXdERzVmR0RDRE4wMWJmaTlfVG9rZW46RVRtbGJwTkVab2h6Wk14WVBhTWNIY1JybndoXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=MjI1Y2RkNGZhOWMyOWNmZGMwZmIwYTU1ZDBiMWY3YjFfMkZmenRsbGRyaVh4NmdMNjFpZWFPTlRVd05PVkhpZW1fVG9rZW46Q2FGWGJzZnJ6b0xPTHl4bWNVQ2NHQlVUbjhiXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

## 5.formSetWizardSelectMode Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetWizardSelectMode function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=NTQzNWJhZGMzMmY1MGMxMDNkODc2NTRlMDgxMTdiNmJfWHYxWVZYQnZZRlQ4TWl2TWQ4U1lMTVlYOUx3bXBlTzdfVG9rZW46RVdLcGIzRTF0b3dnMWt4NTVvemNzVDNQbjZmXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=MWZkNDZmNzQzYWM4NDljOTA3OTM2ZGQzMDI2YTQ5MjlfUWxmUE5xYm1idFdKT3JKNVlkdGMzdGtGZUgyNXY0NWdfVG9rZW46VmUzNWJnUWNPb1NDMDh4bGp6UWNTVUI1bmRoXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

## 6.formLogin Function

### Vulnerability analysis

The data gets from front-end is processed in the formLogin function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=YjcxNjQzZmE5ZWFiOTc1ZDZlYjY1MzA5MWNhMGRhMDRfVzdTT2F6RllQaWFzbGFyT215Z3JlWWRZYWtIWnQ5c25fVG9rZW46TW55dGJBMVFrb0dTREV4MHY1RmNIakRkblFiXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=YzUxMDUyYTg4MmFmMjMzZGJkZmZiOTkyNTE0OTc0ODFfVk5jaFFoTUN3VDFRZ25sRUdRVG9ZRVQ2a2xKNFFDUVhfVG9rZW46Q1paZ2JudHpYb1VuVlJ4RlBEYWNxSnRrblI3XzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=ZThiNDQ3ZGQxMWEyYzkwYjc3MTc3OWIxODk5NmExYTZfV01Fc1hmS0lFNzNJTTJ0VlZZU2ZiaklocEx4ZWVEcnhfVG9rZW46UU85VmJmN21Tb0pUSVR4S0pIcWM2SG1kbjRlXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

## 7.formSetEmail Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetEmail function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=NjJkNGM5MzFlMzJjY2Y2MmM3ZWM4MTE5YzUxM2RjMjhfSUZhNmlVV1VzclZQOHE1MTM2SXhkNmZ1VmR6Y3VIN2hfVG9rZW46TjVBeWJmOWJTb0Z2ZDZ4ZlNpRmNYOWxhbmdlXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=OTE0MWE1ZTk1ZWI1MzIyOTUyNmEzYjI2MmMzMDAzYmVfbkN0Smp1ajljaDVBOERGTTVBVEg3RFR1M2hkdjN6bHpfVG9rZW46TkswTmJTRTJXb0JIRmJ4cElUWmMzRG84bkVlXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=NDVlZGZmMjcwMWQ3MWU5ZWVkYzdlNWRhODMwY2M0MjlfRWNKQjFhUTBvQnVaTmN2U0Z0T0NsTWJ4ZERaRXJRaG5fVG9rZW46RDVUV2Iydlpqb09XUXl4ckNWUmNZWlo2bjVmXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

## 8.formEasySetupWizard Function

### Vulnerability analysis

The data gets from front-end is processed in the formEasySetupWizard function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=MmY0NDA0YjVmZWFlZmYzODg3YjYyZjVjOWE0NGQ0NTFfSGpPcVNPNDBwY1NPbUZDaTM0YVVNSEtjd1pWdURhMnBfVG9rZW46SzljU2J4cmN3b2lrd0F4YTFIWGNvVllhbnNjXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=Y2Q5YmEwZjY2ZDE5NjQ0NWIxZjQ3NWViM2YzMzgyMmZfWU5XT292ZjVjNnBOa1c0bnpHSlcxNmRqbXhNbFdiV1lfVG9rZW46Qk56bmI4OWNjbzhGUHJ4YnJMaGNBRU1FbmtjXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

## 9.formSetPassword Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetPassword function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=ZGY2ZGUzYTk2MDg4MDM2ZTkwOTQ4ZTI0M2Y2ZGU4OTBfSWpVOGpDb0xvWjVKNDJRWU1vNGhCT2JVdDAyUEJqZGlfVG9rZW46RWJ3OWI1ZHR1b3Fja0R4U2RhV2NFcllobkZmXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=YTZlMDRkNDhiNDEzNzE5OWVkZWI5YjEzYjFmN2VlZDlfZmJ1U0NMTlliUUJ3UFplWThhVnVZdlByQkQ3aHRJdUhfVG9rZW46UjRvRWJsSUhnb3lYejN4b095VmNZQWRzbjhjXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=YTM1ZDAyMzRmNWRmZjEzZmE2YTgxNDQxOGZiZDAyYThfWlE1akN1T3JHcmtMOU9OZ0NQbmNMd0NBZmpCVEpRMnZfVG9rZW46WkxoR2J1dlBLb0ZqRG14dkJ1YWNnS3l2bnhkXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

## 10.formSetEasy_Wizard Function

### Vulnerability analysis

The data gets from front-end is processed in the formSetEasy_Wizard function, the websGetVar function gets the data passed in from the front end, and the sprintf is used later to directly store the data in the stack buffer. so it will overwrite the normal data in the stack, and that will cause crash.

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=YWE0NmMzOTAxNmQwNTg0YmEzM2VhMDJjYzkxMWU2NmFfa1pqYkZBTzY1Q0ZWc3ZZbE55dFZjRTVKWkxGcXhKazNfVG9rZW46UnJoTGJuV1JLbzJ5blp4Q1pIeWM5Z2NWbkRnXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)

### POC

![img](https://r1bj0v83p8l.feishu.cn/space/api/box/stream/download/asynccode/?code=Y2QyNjA3N2ViNTM4NjEwNDdiYzdkZTgwNmFmYjY3ZDVfNTloNzQwSDQxRnowa3pYU0ZEbkViN1M3allHR0w4bEdfVG9rZW46TW1VcGJERlNZb2VRbmp4T3VJT2NSSVc4blZiXzE2OTM5ODM5NDA6MTY5Mzk4NzU0MF9WNA)
