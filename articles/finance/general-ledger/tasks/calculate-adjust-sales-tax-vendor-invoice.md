---
title: คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย
description: บทความนี้อธิบายวิธีการปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่ายใน Dynamics 365 Finance
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a1093631688351d065d6b55bc65055b6f92d256
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868386"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายวิธีการปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย ถ้าเอกสารต้นทางที่เป็นต้นฉบับแสดงยอดเงินภาษีที่แตกต่างกันจากการคำนวณ คุณสามารถปรับปรุงยอดเงินเหล่านั้นก่อนที่จะลงรายการบัญชี งานนี้ใช้บริษัทสาธิต DEMF

1. ไปที่ **บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > สมุดรายวันใบแจ้งหนี้**
2. เลือก **ใหม่**
3. ในฟิลด์ **ชื่อ** ของแถวใหม่ ให้เลือกตัวเลือกในเมนูแบบหล่นลง
4. ในบานหน้าต่างการดำเนินการ เลือก **รายการ**
5. ในฟิลด์ **บัญชี** ให้ระบุค่าที่ต้องการ
6. ในฟิลด์ **ใบแจ้งหนี้** ให้พิมพ์ค่า
7. ในฟิลด์ **เครดิต** ให้ป้อนหมายเลข
8. ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ
9. เลือก **ภาษีขาย**
10. ในฟิลด์ **ยอดภาษีขายจริงรวม** ให้ป้อนตัวเลข
11. บนแท็บ **การปรับปรุง** สามารถปรับปรุงยอดภาษีขายได้สำหรับรหัสภาษีขายแต่ละรายการ
12. เลือก **รีเซ็ตยอดจริงจากยอดที่คำนวณ**
13. เลือก **ตกลง**
14. เลือก **บันทึก**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
