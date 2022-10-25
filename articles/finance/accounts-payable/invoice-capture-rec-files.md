---
title: ไฟล์ที่ได้รับของ Invoice Capture
description: บทความนี้จะอธิบายวิธีรวบรวมไฟล์ใบแจ้งหนี้จากแหล่งที่มาต่างๆ ใน Invoice Capture
author: sunfzam
ms.date: 10/13/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c55540d11a67d4d4c4c8477d51cb6f1f5777767
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690141"
---
# <a name="invoice-capture-received-files"></a>ไฟล์ที่ได้รับของ Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

ใน Invoice Capture หน้า **ไฟล์ที่ได้รับ** คือส่วนกลางที่ซึ่งได้รับไฟล์ใบแจ้งหนี้จากแหล่งที่มาต่างๆ

## <a name="upload-invoice-files"></a>อัปโหลดไฟล์ใบแจ้งหนี้

เสมียนบัญชีเจ้าหนี้ (AP) สามารถอัแโหลดรูปภาพใบแจ้งหนี้โดยเลือก **อัปโหลดไฟล์** เพื่อเปิดกล่องโต้ตอบ **อัปโหลด** หลังจากเสมียน AP เลือกไฟล์แล้ว ปุ่ม **อัปโหลด** จะพร้อมใช้งาน

## <a name="include-or-obsolete-invoice-files"></a>รวมหรือล้าสมัยไฟล์ใบแจ้งหนี้

ผู้ใช้สามารถเลือกใบแจ้งหนี้ที่มีข้อผิดพลาดหรือคําเตือน จากนั้นรวมหรือล้าสมัยใบแจ้งหนี้ ด้วยการเลือกปุ่มที่ตรงกันในบานหน้าต่างการดำเนินการ ใบแจ้งหนี้ที่ทำเครื่องหมายเป็นล้าสมัยจะไม่ปรากฏในมุมมอง **ไฟล์ที่ได้รับ (ล้าสมัย)**

## <a name="view-captured-invoices"></a>ดูใบแจ้งหนี้ที่บันทึก

หลังจากรับรู้ไฟล์ที่ได้รับเสร็จเรียบร้อยแล้ว ข้อมูลใบแจ้งหนี้ที่รวบรวมไว้จะถูกส่งคืนโดยโมเดล AI และป้อนเข้า Microsoft Dataverse จากนั้นเสมียน AP จะสามารถตรวจสอบรายละเอียดใบแจ้งหนี้โดยเลือก **ดูใบแจ้งหนี้ที่บันทึก** ผู้ใช้สามารถดาวน์โหลดไฟล์ใบแจ้งหนี้ต้นฉบับได้ตามที่ต้องการ
