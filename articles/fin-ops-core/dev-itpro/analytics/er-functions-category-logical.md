---
title: รายการของฟังก์ชั่น ER ในประเภทตรรกะ
description: บทความนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันตรรกะที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 1d011968d9cfa4125e7283ca36c3558e3e79b93a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291308"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>รายการของฟังก์ชั่น ER ในประเภทตรรกะ

[!include [banner](../includes/banner.md)]

ฟังก์ชันตรรกะของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อทำงานกับค่าตรรกศาสตร์เพื่อดำเนินการเปรียบเทียบมากกว่าหนึ่งในนิพจน์เดียวหรือทดสอบหลายเงื่อนไข บทความนี้แสดงสรุปของฟังก์ชันเหล่านี้

## <a name="list-of-supported-functions"></a>รายการฟังก์ชันที่ได้รับการสนับสนุน

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [และ](er-functions-logical-and.md)                       | ฟังก์ชันนี้ส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |
| [กรณี](er-functions-logical-case.md)                     | ฟังก์ชันนี้ประเมินค่าของนิพจน์ที่ระบุกับตัวเลือกอื่นที่ระบุและส่งกลับผลลัพธ์ของตัวเลือกแรกที่เท่ากับค่าของนิพจน์ที่ระบุ มิฉะนั้นจะส่งกลับผลลัพธ์เริ่มต้นที่เป็นตัวเลือกหากมีการระบุผลลัพธ์เริ่มต้นเป็นอาร์กิวเมนต์สุดท้ายของฟังก์ชันที่เรียกว่าไม่ได้นำหน้าด้วยตัวเลือก ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน |
| [มี](er-functions-logical-contains.md)             | ฟังก์ชันนี้จะระบุว่าข้อมูลป้อนเข้าที่ระบุมีข้อความที่ระบุหรือไม่ จะส่งกลับค่า *Boolean* ของ **TRUE** หากอินพุตที่ระบุมีข้อความที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |
| [EndsWith](er-functions-logical-endswith.md)             | ฟังก์ชันนี้จะระบุว่าข้อมูลป้อนเข้าที่ระบุลงท้ายด้วยข้อความที่ระบุหรือไม่ จะส่งกลับค่า *Boolean* ของ **TRUE** หากอินพุตที่ระบุลงท้ายด้วยข้อความที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |
| [ถ้า](er-functions-logical-if.md)                         | ฟังก์ชันนี้ส่งคืนค่าที่ระบุค่าแรก หากตรงตามเงื่อนไขที่ที่ระบุ มิฉะนั้นจะส่งคืนค่าที่สองที่ระบุ ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน |
| [ไม่ใช่](er-functions-logical-not.md)                       | ฟังก์ชันนี้ส่งกลับค่าตรรกศาสตร์ที่ถูกย้อนกลับของเงื่อนไขที่ระบุเป็นค่า *บูลีน* |
| [Or](er-functions-logical-or.md)                         | ฟังก์ชันนี้ส่งกลับค่า *บูลีน* ของ **FALSE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นเท็จ ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง ฟังก์ชันจะส่งกลับค่า *บูลีน* ของ **TRUE** |
| [StartsWith](er-functions-logical-startswith.md)         | ฟังก์ชันนี้จะระบุว่าข้อมูลป้อนเข้าที่ระบุเริ่มต้นด้วยข้อความที่ระบุหรือไม่ จะส่งกลับค่า *Boolean* ของ **TRUE** หากอินพุตที่ระบุเริ่มด้วยข้อความที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |
| [ValueIn](er-functions-logical-valuein.md)               | ฟังก์ชันนี้กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่าใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่ จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | ฟังก์ชันนี้กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่า *Int64* หรือ *Integer* ใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่ จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |


## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)

[ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting-formula-designer.md)

[ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
