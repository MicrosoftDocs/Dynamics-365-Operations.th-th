---
title: กระทบยอดการขนส่งด้วยตนเอง
description: 'กระบวนงานนี้แสดงวิธีการกระทบยอดการขนส่งด้วยตนเอง '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: becda50b5d176ceb350c471b154aed1842c31a3b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247201"
---
# <a name="reconcile-freight-manually"></a>กระทบยอดการขนส่งด้วยตนเอง

[!include [banner](../../includes/banner.md)]]

กระบวนงานนี้แสดงวิธีการกระทบยอดการขนส่งด้วยตนเอง  ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง  คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF 


## <a name="select-a-load-to-reconcile"></a>เลือกจำนวนงานในศูนย์การผลิตที่จะกระทบยอด
1. ไปที่ การจัดการการขนส่ง > การวางแผน > เวิร์กเบนช์การวางแผนการบรรทุก
2. ล้างข้อมูลกล่องกาเครื่องหมาย ซ่อนสินค้าที่จัดส่งและที่รับ 
3. ในรายการ เลือกจำนวนงานในศูนย์การผลิตที่มีรหัสจำนวนงานในศูนย์การผลิต 00006

## <a name="create-a-carrier-invoice"></a>สร้างใบแจ้งหนี้ของผู้ขนส่ง
หากคุณกระทบยอดการขนส่งด้วยตนเอง และไม่ได้รับใบแจ้งหนี้ของผู้ขนส่งโดยอัตโนมัติ คุณสามารถสร้างใบแจ้งหนี้ตามบิลการขนส่งได้  
1. คลิก ข้อมูลที่เกี่ยวข้อง
2. คลิก รายละเอียดของบิลการขนส่ง
3. คลิก สร้างใบแจ้งหนี้บิลค่าขนส่ง
4. ในฟิลด์ใบแจ้งหนี้ ให้พิมพ์ค่า
5. คลิก ตกลง

## <a name="reconcile-the-invoice"></a>กระทบยอดใบแจ้งหนี้
คุณจะต้องกระทบยอดใบแจ้งหนี้ของผู้ขนส่งและบิลการขนส่งทีละบรรทัด  
1. คลิก จับคู่บิลและใบแจ้งหนี้การขนส่ง
2. ขยายส่วนรายละเอียดใบแจ้งหนี้
3. ขยายส่วน รายละเอียดบิลการขนส่งที่ไม่ตรงกัน
4. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
5. คลิก จับคู่
6. ขยายส่วน รายละเอียดบิลการขนส่งที่ตรงกัน

## <a name="submit-the-invoice-for-approval"></a>ส่งใบแจ้งหนี้เพื่ออนุมัติ
1. คลิก ส่งเพื่ออนุมัติ
2. ปิดหน้า
3. คลิกกล่องกาเครื่องหมาย ซ่อนรายการที่อนุมัติ 
4. คลิก สมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย
5. คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขสมุดรายวันการอ้างอิง
6. คลิก รายการ



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]