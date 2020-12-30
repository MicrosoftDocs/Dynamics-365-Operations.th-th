---
title: ฟังก์ชั่น FORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ FORMAT (ER)
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b347a7209ee543f6bd687c2864203eb632d6a4a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688424"
---
# <a name="format-er-function"></a>ฟังก์ชั่น FORMAT ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `FORMAT` ส่งคืนสตริงที่ระบุเป็นค่า *สตริง* หลังจากที่ได้ถูกจัดรูปแบบโดยการแทนที่การเกิดเหตุการณ์ใดๆ ของ **%N** ด้วยอาร์กิวเมนต์ลำดับที่ *N*

## <a name="syntax"></a>ไวยากรณ์

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>อาร์กิวเมนต์

`string`: *สตริง*

การอ้างอิงถึงแหล่งข้อมูลของชนิด *สตริง* ที่ต้องถูกจัดรูปแบบ ต้องระบุอาร์กิวเมนต์นี้

`argument 1`: *สตริง*

อาร์กิวเมนต์แรกซึ่งใช้ในการแทนที่เหตุการณ์ของ **%1** ต้องระบุอาร์กิวเมนต์นี้

`argument N`: *สตริง*

อาร์กิวเมนต์ลำดับที่ *N* ซึ่งใช้ในการแทนที่เหตุการณ์ของ **%2** **%3** และอื่นๆ อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ถ้าอาร์กิวเมนต์ไม่ได้มีให้สำหรับพารามิเตอร์ พารามิเตอร์จะถูกส่งกลับเป็น **"%N"** ในสตริง สำหรับค่าของชนิด *จำนวนจริง* การแปลงสตริงเริ่มต้นจะถูกจำกัดเป็นทศนิยมสองตำแหน่ง

## <a name="example"></a>ตัวอย่าง

ในภาพประกอบต่อไปนี้ แหล่งข้อมูล **PaymentModel** ส่งกลับรายการของเรกคอร์ดลูกค้าโดยใช้ส่วนประกอบ **ลูกค้า** จะส่งกลับค่าวันที่ประมวลผลโดยใช้ฟิลด์ **ProcessingDate**

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่ถูกออกแบบเพื่อสร้างไฟล์อิเล็กทรอนิกส์สำหรับลูกค้าที่เลือกไว้ **PaymentModel** จะถูกเลือกเป็นแหล่งข้อมูล และจะควบคุมโฟลว์การประมวลผล เมื่อลูกค้าที่เลือกถูกหยุดดำเนินการสำหรับวันที่ เมื่อมีการประมวลผลรายงาน ข้อยกเว้นถูกส่งเพื่อแจ้งผู้ใช้ สูตรที่ออกแบบมาสำหรับการประมวลผลตัวควบคุมชนิดนี้สามารถใช้ทรัพยากรต่อไปนี้:

- สัญลักษณ์ SYS70894 ประกอบไปด้วยข้อความต่อไปนี้:

    - **สำหรับภาษา EN-US:** "ไม่มีสิ่งที่จะพิมพ์"
    - **สำหรับภาษา DE:** "Nichts zu drucken"

- สัญลักษณ์ SYS18389 ประกอบไปด้วยข้อความต่อไปนี้:

    - **สำหรับภาษา EN-US:** "ลูกค้า %1 ถูกหยุดสำหรับ %2"
    - **สำหรับภาษา DE:** "Debitor '%1' wird für %2 gesperrt"

นี่คือนิพจน์ที่สามารถถูกออกแบบได้

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

ถ้ามีการประมวลผลรายงานสำหรับลูกค้า **Litware Retail** เมื่อวันที่ 17 ธันวาคม 2015 ในวัฒนธรรม **EN-US** และภาษา **EN-US** สูตรนี้จะส่งคืนข้อความต่อไปนี้ ซึ่งสามารถแสดงเป็นข้อความต่อผู้ใช้ เป็นข้อความแสดงข้อยกเว้น:

*ไม่มีสิ่งใดจะพิมพ์ Customer Litware Retail ถูกหยุดดำเนินการสำหรับ 12/17/2015"*

ถ้ารายงานเดียวกันถูกประมวลผลสำหรับลูกค้า **Litware Retail** เมื่อวันที่ 17 ธันวาคม 2015 ในวัฒนธรรม **DE** และภาษา **DE** สูตรจะคืนค่าข้อความต่อไปนี้ ซึ่งใช้รูปแบบวันที่ที่แตกต่างกัน:

*Nichts zu drucken Debitor 'Litware Retail' wird für 17.12.2015 gesperrt*

>[!NOTE]
> ไวยากรณ์ต่อไปนี้จะใช้ในสูตร ER สำหรับป้ายชื่อ:
>
> - **สำหรับป้ายชื่อจากทรัพยากรในแอป Microsoft Dynamics 365 Finance :** **\@X** ที่ซึ่ง **X** คือรหัสป้ายชื่อใน Application Object Tree (AOT)
> - **สำหรับป้ายชื่อที่อยู่ในการตั้งค่าคอนฟิก:** **@"GER_LABEL:X"** ที่ซึ่ง **X** คือรหัสป้ายชื่อในการตั้งค่าคอนฟิก ER

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)
