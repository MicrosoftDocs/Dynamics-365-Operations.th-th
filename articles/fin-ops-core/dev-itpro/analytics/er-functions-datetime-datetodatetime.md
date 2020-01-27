---
title: ฟังก์ชัน DATETODATETIME ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATETODATETIME
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916395"
---
# <a name="DATETODATETIME">ฟังก์ชัน DATETODATETIME ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `DATETODATETIME` ส่งกลับค่า *DateTime* ที่ถูกแปลงจากค่าวันที่ที่กำหนดให้เป็นค่าวันที่/เวลาในเวลาสากล (เวลามาตรฐานกรีนิช \[GMT\])

## <a name="syntax"></a>ไวยากรณ์

```
DATETODATETIME (date)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`date`: *วันที่*

ค่าวันที่ที่แสดงวันที่ที่แปลง

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่และเวลา*

ค่าวันที่/เวลาที่เป็นผลลัพธ์

## <a name="example-1"></a>ตัวอย่างที่ 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` ส่งกลับวันที่ของเซสชัน Microsoft Dynamics 365 Finance ปัจจุบัน, 24 ธันวาคม 2015 เป็น **12/24/2015 12:00:00 น** ในตัวอย่างนี้ **CompInfo** เป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ของชนิด **Finance and Operations/Table** และอ้างอิงถึงตาราง CompanyInfo

## <a name="example-2"></a>ตัวอย่างที่ 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` ส่งกลับค่าวันที่/เวลา **11/12/2019 12:00:00 น.**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)
