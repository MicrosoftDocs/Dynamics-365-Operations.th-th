---
title: ฟังก์ชัน FILTER ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FILTER
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: dfa4afdcfad8c1855a10e1fa37c36cc5b20682ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884530"
---
# <a name="filter-er-function"></a>ฟังก์ชัน FILTER ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `FILTER` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* หลังจากที่การสอบถามถูกเปลี่ยนเพื่อให้กรองตามเงื่อนไขที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

`condition`: *บูลีน*

นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ใช้ในการกรองเรกคอร์ดของรายการที่ระบุ

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a><a name="usage-notes"></a>บันทึกย่อการใช้งาน

ฟังก์ชันนี้แตกต่างจากฟังก์ชัน [WHERE](er-functions-list-where.md) เนื่องจากเงื่อนไขที่ระบุจะถูกนำไปใช้กับการรายงานทางอิเล็กทรอนิกส์ (ER) ใดๆ แหล่งข้อมูลของชนิด *เรกคอร์ดตาราง* ที่ระดับฐานข้อมูล สามารถกำหนดรายการและเงื่อนไขได้โดยใช้ตารางและความสัมพันธ์

ถ้าอาร์กิวเมนต์หนึ่งหรือทั้งคู่ที่ถูกกำหนดค่าสำหรับฟังก์ชันนี้ (`list` และ `condition`) อนุญาตให้มีการแปลการร้องขอนี้ไปยังการเรียก SQL โดยตรง จะมีข้อยกเว้นเกิดขึ้นในเวลาออกแบบ ข้อยกเว้นนี้จะแจ้งให้ผู้ใช้ทั้ง `list` หรือ `condition` ทราบว่าหรือไม่สามารถใช้เพื่อสอบถามฐานข้อมูล

> [!NOTE]
> ฟังก์ชัน `FILTER` ใช้แตกต่างจากฟังก์ชัน `WHERE` เมื่อฟังก์ชัน [`VALUEIN`](er-functions-logical-valuein.md) ใช้เพื่อระบุเงื่อนไขการเลือก
> 
> - ถ้าใช้ฟังก์ชัน `VALUEIN` ในขอบเขตของฟังก์ชัน `WHERE` และอาร์กิวเมนต์ที่สองของ `VALUEIN` อ้างอิงไปยังแหล่งข้อมูลที่ส่งคืนไม่มีเรกคอร์ด ระบบถือว่าค่าบูลีน *[เท็จ](er-formula-supported-data-types-primitive.md#boolean)* ที่`VALUEIN` ส่งคืน ดังนั้น นิพจน์จะไม่ส่งคืน `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` เรกคอร์ดผู้จัดจำหน่าย ถ้าแหล่งข้อมูล **VendGroups** ไม่ส่งคืนเรกคอร์ดกลุ่มผู้จัดจำหน่ายใดๆ
> - ถ้าใช้ฟังก์ชัน `VALUEIN` ในขอบเขตของฟังก์ชัน `FILTER` และอาร์กิวเมนต์ที่สองของ `VALUEIN` อ้างอิงไปยังแหล่งข้อมูลที่ส่งคืนไม่มีเรกคอร์ด ระบบไม่ถือว่าค่าบูลีน *[เท็จ](er-formula-supported-data-types-primitive.md#boolean)* ที่`VALUEIN` ส่งคืน ดังนั้น นิพจน์จะส่งคืน `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` เรกคอร์ดผู้จัดจำหน่ายทั้งหมดของแหล่งข้อมูล **ผู้จัดจำหน่าย** แม้ว่าแหล่งข้อมูล **VendGroups** ไม่ส่งคืนเรกคอร์ดกลุ่มผู้จัดจำหน่าย

## <a name="example-1"></a>ตัวอย่างที่ 1

ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่อ้างอิงถึงตาราง VendTable นิพจน์ `FILTER (Vendors, Vendors.VendGroup = "40")` จะส่งกลับรายการของเพียงแค่ผู้จัดจำหน่ายที่เป็นของกลุ่มผู้จัดจำหน่าย 40

## <a name="example-2"></a>ตัวอย่างที่ 2

ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่อ้างอิงถึงตาราง VendTable และถ้า **parmVendorBankGroup** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่ส่งกลับค่าเป็นชนิดข้อมูล *สตริง* นิพจน์ `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` จะส่งกลับรายการของบัญชีผู้จัดจำหน่ายที่เป็นของกลุ่มธนาคารหนึ่งๆ เท่านั้น

## <a name="example-3"></a>ตัวอย่างที่ 3

คุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("A,B,C", ",")` จากนั้นคุณป้อนนิพจน์อื่น `FILTER( DS, DS.Value = "B")` เมื่อคุณพยายามที่จะบันทึกนิพจน์นี้ในโปรแกรมออกแบบสูตร ER ข้อยกเว้นต่อไปนี้จะเกิดขึ้น: "ข้อผิดพลาดการตรวจสอบ: นิพจน์รายการของฟังก์ชันตัวกรองไม่สามารถเป็นแบบสอบถามได้"

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
