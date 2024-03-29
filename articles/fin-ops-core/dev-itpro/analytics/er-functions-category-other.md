---
title: รายการของฟังก์ชั่น ER ในประเภทเฉพาะโดเมนธุรกิจ
description: บทความนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันเฉพาะโดเมนธุรกิจที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b1ac46cf10d57b40af1fa99021156ad97a17ba20
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272696"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>รายการของฟังก์ชั่น ER ในประเภทเฉพาะโดเมนธุรกิจ

[!include [banner](../includes/banner.md)]

ฟังก์ชันเฉพาะโดเมนของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อทำการคำนวณและการร้องขอการเข้าถึงข้อมูลที่เฉพาะเจาะจงสำหรับการดำเนินการของ Microsoft Dynamics 365 Finance บทความนี้แสดงสรุปของฟังก์ชันเหล่านี้

## <a name="list-of-supported-functions"></a>รายการฟังก์ชันที่ได้รับการสนับสนุน

| ฟังก์ชัน| คำอธิบาย |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้เป็นนิพจน์ MOD10 ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงรหัสมิติทางการเงินเดียวที่ถูกนำมาจากสตริงที่ระบุ สตริงที่ระบุแสดงมิติทั้งหมดเป็นรายการของรหัสที่คั่นด้วยเครื่องหมายจุลภาค |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | ฟังก์ชันนี้ส่งคืนค่า *จริง* ที่แสดงผลลัพธ์ของการแปลงยอดเงินที่ระบุจากสกุลเงินต้นทางที่ระบุเป็นสกุลเงินเป้าหมายที่ระบุ โดยใช้การตั้งค่าของบริษัทที่ระบุในวันที่ที่ระบุ |
| [CurCredRef](er-functions-other-curcredref.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ |
| [FA_Balance](er-functions-other-fabalance.md) | ฟังก์ชันส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่ประกอบด้วยข้อมูลสำหรับยอดดุลสินทรัพย์ถาวรสำหรับสินค้าสินทรัพย์ถาวรที่ระบุ รหัสแบบจำลองมูลค่า ปีการรายงาน และวันที่ที่รายงาน |
| [FA_Sum](er-functions-other-fasum.md) | ฟังก์ชันนี้ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่ประกอบด้วยข้อมูลสำหรับยอดเงินสินทรัพย์ถาวรสำหรับสินค้าสินทรัพย์ถาวรที่ระบุ รหัสแบบจำลองมูลค่า และรอบระยะเวลาของวันที่ |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | ฟังก์ชันนี้ส่งคืนค่า *สตริง* ที่แสดงรหัสสำหรับนิติบุคคล (บริษัท) ที่ผู้ใช้ลงชื่อเข้าใช้ในปัจจุบัน |
| [ISOCredRef](er-functions-other-isocredref.md) | ฟังก์ชันนี้ส่งคืนค่า *สตริง* ที่แสดงการอ้างอิงเจ้าหนี้ขององค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) โดยขึ้นอยู่กับตำแหน่งและสัญลักษณ์เรียงตามลำดับอักษรของหมายเลขใบแจ้งหนี้ที่ระบุ |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | ฟังก์ชันนี้ส่งกลับค่า *บูลีน* เป็น **จริง** หากสตริงที่ระบุแสดงหมายเลขบัญชีธนาคารระหว่างประเทศที่ถูกต้อง (IBAN) มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** |
| [Mod_97](er-functions-other-mod97.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้เป็นนิพจน์ MOD97 ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ |
| [NumSeqValue](er-functions-other-numseqvalue.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงค่าที่สร้างขึ้นใหม่ของลำดับหมายเลข ตามลำดับหมายเลข ขอบเขต และรหัสขอบเขตที่ระบุ รหัสขอบเขตจะเท่ากับรหัสบริษัทที่จัดหาโดยบริบทที่เรียกใช้รูปแบบ ER |
| [RoundAmount](er-functions-other-roundamount.md) | ฟังก์ชันนี้ส่งกลับค่า *จริง* ที่แสดงถึงผลลัพธ์ของการปัดเศษจำนวนที่ระบุให้เป็นจำนวนตำแหน่งทศนิยมที่ระบุตามกฎการปัดเศษที่ระบุ |
| [TableName2ID](er-functions-other-tablename2id.md) | ฟังก์ชันนี้ส่งกลับการแสดงตัวเลขของรหัสตารางสำหรับชื่อตารางที่ระบุเป็นค่า *จำนวนเต็ม* |

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)

[ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting-formula-designer.md)

[ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
