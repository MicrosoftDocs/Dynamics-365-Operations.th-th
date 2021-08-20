---
title: รายการของฟังก์ชั่น ER ในประเภทคอนเทนเนอร์
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันคอนเทนเนอร์ที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
ms.date: 12/14/2020
ms.prod: ''
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
ms.openlocfilehash: 522fc6b8ad414745c3949268d9690aa2d258b92971e7d7b4f82428398bfec170
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760109"
---
# <a name="list-of-er-functions-in-the-container-category"></a>รายการของฟังก์ชั่น ER ในประเภทคอนเทนเนอร์

[!include [banner](../includes/banner.md)]

[การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) คอนเทนเนอร์ [ฟังก์ชัน](er-formula-language.md#Functions) สามารถใช้เพื่อดำเนินการกับแหล่งข้อมูลที่เกี่ยวข้องของชนิดข้อมูล *คอนเทนเนอร์* การดําเนินงานเหล่านี้เกิดขึ้นเมื่อข้อมูลการประมวลผลแสดงถึงชุดข้อมูลฐานสอง ในรูปแบบฐานสองของออบเจ็กต์ขนาดใหญ่ (BLOB) หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้

## <a name="list-of-supported-functions"></a>รายการฟังก์ชันที่ได้รับการสนับสนุน

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | ฟังก์ชันนี้จะส่งคืนค่า *คอนเทนเนอร์* ที่ประกอบด้วยเนื้อหาฐานสอ งซึ่งตัดออกจากสตริง ASCII ที่ระบุ ซึ่งแสดงถึงกลุ่ม Base64 ของแผนงานการเข้ารหัสฐานสองถึงข้อความ |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)

[ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting-formula-designer.md)

[ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
