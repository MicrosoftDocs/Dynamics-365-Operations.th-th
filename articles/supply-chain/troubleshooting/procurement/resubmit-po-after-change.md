---
title: ข้อผิดพลาดเกี่ยวกับการส่งใบสั่งซื้อไปยังลำดับงานอีกครั้ง หลังจากการเปลี่ยนแปลง
description: ข้อผิดพลาดเกี่ยวกับการส่งใบสั่งซื้อไปยังลำดับงานอีกครั้ง หลังจากการเปลี่ยนแปลง
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477787"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>ข้อผิดพลาดเกี่ยวกับการส่งใบสั่งซื้อไปยังลำดับงานอีกครั้ง หลังจากการเปลี่ยนแปลง


## <a name="symptoms"></a>อาการ

เกิดข้อผิดพลาดต่อไปนี้ในลำดับงานเมื่อส่งใบสั่งซื้ออีกครั้งหลังจากที่มีการเปลี่ยนแปลง:

> หยุด (ข้อผิดพลาด): ข้อยกเว้น X++: การเปลี่ยนแปลงใบสั่งซื้อ PO0000569 เท่านั้นที่สามารถใช้ได้เฉพาะในแบบร่างสถานะที่มีการเรียกใช้การจัดการการเปลี่ยนแปลง<br>
SysWorkflowParticipantProvider-แก้ไข<br>
SysWorkflowParticipantProvider-แก้ไขผู้เข้าร่วม<br>
SysWorkflowServiceProvider-แก้ไขผู้เข้าร่วม<br>
SysWorkflowQueue-ดำเนินการต่อ

ปัญหานี้จะเกิดขึ้นเฉพาะเมื่อใบสั่งซื้ออยู่ในสถานะ *ยืนยัน* ก่อนที่คุณจะร้องขอการเปลี่ยนแปลง ถ้าคุณร้องขอการเปลี่ยนแปลงในขณะที่ใบสั่งซื้ออยู่ในสถานะ *อนุมัติแล้ว* คุณสามารถประมวลผลลำดับงานเสร็จเรียบร้อยแล้ว

## <a name="resolution"></a>การแก้ปัญหา

ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ

เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ** สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)

จะมีการแก้ไขปัญหานี้ผ่านทาง [บทความฐานความรู้ของ Microsoft (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138)
