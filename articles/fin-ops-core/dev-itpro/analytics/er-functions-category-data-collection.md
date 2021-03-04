---
title: รายการของฟังก์ชั่น ER ในประเภทการรวบรวมข้อมูล
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันการรวบรวมข้อมูลที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686304"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>รายการของฟังก์ชั่น ER ในประเภทการรวบรวมข้อมูล

[!include [banner](../includes/banner.md)]

ฟังก์ชันการรวบรวมข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) จะถูกใช้เพื่อทำการนับและการสรุปในรูปแบบ ER ที่กำลังรัน ขึ้นอยู่กับข้อมูลของผลลัพธ์ที่สร้างไว้ในรูปแบบ **ข้อความ** หรือ **Xml** วิธีการนี้จะใช้เพื่อช่วยปรับปรุงประสิทธิภาพของรูปแบบ ER ที่รันเพื่อป้อนค่าของการรันผลรวมในเอกสารที่สร้างขึ้นและเพื่อวัตถุประสงค์อื่นๆ หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้

## <a name="list-of-supported-functions"></a>รายการฟังก์ชันที่ได้รับการสนับสนุน

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | ฟังก์ชันนี้ส่งคืนค่า *รายการเรกคอร์ด* ที่ประกอบด้วยรายการของค่าที่ถูกส่งกลับโดยคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ขององค์ประกอบรูปแบบและเก็บรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ แต่ละเงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์ |
| [CountIF](er-functions-datacollection-countif.md) | ฟังก์ชันนี้ส่งกลับค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนขององค์ประกอบรูปแบบที่ถูกรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ เงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์ |
| [CountIFs](er-functions-datacollection-countifs.md) | ฟังก์ชันนี้ส่งกลับค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนขององค์ประกอบรูปแบบที่ถูกรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ แต่ละเงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์ |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงชื่อขององค์ประกอบรูปแบบ ER ปัจจุบัน |
| [SumIF](er-functions-datacollection-sumif.md) | ฟังก์ชันนี้ส่งกลับค่า *จำนวนจริง* ที่แสดงถึงผลรวมของค่าที่ส่งคืนโดยการผูกองค์ประกอบรูปแบบและการเก็บรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ เงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์ |
| [SumIFs](er-functions-datacollection-sumifs.md) | ฟังก์ชันนี้ส่งกลับค่า *จำนวนจริง* ที่แสดงถึงผลรวมของค่าที่ส่งคืนโดยการผูกองค์ประกอบรูปแบบและการเก็บรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ แต่ละเงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์ |

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)

[ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting-formula-designer.md)

[ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]