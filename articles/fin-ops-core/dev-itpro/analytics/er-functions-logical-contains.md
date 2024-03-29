---
title: ฟังก์ชัน CONTAINS ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชัน CONTAINS การรายงานทางอิเล็กทรอนิกส์ (ER)
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0b2831f8aec4847279953ebcea583c9218d214a7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273142"
---
# <a name="contains-er-function"></a>ฟังก์ชัน CONTAINS ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `CONTAINS` นี้จะระบุว่าข้อมูลป้อนเข้าที่ระบุมีข้อความที่ระบุหรือไม่ จะส่งกลับค่า *Boolean* ของ **TRUE** หากอินพุตที่ระบุมีข้อความที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**

## <a name="syntax"></a>ไวยากรณ์

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`input`: *สตริง*

พาธที่ถูกต้องของสินค้าของแหล่งข้อมูลของชนิด *สตริง* หรือค่าคงที่ของสตริง ค่าที่อาจมีอาร์กิวเมนต์ที่สอง

`search text`: *สตริง*

พาธที่ถูกต้องของสินค้าของแหล่งข้อมูลของชนิด *สตริง* หรือค่าคงที่ของสตริง ค่าที่อาจมีอาร์กิวเมนต์แรก

## <a name="return-values"></a>ค่าที่ส่งคืน

*บูลีน*

ค่า *บูลีน* ที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ฟังก์ชันนี้สามารถใช้เพื่อระบุนิพจน์เงื่อนไขของฟังก์ชัน [ตัวกรองข้อมูล](er-functions-list-filter.md) เฉพาะเมื่อตั้งค่าคอนฟิกการแม็ปที่เกี่ยวข้องใน [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) เพื่อเข้าถึง [Microsoft Dataverse](/power-platform/admin/data-integrator) มิฉะนั้น ข้อยกเว้นจะเกิดขึ้นในขณะออกแบบ ข้อความที่คุณได้รับจะแนะนำให้คุณใช้ฟังก์ชัน [WHERE](er-functions-list-where.md) แทนที่จะใช้ฟังก์ชัน `FILTER`

## <a name="example-1"></a>ตัวอย่างที่ 1

นิพจน์ `CONTAINS ("abc", "d")` จะส่งคืน **FALSE** ในขณะที่นิพจน์ `CONTAINS ("abc", "C")` ส่งคืน **TRUE**

## <a name="example-2"></a>ตัวอย่างที่ 2

นิพจน์ `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` จะส่งคืน **TRUE** ถ้าค่าของฟิลด์ **ที่อยู่** ของแหล่งข้อมูล **แบบจำลอง** มีสตริง **DEU** มิฉะนั้น จะส่งคืน **FALSE**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันตรรกะ](er-functions-category-logical.md)
