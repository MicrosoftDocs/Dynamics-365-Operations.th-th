---
title: แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams
description: หัวข้อนี้ครอบคลุมวิธีการแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Dynamics 365 Commerce ถ้าองค์กรของคุณสร้างทีมงานไว้แล้วใน Microsoft Teams ก่อนการรวม Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3edd176788b24a5f5246e9b7bcb3c6fbcdca2254
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842753"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

หัวข้อนี้ครอบคลุมวิธีการแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Dynamics 365 Commerce ถ้าองค์กรของคุณสร้างทีมงานไว้แล้วใน Microsoft Teams ก่อนการรวม Commerce

องค์กรของคุณอาจสร้างทีมงานให้กับร้านค้าของคุณบางส่วนหรือทั้งหมดก่อนที่จะรวม Dynamics 365 Commerce และ Microsoft Teams ในกรณีนี้ ให้สร้างการซิงโครไนส์งานระหว่าง Commerce POS และ Microsoft Teams คุณต้องระบุการแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Commerce

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>แม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Commerce 

หากต้องการแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการระบบ \> พื้นที่ทำงาน \> การจัดการข้อมูล**
1. เลือก **ส่งออก** 
1. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
1. ภายใต้ **ชื่อกลุ่ม** ให้ป้อน "การแม็ป Teams ส่งออก"
1. ในแท็บด่วน **เอนทิตีที่เลือก** ให้เลือก **เพิ่มเอนทิตี** กล่องโต้ตอบ **เพิ่มเอนทิตี** จะปรากฏขึ้น  
1. ในรายการแบบหล่นลงของ **ชื่อเอนทิตี** ให้เลือก **การแม็ป Teams ระหว่างต้นทางและทีมงาน**
1. ในรายการแบบหล่นลงของ **รูปแบบข้อมูลเป้าหมาย** ให้เลือก **CSV**
1. เลือก **เพิ่ม** แล้วเลือก **ปิด**
1. ที่ด้านบนซ้ายภายใต้บานหน้าต่างการกิจกรรม ให้เลือก **ส่งออกทันที**
1. ภายใต้ **สถานะการประมวลผลเอนทิตี** ให้เลือก **ดาวน์โหลดไฟล์**
1. ในไฟล์ CSV ที่ส่งออก ให้ป้อนค่าให้กับ **SOURCETYPE** **SOURCEID** และ **TEAMID** ดังนี้:
    - เช่น **SOURCETYPE** ป้อน "RetailStore" 
    - ตัวอย่างเช่น **SOURCEID** ป้อนหมายเลขร้านค้า (ตัวอย่างเช่น "000135" สำหรับร้านค้าซานฟรานซิสโก) คุณสามารถค้นหาหมายเลขร้านค้าที่ **Retail และ Commerce \> ช่องทาง \> ร้านค้า**
    - เพื่อ **TEAMID** ให้ป้อนรหัสทีมงานที่เกี่ยวข้องจาก Microsoft Teams (ตัวอย่างเช่น "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c") คุณสามารถค้นหาข้อมูลรหัสทีมงานที่ [admin.teams.microsoft.com](https://admin.teams.microsoft.com) ได้
1. บันทึกไฟล์ CSV ลงในเครื่องคอมพิวเตอร์ของคุณ
1. ไปที่ **การจัดการระบบ \> พื้นที่ทำงาน \> การจัดการข้อมูล** และจากนั้นเลือก **ส่งออก**
1. ในแท็บด่วน **เอนทิตีที่เลือก** ให้เลือก **เพิ่มไฟล์** กล่องโต้ตอบ **เพิ่มไฟล์** จะปรากฏขึ้น
1. ในรายการแบบหล่นลงของ **ชื่อเอนทิตี** ให้เลือก **การแม็ป Teams ระหว่างต้นทางและทีมงาน**
1. ในรายการแบบหล่นลงของ **รูปแบบข้อมูลต้นทาง** ให้เลือก **CSV**
1. เลือก **อัพโหลดและเพิ่ม** เลือกไฟล์ CSV ที่คุณบันทึกก่อนหน้านี้ แล้วเลือก **เปิด**
1. ในกล่องโต้ตอบ **เพิ่มไฟล์** ให้เลือก **ปิด**
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **บันทึก** แล้วจากนั้น เลือก **นำเข้า**

รูปภาพตัวอย่างต่อไปนี้จะแสดงกลุ่ม **การแม็ปทีมงานส่งออก** ใน Commerce ที่มีองค์ประกอบ **เพิ่มเอนทิตี** และส่วนหัวของไฟล์ CSV ที่ส่งออกถูกเน้น

![การแม็ปทีมงานส่งออก ใน Commerce ที่มีองค์ประกอบเพิ่มเอนทิตี และส่วนหัวของไฟล์ CSV ที่ส่งออกถูกเน้น](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> หลังจากที่คุณปฏิบัติตามขั้นตอนต่างๆ ที่เตรียมการล่วงหน้าแล้ว ให้ปฏิบัติตามขั้นตอนต่างๆ ใน [การซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams กับ POS](synchronize-tasks-teams-pos.md) เพื่อซิงโครไนส์การจัดการงาน 

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams](commerce-teams-integration.md)

[เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams](enable-teams-integration.md)

[สํารอง Microsoft Teams จาก Dynamics 365 Commerce](provision-teams-from-commerce.md)

[ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[จัดการบทบาทผู้ใช้ใน Microsoft Teams](manage-user-roles-teams.md)

[คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams](teams-integration-faq.md)
