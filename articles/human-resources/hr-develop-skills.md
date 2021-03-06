---
title: การจัดทักษะแรงงานกับความต้องการทางธุรกิจ
description: คุณสามารถติดตามทักษะที่ผู้ปฏิบัติงาน ผู้สมัคร หรือผู้ติดต่อที่มีหรือควรมี เพื่อตอบสนองหน้าที่ต่าง ๆ อย่างมีประสิทธิภาพมากขึ้น คุณยังสามารถระบุทักษะที่จำเป็นสำหรับงานระบุ
author: andreabichsel
manager: tfehr
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 26493306a8bd810f936b15160b07263ca41f87ae
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115595"
---
# <a name="align-workforce-skills-with-business-needs"></a>การจัดทักษะแรงงานกับความต้องการทางธุรกิจ

คุณสามารถติดตามทักษะที่ผู้ปฏิบัติงาน ผู้สมัคร หรือผู้ติดต่อที่มีหรือควรมี เพื่อตอบสนองหน้าที่ต่าง ๆ อย่างมีประสิทธิภาพมากขึ้น คุณยังสามารถระบุทักษะที่จำเป็นสำหรับงานระบุ

ตัวอย่างของทักษะที่คุณจะสามารถติดตามได้รวมถึงสิ่งต่อไปนี้:
-   การควบคุมงาน – ความสามารถในการควบคุมงานของบุคคลอื่น
-   ความเป็นผู้นำ – ความสามารถในการนำพนักงานและโดเมนธุรกิจ
-   การวางแผน – ความสามารถในการมองไปข้างหน้า มีวิสัยทัศน์ และวิเคราะห์ถึงสิ่งที่จะเกิดขึ้นได้
-   HTML – ความสามารถในการเขียนโค้ด HTML

ก่อนที่คุณจะสามารถกำหนดทักษะให้บุคคลหรืองาน สร้างการค้นหาการแม็ปทักษะ หรือสร้างโพรไฟล์ทักษะ คุณต้องป้อนข้อมูลเกี่ยวกับทักษะในหน้า **ทักษะ** สำหรับแต่ละทักษะ คุณสามารถเลือกชนิดของทักษะและแบบจำลองการประเมิน

## <a name="rating-models"></a>รูปแบบการประเมิน
รูปแบบการประเมินช่วยประเมินระดับจริงของทักษะของบุคคล ระดับของบุคคลควรทำงานเพื่อให้บรรลุผลสำเร็จ หรือระดับของทักษะที่จำเป็นสำหรับงาน คุณสามารถป้อนได้ถึง 10 ระดับสำหรับรูปแบบการประเมิน  มีกำหนดแต่ละระดับในรูปแบบการประเมินตัวคูณ  ค่าตัวคูณจะถูกใช้เพื่อปรับคะแนนทักษะให้เป็นปกติที่ใช้รูปแบบการประเมินที่แตกต่างกัน  ตัวคูณต้องเป็นตัวเลขระหว่าง 0-9 และแต่ละระดับต้องมีตัวคูณที่ไม่ซ้ำกัน  ระดับที่มีค่าตัวคูณที่สูงกว่ามีน้ำหนักมากกว่าในรูปแบบการประเมิน

## <a name="specify-job-skills"></a>ระบุทักษะสำหรับงาน
เมื่อคุณป้อนข้อมูลเกี่ยวกับงาน คุณสามารถระบุทักษะที่บุคคลควรมีในการดำเนินงานทีจำเป็นสำหรับงาน  นอกจากนี้ คุณสามารถระบุระดับที่ต้องการสำหรับแต่ละทักษะด้วยระดับความสำคัญของทักษะ งานที่แตกต่างกันอาจต้องการทักษะเดียวกันในระดับความสำคัญที่แตกต่างกัน

## <a name="enter-skills-for-workers-applicants-or-contacts"></a>ป้อนทักษะสำหรับผู้ปฏิบัติงาน ผู้สมัคร หรือผู้ติดต่อ
คุณสามารถป้อนเป้าหมายทักษะทักษะที่แท้จริงสำหรับผู้ปฏิบัติงาน ผู้สมัคร หรือผู้ติดต่อ ทักษะเป้าหมายเป็นทักษะที่บุคคลวางแผนเพื่อให้บรรลุผลสำเร็จ ทักษะที่แท้จริงเป็นทักษะที่บุคคลมีอยู่ในขณะนี้

## <a name="skill-mapping-and-skill-mapping-profiles"></a> การแม็ปทักษะและโพรไฟล์การแม็ปทักษะ
คุณสามารถสร้างการค้นหาการแม็ปทักษะเพื่อค้นหาผู้ปฏิบัติงาน ผู้สมัคร หรือผู้ติดต่อที่มีคุณสมบัติเหมาะสมที่จะทำภารกิจบางอย่าง การค้นหาการแม็ปทักษะระหว่างทักษะ การศึกษา ใบรับรอง ตำแหน่งตัวแทนบริษัทและประสบการณ์โครงการ และส่งกลับผลลัพธ์ที่ตรงกับเงื่อนไขที่ป้อน  ตัวอย่างเช่น อาจมีประโยชน์เพื่อให้ทราบซึ่งผู้ปฏิบัติงานในองค์กรของคุณได้รับ CPA ของพวกเขา

โพรไฟล์การแม็ปทักษะให้คุณสามารถค้นหาพนักงานหรือผู้สมัครปัจจุบันที่มีคุณสมบัติที่ตรงกับความต้องการทางธุรกิจ  ตัวอย่างเช่น คุณสามารถสร้างโพรไฟล์การแม็ปทักษะสำหรับตำแหน่งที่เปิดในองค์กรของคุณ โดยการสร้างโพรไฟล์สำหรับงานเฉพาะ และคัดลอกทักษะ การศึกษา และใบรับรองจากงานนั้นไปที่โพรไฟล์ คุณสามารถค้นหาผู้ปฏิบัติงาน ผู้สมัคร และผู้ติดต่อที่ตรงกับเกณฑ์ป้อนไว้ในโพรไฟล์อย่างน้อยหนึ่งเกณฑ์ได้อย่างรวดเร็ว และดูรายการของผู้สมัครที่มีทักษะใกล้เคียงกับทักษะจำเป็นสำหรับงานนั้น

> **หมายเหตุ** เฉพาะผู้ปฏิบัติงาน ผู้สมัคร และผู้ติดต่อที่เลือกที่จะรวมไว้ในการค้นหาการแม็ปทักษะ สามารถแสดงในรายการผลลัพธ์ของการแม็ปทักษะ หรือรวมอยู่ในโพรไฟล์ทักษะ เมื่อต้องการรวมผู้ปฏิบัติงาน ผู้สมัคร หรือผู้ติดต่อในการค้นหาการแม็ปทักษะ ตั้งการเลือกใช่ **รวมในการแม็ปทักษะ** ในหน้าต่อไปนี้:
> 
> + ผู้ปฏิบัติงาน
> + พนักงาน
> + ผู้ขอเปิด
> + ผู้ติดต่อ

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>การวิเคราะห์และการวิเคราะห์ช่องว่างของทักษะ
คุณสามารถสร้างการวิเคราะห์โพรไฟล์ทักษะเพื่อดูรายการความสามารถของผู้ปฏิบัติงาน ผู้สมัคร หรือผู้ติดต่อ ณ เฉพาะวันที่ได้ คุณสามารถสร้างการวิเคราะห์ช่องว่างของทักษะเพื่อเปรียบเทียบทักษะของบุคลากรและทักษะที่จำเป็นสำหรับงานระบุ  


