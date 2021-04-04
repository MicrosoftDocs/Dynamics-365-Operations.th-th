---
title: ฟังก์ชัน QRCODE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ QRCODE (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
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
ms.openlocfilehash: 92665936decc87b29f2fabb346f4d16745d0a30b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562672"
---
# <a name="qrcode-er-function"></a>ฟังก์ชัน QRCODE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `QRCODE` ส่งกลับค่า *คอนเทนเนอร์* ที่แสดงรูป Quick Response code (QR code) สำหรับสตริงที่ระบุในรูปแบบไบนารี

## <a name="syntax"></a>ไวยากรณ์

```vb
QRCODE (text)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ

## <a name="return-values"></a>ส่งคืนค่า

*คอนเทนเนอร์*

สตรีมไบนารีที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

คุณสามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารขาออกในรูปแบบ Microsoft Office (สมุดงาน Excel หรือเอกสาร Word) โดยใช้เท็มเพลตที่กำหนดไว้ล่วงหน้า เท็มเพลตนี้อาจมีออบเจ็กต์ **รูปภาพ** (สมุดงาน Excel) หรือ **ตัวควบคุมเนื้อหารูปภาพ** (เอกสาร WORD) เป็นตัวยึดสำหรับรูปภาพคิวอาร์โค้ด คุณต้องเพิ่มองค์ประกอบ **เซลล์** ไปยังรูปแบบ ER ที่ถูกตั้งค่าคอนฟิกที่จะใช้ในการเติมข้อมูลตัวยึดนี้ เพื่อระบุข้อมูลที่จะถูกเก็บไว้ในคิวอาร์โค้ด คุณต้องกำหนดการผูกข้อมูลสำหรับองค์ประกอบ **เซลล์** นี้ ตัวอย่างเช่น คุณสามารถตั้งค่าคอนฟิกการผูกข้อมูลดังกล่าวตามที่มีนิพจน์ต่อไปนี้:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

เมื่อคุณเรียกใช้รูปแบบ ER ที่ถูกตั้งค่าคอนฟิก ค่าข้อความของฟิลด์ **LabelText** ของแหล่งข้อมูล **model.ListOfShelfLabels** จะถูกใช้ในการสร้างรูปภาพคิวอาร์โค้ด รูปนี้จะแทนที่ตัวยึดรูปภาพคิวอาร์โค้ดในเท็มเพลตเอกสารโดยใช้เพื่อสร้างเอกสารขาออก เมื่อรูปภาพของเอกสารที่สร้างขึ้นนี้ถูกสแกน จะส่งกลับข้อความที่ถูกนำมาจากฟิลด์ **LabelText** ของแหล่งข้อมูล **model.ListOfShelfLabels** สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ฝังรูปภาพและรูปร่างในเอกสารที่คุณสร้างโดยใช้ ER](electronic-reporting-embed-images-shapes.md)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]