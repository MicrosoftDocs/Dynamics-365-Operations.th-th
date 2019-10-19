---
title: การรวม Attract กับ FAQ เกี่ยวกับ LinkedIn
description: หัวข้อนี้จะตอบคำถามที่คุณอาจพบเกี่ยวกับการรวมระหว่าง LinkedIn กับ Microsoft Microsoft Dynamics 365 Talent - Attract
author: hasrivas
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d66ebc01597f8038a38b46a9f1b70feaa5dc505e
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008650"
---
# <a name="linkedin-integration-faq"></a>FAQ เกี่ยวกับการรวม LinkedIn

[!include [banner](includes/banner.md)]

LinkedIn เป็นเครือข่ายมืออาชีพออนไลน์ที่ใหญ่ที่สุดในโลก Microsoft Dynamics Talent: Attract รวมกับ LinkedIn เพื่อให้คุณสามารถเข้าถึงผู้มีสามารถพิเศษระดับต้นของโลก Attract ช่วยให้คุณลงประกาศงานไปยัง LinkedIn โดยตรง และยังช่วยให้คุณสามารถดึงข้อมูลผู้สมัครจาก LinkedIn ไปยัง Attract

## <a name="for-recruiters-and-hiring-managers"></a>สำหรับผู้สรรหาบุคลากรและผู้จัดการที่ว่าจ้าง

ต่อไปนี้เป็นคำตอบของคำถามที่พบบ่อยเกี่ยวกับวิธีการใช้ Attract และ LinkedIn ร่วมกัน

### <a name="what-linkedin-features-do-i-get-with-attract"></a>คุณลักษณะใดของ LinkedIn ที่ฉันจะได้รับเมื่อใช้ Attract

การรวม Attract กับ LinkedIn ช่วยให้คุณสามารถดำเนินงานต่อไปนี้:

- [ลงประกาศงานไปยัง LinkedIn](./attract-post-jobs-to-linkedin.md) (เป็นรายการจำกัดฟรี)
- [ส่งออกข้อมูลผู้สมัครจาก LinkedIn ไปยัง Attract](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click)
- [อนุญาตให้ผู้สมัครสมัครงานของคุณกับ LinkedIn ได้](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract)

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>ฉันต้องทำอะไรก่อนบ้างจึงจะสามารถลงประกาศงานไปยัง LinkedIn ได้

ผู้ดูแลระบบต้อง [ตั้งค่าคอนฟิกการรวม LinkedIn ใน Attract](./attract-admin-linkedin.md#configure-job-posting-to-linkedin) หลังจากนั้น คุณก็จะพร้อมที่จะเริ่มต้นแล้ว

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>ฉันจะลงประกาศงานใน LinkedIn จาก Attract อย่างไร

หลังจากที่คุณสร้างงานใน Attract แล้ว คุณต้องเลือกปุ่ม **โพสต์เดี๋ยวนี้** ที่สอดคล้องกับ LinkedIn สำหรับข้อมูลเพิ่มเติมให้ ดูที่ [การลงประกาศงานไปยัง LinkedIn จาก Attract](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin)

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>ฉันสามารถรับข้อมูลผู้สมัครจาก LinkedIn ไปยัง Attract ได้หรือไม่

ใช่ หากคุณเห็นผู้สมัครที่ดีบน LinkedIn คุณสามารถส่งออกข้อมูลของผู้สมัครนั้นไปยัง Attract ได้อย่างง่ายดาย สำหรับข้อมูลเพิ่มเติม ดูที่ [จัดหาผู้สมัครด้วย LinkedIn Recruiter](attract-linkedin-recruiter.md)

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>ฉันจะรับความช่วยเหลือในการเข้าถึง LinkedIn จาก Attract ได้อย่างไร

ถ้าคุณมีปัญหาในการลงชื่อเข้าใช้หรือลงประกาศงานใน LinkedIn จาก Atrract ดูที่ [การแก้ไขปัญหาการรวมกับ LinkedIn](./attract-troubleshoot-linkedin.md)

สำหรับปัญหาอื่นๆ เกี่ยวกับ Attract ดูที่ [ขอความช่วยเหลือสำหรับความสามารถพิเศษ](./talent-support.md) สำหรับความช่วยเหลือเกี่ยวกับ LinkedIn โปรดดูที่ [หน้าสนับสนุน LinkedIn](https://www.linkedin.com/help)

## <a name="for-admins-and-developers"></a>สำหรับผู้ดูแลระบบและนักพัฒนา

ต่อไปนี้เป็นคำตอบของคำถามที่พบบ่อยเกี่ยวกับวิธีการตั้งค่าคอนฟิกการรวมระหว่าง Attract และ LinkedIn

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>ฉันจะตั้งค่าคอนฟิก Attract เพื่อให้ผู้สรรหาบุคลากรและผู้จัดการที่ว่าจ้างลงประกาศงานไปยัง LinkedIn ได้อย่างไร

คุณสามารถตั้งค่าคอนฟิกตัวเลือก**ที่พร้อม**ใช้งานบนแท็บการรวม LinkedIn ในศูนย์ดูแล สำหรับข้อมูลเพิ่มเติม ดูที่ [การตั้งค่าการรวมกับ LinkedIn](./attract-admin-linkedin.md)

### <a name="can-i-export-candidate-information-from-linkedin"></a>ฉันสามารถส่งออกข้อมูลผู้สมัครจาก LinkedIn ได้หรือไม่

ได้ แต่คุณต้องตั้งค่าคอนฟิกการรวมกับ LinkedIn Recruiter ก่อน สำหรับข้อมูลเพิ่มเติม ดูที่ [การตั้งค่าการรวมกับ LinkedIn](./attract-admin-linkedin.md)

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>ฉันสามารถลงประกาศงานไปยังช่องงานพิเศษบน LinkedIn ได้อย่างไร?

แม้ว่า Attract จะให้โซลูชันที่มีประสิทธิภาพสำหรับการลงประกาศงานไปยัง LinkedIn แต่คุณอาจพบว่าคุณต้องการความยืดหยุ่นเพิ่มเติม ตัวอย่างเช่น คุณอาจต้องการให้สามารถลงประกาศช่องงานพิเศษนอกเหนือจากรายการที่จำกัดไว้ฟรี หรือคุณอาจต้องการให้ LinkedIn ประมวลผลการลงประกาศชุดงานของคุณมากกว่าหนึ่งครั้งต่อวัน

#### <a name="types-of-linkedin-job-posts"></a>ชนิดของการลงประกาศงานบน LinkedIn

LinkedIn มีการลงประกาศงานชนิดต่อไปนี้:

- **การแสดงรายการที่จำกัด** – การลงประกาศงานฟรีที่ปรากฏขึ้นในผลการค้นหาเมื่อผู้สมัครทำการค้นหางานบน linkedIn และบนหน้า LinkedIn ของบริษัท การแสดงรายการที่จำกัดมีการกำหนดเป้าหมายไปยังผู้ที่กำลังหางานอยู่ ชนิดของรายการนี้คือชนิดที่ Attract ให้กับ LinkedIn คุณไม่สามารถส่งเสริมรายการงานที่จำกัดบน LinkedIn ถ้าคุณต้องการส่งเสริมการแสดงรายการที่จำกัด คุณต้องทำงานกับ LinkedIn เพื่อเปิดใช้งาน Job Wrapping สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Job Wrapping ให้ดูที่ [การแสดงรายการที่จำกัดเทียบกับช่องงานพิเศษสำหรับ Job Wrapping](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) และ [Job Wrapping Plus - FAQs](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)
- **ช่องงานพิเศษ**– การลงประกาศที่ซื้อซึ่งจะปรากฏไปทั่วทั้ง LinkedIn เช่น หน้าฟีด LinkedIn อีเมล และพื้นที่ **งานที่คุณอาจสนใจ** ช่องงานพิเศษมีการกำหนดเป้าหมายให้กับผู้สมัครที่ไม่ได้กำลังหางาน แต่จะปรากฏในการค้นหางานด้วย

ลงประกาศงานจาก Attract ไปยัง LinkedIn เป็นรายการจำกัดฟรี ถ้าคุณต้องการใช้ช่องงานพิเศษ คุณต้องใช้ Job Wrapping ผ่าน LinkedIn Recruiter Job Wrapping ต้องใช้สัญญา Job Wrapping กับ LinkedIn สำหรับข้อมูลเพิ่มเติม ดูที่ [Job Wrapping ผ่าน LinkedIn Recruiter - ภาพรวม](https://www.linkedin.com/help/recruiter/answer/79037)

#### <a name="frequency-of-batch-processing-on-linkedin"></a>ความถี่ของการประมวลผลชุดงานบน LinkedIn

LinkedIn ประมวลผลประกาศงานในชุดงานผ่าน Attract หนึ่งครั้งต่อวัน ดังนั้นจึงสามารถใช้เวลาไม่เกิน 48 ชั่วโมง สำหรับงานที่จะปรากฏบน LinkedIn หลังจากที่มีการลงประกาศผ่าน Attract แล้ว ถ้าคุณต้องการให้งานปรากฎใน LinkedIn เร็วขึ้น หรือถ้าคุณต้องการความยืดหยุ่นเพิ่มเติม คุณสามารถใช้ Application Programming Interface (API) สำหรับ Recruiter System จาก LinkedIn สำหรับข้อมูลเพิ่มเติม ดูที่ [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect)

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>ตารางของตัวเลือกสำหรับการลงประกาศงานไปยัง LinkedIn

ตารางต่อไปนี้จะให้คำอธิบายเกี่ยวกับตัวเลือกต่างๆ สำหรับการลงประกาศงานไปยัง LinkedIn ซึ่งรวมถึงข้อดีของตัวเลือกแต่ละรายการและข้อมูลเพิ่มเติม

|  | ดึงดูด | Job Wrapping ผ่าน LinkedIn Recruiter | API การเชื่อมต่อระบบผู้สรรหา |
|---|---|---|---|
| **คำอธิบาย** | ลงประกาศงานจาก Attract ไปยัง LinkedIn เป็นแบบฟีด XML | บริษัททำสัญญากับ LinkedIn และแสดฟีด XML สำหรับการลงประกาศงาน | ลูกค้าใช้ API เพื่อซิงค์ข้อมูลระหว่าง Attract และ LinkedIn Recruiter |
| **ฉันสามารถลงประกาศงานประเภทใดได้บ้าง?** | รายการที่จำกัด | ช่องงานพิเศษหรือรายการที่จำกัด | รายการที่จำกัด |
| **ฉันจะส่งเสริมงานบน LinkedIn ได้หรือไม่** | ไม่ | ช่องงานพิเศษ: ใช่<br>รายการที่จำกัด: ไม่ | ไม่ |
| **LinkedIn ลงประกาศงานบ่อยแค่ไหน** | วันละครั้ง | วันละครั้ง | หลายครั้งต่อวันตามที่กำหนดโดย API |
| **แนะนำโดย LinkedIn หรือไม่** | ไม่ | ใช่ | ไม่ |
| **ฉันควรต้องการอะไรบ้าง** | การซื้อ Attract | สัญญา Job Wrapping กับ LinkedIn และการซื้อช่องงานพิเศษ | ข้อตกลง API กับ LinkedIn | 
| **ฉันจะหาข้อมูลเพิ่มเติมได้ที่ไหน** | [ตั้งค่าการรวมกับ LinkedIn](./attract-admin-linkedin.md) | [Job Wrapping ผ่าน LinkedIn Recruiter - ภาพรวม](https://www.linkedin.com/help/recruiter/answer/79037) | [การเชื่อมต่อระบบผู้สรรหา](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> คุณไม่จำเป็นต้องใช้ใบอนุญาต LinkedIn Recruiter System Connect ในการลงประกาศงานไปยัง LinkedIn ด้วย Attract

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ตั้งค่าการรวมกับ LinkedIn](./attract-admin-linkedin.md)

[ลงประกาศงานใน LinkedIn จาก Attract](./attract-post-jobs-to-linkedin.md)

[จัดหาผู้สมัครด้วย LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[แก้ไขปัญหาการรวมกับ LinkedIn](./attract-troubleshoot-linkedin.md)
