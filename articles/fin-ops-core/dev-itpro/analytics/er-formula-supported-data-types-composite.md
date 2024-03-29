---
title: ชนิดข้อมูลแบบรวมที่ได้รับการสนับสนุนสําหรับสูตรการรายงานทางอิเล็กทรอนิกส์
description: บทความนี้แสดงข้อมูลเกี่ยวกับชนิดข้อมูลแบบรวมที่รองรับในสูตรการรายงานทางอิเล็กทรอนิกส์ (ER)
author: kfend
ms.date: 06/02/2021
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: ea6f8ab1f0cd26fd2414a17be559aa60fc52e7d3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272726"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>ชนิดข้อมูลแบบรวมที่ได้รับการสนับสนุนสําหรับสูตรการรายงานทางอิเล็กทรอนิกส์

[!include [banner](../includes/banner.md)]

บทความนี้แสดงข้อมูลเกี่ยวกับชนิดข้อมูลแบบรวมที่รองรับในนิพจน์ [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) ชนิดข้อมูลแบบรวมคือ [คลาส](#class) [คอนเทนเนอร์](#container) [เรกคอร์ด](#record) [รายการเรกคอร์ด](#record-list) และ [ออบเจ็กต์](#object)

## <a name="class"></a><a name="class"></a>คลาส

ชนิดข้อมูล *คลาส* อ้างอิงถึงคลาสแอปพลิเคชันสาธารณะ ใน ER จะแสดงเป็น [*เรกคอร์ด*](#record) ที่มีฟิลด์แยกต่างหากสําหรับวิธีการสาธารณะทั้งหมดของคลาสที่อ้างอิง เมื่อการเรียกของวิธีการถูกทำเป็นพารามิเตอร์ คุณต้องระบุอาร์กิวเมนต์ที่จำเป็นของชนิดที่เหมาะสมในนิพจน์ ER ที่กำหนดค่าเพื่อเรียกใช้วิธีการ

ในส่วนประกอบการแมปและรูปแบบ ER คุณสามารถเพิ่มแหล่งข้อมูล **คลาส** ที่แสดงเป็นแหล่งข้อมูลและส่งกลับค่าชนิด *คลาส* ได้ แหล่งข้อมูลนี้แสดงวิธีการสาธารณะของคลาสที่สามารถเรียกขณะใช้งานจริง

> [!NOTE]
> เฉพาะวิธีการที่ส่งกลับค่าเท่านั้นที่สามารถเรียกได้จากนิพจน์ ER
>
> เฉพาะวิธีการที่มีช่วงของอาร์กิวเมนต์ศูนย์ถึงแปดอาร์กิวเมนต์เท่านั้นที่สามารถเรียกได้จากนิพจน์ ER

ค่าเริ่มต้นของ *คลาส* คือ **null**

ภาพประกอบต่อไปนี้แสดงวิธีการเพิ่มแหล่งข้อมูล **ข้อมูลระบบ (xInfo)** ของชนิด **คลาส** เพื่อทําให้อินสแตนซ์ของคลาสแอปพลิเคชัน **xInfo** และเรียกใช้วิธีการ **productName()** เพื่อรับชื่อของแอปพลิเคชันปัจจุบัน ชื่อของแอปพลิเคชันปัจจุบันถูกดึงมาขณะทํางานโดยการดําเนินการของการผูก `xInfo.productName` ที่ถูกกําหนดค่าสําหรับฟิลด์ **ชื่อซอฟต์แวร์ (SoftwareName)** ของรูปแบบข้อมูล ER การผูกข้อมูลนี้เรียกวิธีการ `productName()` ของคลาสแอปพลิเคชัน **xInfo** ที่แสดงในการแมปแบบจําลองปัจจุบันเป็นแหล่งข้อมูล **ข้อมูลระบบ (xInfo)**

[![ตั้งค่าคอนฟิกแหล่งข้อมูลคลาส ในหน้าตัวออกแบบการแมปแบบจำลอง ER](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

ภาพประกอบต่อไปนี้แสดงวิธีการตั้งค่าคอนฟิกรูปแบบ ER เพื่อใส่ชื่อแอปพลิเคชันที่ให้ไว้ในเอกสารที่สร้างขึ้น ฟิลด์ **ชื่อซอฟต์แวร์ (SoftwareName)** ของรูปแบบข้อมูลที่ใช้ถูกผูกอยู่กับส่วนประกอบ **สตริง** ที่ซ้อนกันภายใต้องค์ประกอบ XML **softwareUsed** ของรูปแบบ ER ดังนั้นชื่อของแอปพลิเคชันปัจจุบันจะถูกวางขณะใช้งานจริงไปยังองค์ประกอบ XML **softwareUsed** ของเอกสารที่สร้างขึ้นในรูปแบบ XML

[![การตั้งค่าคอนฟิกโครงสร้างของเอกสารขาออกทางอิเล็กทรอนิกส์ในตัวออกแบบรูปแบบ ER](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>คอนเทนเนอร์

ชนิดข้อมูล *คอนเทนเนอร์* มีเนื้อหาแบบไบนารี ค่า *คอนเทนเนอร์* สามารถใช้ส่งผ่านข้อมูลเฉพาะจากที่เก็บข้อมูลไปยังเอกสารที่สร้างขึ้น ในกรอบงาน ER ชนิดข้อมูลนี้มักใช้ในใส่เนื้อหาสื่อ เช่น โลโกบริษัทในเอกสารที่สร้างขึ้น

> [!NOTE]
> แม้ว่าทุกรายการสื่อสามารถแสดงเป็นค่า *คอนเทนเนอร์* แต่ไม่ใช่ทุก *คอนเทนเนอร์* ที่แสดงถึงรายการสื่อได้ ดังนั้นถ้าคุณกําหนดค่ารูปแบบ ER เพื่อให้ใช้ *คอนเทนเนอร์* เพื่อใส่รูปในเอกสารที่สร้างขึ้น แต่ *คอนเทนเนอร์* ที่อ้างอิงไม่ส่งคืนเนื้อหาสื่อ ข้อยกเว้นที่คล้ายกับตัวอย่างต่อไปนี้อาจถูกโยน: "ข้อผิดพลาดในการดําเนินการรหัส: ไบนารี (วัตถุ)

ค่าเริ่มต้นของ *คอนเทนเนอร์* คือ **null**

ภาพประกอบต่อไปนี้แสดงวิธีที่ฟิลด์ **บิตแมป(ภาพ)** ของชนิด *คอนเทนเนอร์* ถูกผูกอยู่กับฟิลด์ **โลโก้** รูปแบบข้อมูลของชนิด **คอนเทนเนอร์** ในการแมปแบบจําลอง **ใบแจ้งหนี้การขาย** การผูกนี้ทําให้โลโก้บริษัทพร้อมใช้งานสําหรับรูปแบบ ER ใดๆ ที่ออกแบบมาสําหรับคํานิยามราก **SalesInvoice** และใช้การแมปแบบจําลองนี้ในขณะทํางาน

[![การผูกฟิลด์ของชนิดคอนเทนเนอร์ในตัวออกแบบการแมปแบบจําลอง ER](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>เรกคอร์ด

*เรกคอร์ด* คือชุดของฟิลด์ที่มีชื่อ ซึ่งแต่ละเรกคอร์ดจะสัมพันธ์กับค่าของชนิดข้อมูล [พื้นฐาน](er-formula-supported-data-types-primitive.md) หรือชนิดข้อมูลแบบรวม โดยปกติแล้ว *เรกคอร์ด* จะใช้เพื่อแสดงเรกคอร์ดเดียวของรายการเรกคอร์ด ในกรณีนี้ สินค้าทุกรายการจะแสดงฟิลด์ วิธีการ และความสัมพันธ์แต่ละฟิลด์

ค่าเริ่มต้นของ *เรกคอร์ด* คือ **ว่าง**

> [!NOTE]
> เมื่อคุณได้รับค่าของฟิลด์ของ *เรกคอร์ด* ว่าง ค่าเริ่มต้นของชนิดข้อมูลที่เหมาะสมจะถูกส่งกลับ

*เรกคอร์ด* สามารถได้รับโดยใช้ฟังก์ชันต่อไปนี้

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแปลงค่า *เรกคอร์ด* โปรดดูที่ [รายการของฟังก์ชัน ER ในประเภทรายการ](er-functions-category-list.md)

## <a name="record-list"></a><a name="record-list"></a>รายการเรกคอร์ด

*รายการเรกคอร์ด* คือรายการข้อมูลของชนิด *เรกคอร์ด* โดยปกติแล้ว *รายการเรกคอร์ด* จะใช้เพื่อแสดงรายการของเรกคอร์ดที่นํามาใช้จากตารางฐานข้อมูล

ตามค่าเริ่มต้น เรกคอร์ดของ *รายการเรกคอร์ด* จะเข้าถึงตามลําดับ เมื่อต้องการเข้าถึงเรกคอร์ดที่ระบุ คุณสามารถใช้ฟังก์ชัน [INDEX](er-functions-list-index.md) และระบุดัชนี *จำนวนเต็ม*

ค่าเริ่มต้นของ *รายการเรกคอร์ด* คือ **ว่าง** คุณสามารถใช้ฟังก์ชัน [ISEMPTY](er-functions-list-isempty.md) เพื่อประเมินว่า *รายการเรกคอร์ด* ว่างเปล่าหรือไม่

> [!NOTE]
> ถ้า *รายการเรกคอร์ด* ว่างเปล่า ความพยายามใดๆ ที่จะรับค่าฟิลด์สำหรับ *เรกคอร์ด* จะทำให้เกิดข้อยกเว้นถูกโยนในเวลาที่รัน เมื่อต้องการเรียนรู้วิธีที่คุณสามารถช่วยป้องกันข้อยกเว้นรันไทม์ของชนิดนี้ ให้ดูที่ [การพิจารณากรณีของรายการที่ว่าง](er-components-inspections.md#i9)

*รายการเรกคอร์ด* สามารถเริ่มโดยใช้ฟังก์ชันต่อไปนี้

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแปลงค่า *รายการเรกคอร์ด* โปรดดูที่ [รายการของฟังก์ชัน ER ในประเภทรายการ](er-functions-category-list.md) เมื่อต้องการเรียนรู้วิธีใช้ *รายการเรกคอร์ด* ใส่ข้อมูลแอปพลิเคชัน แล้วใช้ข้อมูลเพื่อสร้างเอกสารทางธุรกิจ ให้ดูที่ [ออกแบบโซลูชัน ER ใหม่เพื่อพิมพ์รายงานแบบกําหนดเอง](er-quick-start1-new-solution.md)

## <a name="object"></a><a name="object"></a>ออบเจ็กต์

*ออบเจกต์* อ้างถึงอินสแตนซ์ของ *คลาส* โดยปกติแล้ว *ออบเจกต์* จะถูกเริ่มต้นในโค้ดต้นฉบับ จากนั้นจะถูกส่งผ่านไปยังการแมปแบบจําลอง ER และให้รายละเอียดของบริบทการดําเนินการ

ค่าเริ่มต้นของ *ออบเจกต์* คือ **null**

ภาพประกอบต่อไปนี้แสดงวิธีการเพิ่มแหล่งข้อมูล **ReportDataContract** ของชนิด *ออบเจ็กต์* เพื่อส่งผ่านข้อมูลเกี่ยวกับใบแจ้งหนี้ที่สร้างขึ้นจากรหัสแหล่งที่มาไปยังการแมปแบบจําลอง **ใบแจ้งหนี้โครงการ** ตัวอย่างเช่น ข้อความอินสแตนซ์ใบแจ้งหนี้จะถูกส่งผ่านเป็นส่วนหนึ่งของบริบทการดําเนินการ ข้อความนี้นํามาจากซอร์สโค้ดขณะรันไทม์โดยการดําเนินการผูกข้อมูล `ReportDataContract.parmInvoiceInstanceText` ที่ถูกกําหนดค่าสําหรับฟิลด์ **หมายเหตุ** ของรูปแบบข้อมูล ER การผูกข้อมูลนี้เรียกวิธีการ `parmInvoiceInstanceText()` ของคลาสแอปพลิเคชัน **PSAProjInvoiceContract** ที่แสดงในการแมปแบบจําลองปัจจุบันเป็นแหล่งข้อมูล **ReportDataContract**

[![ตั้งค่าคอนฟิกแหล่งข้อมูลออบเจกต์ ในหน้าตัวออกแบบการแมปแบบจำลอง ER](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

เมื่อต้องการเรียนรู้วิธีส่งผ่านรายละเอียดของบริบทการดําเนินการจากโค้ดต้นฉบับไปยังโซลูชัน ER ที่กําลังทํางานอยู่ ให้ดูที่ [พัฒนาสิ่งประดิษฐ์ของแอปพลิเคชันเพื่อเรียกใข้รายงานที่ออกแบบไว้](er-quick-start1-new-solution.md#DevelopCustomCode)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)
- [ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)
- [ชนิดข้อมูลพื้นฐานที่รองรับ](er-formula-supported-data-types-primitive.md)
