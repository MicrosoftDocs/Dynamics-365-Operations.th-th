---
title: ภาพรวมการสรรหาบุคลากร
description: บทความนี้อธิบายการสรรหาบุคลากร ใน Dynamics 365 Human Resources
author: twheeloc
ms.date: 04/22/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 2f0bed18ced28b2110e1e0533a8496c7b5a29aef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899569"
---
# <a name="dynamics-365-human-resources-recruitment"></a>การสรรหาบุคลากรของ Dynamics 365 Human Resources

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ในการจัดการทรัพยากรบุคคล การสรรหาบุคลากรคือกระบวนการค้นหาและการจ้างงานผู้สมัครที่เข้าเกณฑ์มากที่สุดในการเปิดรับสมัครงาน และยังสามารถกําหนดเป็นกระบวนการค้นหาผู้ที่มีแนวโน้มจะเป็นลูกค้าได้อีกด้วย 

ใน Dynamics 365 Human Resources (โครงสร้างพื้นฐานที่รวม) มีประสบการณ์การสรรหาบุคลากรอยู่สองอย่างคือ **โครงการสรรหาบุคลากร** และ **การสรรหาบุคลากรของ HR** การตั้งค่าเริ่มต้นคือ **โครงการสรรหาบุคลากร** จนกว่า **การสรรหาบุคลากรของ HR** จะเปิดใช้งานผ่านการจัดการคุณลักษณะและพารามิเตอร์ HR  

โครงการสรรหาบุคลากรจัดระเบียบขั้นตอนต่างๆ ที่จะดำเนินการเมื่อกรอกข้อมูลในตำแหน่งที่เปิดในแผนกนิติบุคคล ผู้สมัครเป็นผู้ที่ใช้สำหรับการจ้างงานให้กับองค์กรของคุณ แอปพลิเคชันของผู้สมัครคือการแสดงตัวตนของผู้สมัครที่จะแสดงความสนใจที่จะทำงานในบริษัทนั้นๆ และอาจเชื่อมโยงกับโครงการสรรหาบุคลากร ผู้สมัครเดียวอาจมีหลายใบสมัครหลายใบ ในนิติบุคคลเดียว หรือ ระหว่างบริษัทหลายบริษัทในองค์กร 

การสรรหาบุคลากรของ HR ช่วยจัดการคำขอสรรหาบุคลากร นอกจากนี้ยังช่วยให้คุณสามารถเปลี่ยนผู้สมัครงานเป็นพนักงาน ถ้าองค์กรของคุณใช้แอปพลิเคชันการสรรหาบุคลากรที่แยกต่างหาก กระบวนการสรรหาบุคลากรของคุณอาจประกอบด้วยขั้นตอนต่อไปนี้: 

1. ป้อนคำขอสรรหาบุคลากรของคุณในทรัพยากรบุคคล 
2. รับการอ้างอิงของผู้สมัครในทรัพยากรบุคคลจากแอปพลิเคชันการสรรหาบุคลากร 
3. ดำเนินการขั้นตอนการอนุมัติของผู้สมัครในทรัพยากรบุคคลให้เสร็จสมบูรณ์ 

ถ้าคุณไม่ได้ใช้แอปพลิเคชันการสรรหาบุคลากรที่แยกต่างหาก คุณสามารถจัดการผู้สมัครในทรัพยากรบุคคลด้วยตนเองได้ 

> [!Important] 
> Dynamics 365 Human Resources (การติดตั้งแยกต่างหาก) ช่วยคุณในการจัดการคำขอสรรหาบุคลากร นอกจากนี้ยังช่วยให้คุณสามารถเปลี่ยนผู้สมัครงานเป็นพนักงานได้อย่างราบรื่น
