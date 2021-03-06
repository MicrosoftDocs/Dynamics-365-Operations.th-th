---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent - Core HR (31 ตุลาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Talent - Core HR
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462723"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent - Core HR (31 ตุลาคม 2018)

**สร้าง 8.1.2031**

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR

## <a name="create-links-from-talent-to-finance"></a>สร้างลิงค์จาก Talent ไปยัง Finance
ฟังก์ชันการนำทางใหม่นี้ช่วยให้คุณสามารถเชื่อมโยงจาก Talent ไปยัง Finance โดยให้การนำทางโดยตรงไปยังหน้า Finance เมื่อมีการกำหนดค่าคอนฟิกลิงค์ คุณสามารถระบุชื่อและกลุ่มของลิงค์ ในตำแหน่งที่ลิงค์ควรแสดงใน Talent และหน้าเป้าหมายควรถูกเปิดภายใน Finance

#### <a name="coming-soon"></a>เร็วๆ นี้
บริบทของฟิลด์จะถูกเพิ่มในอนาคตเพื่ออนุญาตให้นำทางโดยตรงไปยังเรกคอร์ดที่สอดคล้องกันใน Finance ตัวอย่างเช่น คุณสามารถใช้ **ลิงค์ไปยังฟิลด์** เพื่อให้บริบทที่จะนำทางโดยตรงไปยังพนักงานหรือตำแหน่งเฉพาะใน Finance 

### <a name="configure-target-systems"></a>ตั้งค่าคอนฟิกระบบปลายทาง

ใน Talent ผู้ดูแลระบบสามารถกำหนดลิงค์ที่จะแสดงถึงพื้นที่ทำงานการดูแลระบบ ส่วนหนึ่งของการตั้งค่าคอนฟิกคือสภาพแวดล้อม Finance ที่คุณต้องการให้นำทางไปเป็น "เป้าหมาย" ของการเชื่อมโยง คุณดำเนินการนี้ได้โดยการตั้งชื่อระบบปลายทาง และใส่ URL ของสภาพแวดล้อม Finance นี่คือตัวอย่าง URL ของ Finance ที่คุณจะต้องระบุ: https://devax00124aos.cloud.test.dynamics.com/ หลังจากที่คุณตั้งค่าคอนฟิกระบบเป้าหมายของคุณ คุณสามารถกำหนดการเชื่อมโยงของคุณได้

### <a name="configure-links"></a>ตั้งค่าคอนฟิกลิงก์

การเชื่อมโยงแต่ละรายการที่สร้างขึ้นจะมีการกำหนดข้อมูลต่อไปนี้

- ลิงค์ - ชื่อของลิงค์ ที่ใช้สำหรับการระบุรหัสประจำตัวเท่านั้น

- เปิดใช้งานลิงค์นี้ - ตั้งค่าเป็น **ใช่** ถ้าคุณต้องการแสดงลิงค์ต่อผู้ใช้ของ Talent

- ชื่อที่แสดง - กำหนดชื่อที่จะปรากฏเป็นลิงค์ไปยัง Finance ในขณะนี้ ไม่มีการแปลข้อมูลนี้

- แสดงลิงค์บนฟอร์ม - เลือกหน้าที่คุณต้องการแสดงลิงค์

- กลุ่ม - ไม่จำเป็นต้องมีกลุ่ม แต่ถ้าคุณต้องการจัดระเบียบลิงค์ของคุณโดยใช้กลุ่ม เลือกกลุ่มที่มีอยู่ หรือสร้างใหม่โดยใช้ฟิลด์ **กลุ่ม**

- ระบบเป้าหมาย - เลือกระบบเป้าหมายที่สร้างโดยใช้ตัวเลือก **ตั้งค่าคอนฟิกระบบเป้าหมาย** นี่จะเป็นสภาพแวดล้อม Finance ที่จะใช้ เมื่อมีการนำทางโดยใช้การเชื่อมโยง

- ใช้บริษัทปัจจุบันของผู้ใช้ - เลือก **ใช่** ถ้าคุณต้องการใช้บริบทของบริษัทปัจจุบันของ User เมื่อนำทางไปยัง Finance ถ้าเลือก **ไม่** จากนั้นคุณจะสามารถเลือกบริษัทที่ควรใช้ได้

- รายการเมนูเป้าหมาย - ป้อนรายการเมนูจาก Finance ที่การเชื่อมโยงควรใช้ เมื่อมีการนำทาง รายการเมนูที่คุณนำทางโดยตรงไป จะพร้อมใช้งาน เพื่อค้นหารายการเมนูที่จำเป็น เปิด Finance และเปิดหน้าซึ่งเป็นเป้าหมายของการนำทาง คัดลอกรายการเมนูจาก URL ตัวอย่างเช่น ถ้าคุณต้องการให้การเชื่อมโยงนำคุณไปยังรายการพนักงานใน Finance and Operations ป้อนค่าที่ปรากฏหลังจาก "&mi" ใน URL https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees รายการเมนูที่จะนำทางไปยังหน้ารายการพนักงานในตัวอย่างนี้คือ: HcmWorkerListPage_Employees

- การเชื่อมโยงไปยังแหล่งข้อมูล - เลือกแหล่งที่มาของข้อมูลที่กำลังอ้างอิงการเชื่อมโยง แหล่งทั่วไปที่สุด เช่น **ผู้ปฏิบัติงาน** และ **ตำแหน่ง** จะพร้อมใช้งาน

- การเชื่อมโยงไปยังฟิลด์ - (เร็วๆ นี้) การเลือกฟิลด์นี้จะอนุญาตสำหรับการนำทางโดยตรงจากเรกคอร์ดเดียวใน Talent ไปยังเรกคอร์ดเดียวใน Finance

### <a name="access-to-links"></a>การเข้าถึงลิงค์

ผู้ดูแลระบบจะมองเห็นการเชื่อมโยงที่สร้างขึ้นใหม่บนหน้าที่กำหนด แม้ว่าตัวเลือก **เปิดใช้งานการเชื่อมโยงนี้** จะถูกตั้งค่าเป็น **ไม่** ซึ่งสามารถใช้ได้สำหรับการทดสอบการเชื่อมโยง ก่อนการแสดงให้กับพนักงานอื่น บทบาทอื่นๆ ทั้งหมดจะเห็นเฉพาะลิงค์ที่ตั้งค่าคอนฟิก หลังจากตัวเลือก **เปิดใช้งานการเชื่อมโยงนี้** ถูกตั้งค่าเป็น **ใช่** พนักงานที่มีการเข้าถึงไปยังหน้าที่ซึ่งการเชื่อมโยงจะปรากฏ จะมีการเข้าถึงไปยังการเชื่อมโยง

ผู้ใช้ยังสามารถมีสิทธิ์ความปลอดภัยภายใน Finance ที่กำหนดให้เข้าถึงหน้าใน Finance and Operations ถ้าไม่ จะปรากฏกล่องโต้ตอบความปลอดภัยเมื่อใช้การเชื่อมโยง


## <a name="other-changesfixes"></a>การเปลี่ยนแปลง/การแก้ไขอื่นๆ

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>ไม่สามารถกำหนดตำแหน่งที่มีวันที่เริ่มต้นในอนาคตให้กับพนักงานใหม่ได้

มีการทำการเปลี่ยนแปลงเพื่ออนุญาตให้มีการกำหนดพนักงานให้กับตำแหน่งที่เป็นวันที่ในอนาคต คุณสามารถเลือกตำแหน่งที่มีวันที่เริ่มต้นในอนาคต และจะมีการกำหนดพนักงานเมื่อมีการบันทึกหรือเสร็จสิ้นลำดับงาน (ถ้ามีการเปิดใช้งานลำดับงาน)

### <a name="new-employee-cannot-be-assigned-existing-position"></a>พนักงานใหม่ไม่สามารถถูกกำหนดตำแหน่งที่มีอยู่ได้

มีการทำการเปลี่ยนแปลง ดังนั้นจึงสามารถกำหนดการมอบหมายพนักงานใหม่ไปยังตำแหน่งที่มีอยู่ในขณะนี้ได้

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>ที่ตั้งสำนักงาน/วันอายุงาน จะหายไปเมื่อวันที่เริ่มต้นการจ้างงานอยู่ในอดีต และมีการบันทึกเรกคอร์ด

มีการทำการเปลี่ยนแปลงเพื่อแก้ไขการมองเห็นได้ของ **วันที่ของอายุงาน** และ **ที่ตั้งสำนักงาน** เมื่อบันทึกการเปลี่ยนแปลงสำหรับพนักงานในอดีต

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>ไม่สามารถป้อนข้อมูลสำหรับการจ้างงานที่เป็นวันที่ในอนาคตได้บนหน้าผู้ปฏิบัติงาน

ข้อมูลการจ้างงานสำหรับการจ้างงานที่เป็นวันที่ในอนาคตถูกระงับบนหน้าผู้ปฏิบัติงานหลัก คุณสามารถป้อนข้อมูลการจ้างงานผ่านทางหน้า **ตัวจัดการวันที่** ได้ จะสามารถทำการเปลี่ยนแปลงเพิ่มเติมได้ในการนำออกใช้ในอนาคต เพื่อเปิดใช้งานการป้อนข้อมูลการจ้างงานโดยตรงในระหว่างกระบวนการลำดับงาน

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>เพิ่ม ValidFrom และ ValidTo ไปยัง HcmPersonalContactPersonEntity

มีการอัพเดตเอนทิตี Data Management Framework (DMF) HcmPersonalContactPersonEntity เพื่อรวมวันที่ "มีผลบังคับใช้ตั้งแต่" และ "มีผลบังคับใช้จนถึง" เพื่อเปิดใช้งานสถานการณ์การรวมสวัสดิการบางรายการ 

## <a name="known-issue"></a>ปัญหาที่ทราบ
- **ปัญหา**: เมื่อเพิ่มสิ่งที่แนบมาใหม่กับผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** จะกลายเป็นสีเทา 
- **วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่าก FactBoxes บนหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน (ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)


[!INCLUDE[footer-include](../includes/footer-banner.md)]