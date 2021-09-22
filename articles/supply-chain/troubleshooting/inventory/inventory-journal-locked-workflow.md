---
title: สมุดรายวันสินค้าคงคลังของคุณถูกล็อคและชุดงานลำดับงานไม่ทำงาน
description: หนึ่งในสมุดรายวันสินค้าคงคลังของคุณถูกล็อคไว้โดยการดําเนินงานบางอย่างและยังไม่ถูกปล่อยออกใช้
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477713"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>สมุดรายวันสินค้าคงคลังของคุณถูกล็อคและชุดงานลำดับงานไม่ทำงาน

## <a name="symptoms"></a>อาการ

หนึ่งในสมุดรายวันสินค้าคงคลังของคุณถูกล็อคไว้โดยการดําเนินงานบางอย่างและยังไม่ถูกปล่อยออกใช้ ตัวอย่างเช่น ถ้าเกิดข้อผิดพลาดที่ไม่รู้จักระหว่างการลงรายการบัญชี (ซึ่งเป็นการดําเนินการล็อคระบบ) สมุดรายวันอาจยังคงอยู่ในสถานะที่ระบบล็อค ในกรณีนี้ ตัวจัดการรายการงานของลำดับงานจะส่งข้อผิดพลาดขณะตรวจสอบความถูกต้องของการล็อค

## <a name="resolution"></a>การแก้ปัญหา

เข้าสู่ระบบอินสแตนซ์ SQL Server ของ Supply Chain Management และตรวจสอบว่า **InventJournalTable.SystemBlocked** ถูกตั้งค่าเป็น *1* หรือไม่ ถ้าใช่ ให้ตรวจสอบให้แน่ใจว่าสมุดรายวันไม่ควรอยู่ในสถานะล็อค แล้วรีเซ็ต **InventJournalTable.SystemBlocked** เป็น *0*
