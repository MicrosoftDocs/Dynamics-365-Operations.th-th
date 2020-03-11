---
title: ฟังก์ชัน CHAR ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CHAR (ER)
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041249"
---
# <a name="CHAR">ฟังก์ชัน CHAR ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `CHAR` ส่งกลับค่า *สตริง* ที่นำเสนออักขระเดี่ยวที่ถูกอ้างอิงโดยหมายเลข Unicode ที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
CHAR (number)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *เลขจำนวนเต็ม*

ตัวเลขที่สอดคล้องกับอักขระเดี่ยวที่คาดไว้

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

สตริงที่ฟังก์ชันนี้ส่งคืนจะขึ้นอยู่กับการเข้ารหัสที่เลือกไว้ในองค์ประกอบรูปแบบ **FILE** หลัก สำหรับรายการของการเข้ารหัสที่สนับสนุน ดู [การเข้ารหัสคลาส](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx)

## <a name="example"></a>ตัวอย่าง

`CHAR (255)` ส่งกลับค่า **"ÿ"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)
