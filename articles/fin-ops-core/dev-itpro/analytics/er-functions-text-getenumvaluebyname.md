---
title: ฟังก์ชัน GETENUMVALUEBYNAME ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ GETENUMVALUEBYNAME (ER)
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916855"
---
# <a name="GETENUMVALUEBYNAME">ฟังก์ชัน GETENUMVALUEBYNAME ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `GETENUMVALUEBYNAME` ค้นหาค่า *Enum* เฉพาะในแหล่งข้อมูลการแจงนับที่ระบุ โดยใช้ชื่อการแจงนับที่ระบุเป็นค่า *สตริง* ถ้าพบค่า *Enum* ฟังก์ชันจะส่งคืน มิฉะนั้น ฟังก์ชันจะส่งกลับค่าการแจงนับ **null**

## <a name="syntax"></a>ไวยากรณ์

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`enumeration data source path`: *การแจงนับ*

พาธที่ถูกต้องของแหล่งข้อมูลของหนึ่งในชนิดการแจงนับต่อไปนี้:

- การแจงนับแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER)
- การแจงนับรูปแบบ ER
- การแจงนับ Microsoft Dynamics 365 Finance

`enumeration value text`: *สตริง*

ค่าสตริงที่แสดงชื่อของค่าการแจงนับเดียว

## <a name="return-values"></a>ส่งคืนค่า

*Enum* ที่สามารถเว้นว่างได้

ค่าการแจงนับที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ไม่มีข้อยกเว้น หากไม่พบค่า *Enum* โดยใช้ชื่อของค่าการแจงนับที่ระบุเป็นค่า *สตริง*

## <a name="example"></a>ตัวอย่าง

ในแผนภาพต่อไปนี้ การแจงนับ **ReportDirection** ถูกนำมาใช้ในแบบจำลองข้อมูล โปรดทราบว่า ป้ายชื่อถูกกำหนดไว้สำหรับค่าแจงนับ

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

ภาพประกอบต่อไปนี้แสดงรายละเอียดเหล่านี้:

- แหล่งข้อมูล **$ทิศทาง** ถูกตั้งค่าคอนฟิกในรายงาน ER แหล่งข้อมูลนี้ถูกตั้งค่าคอนฟิกตามการแจงนับแบบจำลอง **ReportDirection**
- นิพจน์ `$IsArrivals` ถูกออกแบบมาเพื่อใช้การแจงนับแบบจำลอง–ที่ขึ้นกับ **$ทิศทาง** เป็นพารามิเตอร์ของฟังก์ชันนี้
- ค่าของนิพจน์การเปรียบเทียบนี้คือ **จริง**

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)
