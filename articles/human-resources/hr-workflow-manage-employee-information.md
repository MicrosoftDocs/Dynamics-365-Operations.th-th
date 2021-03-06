---
title: ใช้ลำดับงานเพื่อจัดการข้อมูลพนักงาน
description: บทความนี้อธิบายถึงวิธีการที่คุณสามารถใช้ความสามารถของลำดับงานสำหรับฝ่ายทรัพยากรบุคคลเพื่อจัดการข้อมูลพนักงาน ตัวอย่างเช่น คุณสามารถเชื่อมโยงลำดับงานกับตำแหน่งงาน และตั้งค่าคอนฟิกลำดับงานการอนุมัติที่เริ่มต้นเมื่อพนักงานเปลี่ยนบันทึกของพวกเขา
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c5bb0a363a3094626d81af3d5ffea38d9a1b12a8
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129814"
---
# <a name="use-workflows-to-manage-employee-information"></a>ใช้ลำดับงานเพื่อจัดการข้อมูลพนักงาน

บทความนี้อธิบายถึงวิธีการที่คุณสามารถใช้ความสามารถของลำดับงานสำหรับฝ่ายทรัพยากรบุคคลเพื่อจัดการข้อมูลพนักงาน ตัวอย่างเช่น คุณสามารถเชื่อมโยงลำดับงานกับตำแหน่งงาน และตั้งค่าคอนฟิกลำดับงานการอนุมัติที่เริ่มต้นเมื่อพนักงานเปลี่ยนบันทึกของพวกเขา

ความสามารถของลำดับงานสำหรับฝ่ายทรัพยากรบุคคลให้ลำดับงานจำนวนมากสำหรับการจัดการกิจกรรมของฝ่ายทรัพยากรบุคคล นอกจากนี้ ยังมีตัวเลือกจำนวนมากที่พร้อมใช้งานเพื่อให้คุณสามารถปรับเปลี่ยนลำดับงานที่เฉพาะเจาะจง และเชื่อมโยงกับลำดับชั้นการรายงาน ลำดับงานจะพร้อมใช้งานเพื่อช่วยในการจัดการการเปลี่ยนแปลงข้อมูลพนักงานชนิดมาตรฐานจำนวนมาก คุณสามารถเชื่อมโยงลำดับงานกับตำแหน่ง จากนั้น ถ้าพนักงานเปลี่ยนบันทึกพนักงานของตน ลำดับงานจะเริ่มต้นซึ่งต้องมีการอนุมัติก่อนที่จะบันทึกข้อมูลใหม่ ลำดับงานจะถูกกำหนดล่วงหน้าสำหรับชนิดของข้อมูลต่อไปนี้เพื่อช่วยคุณในการจัดการการเปลี่ยนแปลงได้อย่างมีประสิทธิภาพ และรักษาให้ข้อมูลของพนักงานของคุณถูกต้อง:

-   หมายเลขรหัส
-   หลักสูตร
-   การศึกษา
-   รูปภาพ
-   รายการที่ยืม
-   ประสบการณ์ทำงาน
-   ประสบการณ์โครงการ
-   ทักษะ
-   ตำแหน่งตัวแทนของบริษัท
-   การดำเนินการของฝ่ายทรัพยากรบุคคล
-   การลงทะเบียนหลักสูตร

เมื่อพนักงานได้รับการจ้างงาน โอนย้าย สิ้นสุดการจ้างงาน ลำดับงานอาจรวมถึงกระบวนการตรวจทาน ด้วยวิธีนี้ คุณสามารถแก้ไขเอกสารหรือกำหนดเงื่อนไขของการดำเนินการโดยเป็นส่วนหนึ่งของลำดับงาน เมื่อกระบวนการตรวจทานเสร็จสมบูรณ์ เอกสารหรือการดำเนินการจะเสร็จสมบูรณ์ และลำดับงานจะย้ายไปยังขั้นตอนการอนุมัติขั้นสุดท้าย

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>เชื่อมโยงลำดับงานกับลำดับชั้นของตำแหน่ง
คุณสามารถเชื่อมโยงลำดับงานกับลำดับชั้นใด ๆ ที่คุณตั้งค่าคอนฟิก ตัวอย่างเช่น ถ้าตำแหน่งถูกเชื่อมโยงกับลำดับชั้นการรายงานเมทริกซ์ คุณอาจตั้งค่าคอนฟิกลำดับงานที่ใช้ในค่าใช้จ่ายสำหรับโครงการที่เฉพาะเจาะจงไปยังลูกค้าเป้าหมายของโครงการแทนผู้จัดการของพนักงานที่เกี่ยวข้องกับตำแหน่งงานนั้น เมื่อต้องการสร้างลำดับงานใหม่หรือปรับเปลี่ยนลำดับงานที่มีอยู่ บนหน้า **ลำดับงานของฝ่ายทรัพยากรบุคคล** คลิก **สร้าง** เลือกลำดับงานในรายการเพื่อเริ่มการทำงานของโปรแกรมออกแบบลำดับงาน คุณสามารถใช้ตัวออกแบบในการสร้างลำดับงานใหม่หรือเปลี่ยนแปลงขั้นตอนในลำดับงานที่มีอยู่ เมื่อคุณเปลี่ยนลำดับงานที่มีอยู่ การเปลี่ยนแปลงของคุณจะถูกบันทึกเป็นเวอร์ชันใหม่ ดังนั้น คุณสามารถกลับไปยังเวอร์ชันก่อนหน้านี้ได้เสมอถ้าจำเป็น

## <a name="configure-a-human-resources-workflow"></a>ตั้งค่าคอนฟิกลำดับงานของฝ่ายทรัพยากรบุคคล
เมื่อต้องการตั้งค่าคอนฟิกลำดับงานพื้นฐานที่เริ่มต้นเมื่อพนักงานร้องขอการเปลี่ยนแปลงรหัสประจำตัวของพวกเขา ให้ทำตามขั้นตอนเหล่านี้

1.  ในหน้า **ลำดับงานของฝ่ายทรัพยากรบุคคล** คลิก **สร้าง**
2.  ในรายการของลำดับงานที่พร้อมใช้งาน เลือก **หมายเลขประจำตัว**
3.  คลิก **รัน** เพื่อเริ่มการทำงานของโปรแกรมออกแบบลำดับงาน และจากนั้น ป้อนชื่อผู้ใช้และรหัสผ่านของคุณเมื่อคุณได้รับพร้อมท์
4.  ลากองค์ประกอบ **อนุมัติหมายเลขรหัส** จากรายการขององค์ประกอบลำดับงานไปยังผืนผ้าใบโปรแกรมออกแบบ
5.  เชื่อมต่อองค์ประกอบการอนุมัติเพื่อ **เริ่มต้น** และ **สิ้นสุด**
6.  คลิกสองครั้งที่ **อนุมัติองค์ประกอบ** แล้วคลิกขวาและเลือก **คุณสมบัติ**
7.  ทำตามขั้นตอนเหล่านี้เพื่อเพิ่มคำแนะนำเกี่ยวกับรายการงาน:
    1.  เลือก **การกำหนด** และจากนั้นเลือก **ลำดับชั้น** ภายใต้ชนิดการกำหนด
    2.  ภายใต้การเลือก **ลำดับชั้น** เลือก **ลำดับชั้นที่ตั้งค่าคอนฟิกได้**
    3.  เพิ่มเงื่อนไขการหยุด และปิดหน้า

8.  ทำคำแนะนำเพิ่มเติมใดๆ ให้เสร็จสมบูรณ์ (ไม่ควรมีคำเตือนเพิ่มเติมใดๆ)
9.  คลิก **บันทึกและปิด** เรียกใช้ลำดับงานใหม่เมื่อกล่องโต้ตอบเปิดขึ้น และเลือก **เปิดใช้งาน**
10. ไปที่ **ทรัพยากรบุคคล** &gt; **ตำแหน่ง** &gt; **ชนิดลำดับชั้นของตำแหน่งงาน**
11. เลือก **เมทริกซ์**
12. เพิ่มลำดับงาน **หมายเลขรหัสผู้ปฏิบัติงาน** ลงในรายการ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ดูและจัดการการเปลี่ยนแปลงที่อยู่](hr-personnel-view-address-changes.md) 



