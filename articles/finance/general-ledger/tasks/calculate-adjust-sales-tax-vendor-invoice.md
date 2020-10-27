---
title: คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีการปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่ายใน Dynamics 365 Finance
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03313d875d23489b3293376dd94f808c73a4bd15
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983560"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย

[!include [banner](../../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย ถ้าเอกสารต้นทางที่เป็นต้นฉบับแสดงยอดเงินภาษีที่แตกต่างกันจากการคำนวณ คุณสามารถปรับปรุงยอดเงินเหล่านั้นก่อนที่จะลงรายการบัญชี งานนี้ใช้บริษัทสาธิต DEMF

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > สมุดรายวันใบแจ้งหนี้**
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

