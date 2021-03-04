---
title: ผู้ใช้ Attract ไม่สามารถสมัครงานจากพอร์ทัลการทำงานได้
description: หัวข้อนี้จะอธิบายถึงวิธีการแก้ไขปัญหาที่ผู้ใช้ Attract ไม่สามารถสมัครงานจากพอร์ทัลการทำงานได้
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462675"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>ผู้ใช้ Attract ไม่สามารถสมัครงานจากพอร์ทัลการทำงานได้

[!include [banner](includes/banner.md)]

## <a name="issue"></a>ออก

ผู้ใช้ Attract ไม่สามารถสมัครงานจากพอร์ทัลการทำงานได้ เมื่อพวกเขาพยายามสมัครงานที่สร้างขึ้นใน Dynamics 365 Talent: Attract เบราว์เซอร์จะโหลดหน้าดังกล่าวอย่างต่อเนื่อง และไม่ทำการดำเนินการให้เสร็จสมบูรณ์ได้

## <a name="cause"></a>สาเหตุ

ปัญหานี้จะเกิดขึ้นเมื่อ Talent Relationship Team ไม่มีบทบาทผู้ใช้ Talent

## <a name="resolution"></a>ความละเอียด

กำหนดบทบาทผู้ใช้ Talent ให้กับ Talent Relationship Team

1. ล็อกอินไปยัง [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com) โดยใช้ข้อมูลประจำตัวของผู้ดูแลระบบต่อไปนี้:

   - ผู้ดูแลระบบ Dynamics 365
   - ผู้ดูแลระบบส่วนกลาง
   - ผู้ดูแลระบบ Power Platform

2. ในบานหน้าต่างนำทาง ให้เลือก **สภาพแวดล้อมแล้ว** จากนั้นเลือกสภาพแวดล้อมที่จะกำหนดบทบาทผู้ใช้ Talent ให้กับ Talent Relationship Team

   ![เลือกสภาพแวดล้อม](./media/attract-troubleshoot-career-portal-select-environment.png)

3. ในบานหน้าต่าง **สภาพแวดล้อม** ให้เลือก **URL ของสภาพแวดล้อม** และล็อกอินไปยังพอร์ทัลผู้ดูแลระบบของสภาพแวดล้อม (ตัวอย่างเช่น https:<orgname>crm.dynamics.com)

4. เลือก **การตั้งค่า** เลือก **ระบบ** แล้วเลือก **ความปลอดภัย**

   ![นำทางไปยังความปลอดภัย](./media/attract-troubleshoot-career-portal-security.png)

5. เลือก **Teams**

   ![เลือก Teams](./media/attract-troubleshoot-career-portal-security-teams.png)

6. ค้นหา **Talent Relationship Team** ในกล่องค้นหา แล้วเลือกทีมจากผลการค้นหา

7. เลือก **MANAGE ROLES** จาก ribbon

8. ในกล่องโต้ตอบ **จัดการบทบาทของทีม** ให้เลือก **ผู้ใช้ Talent** จากรายการของบทบาทที่มีอยู่ แล้วเลือก **ตกลง** เพื่อใช้บทบาท

   ![ใช้บทบาท](./media/attract-troubleshoot-career-portal-apply-role.png)

9. ทดสอบการเปลี่ยนแปลงของคุณ:

   1. ล็อกอินไปยังพอร์ทัลการทำงานจากหน้าต่างเบราเซอร์ใหม่
   2. สมัครงานจากพอร์ทัลการทำงาน 

[!INCLUDE[footer-include](../includes/footer-banner.md)]