---
title: ตั้งค่าการรวมกับ LinkedIn สำหรับ Microsoft Dynamics 365 Talent - Attract
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกการรวม Linkedin สำหรับ Microsoft Dynamics 365 Talent - Attract เพื่อให้คุณสามารถลงประกาศงานไปยัง Linkedin จาก Attract ได้ง่าย และเพื่อให้ผู้สรรหาของคุณสามารถซิงค์ข้อมูลการสรรหาบุคลากรกับโพรไฟล์ LinkedIn ของผู้สมัคร
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6b86cafdf364f2de051f3d8ceab7413c2c13c3a5
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009981"
---
# <a name="set-up-linkedin-integration"></a>ตั้งค่าการรวม LinkedIn

[!include[banner](../includes/banner.md)]

ช่วยให้ผู้สรรหาและผู้จัดการจ้างงานของคุณดึงดูดผู้มีความสามารถพิเศษระดับต้นโดยการตั้งค่าคอนฟิกการรวม LinkedIn กับ Microsoft Dynamics 365 Talent: Attract Attract ช่วยให้คุณสามารถลงประกาศงานโดยตรงไปยัง LinkedIn เครือข่ายออนไลน์ของมืออาชีพที่ใหญ่ที่สุด

งานที่คุณลงประกาศไปยัง LinkedIn ผ่าน Attract มีการแสดงรายการที่จำกัดและไม่มีต้นทุนเพิ่มเติมให้กับบริษัทของคุณ การแสดงรายการเหล่านี้จะพร้อมใช้งานผ่านพันธมิตรซอฟต์แวร์ LinkedIn เท่านั้น เช่น Attract ผู้ใช้จะไม่ปรากฏในแผง **อาชีพ** บนหน้า LinkedIn ของบริษัทของคุณ เนื่องจากมีเฉพาะการแสดงรายการที่ชำระเงินไว้เท่านั้นที่จะปรากฏขึ้นที่นั่น อย่างไรก็ตาม จะแสดงขึ้นเมื่อผู้สมัครที่มีโอกาสดูงานที่มีอยู่ทั้งหมด การแสดงรายการที่จำกัดยังแสดงอยู่ในการค้นหางาน LinkedIn ด้วย

Attract มีสองวิธีให้ใช้ในการรวมกับ LinkedIn เพื่อช่วยให้คุณจัดหาผู้สมัครจากเว็บไซต์อาชีพที่เป็นที่นิยมนี้:

- ลงประกาศงานจาก Attract ไปยัง LinkedIn
- จัดหาผู้สมัครจาก LinkedIn ไปยัง Attract

คุณสามารถตั้งค่าคอนฟิกทั้งสองตัวเลือกบนแท็บ **การรวม LinkedIn** ในศูนย์การจัดการ หากต้องการเปิดศูนย์การจัดการ ให้ไปที่ <https://attract.talent.dynamics.com/adminsettings>

> [!NOTE]
> หากต้องการใช้การรวม LinkedIn Recruiter กับ Attract คุณต้องใช้ [add-on การจ้างงานที่ครอบคลุม](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) และ [LinkedIn Recruiter สิทธิ์การใช้งาน](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18) สำหรับข้อมูลเพิ่มเติมให้ ดูที่ [Attract รุ่นใด](./attract-comprehensive-hiring.md).

หากคุณกำลังมีปัญหาในการลงประกาศงานใน LinkedIn โปรดดูที่ [แก้ไขปัญหาการรวมกับ LinkedIn](./attract-troubleshoot-linkedin.md)

สำหรับข้อมูลเกี่ยวกับวิธีการอื่นๆ ในการลงประกาศงานไปยัง LinkedIn ดูที่ [LinkedIn FAQ](./attract-linkedin-faq.md)

## <a name="configure-job-posting-to-linkedin"></a>ตั้งค่าคอนฟิกการประกาศงานไปยัง LinkedIn

ก่อนที่คุณจะสามารถลงประกาศงานจาก Attract ไปยัง LinkedIn คุณต้องใช้ [รหัสบริษัท LinkedIn](https://aka.ms/findID) รหัสบริษัท LinkedIn ของคุณคือ สตริงของหมายเลขที่ระบุบริษัทของคุณโดยเฉพาะใน LinkedIn สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การเชื่อมโยงรหัสบริษัท Linkedin กับบอร์ดงาน Linkedin - คำถามที่พบบ่อย](https://aka.ms/findID)

Attract ส่งฟีดการลงประกาศงานไปยัง LinkedIn ของคุณ และ LinkedIn จะตรวจสอบฟีดนั้นหนึ่งครั้งต่อวันโดยประมาณ อาจใช้เวลานานถึง 48 ชั่วโมงสำหรับการลงประกาศไปยังไซต์

งานที่โพสต์ไปยัง LinkedIn ปรากฏขึ้นบนไซต์ LinkedIn ขณะใช้งานจริง LinkedIn ไม่มีสภาพแวดล้อมการทดสอบสำหรับการลงประกาศงาน ดังนั้น โปรดตรวจสอบให้แน่ใจว่าคุณไม่ได้ลงประกาศงานทดสอบใดๆโดยไม่ได้ตั้งใจ 

1. ในเมนู **ตั้งค่า** (สัญลักษณ์เกียร์) ในมุมบนด้านขวา เลือก **ศูนย์ผู้ดูแลระบบ** หรือไปที่ <https://attract.talent.dynamics.com/adminsettings>
2. เลือกแท็บ **การรวม LinkedIn**
3. ภายใต้ **ชื่อบริษัท** ให้ป้อนชื่อบริษัทของคุณและภายใต้ **รหัสบริษัท** โปรดป้อนรหัสบริษัท LinkedIn ของคุณ ตรวจสอบให้แน่ใจว่าชื่อบริษัทตรงกับชื่อที่ปรากฏบนหน้า LinkedIn ของบริษัทของคุณ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสบริษัท LinkedIn โปรดดูที่ [การเชื่อมโยงรหัสบริษัท Linkedin กับบอร์ดงาน Linkedin - คำถามที่ถามบ่อย](https://www.linkedin.com/help/linkedin/answer/98972)

    ถ้าคุณต้องการเปลี่ยนแปลงข้อมูลใดๆ สำหรับองค์กรของคุณ ให้ดูที่ [เปลี่ยนที่อยู่ขององค์กรของคุณ ผู้ติดต่อด้านเทคนิค และอื่นๆ](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more) ถ้าคุณยังคงพบปัญหาอยู่ โปรดติดต่อ [ฝ่ายสนับสนุน LinkedIn](https://www.linkedin.com/help/linkedin)

4. เลือก **บันทึก**

## <a name="set-up-linkedin-recruiter-with-attract"></a>ตั้งค่า LinkedIn Recruiter กับ Attract 

หากคุณต้องการอนุญาตให้ผู้สรรหาสามารถค้นหางานผ่าน LinkedIn Recruiter ได้ คุณต้องตั้งค่าคอนฟิกการรวมกับ LinkedIn Recruiter ใน Attract เมื่อต้องการดำเนินการขั้นตอนการตั้งค่าคอนฟิกให้เสร็จสมบูรณ์ คุณต้องทำงานกับผู้ใช้ที่เป็นผู้ดูแลระบบในสัญญา LinkedIn Recruiter ขององค์กรของคุณ

1. ในเมนู **ตั้งค่า** (สัญลักษณ์เกียร์) ในมุมบนด้านขวา เลือก **ศูนย์ผู้ดูแลระบบ** หรือไปที่ <https://attract.talent.dynamics.com/adminsettings>
2. เลือกแท็บ **การรวม LinkedIn**

    [![มุมมองผู้ดูแลระบบ Attract เพื่อเริ่มต้นการรวม LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. เลือก **เชื่อมต่อ** เพื่อเริ่มต้นการตั้งค่า คุณจะได้รับการแนะนำผ่านกระบวนการลงชื่อเข้าใช้ LinkedIn
4. ถ้าคุณมีสิทธิ์การใช้งานในสัญญา LinkedIn หลายรายการ เลือกสัญญาที่คุณต้องการให้เชื่อมต่อกับระบบ Attract ถ้าคุณสิทธิ์การใช้งานในสัญญา LinkedIn เพียงรายการเดียวเท่านั้น คุณสามารถข้ามขั้นตอนนี้ได้
5. ภายใต้ **การเชื่อมต่อระบบผู้สรรหา (RSC)** เลือก **ร้องขอ**

    [![มุมมองผู้ดูแลระบบ Attract เพื่อขอการรวม LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. ในขณะนี้ การตั้งค่า **การเชื่อมต่อระบบผู้สรรหา (RSC)** ควรแสดงเป็น **คู่ค้าพร้อม** ถ้าคุณเห็น **แจ้งให้คู่ค้าทราบ** บนหน้านี้ ให้รอสักครู่ เลือก **แจ้งให้คู่ค้าทราบ** แล้วรีเฟรชหน้านั้น ขณะนี้ การตั้งค่าควรแสดงเป็น **คู่ค้าพร้อม**

    [![มุมมองผู้ดูแลระบบ Attract เพื่อบ่งชี้ฝั่ง Attract ของคำขอได้ถูกดำเนินการเสร็จสมบูรณ์แล้ว](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. เพื่อดำเนินการให้ขั้นตอนถัดไปเสร็จสิ้น คุณต้องมีสิทธิ์ผู้ดูแลระบบบนสัญญา LinkedIn Recruiter ของคุณ

    1. ลงชื่อเข้าใช้ LinkedIn โดยใช้บัญชีผู้ดูแลระบบ แล้วเลือก **LinkedIn Recruiter** ที่ด้านขวาบน 
    2. ในเมนู **เพิ่มเติม** ที่ด้านบนของหน้า เลือก **การตั้งค่าผู้ดูแลระบบ** แล้วเลือกแท็บ **ATS**
    3. เมื่อต้องการเปิดใช้งานการส่งออกแบบคลิกเดียวสำหรับสัญญาเพียงรายการเดียว ให้เปิดใช้งาน **การเข้าถึงระดับสัญญา (สำหรับทุกที่นั่งในสัญญานี้** เมื่อต้องการเปิดใช้งานสำหรับทั้งบริษัท ให้เปิดใช้งาน **การเข้าถึงระดับบริษัท (สำหรับสัญญาทั้งหมดในบริษัทของคุณ**

    [![เปิดการรวม Attract จากมุมมองผู้ดูแลระบบของ LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)

8. ในศูนย์การจัดการ Attract ให้เลือกแท็บ **การรวม LinkedIn** การตั้งค่า **การเชื่อมต่อระบบผู้สรรหา (RSC)** ควรแสดงเป็น **เปิดใช้งานแล้ว** ในขณะนี้

    [![การรวม LinkedIn Recruiter เสร็จสมบูรณ์](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>ตั้งค่า สมัครด้วย LinkedIn ใน Attract

คุณสามารถอนุญาตให้ผู้สมัครทำการสมัครงานของคุณได้โดยใช้โพรไฟล์ LinkedIn สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสมัครด้วย LinkedIn โปรดดู [พลังของ LinkedIn ในทุกที่: สมัครด้วย LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin)

คุณลักษณะนี้อยู่ในการแสดงตัวอย่างในขณะนี้ ก่อนที่คุณจะทำตามขั้นตอนต่อไปนี้ โปรดตรวจสอบให้แน่ใจว่ามีการเปิดใช้งาน สมัครด้วย LinkedIn สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเปิดใช้งานลักษณะการทำงานของการแสดงตัวอย่าง ดู [เข้าถึงลักษณะการทำงานของการแสดงตัวอย่างใน Talent](./access-preview-feature.md)

1. ในเมนู **ตั้งค่า** (สัญลักษณ์เกียร์) ในมุมบนด้านขวา เลือก **ศูนย์ผู้ดูแลระบบ** หรือไปที่ <https://attract.talent.dynamics.com/adminsettings>
2. เลือกแท็บ **การรวม LinkedIn**

    [![มุมมองผู้ดูแลระบบ Attract เพื่อเริ่มต้นการรวม LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. ถัดจาก **สมัครด้วย LinkedIn** เลือก **เชื่อมต่อ** เพื่อเริ่มต้นการตั้งค่า คุณจะได้รับการแนะนำผ่านกระบวนการที่เหลือด้วย LinkedIn

## <a name="see-also"></a>ดูเพิ่มเติมที่

[FAQ เกี่ยวกับ LinkedIn](./attract-linkedin-faq.md)

[ลงประกาศงานลงในไซต์ภายนอกจาก Attract](./posting-jobs-external.md)

[จัดหาผู้สมัครด้วย LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[สร้างงาน](./creating-jobs-attract.md)

[แก้ไขปัญหาการรวมกับ LinkedIn](./attract-troubleshoot-linkedin.md)
