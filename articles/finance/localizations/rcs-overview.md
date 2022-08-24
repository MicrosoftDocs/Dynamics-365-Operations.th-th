---
title: Regulatory Configuration Service
description: บทความนี้แสดงภาพรวมของความสามารถของ Regulatory Configuration Service (RCS) และอธิบายวิธีการเข้าถึงบริการ
author: kfend
ms.date: 06/04/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
ms.openlocfilehash: 01614aec0da097ee5c0c90bcbe9c7e0065f1d4fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277191"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) เป็นโปรแกรมออกแบบแบบสแตนด์อโลนและบริการจัดการวงจรชีวิตสำหรับฟังก์ชันแบบสากลไม่มีรหัส/รหัสต่ำ ผู้มีส่วนได้ส่วนเสียแบบสากลของ RCS ขยายและปรับเปลี่ยนพื้นที่หลักของภาษี การออกใบแจ้งหนี้อิเล็กทรอนิกส์ การรายงานตามระเบียบบังคับ การธนาคาร และเอกสารทางธุรกิจโดยไม่เกี่ยวข้องกับนักพัฒนา แนวทางแบบสากลไม่มีรหัส/รหัสต่านี้ช่วยให้เป็นสากลง่ายขึ้น เร็วกว่า และต้นทุนที่มีประสิทธิภาพมากกว่าในการสร้างหรือขยาย

RCS ให้ความสามารถต่อไปนี้:

- การสนับสนุนฟังก์ชันทั้งหมดที่ได้รับจากการรายงานทางอิเล็กทรอนิกส์ (ER)
- เงื่อนไขเบื้องต้นในการตั้งค่าคอนฟิกไมโครเซอร์วิสแบบสากลใหม่
- สนับสนุนสำหรับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ สำหรับข้อมูลเพิ่มเติม โปรดดู [การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga)
- สนับสนุนการคํานวณภาษี สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [บริการภาษี](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview)
- การสนับสนุนฟังก์ชันคุณลักษณะสากลใหม่ซึ่งช่วยให้การจัดการรอบเวลาของลักษณะการการใช้ฟังก์ชันหลายส่วนประกอบง่ายขึ้น และช่วยให้สามารถตั้งค่าคอนฟิกการการและตั้งค่าพารามิเตอร์ลักษณะการใช้งานต่าง ๆ ง่ายขึ้น หากต้องการข้อมูลเพิ่มเติม โปรดดูที่ [Regulatory Configuration Service – การจัดการคุณลักษณะสากลแบบง่ายสำหรับบริการสากล](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)
- สนับสนุนการเผยแพร่ การจัดเก็บ และการแบ่งปันการตั้งค่าคอนฟิกที่กําหนดเองจากส่วนกลางในที่เก็บส่วนกลางเพื่อให้การจัดการการตั้งค่าคอนฟิกง่ายขึ้นโดยไม่ต้องใช้ Microsoft Dynamics Lifecycle Services (LCS)

## <a name="access-rcs"></a>การเข้าถึง RCS

คุณสามารถลงชื่อสมัครหรือเข้าสู่ระบบ RCS จาก [หน้า Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/)

![ลงชื่อสมัครใช้/ลงชื่อเข้าใช้ RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

บนหน้า **Regulatory Configuration Service** ให้ตรวจทานและยอมรับข้อกําหนดและเงื่อนไขเพิ่มเติมเพื่อใช้บริการ แล้วเลือกปุ่มใดปุ่มหนึ่งต่อไปนี้

- **ลงชื่อสมัคร** หากคุณเป็นผู้ใช้ครั้งแรกของบริการ และคุณใช้ที่อยู่อีเมลธุรกิจเพื่อเตรียมใช้งานสภาพแวดล้อมบริการขององค์กร
- **เข้าสู่ระบบ** ถ้าคุณเคยลงชื่อสมัครใช้บริการแล้วก่อนหน้านี้ และคุณต้องการเข้าถึงสภาพแวดล้อมขององค์กร

> [!NOTE] 
> หลังจากที่คุณลงชื่อสมัคร เราขอแนะนาให้คุณเพิ่มผู้ใช้ SysAdmin เพิ่มเติมในสภาพแวดล้อม RCS ผู้ใช้รายนี้จะถูกเตรียมใช้งานเป็นผู้ดูแลระบบร่วมของสภาพแวดล้อม โดยจะช่วยให้มั่นใจถึงเสถียรภาพในการเข้าถึงสภาพแวดล้อม RCS ได้ เนื่องจากบทบาท SysAdmin คือการจัดการผู้ใช้ให้กับสภาพแวดล้อมนั้น คุณสามารถเพิ่มผู้ใช้โดยใช้ **พื้นที่ทำงาน RCS > การจัดการระบบ**

## <a name="regional-availability"></a>ความพร้อมของภูมิภาค

โดยทั่วไป RCS จะพร้อมใช้งานในภูมิภาคต่อไปนี้:

- สหรัฐ
- อินเดีย
- ฝรั่งเศส
- ยุโรป

ดูรายการภูมิภาคทั้งหมด โปรดดูที่ [Dynamics 365 และ Power Platform: ความพร้อมใช้งาน ที่ตั้งข้อมูล ภาษา และการแปลเป็นภาษาท้องถิ่น](https://aka.ms/dynamics_365_international_availability_deck)

## <a name="rcs-default-company"></a>บริษัทเริ่มต้น RCS

มีการใช้ฟังก์ชันเวลาการออกแบบที่ใช้ใน RCS ร่วมกันระหว่างบริษัททั้งหมด ไม่มีฟังก์ชันเฉพาะบริษัท ดังนั้น เราขอแนะนำให้ใช้บริษัทหนึ่งแห่ง **DAT** กับสภาพแวดล้อม RCS ของคุณ

อย่างไรก็ตาม ในบางสถานการณ์ คุณอาจต้องการให้รูปแบบ ER ใช้พารามิเตอร์ที่เกี่ยวข้องกับนิติบุคคลหนึ่งๆ ในสถานการณ์เหล่านี้เท่านั้น คุณควรใช้ตัวสลับบริษัทเริ่มต้น สำหรับตัวอย่าง ให้ดูที่ [ตั้งค่าคอนฟิกรูปแบบ ER เพื่อใช้พารามิเตอร์ที่ระบุสำหรับนิติบุคคลแต่ละรายการ](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md)

## <a name="related-rcs-documentation"></a>คู่มือ RCS ที่เกี่ยวข้อง

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับส่วนประกอบที่เกี่ยวข้อง ให้ดูที่หัวข้อต่อไปนี้:

- **RCS:**

    - [สร้างการตั้งค่าคอนฟิก ER ใน RCS และอัปโหลดไปยังที่เก็บส่วนกลาง](rcs-global-repo-upload.md)

- **ที่เก็บส่วนกลาง:**

    - [สร้างการตั้งค่าคอนฟิก ER & อัปโหลดไปที่ที่เก็บส่วนกลาง](rcs-global-repo-upload.md)
    - [แบ่งปันการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง](rcs-global-repo-share-configuration.md)
    - [การกรองข้อมูลขั้นสูงในที่เก็บส่วนกลาง](enhanced-filtering-global-repo.md)
    - [ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลาง](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [ยกเลิกการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) – การคิดค่าเสื่อมราคาที่เก็บข้อมูล Lifecycle Services (LCS)](rcs-lcs-repo-dep-faq.md)

- **คุณลักษณะที่ใช้ทั่วโลก**

    - [Regulatory configuration service (RCS) - คุณลักษณะที่ใช้ทั่วโลก](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>การแก้ไขปัญหาการลงทะเบียน RCS

เมื่อคุณลงชื่อสมัครใน RCS จากหน้าบริการ คุณอาจพบปัญหาที่เกี่ยวข้องกับ Azure Active Directory (Azure AD) ข้อความแสดงข้อผิดพลาดที่คุณได้รับบ่งชี้ว่าการลงชื่อสมัครใน RCS ปิดอยู่ในขณะนี้ และต้องเปิดอยู่ก่อนที่คุณจะสามารถประมวลผลการลงชื่อสมัครให้เสร็จสมบูรณ์

![ข้อความแสดงข้อผิดพลาดการลงชื่อสมัครใน RCS](media/01_RCSSignUpError.jpg)

ปัญหาเกิดขึ้นเนื่องจากคุณถูกบล็อคไม่ให้ลงชื่อสมัครบอกรับเป็นสมาชิกเฉพาะทาง และต้องเปิดใช้งานคุณสมบัติ `AllowAdHocSubscriptions` ในผู้เช่าของคุณ 

- หากแผนกไอทีของคุณจัดการผู้เช่าใน Azure ขององค์กร ให้ติดต่อแผนกนั้นเพื่อรายงานปัญหา
- หากคุณรับผิดชอบการจัดการผู้เช่า Azure ของคุณ คุณสามารถแก้ไขปัญหาโดยการปฏิบัติตามขั้นตอน [การลงชื่อสมัครใช้ระบบบริการ Azure Active Directory ด้วยตนเองคืออะไร](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings)
