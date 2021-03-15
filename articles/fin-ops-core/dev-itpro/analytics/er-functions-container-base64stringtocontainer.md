---
title: ฟังก์ชัน Base64StringToContainer ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) Base64StringToContainer
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739116"
---
# <a name="base64stringtocontainer-er-function"></a>ฟังก์ชัน Base64StringToContainer ER

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [ฟังก์ชัน](er-formula-language.md#functions) แปลงอินพุตที่ระบุของชนิด *สตริง* เป็นรายการข้อมูลของชนิด *[คอนเทนเนอร์](er-functions-category-container.md)*

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