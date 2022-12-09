---
title: ระงับคำขอลางาน
description: คุณสามารถระงับการลางานของพนักงานใน Dynamics 365 Human Resources
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SuspendLeave, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9c8262fb34175f6f9326d6be82c922b2170fc5a7
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805273"
---
# <a name="suspend-leave"></a>ระงับการลางาน

>[!Important]
>ฟังก์ชันที่ระบุไว้ในบทความนี้สามารถใช้งานได้กับลูกค้า Dynamics 365 Human Resources ในระบบที่แยกต่างหากได้แล้ว ฟังก์ชันบางส่วนหรือทั้งหมดจะสามารถใช้งานในลักษณะเป็นส่วนหนึ่งของการเผยแพร่ในอนาคตในโครงสร้างพื้นฐานของ Finance หลังจากการเผยแพร่ Finance 10.0.26

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

คุณสามารถระงับการลางานสำหรับพนักงานเพื่อหยุดกระบวนการของการค้างรับการลางานสำหรับชนิดการลางานที่เลือก

## <a name="suspend-leave-and-absence-for-an-employee"></a>ระงับการลางานและการขาดงานสำหรับพนักงาน

1. บนเรกคอร์ดของพนักงาน ให้เลือก **ลา**

2. เลือก **ระงับการลางาน**

3. เลือก **ใหม่**

4. ในกล่องโต้ตอบ **ระงับการค้างรับ** ให้เลือก **ชนิดการลางาน** พร้อมกับ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** สำหรับการระงับ

5. อีกทางหนึ่งคือ คุณสามารถเพิ่ม **ข้อคิดเห็น** สำหรับการระงับได้ 

ถ้ามีการดำเนินการค้างรับในขณะที่การลางานของพนักงานถูกระงับ จะไม่มีการค้างรับสำหรับชนิดการลางานที่ถูกระงับ

> [!NOTE]
> คำขอการลางานจะระงับคำขอการหยุดพัก แต่คำขอการหยุดพักจะไม่ระงับคำขอการลางาน

## <a name="see-also"></a>ดูเพิ่มเติมที่

- [ภาพรวมการลางานและการขาดงาน](hr-leave-and-absence-overview.md)
- [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)
- [การรับรู้แผนการลางานและการขาดงาน](hr-leave-and-absence-accrue.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
