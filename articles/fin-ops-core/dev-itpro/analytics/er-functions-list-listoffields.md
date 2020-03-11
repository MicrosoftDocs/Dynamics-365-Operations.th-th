---
title: ฟังก์ชัน LISTOFFIELDS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LISTOFFIELDS
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
ms.openlocfilehash: 0d51b59c437bd216c6d229546136bb604239fa92
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042009"
---
# <a name="LISTOFFIELDS">ฟังก์ชัน LISTOFFIELDS ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `LISTOFFIELDS` ส่งกลับค่า *รายการเรกคอร์ด* ที่สร้างขึ้นตามโครงสร้างของอาร์กิวเมนต์ที่ระบุของชนิด *การแจงนับ* หรือ *คอนเทนเนอร์ (เรกคอร์ด)*

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`path`: การอ้างอิงแหล่งข้อมูล

พาธอ้างอิงที่ถูกต้องของแหล่งข้อมูลของหนึ่งในชนิดข้อมูลต่อไปนี้:

- การแจงนับแบบจำลอง
- การแจงนับรูปแบบ
- การแจงนับแอปพลิเคชัน
- คอนเทนเนอร์ (เรกคอร์ด)

`language`: *สตริง*

ข้อความที่แสดงถึงรหัสภาษา

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

รายการที่สร้างขึ้นประกอบด้วยเรกคอร์ดที่มีฟิลด์ต่อไปนี้:

- **ชื่อ** (ชนิดข้อมูล *สตริง*)
- **ป้ายกำกับ** (ชนิดข้อมูล *สตริง*)
- **คำอธิบาย** (ชนิดข้อมูล *สตริง*)
- **IsTranslated** (ชนิดข้อมูล *บูลีน*)

ถ้าอาร์กิวเมนต์ `path` อ้างอิงถึงแหล่งข้อมูลของชนิด *คอนเทนเนอร์ (Record)* สำหรับทุกฟิลด์ของเรกคอร์ดคอนเทนเนอร์ที่อ้างอิง เรกคอร์ดใหม่จะถูกเพิ่มลงในรายการที่สร้างขึ้น สำหรับทุกเรกคอร์ดที่สร้างขึ้น ฟิลด์ **ชื่อ** จะส่งกลับชื่อของฟิลด์ของเรกคอร์ดคอนเทนเนอร์ที่อ้างอิงที่มีการสร้างเร็กคอร์ดปัจจุบัน

ถ้าอาร์กิวเมนต์ `path` อ้างอิงถึงแหล่งข้อมูลของชนิด *การแจงนับ* สำหรับทุกค่าการแจงนับของการแจงนับที่อ้างอิง เรกคอร์ดใหม่จะถูกเพิ่มลงในรายการที่สร้างขึ้น สำหรับทุกเรกคอร์ดที่ถูกสร้าง ฟิลด์ **ชื่อ** จะส่งกลับค่าของการแจงนับอ้างอิงที่มีการสร้างเร็กคอร์ดปัจจุบัน ฟิลด์ **คำอธิบาย** ส่งกลับคำอธิบายของการแจงนับนั้น และฟิลด์ **ป้ายชื่อ** ส่งกลับป้ายชื่อของการแจงนับนั้น

ขณะรันไทม์เมื่อมีใช้ไวยากรณ์ 1 ฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะต้องส่งคืนค่าที่ขึ้นอยู่กับการตั้งค่าภาษาของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่กำลังทำงานอยู่:

- ถ้าป้ายชื่อและคำอธิบายสำหรับภาษาที่ร้องขอพร้อมใช้งานฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะส่งกลับค่าที่เป็นไปตามภาษา และฟิลด์ **IsTranslated** ส่งคืนเป็น **จริง**
- ถ้าป้ายชื่อและคำอธิบายสำหรับภาษาที่ร้องขอไม่พร้อมใช้งาน ฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะส่งกลับค่าที่เป็นไปตามภาษาเริ่มต้น **EN-US** และฟิลด์ **IsTranslated** ส่งคืนเป็น **เท็จ**

ขณะรันไทม์เมื่อมีใช้ไวยากรณ์ 2 ฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะต้องส่งคืนค่าที่ขึ้นอยู่กับการตั้งค่าภาษาที่ระบุเป็นอาร์กิวเมนต์รองของฟังก์ชันที่เรียกใช้:

- ถ้าป้ายชื่อและคำอธิบายสำหรับภาษาที่ร้องขอพร้อมใช้งานฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะส่งกลับค่าที่เป็นไปตามภาษา และฟิลด์ **IsTranslated** ส่งคืนเป็น **จริง**
- ถ้าป้ายชื่อและคำอธิบายสำหรับภาษาที่ร้องขอไม่พร้อมใช้งาน ฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะส่งกลับค่าที่เป็นไปตามภาษา **EN-US** และฟิลด์ **IsTranslated** ส่งคืนเป็น **เท็จ**

## <a name="example-1"></a>ตัวอย่างที่ 1

ในแผนภาพต่อไปนี้ การแจงนับถูกนำมาใช้ในแบบจำลองข้อมูล ER

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

ภาพประกอบต่อไปนี้แสดงรายละเอียดเหล่านี้:

- การแจงนับแบบจำลองถูกใส่ลงในรายงานเป็นแหล่งข้อมูล
- นิพจน์ ER ใช้การแจงนับแบบจำลองเป็นพารามิเตอร์ของฟังก์ชัน `LISTOFFIELDS`
- แหล่งข้อมูลของชนิด *รายการเรกคอร์ด* ถูกแทรกลงในรายงานโดยใช้นิพจน์ ER ที่ถูกสร้างขึ้น

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

ตัวอย่างต่อไปนี้แสดงองค์ประกอบรูปแบบ ER ที่ผูกอยู่กับแหล่งข้อมูลของ *ชนิดรายการเรกคอร์ด* ที่ถูกสร้างโดยใช้ฟังก์ชัน `LISTOFFIELDS`

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบที่มีการออกแบบ

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> โดยสอดคล้องกับการตั้งค่าภาษาของ **FILE** หลักและองค์ประกอบรูปแบบ **FOLDER** ข้อความที่แปลสำหรับป้ายชื่อและคำอธิบายจะถูกป้อนลงในผลลัพธ์ของรูปแบบ ER

## <a name="example-2"></a>ตัวอย่างที่ 2

คุณใช้ชนิดแหล่งข้อมูล *ฟิลด์ที่คำนวณได้* เพื่อตั้งค่าคอนฟิกแหล่งข้อมูล **enumType\_de** และ **enumType\_deCH** สำหรับการแจงนับแบบจำลองข้อมูล **enumType**

- **enumType\_เดอ** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

ในกรณีนี้ คุณสามารถใช้นิพจน์ต่อไปนี้ในการเรียกใช้ป้ายชื่อของค่าการแจงนับในภาษาเยอรมันสวิสได้ ถ้าการแปลนี้พร้อมใช้งาน ถ้าไม่มีการแปลภาษาเยอรมันสวิส ป้ายชื่อจะอยู่ในภาษาเยอรมัน

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)
