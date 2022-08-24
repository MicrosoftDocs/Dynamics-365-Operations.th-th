---
title: ฟังก์ชัน Base64StringToContainer ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) Base64StringToContainer
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 96dfffc3d899f1106c6c931efb08c941f5b3c1a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291248"
---
# <a name="base64stringtocontainer-er-function"></a>ฟังก์ชัน Base64StringToContainer ER

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [ฟังก์ชัน](er-formula-language.md#Functions) แปลงอินพุตที่ระบุของชนิด *สตริง* เป็นรายการข้อมูลของชนิด *[คอนเทนเนอร์](er-functions-category-container.md)*

## <a name="syntax"></a>ไวยากรณ์

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`input`: *สตริง*

พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*

## <a name="return-values"></a>ค่าที่ส่งคืน

*ตู้บรรจุสินค้า*

ค่าฐานสองที่ได้ในรูปแบบฐานสองของออบเจ็กต์ขนาดใหญ่ (BLOB)

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

มีข้อยกเว้น "พารามิเตอร์ไม่ถูกต้อง" ถ้าสตริงอินพุทไม่มีกลุ่ม Base64 ที่ถูกต้องของแผนงานการเข้ารหัสฐานสองต่อข้อความ

## <a name="example"></a>ตัวอย่าง

คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:

- แหล่งข้อมูล **DocuTypeGroupEnum** ราก ของชนิด *Dynamics 365 for Operations / การแจงนับ* ที่อ้างอิงถึงการแจงนับของแอพลิเคชัน **DocuTypeGroup**
- แหล่งข้อมูล **ลูกค้า** ราก ของชนิด *Dynamics 365 for Operations / เรกคอร์ดของตาราง* ที่อ้างอิงถึงตารางของแอพลิเคชัน **CustTable**
- แหล่งข้อมูล **\#สื่อ** ของชนิด *ฟิลด์ที่คํานวณได้* ซึ่งตั้งค่าคอนฟิกในลักษณะต่อไปนี้:

    - เพิ่มเป็นแหล่งข้อมูลรองของแหล่งข้อมูล **ลูกค้า**
    - ซึ่งมีนิจน์ของ `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`

- แหล่งข้อมูล **\#MediaAsBase64String** ของชนิด *ฟิลด์ที่คํานวณได้* ซึ่งตั้งค่าคอนฟิกในลักษณะต่อไปนี้:

    - เพิ่มเป็นแหล่งข้อมูลรองของแหล่งข้อมูล **Customer.'\#Media'**
    - ซึ่งมีนิจน์ของ `Customer.'#Media'.'getFileContentAsBase64String()'`

- แหล่งข้อมูล **\#BlobFomBase64** ของชนิด *ฟิลด์ที่คํานวณได้* ซึ่งตั้งค่าคอนฟิกในลักษณะต่อไปนี้:

    - เพิ่มเป็นแหล่งข้อมูลรองของแหล่งข้อมูล **Customer.'\#Media'**
    - ซึ่งมีนิจน์ของ `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`

ในตัวอย่างนี้ แหล่งข้อมูล **\#MediaAsBase64String** จะเข้ารหัสเนื้อหาฐานสองของส่วนแนบของสื่อปัจจุบัน เป็นข้อความที่แสดงถึงกลุ่ม Base64 ของแผนงานการเข้ารหัสฐานสองถึงข้อความ แหล่งข้อมูล **\#BlobFomBase64** จะถอดรหัสสตริง Base64 และส่งคืนค่าฐานสองในรูปแบบ BLOB

![แหล่งข้อมูลตัวอย่างในหน้าตัวออกแบบการแม็ปแบบจำลอง ER](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันคอนเทนเนอร์](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
