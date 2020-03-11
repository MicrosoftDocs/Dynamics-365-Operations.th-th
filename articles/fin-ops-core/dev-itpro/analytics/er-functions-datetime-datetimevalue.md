---
title: ฟังก์ชัน DATETIMEVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATETIMEVALUE
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 29d81599563dec2827fa8a82c86b74cb9e34eea2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070701"
---
# <a name="DATETIMEVALUE">ฟังก์ชัน DATETIMEVALUE ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `DATETIMEVALUE` ส่งกลับค่า *DateTime* ที่แปลงจากค่าข้อความที่ให้ในรูปแบบที่ระบุและใน [Culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ข้อความที่แสดงถึงค่าไปยังรูปแบบ

`format`: *สตริง*

รูปแบบของข้อความที่ให้

`culture`: *สตริง*

วัฒนธรรมที่ใช้สำหรับการจัดรูปแบบของข้อความที่กำหนด

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่และเวลา*

ค่าวันที่/เวลาที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

เมื่อวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก ตัวอย่างเช่น ถ้าฟังก์ชัน `DATETIMEVALUE` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน ค่า `culture` เริ่มต้นคือ **EN-US**

## <a name="example-1"></a>ตัวอย่างที่ 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` ส่งกลับ **2:55:00 AM ในวันที่ 21 ธันวาคม 2016** ขึ้นอยู่กับรูปแบบที่กำหนดเองที่ระบุและวัฒนธรรม **EN-US** ของแอปพลิเคชันเริ่มต้น

## <a name="example-2"></a>ตัวอย่างที่ 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` ส่งกลับ **2:55:00 AM ในวันที่ 21 ธันวาคม 2016** ตามรูปแบบและวัฒนธรรมที่กำหนดเองที่ระบุ

อย่างไรก็ตาม `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` จะส่งข้อยกเว้นเพื่อแจ้งผู้ใช้ว่าไม่รับรู้สตริงที่ระบุว่าเป็นค่าวันที่/เวลาสำหรับวัฒนธรรมที่ระบุที่ถูกต้อง

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)
