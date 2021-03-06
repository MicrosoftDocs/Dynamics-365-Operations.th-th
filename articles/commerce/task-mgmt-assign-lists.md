---
title: กำหนดรายการงานให้กับร้านค้าหรือพนักงาน
description: หัวข้อนี้จะอธิบายถึงวิธีการกำหนดรายการงานให้กับร้านค้าหรือพนักงานใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ee924f5bf95d47814e7ca09b392a3d10b5e9b9dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006271"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>กำหนดรายการงานให้กับร้านค้าหรือพนักงาน

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการกำหนดรายการงานให้กับร้านค้าหรือพนักงานใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

การจัดการงานใน Dynamics 365 Commerce ช่วยให้คุณสามารถกำหนดรายการงานให้กับร้านค้าหรือพนักงานหลายแห่ง หรือสำหรับชุดของร้านค้าและพนักงาน ตัวอย่างเช่น ผู้จัดการภูมิภาคสำหรับ 20 ร้านค้า อาจต้องการกำหนดรายการงาน **การจัดเตรียมเทศกาลวันหยุด** ให้กับร้านค้าทั้งหมด 20 ร้าน

## <a name="start-the-task-list-assignment-process"></a>เริ่มต้นกระบวนการกำหนดรายการงาน

เมื่อต้องการเริ่มต้นกระบวนการกำหนดรายการงาน ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> การจัดการดูแลการจัดการงาน**
1. เลือกรายการงานที่จะกำหนด
1. เลือก **เริ่มกระบวนการ**
1. ในกล่องโต้ตอบ **เริ่มต้นกระบวนการ** บนแท็บ **ทั่วไป** ในฟิลด์ **ชื่อกระบวนการ** ให้ป้อนชื่อ (ตัวอย่างเช่น **ร้านค้าภาคตะวันออก**)
1. ในฟิลด์ **วันที่เป้าหมาย** ให้ระบุวันที่
1. เมื่อต้องการกำหนดรายการงานให้กับร้านค้าบนแท็บ **ร้านค้า** ให้ใช้ตัวกรอง **ลำดับชั้นขององค์กร** ในการค้นหาและเลือกร้านค้า

    เมื่อต้องการกำหนดรายการงานให้กับพนักงาน บนแท็บ **ผู้ปฏิบัติงาน** ให้ค้นหาและเลือกพนักงาน

1. เลือก **ตกลง** เพื่อเริ่มต้นกระบวนการ รายการงานมีการกำหนดให้กับร้านค้าหรือพนักงานที่เลือก

ภาพประกอบต่อไปนี้แสดงตัวอย่างของวิธีการค้นหาและเลือกร้านค้าในกล่องโต้ตอบ **เริ่มต้นกระบวนการ**

![การค้นหาและการเลือกร้านค้าในกล่องโต้ตอบเริ่มต้นกระบวนการ](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>กำหนดรายการงานบนฐานที่เกิดซ้ำ

บางครั้งผู้ค้าปลีกมีงานที่เกิดขึ้น เช่น "รายการตรวจสอบการปิดวันพฤหัสบดี" หรือ "รายการตรวจสอบวันแรกของเดือน" ดังนั้นผู้ใช้งานอาจต้องการกำหนดรายการงานให้เป็นฐานที่เกิดซ้ำ

1. ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> การจัดการดูแลการจัดการงาน**
1. เลือกรายการงานที่จะกำหนด
1. เลือก **เริ่มกระบวนการ**
1. ในกล่องโต้ตอบ **เริ่มต้นกระบวนการ** บนแท็บ **ทั่วไป** ในฟิลด์ **ชื่อกระบวนการ** ให้ป้อนชื่อ
1. ตั้งค่าตัวเลือก **การเกิดซ้ำ** เป็น **ใช่**
1. ในฟิลด์ **วันที่เป้าหมายการเกิดซ้ำของออฟเซ็ตในหน่วยจำนวนวัน** ให้ป้อนจำนวนวัน ตัวอย่างเช่น ถ้าคุณป้อน **4** วันที่เป้าหมายคือวันที่มีการเกิดซ้ำบวกสี่วัน
1. บนแท็บ **รันในพื้นหลัง** เลือก **การเกิดซ้ำ**
1. ในกล่องโต้ตอบ **กำหนดการเกิดซ้ำ** ให้ป้อนเกณฑ์ความถี่ แล้วเลือก **ตกลง**

ภาพประกอบต่อไปนี้แสดงตัวอย่างของวิธีการป้อนเกณฑ์ความถี่ในกล่องโต้ตอบ **กำหนดการเกิดซ้ำ**

![การป้อนเกณฑ์ความถี่ในกล่องโต้ตอบกำหนดการเกิดซ้ำ](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>ติดตามสถานะรายการงาน

ถ้าคุณเป็นผู้จัดการระดับภูมิภาคหรือผู้จัดการร้านค้า คุณอาจต้องการติดตามสถานะของรายการงานที่กำหนดให้กับร้านค้าหลายแห่งหรือพนักงานหลายคน คุณสามารถติดตามผลกับร้านค้าหรือผู้ปฏิบัติงานที่ไม่ได้ทำงานที่กำหนดไว้ให้เสร็จสมบูรณ์ทันเวลา ฝ่ายสนับสนุนการค้าช่วยให้คุณสามารถดูสถานะของรายการงาน มอบหมายงาน หรือเปลี่ยนสถานะของงานได้

เมื่อต้องการติดตามสถานะรายการงานสำหรับงานทั้งหมด ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> กระบวนการจัดการงาน**
1. เลือกแท็บ **รายการงานทั้งหมด** เพื่อดูสถานะของรายการงานทั้งหมดที่กำหนดให้กับร้านค้าต่างๆ

เมื่อต้องการติดตามสถานะรายการงานสำหรับงานทั้งหมดที่คุณได้รับมอบหมาย ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> กระบวนการจัดการงาน**
1. เลือก **งานของฉัน** หรือแท็บ **งานทั้งหมด** เพื่อดูหรืออัปเดตสถานะของงานที่กำหนดให้กับคุณ

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของการจัดการงาน](task-mgmt-overview.md)

[ตั้งค่าคอนฟิกการจัดการงาน](task-mgmt-configure.md)

[สร้างรายการงานและเพิ่มงาน](task-mgmt-create-lists.md)

[การจัดการงานใน POS](task-mgmt-POS.md)
