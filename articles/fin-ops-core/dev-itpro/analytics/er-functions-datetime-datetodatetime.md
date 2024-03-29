---
title: ฟังก์ชัน DATETODATETIME ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATETODATETIME
author: kfend
ms.date: 12/04/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 30fe75c7fd68edfff3e3778192723792d0f342ab
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287322"
---
# <a name="datetodatetime-er-function"></a>ฟังก์ชัน DATETODATETIME ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `DATETODATETIME` ส่งกลับค่า *DateTime* ที่ถูกแปลงจากค่าวันที่ที่กำหนดให้เป็นค่าวันที่/เวลาในเวลาสากล (เวลามาตรฐานกรีนิช \[GMT\])

## <a name="syntax"></a>ไวยากรณ์

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`date`: *วันที่*

ค่าวันที่ที่แสดงวันที่ที่แปลง

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่และเวลา*

ค่าวันที่/เวลาที่เป็นผลลัพธ์

## <a name="example-1"></a>ตัวอย่างที่ 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` ส่งกลับวันที่ของเซสชัน Microsoft Dynamics 365 Finance ปัจจุบัน, 24 ธันวาคม 2015 เป็น **12/24/2015 12:00:00 น** ในตัวอย่างนี้ **CompInfo** เป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ของชนิด **การเงินและการดำเนินงาน/ตาราง** และอ้างอิงถึงตาราง CompanyInfo

## <a name="example-2"></a>ตัวอย่างที่ 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` ส่งกลับค่าวันที่/เวลา **11/12/2019 12:00:00 น.**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
