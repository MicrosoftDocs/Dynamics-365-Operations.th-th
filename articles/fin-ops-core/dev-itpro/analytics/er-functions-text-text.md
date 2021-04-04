---
title: ฟังก์ชัน TEXT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TEXT (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560072"
---
# <a name="text-er-function"></a>ฟังก์ชัน TEXT ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `TEXT` ส่งคืนตัวเลขที่ระบุเป็นค่า *สตริง* หลังจากที่ได้ถูกแปลงเป็นข้อความแบบสตริงที่ถูกจัดรูปแบบตามการตั้งค่าตำแหน่งที่ตั้งของเซิร์ฟเวอร์ของอินสแตนซ์ของแอพลิเคชันปัจจุบัน

## <a name="syntax"></a>ไวยากรณ์

```vb
TEXT (number)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *จำนวนเต็ม* หรือ *จำนวนจริง*

หมายเลขที่ต้องถูกแปลงเป็นสตริงข้อความ

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

สำหรับค่าของชนิด *จำนวนจริง* การแปลงสตริงจะถูกจำกัดเป็นทศนิยมสองตำแหน่ง

## <a name="example"></a>ตัวอย่าง

ถ้าตำแหน่งที่ตั้งของเซิร์ฟเวอร์ของอินสแตนซ์ Microsoft Dynamics 365 Finance ถูกกำหนดเป็น **EN-US**, `TEXT (NOW ())` จะส่งคืนวันที่ของเซสชัน Finance ปัจจุบัน ซึ่งคือ17 ธันวาคม 2015 เป็นสตริงข้อความ **"12/17/2015 07:59:23 AM"** `TEXT (1/3)` ส่งคืน **"0.33"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]