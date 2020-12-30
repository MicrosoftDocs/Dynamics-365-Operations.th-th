---
title: ฟังก์ชัน CONVERTCURRENCY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CONVERTCURRENCY (ER)
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a27fd30236a61576ab9063010ea6bc38d9cf7a1e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686797"
---
# <a name="convertcurrency-er-function"></a>ฟังก์ชัน CONVERTCURRENCY ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `CONVERTCURRENCY` ส่งคืนค่า *จริง* ที่แสดงผลลัพธ์ของการแปลงยอดเงินที่ระบุจากสกุลเงินต้นทางที่ระบุเป็นสกุลเงินเป้าหมายที่ระบุ โดยใช้การตั้งค่าของบริษัทที่ระบุในวันที่ที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`amount`: *จำนวนเต็ม* หรือ *จำนวนจริง*

ค่าตัวเลขที่แสดงถึงยอดเงินที่ต้องถูกแปลง

`source currency`: *สตริง*

รหัสของสกุลเงินต้นทาง

`target currency`: *สตริง*

รหัสของสกุลเงินเป้าหมาย

`date`: *วันที่*

ค่า *วันที่* ที่แสดงถึงวันที่ที่ใช้ในการกำหนดอัตราแลกเปลี่ยนสำหรับการแปลง

`company`: *สตริง*

ค่า *สตริง* ที่แสดงถึงรหัสของบริษัทที่จัดหาการตั้งค่าที่จะใช้สำหรับการแปลง

## <a name="return-values"></a>ส่งคืนค่า

*จำนวนจริง*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` ส่งกลับค่าหนึ่งยูโรที่เทียบเท่ากับดอลลาร์สหรัฐฯ ในวันที่รอบเวลาปัจจุบัน ตามการตั้งค่าสำหรับบริษัท **DEMF**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)
