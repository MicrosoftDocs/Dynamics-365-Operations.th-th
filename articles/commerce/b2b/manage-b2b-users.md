---
title: จัดการผู้ใช้คู่ค้าทางธุรกิจบนเว็บไซต์อีคอมเมิร์ซของ B2B
description: บทความนี้อธิบายวิธีการเพิ่ม ลบ และแก้ไขผู้ใช้ที่เป็นคู่ค้าทางธุรกิจบนเว็บไซต์อีคอมเมิร์ซระหว่างธุรกิจกับธุรกิจ (B2B) Microsoft Dynamics 365 Commerce และใน Commerce headquarters
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: a59220c16e195ff36980517baec6fb8246a18115
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281184"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>จัดการผู้ใช้คู่ค้าทางธุรกิจบนเว็บไซต์อีคอมเมิร์ซของ B2B

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายวิธีการเพิ่ม ลบ และแก้ไขผู้ใช้ที่เป็นคู่ค้าทางธุรกิจบนเว็บไซต์อีคอมเมิร์ซระหว่างธุรกิจกับธุรกิจ (B2B) Microsoft Dynamics 365 Commerce และใน Commerce headquarters

> [!NOTE]
> - บทความ [จัดการคู่ค้าทางธุรกิจ B2B โดยใช้ลำดับชั้นของลูกค้า](partners-customer-hierarchies.md) เป็นข้อกำหนดเบื้องต้นสำหรับเอกสารนี้
> - ตรวจสอบให้แน่ใจว่าคุณเริ่มต้นเอนทิตี้ชนิดเอกสารใน Commerce headquarters โดยเปิดแบบฟอร์ม **ชนิดเอกสาร** ที่ **การจัดการองค์กร \> การจัดการองค์กร \> ชนิดเอกสาร**

เว็บไซต์อีคอมเมิร์ซของ B2B ต้องการให้องค์กรลงทะเบียนเป็นคู่ค้าทางธุรกิจ หลังจากที่องค์กรส่งรายละเอียดการลงทะเบียนไปที่เว็บไซต์อีคอมเมิร์ซของ B2B แล้ว คำขอการลงทะเบียนจะไปที่กระบวนการรับรองคุณสมบัติ หากองค์กรมีคุณสมบัติเหมาะสม จะได้รับการเตรียมความพร้อมเป็นคู่ค้าทางธุรกิจ

หลังจากที่องค์กรถูกลงทะเบียนไว้ในฐานะคู่ค้าทางธุรกิจแล้ว ผู้ใช้องค์กรที่เริ่มต้นคำขอให้กลายเป็นคู่ค้าทางธุรกิจจะระบุเป็นผู้ใช้ระดับผู้ดูแลระบบและได้รับอนุญาตให้เตรียมพร้อมผู้ใช้ที่ได้รับอนุญาตเพิ่มเติมของเว็บไซต์อีคอมเมิร์ซของ B2B ผู้ใช้ที่ได้รับอนุมัติเหล่านี้สามารถวางใบสั่งในนามของคู่ค้าทางธุรกิจได้

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>ตั้งค่าผู้ใช้ระดับผู้ดูแลระบบให้กับคู่ค้าทางธุรกิจใหม่

คู่ค้าทางธุรกิจที่เป็นไปได้สามารถเริ่มต้นกระบวนการเริ่มเปิดใหม่ให้กับเว็บไซต์อีคอมเมิร์ซ B2B โดยการส่งการร้องขอการเริ่มต้นใหม่ผ่านลิงก์บนเว็บไซต์ B2B จากนั้นคุณสามารถใช้แบบฟอร์มที่ปรับแต่งได้เพื่อจัดเตรียมรายละเอียดที่ต้องใช้ในการเตรียมความพร้อมและลงทะเบียน หลังจากส่งคำขอแล้ว หน้าการยืนยันการส่งจะปรากฏขึ้น หากการส่งได้รับอนุมัติ บริษัทที่ส่งคำขอจะกลายเป็นคู่ค้าทางธุรกิจ และผู้ขอ (นั่นคือ ผู้ใช้ที่เริ่มต้นคำขอการเตรียมความพร้อม) จะกลายเป็นผู้ใช้ที่เป็นผู้ดูแลระบบสำหรับคู่ค้าทางธุรกิจ

หากต้องการอนุมัติคำขอของคู่ค้าทางธุรกิจใน Commerce headquarters ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **ข้อมูลไอทีสำหรับ Retail และ Commerce \> กำหนดการการกระจาย**
1. เรียกใช้งาน **P-0001** เพื่อดึงการร้องขอการเตรียมพร้อมของคู่ค้าทั้งหมดเข้าสู่ Commerce headquarters
1. เมื่อรันงาน **P-0001** เสร็จเรียบร้อยแล้ว ให้ไปที่ **ข้อมูลไอทีสำหรับ Retail และ Commerce \> ลูกค้า** และเรียกใช้ **ซิงโครไนส์ลูกค้าและคำขอช่องทาง** หลังจากรันงานนี้เสร็จเรียบร้อยแล้ว คำขอการจัดตารางใหม่จะถูกสร้างขึ้นเป็นเรกคอร์ดผู้ที่มีแนวโน้มจะเป็นลูกค้าชนิด **ผู้ที่มีแนวโน้มจะเป็นลูกค้า B2B** ใน Commerce headquarters 
1. ไปที่ **ลูกค้า \> ผู้ที่มีแนวโน้มจะเป็นลูกค้าทั้งหมด** เลือกเรกคอร์ดผู้ที่มีแนวโน้มจะเป็นลูกค้าของคู่ค้าทางธุรกิจใหม่เพื่อเปิดหน้ารายละเอียดของผู้ที่มีแนวโน้มจะเป็นลูกค้า
1. บนแท็บ **ทั่วไป** ให้เลือก **แปลง \> การอนุมัติ/ปฏิเสธ** เพื่ออนุมัติคำขอการเตรียมพร้อม เมื่อข้อความยืนยันปรากฏขึ้น ให้ยืนยันว่าคุณต้องการประมวลผลต่อไป และอนุมัติคำขอ การอนุมัติจะเปลี่ยนแปลงฟิลด์ **สถานะ** ของเรกคอร์ดผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็น **อนุมัติแล้ว** จากนั้นอีเมลจะส่งไปยังที่อยู่อีเมลของลูกค้าผู้ขอเพื่อยืนยันว่าองค์กรได้ผ่านการอนุมัติในฐานะคู่ค้าทางธุรกิจ นอกจากนี้ ระบบยังสร้างลระดับชั้นของลูกค้าซึ่งผู้ขอจะถูกเพิ่มเข้าเป็นผู้ดูแลระบบของคู่ค้าทางธุรกิจด้วย

    > [!NOTE]
    > ปัจจุบัน จะมีการส่งอีเมลการยืนยันพร้อมการอนุมัติทันที อย่างไรก็ตาม ฟังก์ชัน Commerce ในอนาคตจะช่วยให้ผู้ดูแลระบบทริกเกอร์อีเมลด้วยตนเอง

1. ไปที่ **ข้อมูลไอทีสำหรับ Retail และ Commerce \> กำหนดการกระจาย** และเรียกใช้ **1010 (ลูกค้า)** เพื่อผลักดันเรกคอร์ดลูกค้าใหม่และลำดับชั้นลูกค้าที่สร้างขึ้นใหม่ไปยังฐานข้อมูลช่องทาง

> [!NOTE]
> เพื่อให้แน่ใจว่าเรกคอร์ดลูกค้าใหม่จะถูกส่งไปยังฐานข้อมูลช่องทาง ควรจะรวมสมุดที่อยู่อย่างน้อยหนึ่งเล่มที่เชื่อมโยงกับลูกค้าในสมุดที่อยู่ของลูกค้าที่เชื่อมโยงกับร้านค้าออนไลน์ คุณสามารถกําหนดกระบวนการนี้โดยอัตโนมัติโดยการตั้งค่าคอนฟิกสมุดที่อยู่จากลูกค้าเริ่มต้นของร้านค้าออนไลน์ เพื่อให้ระบบคัดลอกค่าสมุดที่อยู่ไปให้ลูกค้ารายใหม่ทุกราย

หลังจากเรกคอร์ดลำดับชั้นลูกค้าซิงค์กับฐานข้อมูลช่องทาง ผู้ขอสามารถเข้าสู่ระบบเว็บไซต์อีคอมเมิร์ซของ B2B ได้โดยใช้ที่อยู่อีเมลที่ให้ไว้เมื่อส่งคำขอการเตรียมพร้อม ผู้ใช้สามารถใช้ขั้นตอนการลงทะเบียนเพื่อกําหนดรหัสผ่านของบัญชีของพวกเขา ดูข้อมูลเกี่ยวกับวิธีการเปิดใช้งานเรกคอร์ดผู้ให้บริการข้อมูลประจำตัว Azure Active Directory (Azure AD) B2C ที่เชื่อมโยงกับเรกคอร์ดลูกค้า B2B ที่สร้างขึ้นในการอนุมัติของผู้ที่มีแนวโน้มจะเป็นลูกค้า ดูที่ [เปิดใช้งานการเชื่อมโยงอัตโนมัติ](../identity-record-linking.md)

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>แจ้งเตือนผู้ที่มีแนวโน้มจะเป็นลูกค้า B2B เมื่อได้รับการอนุมัติหรือถูกปฏิเสธ

เมื่อคุณอนุมัติหรือปฏิเสธคำขอการเตรียมความพร้อมผู้ที่มีแนวโน้มจะเป็นลูกค้า B2B คุณสามารถส่งการแจ้งเตือนทางอีเมลไปยังผู้ที่มีแนวโน้มจะเป็นลูกค้าโดยอัตโนมัติ

เมื่อต้องการตั้งค่าการแจ้งเตือนทางอีเมลใน Commerce headquarters สำหรับเหตุการณ์ของชนิดการแจ้งเตือน **ผู้ที่มีแนวโน้มจะเป็นลูกค้า B2B ที่ได้รับอนุมัติ** หรือ **ผู้ที่มีแนวโน้มจะเป็นลูกค้า B2B ที่ปฏิเสธ** ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. สร้างแม่แบบอีเมลสำหรับอีเมลที่จะส่งไปยังผู้ที่มีแนวโน้มจะเป็นลูกค้าเมื่อชนิดการแจ้งเตือน **ผู้ที่มีแนวโน้มจะเป็นลูกค้า B2B** หรือ **ผู้ที่มีแนวโน้มจะเป็นลูกค้า B2B ที่ปฏิเสธ** ถูกทริกเกอร์ หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับตัวยึดที่ชนิดการแจ้งเตือนเหล่านี้รองรับ ดูที่ [ชนิดของการแจ้งเตือน](../email-templates-transactions.md#notification-types) สำหรับข้อมูลเกี่ยวกับวิธีการสร้างแม่แบบอีเมล ให้ดูที่ [สร้างแม่แบบอีเมล](../email-templates-transactions.md#create-an-email-template)
1. เพิ่มชนิดการแจ้งเตือน **ผู้ที่มีแนวโน้มจะเป็นลูกค้า B2B ที่ได้รับอนุมัติ** และ **ผู้ที่มีแนวโน้มจะเป็นลูกค้า B2B ที่ปฏิเสธ** ในโปรไฟล์การแจ้งเตือนทางอีเมลของคุณ และแมปชนิดดังกล่าวกับแม่แบบอีเมลที่คุณสร้างขึ้น สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโปรไฟล์การแจ้งเตือน ดู [ตั้งค่าโพรไฟล์การแจ้งเตือนทางอีเมล](../email-notification-profiles.md)

## <a name="onboard-additional-business-partner-users"></a>เตรียมพร้อมผู้ใช้คู่ค้าทางธุรกิจเพิ่มเติม

ผู้ใช้ผู้ดูแลระบบคู่ค้าทางธุรกิจสามารถเปิดผู้ใช้คู่ค้าทางธุรกิจเพิ่มเติมใหม่ในเว็บไซต์อีคอมเมิร์ซของ B2B ได้ตามที่ต้องการ

หากต้องการลงทะเบียนผู้ใช้คู่ค้าทางธุรกิจเพิ่มเติมใหม่ที่เว็บไซต์อีคอมเมิร์ซของ B2B ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. เข้าสู่ระบบเว็บไซต์อีคอมเมิร์ซของ B2B ในฐานะผู้ดูแลระบบ
1. ไปที่ **บัญชีของฉัน \> ผู้ใช้ในองค์กร \> ดูรายละเอียด** และเลือก **เพิ่มผู้ใช้**
1. ป้อนข้อมูลที่ต้องใช้ แล้วเลือก **บันทึก** สถานะของผู้ใช้ใหม่ถูกตั้งค่าเป็น **ค้างอยู่**

หลังจากงาน **P-0001** และ **ซิงโครไนส์ลูกค้าและคำขอช่องทาง** ทำงาน เรกคอร์ดลูกค้าชนิด **บุคคล** จะถูกสร้างสำหรับผู้ใช้ใหม่ใน Commerce headquarters เรกคอร์ดลูกค้านี้ยังสัมพันธ์กับเรกคอร์ดลำดับชั้นลูกค้าของคู่ค้าทางธุรกิจที่เกี่ยวข้องด้วย นอกจากนี้ อีเมลยังส่งไปยังที่อยู่อีเมลของผู้ใช้ใหม่เพื่อแจ้งให้ผู้ใช้ทราบว่าได้เพิ่มที่อยู่อีเมลดังกล่าวเข้าเป็นผู้ใช้ขององค์กรคู่ค้าทางธุรกิจ แล้วขณะนี้สามารถเข้าสู่ระบบเว็บไซต์อีคอมเมิร์ซของ B2B ได้

จากนั้นเรียกใช้งาน **1010 (ลูกค้า)** เพื่อซิงโครไนส์ผู้ใช้คู่ค้าทางธุรกิจใหม่กับฐานข้อมูลช่องทาง

หลังจากที่ซิงโครไนส์เรกคอร์ดลูกค้าแล้ว สถานะของผู้ใช้ในเว็บไซต์อีคอมเมิร์ซของ B2B จะถูกตั้งค่าเป็น **ใช้งานอยู่** และผู้ใช้ใหม่สามารถล็อกอินเข้าสู่เว็บไซต์อีคอมเมิร์ซ B2B ได้โดยใช้ที่อยู่อีเมลของผู้ใช้ ผู้ใช้สามารถใช้ขั้นตอนการลงทะเบียนเพื่อกําหนดรหัสผ่านของบัญชีของพวกเขา ดูข้อมูลเกี่ยวกับวิธีการเปิดใช้งานเรกคอร์ดผู้ให้บริการข้อมูลประจำตัว Azure AD B2C เชื่อมโยงกับเรกคอร์ดลูกค้า B2B ที่สร้างขึ้นใน Commerce headquarters ที่ [เปิดใช้งานการเชื่อมโยงอัตโนมัติ](/dynamics365/commerce/identity-record-linking.md)

## <a name="edit-business-partner-user-details"></a>แก้ไขรายละเอียดผู้ใช้คู่ค้าทางธุรกิจ

หากต้องการแก้ไขรายละเอียดของผู้ใช้คู่ค้าทางธุรกิจ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. เข้าสู่ระบบเว็บไซต์อีคอมเมิร์ซของ B2B ในฐานะผู้ดูแลระบบ
1. ไปที่ **บัญชีของฉัน \> ผู้ใช้ในองค์กร \> ดูรายละเอียด** เลือกปุ่ม **แก้ไข** (สัญลักษณ์ดินสอ) ทำการเปลี่ยนแปลงที่ต้องใช้ แล้วเลือก **บันทึก** การเปลี่ยนแปลงจะมีผลเฉพาะหลังจากที่เรียกใช้งาน **P-0001**, **ซิงโครไนส์ลูกค้าและคำขอช่องทาง** และ **1010 (ลูกค้า)**

## <a name="remove-a-business-partner-user"></a>ลบผู้ใช้คู่ค้าทางธุรกิจ

ผู้ดูแลระบบสามารถลบผู้ใช้ที่มีอยู่ขององค์กรคู่ค้าทางธุรกิจออกจากรายชื่อผู้ใช้ที่สามารถเข้าถึงเว็บไซต์อีคอมเมิร์ซ B2B ได้ตามที่ต้องการ
หากต้องการนำผู้ใช้คู่ค้าทางธุรกิจออก ให้ทำตามขั้นตอนต่อไปนี้
- เข้าสู่ระบบเว็บไซต์อีคอมเมิร์ซของ B2B ในฐานะผู้ดูแลระบบ
- ไปที่ **บัญชีของฉันt > ผู้ใช้ในองค์กร \> ดูรายละเอียด** และเลือกปุ่ม **นำออก** (สัญลักษณ์ "X") เมื่อข้อความยืนยันปรากฏขึ้น ให้ยืนยันว่าคุณต้องการลบผู้ใช้ออก การเปลี่ยนแปลงจะมีผลเฉพาะหลังจากที่เรียกใช้งาน **P-0001**, **ซิงโครไนส์ลูกค้าและคำขอช่องทาง** และ **1010 (ลูกค้า)**

> [!NOTE]
> เมื่อคุณลบผู้ใช้ออกจากรายชื่อผู้ใช้ที่สามารถเข้าถึงเว็บไซต์อีคอมเมิร์ซของ B2B เรกคอร์ดลูกค้าที่สอดคล้องจะถูกลบออกจากเรกคอร์ดลำดับชั้นของลูกค้าของคู่ค้าทางธุรกิจ อย่างไรก็ตาม ตัวเรกคอร์ดลูกค้าเองไม่ได้ถูกลบออกจาก Commerce headquarters

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>เตรียมความพร้อมลูกค้าที่มีอยู่เป็นคู่ค้าทางธุรกิจบนเว็บไซต์อีคอมเมิร์ซของ B2B

ผู้ดูแลระบบสามารถเตรียมพร้อมคู่ค้าทางธุรกิจและผู้ใช้ได้โดยตรงใน Commerce headquarters ความสามารถนี้มีประโยชน์ต่อการเตรียมความพร้อมคู่ค้าทางธุรกิจที่มีอยู่ของคุณบนเว็บไซต์อีคอมเมิร์ซของ B2B

หากต้องการเตรียมพร้อมคู่ค้าทางธุรกิจและผู้ใช้ใน Commerce headquarters ให้ทำตามขั้นตอนต่อไปนี้

1. สร้างหรือเลือกลูกค้าชนิด **องค์กร** เพื่อเพิ่มเป็นคู่ค้าทางธุรกิจ
1. สร้างหรือเลือกลูกค้าชนิด **บุคคล** เพื่อเพิ่มเป็นผู้ดูแลระบบหรือผู้ใช้ให้กับคู่ค้าทางธุรกิจ ตรวจสอบให้แน่ใจว่าที่อยู่อีเมลหลักเชื่อมโยงกับลูกค้า ที่อยู่อีเมลเหล่านี้ใช้ในกาลงชื่อเข้าใช้เว็บไซต์ 

    > [!NOTE]
    > ระบบต้องสามารถค้นหาเรกคอร์ดลูกค้าเฉพาะของผู้ใช้ที่ควรสามารถลงชื่อเข้าใช้เว็บไซต์ได้ หากระบบค้นหาลูกค้ามากกว่าหนึ่งรายที่มีที่อยู่อีเมลหลักเหมือนกันในนิติบุคคล ผู้ใช้จะไม่สามารถลงชื่อเข้าใช้เว็บไซต์ได้

1. สร้างรหัสลำดับชั้นของลูกค้า
1. ในฟิลด์ **ชื่อ** ป้อนชื่อ
1. ในฟิลด์ **องค์กร** ให้ป้อนลูกค้าองค์กรคู่ค้าทางธุรกิจ
1. บนแท็บด่วน **ลำดับชั้น** ให้เลือก **เพิ่ม**
1. ในฟิลด์ **ชื่อ** เลือกลูกค้าเป็นชนิด **บุคคล**
1. เลือกบทบาท **ผู้ดูแลระบบ** ของลูกค้าที่ควรได้รับการแต่งตั้งเป็นผู้ดูแลระบบ
1. ทําซ้ํากระบวนการนี้เพื่อเพิ่มลูกค้าเพิ่มเติมไปยังลําดับชั้น

## <a name="additional-information"></a>ข้อมูลเพิ่มเติม

- งานทั้งหมดที่กล่าวถึงในบทความนี้สามารถตั้งค่าคอนฟิกให้รันในกําหนดการในรูปแบบชุดงานได้ ความคาดหวังคือคู่ค้าทางธุรกิจจะตั้งค่าคอนฟิกชุดงานตามความกําหนด
- ปัจจุบัน สามารถแต่งตั้งเรกคอร์ดผู้ใช้/ลูกค้าได้เพียงเรกคอร์ดเดียวเป็นผู้ใช้ระดับผู้ดูแลระบบ และสามารถเปลี่ยนบทบาทนั้นใน Commerce headquarters เท่านั้น ไม่มีการสนับสนุนความสามารถด้านการบริการตนเองที่แจ้งให้คู่ค้าทางธุรกิจแต่งตั้งผู้ดูแลหลายคน หรือเปลี่ยนผู้ดูแลระบบจากเว็บไซต์อีคอมเมิร์ซ B2B
- แม้ว่าจะสามารถกําหนดวงเงินการใช้จ่ายให้กับผู้ใช้ แต่การบังคับใช้วงเงินการใช้จ่ายในระหว่างกระบวนการป้อนข้อมูลใบสั่งยังไม่ได้รับการดําเนินการ
- ตรรกะทางธุรกิจทั้งหมดและการตรวจสอบความถูกต้องของประสบการณ์ของผู้ใช้ในเว็บไซต์อีคอมเมิร์ซแบบ B2B ยึดตามการตั้งค่าคอนฟิกของเรกคอร์ดลูกค้าที่ถูกแมปกับผู้ใช้ใน Commerce headquarters

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าไซต์อีคอมเมิร์ซ B2B](set-up-b2b-site.md)

[จัดการคู่ค้าทางธุรกิจ B2B โดยใช้ลำดับชั้นของลูกค้า](partners-customer-hierarchies.md)

[ตั้งค่าคอนฟิกวิธีการชำระเงินด้วยบัญชีลูกค้าสำหรับไซต์อีคอมเมิร์ซของ B2B](payment-method.md)

[ตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์เกี่ยวกับไซต์อีคอมเมิร์ซของ B2B](quantity-limits.md)

[ภาพรวมของลำดับหมายเลข](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
