---
title: ฟังก์ชัน AND ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) AND
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 068b9a3b2cf2e5bffe895bc4e8a7cbb2d8025ad7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560096"
---
# <a name="and-er-function"></a>ฟังก์ชัน AND ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `AND` ส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**

## <a name="syntax"></a>ไวยากรณ์

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>อาร์กิวเมนต์

`condition 1`: *บูลีน*

นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ ต้องระบุอาร์กิวเมนต์นี้

`condition N`: *บูลีน*

นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

## <a name="return-values"></a>ค่าที่ส่งคืน

*บูลีน*

ค่า *บูลีน* ที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ในอาร์กิวเมนต์ของฟังก์ชันตรรกะ คุณสามารถใช้การอ้างอิงแหล่งข้อมูล ค่าตัวเลขและข้อความ ค่าบูลีน ตัวดำเนินการเปรียบเทียบ และฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) อื่นๆ อย่างไรก็ตามอาร์กิวเมนต์ทั้งหมดต้องถูกประเมินเป็นค่า *บูลีน* ของ **TRUE** หรือ **FALSE**

## <a name="example"></a>ตัวอย่าง

`AND (1=1, "a"="a")` ส่งกลับค่า **TRUE**

`AND (1=2, "a"="a")` ส่งกลับค่า **FALSE**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันตรรกะ](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]