---
title: รายการของฟังก์ชั่น ER ในประเภทตรรกะ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันตรรกะที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: a37b3341b05fde1283a21a0c52faec26cd1a7030
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686205"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>รายการของฟังก์ชั่น ER ในประเภทตรรกะ

[!include [banner](../includes/banner.md)]

ฟังก์ชันตรรกะของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อทำงานกับค่าตรรกศาสตร์เพื่อดำเนินการเปรียบเทียบมากกว่าหนึ่งในนิพจน์เดียวหรือทดสอบหลายเงื่อนไข หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้

## <a name="list-of-supported-functions"></a>รายการฟังก์ชันที่ได้รับการสนับสนุน

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [และ](er-functions-logical-and.md)                       | ฟังก์ชันนี้ส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |
| [กรณี](er-functions-logical-case.md)                     | ฟังก์ชันนี้ประเมินค่าของนิพจน์ที่ระบุกับตัวเลือกอื่นที่ระบุและส่งกลับผลลัพธ์ของตัวเลือกแรกที่เท่ากับค่าของนิพจน์ที่ระบุ มิฉะนั้นจะส่งกลับผลลัพธ์เริ่มต้นที่เป็นตัวเลือกหากมีการระบุผลลัพธ์เริ่มต้นเป็นอาร์กิวเมนต์สุดท้ายของฟังก์ชันที่เรียกว่าไม่ได้นำหน้าด้วยตัวเลือก ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน |
| [ถ้า](er-functions-logical-if.md)                         | ฟังก์ชันนี้ส่งคืนค่าที่ระบุค่าแรก หากตรงตามเงื่อนไขที่ที่ระบุ มิฉะนั้นจะส่งคืนค่าที่สองที่ระบุ ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน |
| [ไม่ใช่](er-functions-logical-not.md)                       | ฟังก์ชันนี้ส่งกลับค่าตรรกศาสตร์ที่ถูกย้อนกลับของเงื่อนไขที่ระบุเป็นค่า *บูลีน* |
| [Or](er-functions-logical-or.md)                         | ฟังก์ชันนี้ส่งกลับค่า *บูลีน* ของ **FALSE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นเท็จ ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง ฟังก์ชันจะส่งกลับค่า *บูลีน* ของ **TRUE** |
| [ValueIn](er-functions-logical-valuein.md)               | ฟังก์ชันนี้กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่าใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่ จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | ฟังก์ชันนี้กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่า *Int64* หรือ *Integer* ใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่ จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |


## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)

[ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting-formula-designer.md)

[ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]