---
title: ฟังก์ชัน STARTSWITH ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชัน STARTSWITH การรายงานทางอิเล็กทรอนิกส์ (ER)
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
ms.openlocfilehash: 010646d2ab96d9a326ffb01c369726790b6377a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287232"
---
# <a name="startswith-er-function"></a>ฟังก์ชัน STARTSWITH ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `STARTSWITH` นี้จะระบุว่าข้อมูลป้อนเข้าที่ระบุเริ่มต้นด้วยข้อความที่ระบุหรือไม่ จะส่งกลับค่า *Boolean* ของ **TRUE** หากอินพุตที่ระบุเริ่มด้วยข้อความที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**

## <a name="syntax"></a>ไวยากรณ์

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`input`: *สตริง*

พาธที่ถูกต้องของสินค้าของแหล่งข้อมูลของชนิด *สตริง* หรือค่าคงที่ของสตริง ค่าที่อาจเริ่มต้นด้วยอาร์กิวเมนต์ที่สอง

`start text`: *สตริง*

พาธที่ถูกต้องของสินค้าของแหล่งข้อมูลของชนิด *สตริง* หรือค่าคงที่ของสตริง ค่าที่อาจเริ่มต้นด้วยอาร์กิวเมนต์แรก

## <a name="return-values"></a>ค่าที่ส่งคืน

*บูลีน*

ค่า *บูลีน* ที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ฟังก์ชันนี้สามารถใช้เพื่อระบุนิพจน์เงื่อนไขของฟังก์ชัน [ตัวกรองข้อมูล](er-functions-list-filter.md) เฉพาะเมื่อตั้งค่าคอนฟิกการแม็ปที่เกี่ยวข้องใน [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) เพื่อเข้าถึง [Microsoft Dataverse](/power-platform/admin/data-integrator) มิฉะนั้น ข้อยกเว้นจะเกิดขึ้นในขณะออกแบบ ข้อความที่คุณได้รับจะแนะนำให้คุณใช้ฟังก์ชัน [WHERE](er-functions-list-where.md) แทนที่จะใช้ฟังก์ชัน `FILTER`

## <a name="example-1"></a>ตัวอย่างที่ 1

นิพจน์ `STARTSWITH ("abc", "d")` จะส่งคืน **FALSE** ในขณะที่นิพจน์ `STARTSWITH ("abc", "A")` ส่งคืน **TRUE**

## <a name="example-2"></a>ตัวอย่างที่ 2

นิพจน์ `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` จะส่งคืน **TRUE** ถ้าค่าของฟิลด์ **ที่อยู่** ของแหล่งข้อมูล **แบบจำลอง** เริ่มด้วยสตริง **123 Coffee Street** มิฉะนั้น จะส่งคืน **FALSE**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันตรรกะ](er-functions-category-logical.md)
