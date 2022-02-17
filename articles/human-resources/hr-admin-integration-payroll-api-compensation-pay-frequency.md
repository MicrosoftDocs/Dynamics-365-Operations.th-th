---
title: ความถี่ในการจ่ายค่าตอบแทน
description: หัวข้อนี้แสดงรายละเอียดและการสอบถามตัวอย่างสำหรับเอนทิตีความถี่ในการจ่ายค่าตอบแทนใน Dynamics 365 Human Resources
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 171b7fb7b361bd1fe2e7e637cd555c88a81a8bcf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066154"
---
# <a name="compensation-pay-frequency"></a>ความถี่ในการจ่ายค่าตอบแทน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีความถี่ในการจ่ายค่าตอบแทนใน Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmpayrateconversionentity

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้แสดงข้อมูลเกี่ยวกับการแปลงอัตราค่าจ้างสำหรับความถี่ในการจ่ายค่าตอบแทนที่กําหนด

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **การแปลงอัตราค่าจ้างรายปี**</br>mshr_annualconversionfactor</br>*ทศนิยม* | อ่านอย่างเดียว | ตัวคูณการแปลงรายปีสำหรับความถี่ในการชำระเงิน |
| **คำอธิบาย**</br>msdyn_description</br>*สตริง* | อ่านอย่างเดียว | คำอธิบายของอัตราการแปลง |
| **การแปลงอัตราค่าจ้างรายชั่วโมง**</br>mshr_hourlyconversionfactor</br>*ทศนิยม* | อ่านอย่างเดียว | ตัวคูณการแปลงรายชั่วโมงสำหรับความถี่ในการชำระเงิน |
| **การแปลงอัตราค่าจ้างรายเดือน**</br>mshr_monthlyconversionfactor</br>*ทศนิยม* | อ่านอย่างเดียว | ตัวคูณการแปลงรายเดือนสำหรับความถี่ในการชำระเงิน |
| **การแปลงอัตราค่าจ้าง**</br>mshr_payrateconversion</br>*สตริง* | อ่านอย่างเดียว | สตริงเฉพาะที่จะระบุอัตราการแปลง |
| **รอบระยะเวลา**</br>mshr_period</br>*ชุดตัวเลือกรอบระยะเวลา* | อ่านอย่างเดียว | รอบระยะเวลาหลักสำหรับการแปลงอัตราค่าจ้างที่กำหนด |
| **การแปลงอัตราค่าจ้างรายสัปดาห์**</br>mshr_weeklyconversionfactor</br>*ทศนิยม* | อ่านอย่างเดียว | ตัวคูณการแปลงรายสัปดาห์สำหรับความถี่ในการชำระเงิน |
| **รหัสพื้นที่ข้อมูล**</br>mshr_dataareaid</br>*สตริง* | อ่านอย่างเดียว | นิติบุคคล (บริษัท) |
| **รหัสเอนทิตีของความถี่ในการจ่ายค่าตอบแทน**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | ระบบสร้างขึ้น | ค่ารหัสเฉพาะสากล (GUID) ที่ระบบสร้างขึ้นเพื่อระบุเรกคอร์ดโดยไม่ซ้ำกัน |

## <a name="example-query-for-payroll-employee"></a>ตัวอย่างการสอบถามของพนักงานในบัญชีเงินเดือน

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**การตอบสนอง**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
