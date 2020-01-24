---
title: ฟังก์ชัน CONCATENATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CONCATENATE (ER)
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915774"
---
# <a name="CONCATENATE">ฟังก์ชัน CONCATENATE ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `CONCATENATE` ส่งกลับสตริงข้อความที่ระบุทั้งหมดเป็นค่า *สตริง* หลังจากที่ได้เข้าร่วมเป็นหนึ่งสตริง

## <a name="syntax"></a>ไวยากรณ์

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text 1`: *สตริง*

การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *สตริง* ต้องระบุอาร์กิวเมนต์นี้

`text N`: *สตริง*

การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *สตริง* อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`CONCATENATE ("abc", "def")` ส่งกลับค่า **"abcdef"**

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

นอกจากนี้ นิพจน์  `"abc" & "def"` ยังส่งกลับค่า **"abcdef"** ด้วย

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)
