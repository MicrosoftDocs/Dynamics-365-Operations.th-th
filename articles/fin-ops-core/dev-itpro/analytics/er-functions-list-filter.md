---
title: ฟังก์ชัน FILTER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FILTER
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
ms.openlocfilehash: 55fa3d4ad4427e2a45f7c5fce679c50a91c40b6d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679449"
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

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ฟังก์ชันนี้แตกต่างจากฟังก์ชัน [WHERE](er-functions-list-where.md) เนื่องจากเงื่อนไขที่ระบุจะถูกนำไปใช้กับการรายงานทางอิเล็กทรอนิกส์ (ER) ใดๆ แหล่งข้อมูลของชนิด *เรกคอร์ดตาราง* ที่ระดับฐานข้อมูล สามารถกำหนดรายการและเงื่อนไขได้โดยใช้ตารางและความสัมพันธ์

ถ้าอาร์กิวเมนต์หนึ่งหรือทั้งคู่ที่ถูกกำหนดค่าสำหรับฟังก์ชันนี้ (`list` และ `condition`) อนุญาตให้มีการแปลการร้องขอนี้ไปยังการเรียก SQL โดยตรง จะมีข้อยกเว้นเกิดขึ้นในเวลาออกแบบ ข้อยกเว้นนี้จะแจ้งให้ผู้ใช้ทั้ง `list` หรือ `condition` ทราบว่าหรือไม่สามารถใช้เพื่อสอบถามฐานข้อมูล

## <a name="example-1"></a>ตัวอย่างที่ 1

ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่อ้างอิงถึงตาราง VendTable นิพจน์ `FILTER (Vendors, Vendors.VendGroup = "40")` จะส่งกลับรายการของเพียงแค่ผู้จัดจำหน่ายที่เป็นของกลุ่มผู้จัดจำหน่าย 40

## <a name="example-2"></a>ตัวอย่างที่ 2

ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่อ้างอิงถึงตาราง VendTable และถ้า **parmVendorBankGroup** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่ส่งกลับค่าเป็นชนิดข้อมูล *สตริง* นิพจน์ `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` จะส่งกลับรายการของบัญชีผู้จัดจำหน่ายที่เป็นของกลุ่มธนาคารหนึ่งๆ เท่านั้น

## <a name="example-3"></a>ตัวอย่างที่ 3

คุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("A,B,C", ",")` จากนั้นคุณป้อนนิพจน์อื่น `FILTER( DS, DS.Value = "B")` เมื่อคุณพยายามที่จะบันทึกนิพจน์นี้ในโปรแกรมออกแบบสูตร ER ข้อยกเว้นต่อไปนี้จะเกิดขึ้น: "ข้อผิดพลาดการตรวจสอบ: นิพจน์รายการของฟังก์ชันตัวกรองไม่สามารถเป็นแบบสอบถามได้"

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]