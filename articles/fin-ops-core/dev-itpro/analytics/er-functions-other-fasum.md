---
title: ฟังก์ชัน FA_SUM ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ FA_SUM (ER)
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 03bed091350b39601edb22b5af6bda5a83af47eb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041365"
---
# <a name="FA_SUM">ฟังก์ชัน FA_SUM ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `FA_SUM` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่ประกอบด้วยข้อมูลสำหรับยอดเงินสินทรัพย์ถาวรสำหรับสินค้าสินทรัพย์ถาวรที่ระบุ รหัสแบบจำลองมูลค่า และรอบระยะเวลาของวันที่

## <a name="syntax"></a>ไวยากรณ์

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`fixed asset code`: *สตริง*

ค่า *สตริง* ที่แสดงถึงรหัสของรายการสินทรัพย์ถาวรที่มีการคำนวณยอดดุล

`value model code`: *สตริง*

ค่า *สตริง* ที่แสดงถึงรหัสของแบบจำลองค่าที่มีการคำนวณยอดดุล

`start date`: *วันที่*

ค่า *วันที่* แสดงถึงวันที่เริ่มต้นของรอบระยะเวลาที่มีการคำนวณยอดเงินสินทรัพย์ถาวร

`end date`: *วันที่*

ค่า *วันที่* แสดงถึงวันที่สิ้นสุดของรอบระยะเวลาที่มีการคำนวณยอดเงินสินทรัพย์ถาวร

## <a name="return-values"></a>ส่งคืนค่า

*คอนเทนเนอร์ (เรกคอร์ด)*

ค่าเรกคอร์ดที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` ส่งกลับค่าคอนเทนเนอร์ข้อมูลสำหรับสินทรัพย์ถาวร **COMP-000001** ที่เตรียมไว้สำหรับแบบจำลองค่า **ปัจจุบัน** และสำหรับรอบระยะเวลาตั้งแต่ **Date1** ถึง **Date2**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)
