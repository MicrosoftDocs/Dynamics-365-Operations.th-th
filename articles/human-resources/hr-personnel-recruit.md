---
title: สรรหาผู้สมัครงาน
description: บทความนี้อธิบายวิธีการสรรหาผู้สมัคร ใน Dynamics 365 Human Resources
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 743c78d3526db2707630229d4cf21531f9641dd6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879263"
---
# <a name="recruit-job-candidates"></a>สรรหาผู้สมัครงาน


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources ช่วยคุณในการจัดการคำขอสรรหาบุคลากร นอกจากนี้ยังช่วยให้คุณสามารถเปลี่ยนผู้สมัครงานเป็นพนักงานได้อย่างราบรื่น ถ้าองค์กรของคุณใช้แอปพลิเคชันการสรรหาบุคลากรที่แยกต่างหาก กระบวนการสรรหาบุคลากรของคุณอาจประกอบด้วยขั้นตอนต่อไปนี้:<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- ป้อนคำขอสรรหาบุคลากรของคุณในทรัพยากรบุคคล
- รับการอ้างอิงของผู้สมัครในทรัพยากรบุคคลจากแอปพลิเคชันการสรรหาบุคลากร
- ดำเนินการขั้นตอนการอนุมัติของผู้สมัครในทรัพยากรบุคคลให้เสร็จสมบูรณ์

ถ้าคุณไม่ได้ใช้แอปพลิเคชันการสรรหาบุคลากรที่แยกต่างหาก คุณยังสามารถจัดการผู้สมัครในทรัพยากรบุคคลด้วยตนเองได้ด้วย

> [!NOTE]
> ถ้าคุณเป็นผู้ดูแลระบบหรือนักพัฒนาและต้องการรวมทรัพยากรบุคคลกับแอปพลิเคชันการสรรหาบุคลากรที่สาม ไปที่ [ตั้งค่าคอนฟิกการรวม Dataverse](hr-admin-integration-common-data-service.md) และ [ตั้งค่าคอนฟิกตารางเสมือน Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)
>
> นอกจากนี้ คุณยังสามารถพบแอปการรวมการสรรหาบุคลากรใน [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) ได้ด้วย
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>เปิดใช้งานคำขอการสรรหาบุคลากรบนโครงสร้างพื้นฐานที่รวม

ถ้าคุณต้องการส่งคำขอการสรรหาบุคลากรในการสรรหาบุคลากร คุณต้องเปิดใช้งาน **ประสบการณ์ผู้ใช้ด้าน HR** และคุณลักษณะ **การจัดการกระบวนการสรรหาบุคลากร** ก่อน

เมื่อเปิดคุณลักษณะแล้ว ให้เลือกฟังก์ชันที่มีขั้นตอนต่อไปนี้ 
1. ไปที่ **ทรัพยากรบุคคล** > **การตั้งค่า** > **พารามิเตอร์ทรัพยากรบุคคล**
2. บนแท็บ  **การสรรหาบุคลากร** ให้ตั้งค่าฟิลด์ **เปิดใช้งานการสรรหาบุคลากร** เป็น **ใช่**
3. ในรายการดรอปดาวน์ **ประสบการณ์การสรรหาบุคลากร** เลือก **การสรรหาบุคลากรของ HR**  
4. คลิก **บันทึก** 

> [!Note] 
> เมื่อเลือก **การสรรหาบุคลากรของ HR** **โครงการสรรหาบุคลากร** (ดั้งเดิม) จะไม่พร้อมใช้งาน 


## <a name="add-a-recruiting-request-location"></a>เพิ่มสถานที่ร้องขอการสรรหาบุคลากร

ถ้าองค์กรของคุณมีหลายสถานที่ คุณสามารถเพิ่มได้เพื่อให้ผู้ขอสามารถเลือกสถานที่ที่จะทำงานของการสรรหาใหม่ สถานที่จะถูกรวมอยู่ในการโพสต์งาน

1. ในแถบค้นหา ให้ป้อน **สถานที่ร้องขอการสรรหาบุคลากร**
2. เลือก **ใหม่**
3. ในฟิลด์ **สถานที่ร้องขอการสรรหาบุคลากร** ให้ป้อนชื่อสถานที่

    ![เพิ่มสถานที่ร้องขอการสรรหาบุคลากร](./media/hr-recruit-0a-add-location.png)

4. สำหรับ **คำอธิบาย** ให้ป้อนคำอธิบายสำหรับสถานที่
5. ภายใต้ **สถานที่** เลือก **เพิ่ม** ถ้ากลอ่งโต้ตอบ **ที่อยู่ใหม่** ปรากฏขึ้น ให้ป้อนที่อยู่ของสถานที่<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![ป้อนที่อยู่](./media/hr-recruit-0b-address.png)

6. ภายใต้ **ข้อมูลผู้ติดต่อ** ให้ป้อนข้อมูลสำหรับผู้ติดต่อของสถานที่
7. เลือก **บันทึก**

## <a name="add-a-recruiting-request"></a>เพิ่มคำขอการสรรหาบุคลากร

ผู้จัดการสามารถส่งคำขอการสรรหาบุคลากรในทรัพยากรบุคคล ถ้าคุณใช้แอปพลิเคชันการสรรหาบุคลากรที่แยกต่างหาก การทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์จะส่งคำขอการสรรหาบุคลากรและเริ่มต้นกระบวนการสรรหาบุคลากรในแอปพลิเคชันดังกล่าว หรือให้ทำกระบวนงานนี้ให้เสร็จสมบูรณ์เพื่อเริ่มต้นลำดับงานสำหรับกระบวนการสรรหาบุคลากรภายในของคุณเอง

1. เลือก **ระบบบริการตนเองของพนักงาน**
2. เลือกแท็บ **ทีมงานของฉัน**
3. เลือก **คำขอเพื่อสรรหา**

    ![เริ่มต้นคำขอการสรรหาบุคลากร](./media/hr-recruit-1-request-to-recruit.png)

4. กรอกข้อมูลในฟิลด์ **คำอธิบาย** **งาน** และ **วันที่เริ่มต้นโดยประมาณ**

    ![ดำเนินการคำขอสรรหาบุคลากรให้เสร็จสมบูรณ์](./media/hr-recruit-2-request-to-recruit.png)

5. เลือก **ดำเนินการต่อ** คำขอการสรรหาบุคลากรสำหรับตำแหน่งของคุณจะปรากฏขึ้น
6. ภายใต้ **ทั่วไป** ให้เลือกผู้สรรหาจากรายการดรอปดาวน์ **ผู้สรรหา** และจากนั้น เลือกสถานที่จากรายการดรอปดาวน์ **สถานที่ร้องขอการสรรหาบุคลากร**
7. ภายใต้ **งาน** ให้เปลี่ยนข้อมูลใดๆ ตามความจำเป็น แล้วจากนั้น เลือก **สร้างรายละเอียดจากงาน**

    ![สร้างรายละเอียดจากงาน](./media/hr-recruit-3-create-details-from-job.png)

    ส่วนที่เหลือของคำขอการสรรหาบุคลากรจะเติมด้วยข้อมูลเริ่มต้นสำหรับงานที่คุณป้อน

8. ภายใต้ **คำอธิบายภายนอก** ให้ป้อนคำอธิบายงานที่เชื่อมต่อกับภายนอก
9. ภายใต้ **ตำแหน่ง** ให้เลือก **เพิ่ม** แล้วจากนั้น เลือกตำแหน่งสำหรับคำขอการสรรหาบุคลากรนี้<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![เพิ่มตำแหน่งงาน](./media/hr-recruit-4-select-position.png)

10. ภายใต้ **ทักษะ** ให้เลือก **เพิ่ม** แล้วจากนั้น เลือกทักษะ
11. ภายใต้ **ข้อกำหนดด้านการศึกษา** ให้เลือก **เพิ่ม** แล้วจากนั้น เลือกค่าจากเมนูดรอปดาวน์ **การศึกษา** และ **ระดับของการศึกษา**

    ![เพิ่มข้อกำหนดด้านการศึกษา](./media/hr-recruit-5-select-educational-requirements.png)

12. ภายใต้ **ข้อคิดเห็น** ให้เพิ่มข้อคิดเห็นตามความจำเป็น
13. ภายใต้ **ค่าตอบแทน** เลือกระดับจากรายการดรอปดาวน์ **ระดับ** แล้วจากนั้น ปรับ **ขีดจำกัดต่ำสุด** **จุดควบคุม** และ **ขีดจำกัดสูงสุด** ตามความจำเป็น
14. เมื่อคำขอการสรรหาบุคลากรของคุณเสร็จสมบูรณ์แล้ว และคุณพร้อมที่จะเริ่มกระบวนการสรรหาบุคลากร ให้เลือก **เรียกใช้งาน** ในแถบเมนู

    ![เรียกใช้คำขอการสรรหาบุคลากร](./media/hr-recruit-6-activate-recruit-request.png)

15. เลือก **บันทึก**

## <a name="view-and-edit-your-recruiting-requests"></a>ดูและแก้ไขคำขอการสรรหาบุคลากรของคุณ

ถ้าคุณเป็นผู้จัดการและต้องการดูคำขอของคุณเอง:

1. เลือก **ระบบบริการตนเองของพนักงาน**
2. เลือกแท็บ **ทีมงานของฉัน**
3. ภายใต้ **ข้อมูลทีมงานของฉัน** ให้เลือกแท็บ **คำขอการสรรหาบุคลากร**

    ![เลือกแท็บคำขอการสรรหาบุคลากร](./media/hr-recruit-7-recruiting-requests.png)

4. ถ้าต้องการดูหรือแก้ไขคำขอการสรรหาบุคลากร ให้เลือกในกริด

ถ้าคุณเป็นผู้เชี่ยวชาญด้าน HR หรือต้องการดูคำขอการสรรหาทั้งหมด:

1. เลือก **การจัดการบุคลากร**
2. เลือก **คำขอการสรรหาบุคลากร**

    ![ดูคำขอการสรรหาบุคลากรในการจัดการบุคลากร](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. ถ้าต้องการดูหรือแก้ไขคำขอการสรรหาบุคลากร ให้เลือกในกริด

## <a name="add-or-edit-a-candidate-profile"></a>เพิ่มหรือแก้ไขโพรไฟล์ผู้สมัคร

ถ้าองค์กรของคุณได้รวมกับแอปพลิเคชันอื่นเพื่อจัดการคำขอการสรรหาบุคลากร คำขอการสรรหาบุคลากรจะถูกส่งต่อไปยังแอปพลิเคชันนั้น แอปพลิเคชันการสรรหาบุคลากรส่งข้อมูลผู้สมัครกลับไปยังทรัพยากรบุคคล มิฉะนั้น คุณสามารถปฏิบัติตามกระบวนการสรรหาบุคลากรภายในของตนเอง และป้อนข้อมูลผู้สมัครด้วยตนเอง

1. เลือก **การจัดการบุคลากร**
2. เลือก **ลิงก์**
3. ภายใต้ **การสรรหาบุคลากร** ให้เลือก **ผู้สมัคร**

    ![ดูผู้สมัคร](./media/hr-recruit-9-candidates.png)

4. เมื่อต้องการเพิ่มผู้สมัคร ให้เลือก **สร้าง** ถ้าต้องการแก้ไขผู้สมัครที่มีอยู่ ให้เลือกผู้สมัครจากรายการ และจากนั้นเลือก **แก้ไข** โพรไฟล์ผู้สมัครจะปรากฏขึ้น
5. ภายใต้ **สรุปผู้สมัคร** ป้อนหรือแก้ไขข้อมูลผู้สมัครตามความจำเป็น
6. ภายใต้ **คำขอการสรรหาบุคลากร** ให้เลือกคำขอการสรรหาบุคลากรเพื่อลิงค์กับผู้สมัคร จากนั้นให้กรอกฟิลด์ **วันที่เริ่มต้นโดยประมาณ** **การว่าจ้างผู้จัดการ** **ตำแหน่ง** และ **คำอธิบาย** ตามความเหมาะสม

    ![ลิงค์กับคำขอการสรรหาบุคลากร](./media/hr-recruit-10-link-to-recruiting-request.png)

7. กรอกข้อมูลทั้งหมดในพื้นที่ต่อไปนี้ที่คุณต้องการรวมไว้ในเรกคอร์ดของผู้สมัคร:

    - **ข้อคิดเห็น**
    - **ประสบการณ์การทำงาน**
    - **ข้อมูลการติดต่อ**
    - **การศึกษา**
    - **ทักษะ**
    - **ใบรับรอง**
    - **การคัดเลือก**

8. เลือก **บันทึก**

## <a name="hire-a-candidate"></a>จ้างงานผู้สมัคร

เมื่อคุณพร้อมที่จะจ้างงานผู้สมัคร ให้ทำตามกระบวนงานนี้เพื่อเปลี่ยนผู้สมัครเป็นพนักงาน

1. บนหน้า **ผู้สมัคร** ให้เลือก **จ้าง**

    ![จ้างงานผู้สมัคร](./media/hr-recruit-11-hire.png)

2. บนหน้า **จ้างผู้ปฏิบัติงานใหม่** ภายใต้ **รายละเอียด** ให้กรอกข้อมูลในฟิลด์ทั้งหมด

    ![ป้อนรายละเอียดการจ้างงานใหม่](./media/hr-recruit-12-hire-new-worker.png)

3. ภายใต้ **รายละเอียดตำแหน่ง** ให้ตรวจสอบและเปลี่ยนข้อมูลตามความจำเป็น
4. ภายใต้ **รายการตรวจสอบการเตรียมความพร้อม** เลือกรายการตรวจสอบการเตรียมความพร้อมที่เกี่ยวข้องสำหรับพนักงานนี้
5. เลือก **ดำเนินการต่อ** เพื่อสร้างเรกคอร์ดพนักงาน

    > [!NOTE]
    > โดยขึ้นอยู่กับลำดับงานขององค์กรของคุณ เรกคอร์ดผู้สมัครอาจมีขั้นตอนการอนุมัติเพิ่มเติม ก่อนที่จะกลายเป็นเรกคอร์ดพนักงาน

## <a name="decide-not-to-hire-a-candidate"></a>ตัดสินใจที่จะไม่จ้างผู้สมัคร

ถ้าคุณเลือกที่จะไม่จ้างผู้สมัคร ให้ทำตามกระบวนงานนี้เพื่อลบออกจากกระบวนการตรวจสอบ 

1. บนหน้า **ผู้สมัคร** ให้เลือก **ไม่จ้าง**

    ![ไม่จ้างงานผู้สมัคร](./media/hr-recruit-13-do-not-hire.png)

2. เลือก **รหัสเหตุผล** และรวมข้อคิดเห็นใดๆ
3. เลือก **ตกลง**

## <a name="dismiss-a-candidate"></a>ยกเลิกผู้สมัคร

ถ้าจำเป็น คุณสามารถยกเลิกผู้สมัครได้หลังจากจ้างงานแล้ว ตัวอย่างเช่น ผู้สมัครอาจปฏิเสธข้อเสนอของคุณ หรือไม่แสดงตัวในวันแรกของพวกเขา

- บนหน้า **ผู้สมัคร** ให้เลือก **ยกเลิกผู้สมัคร**

    ![ยกเลิกผู้สมัคร](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ตั้งค่าคอนฟิกตารางเสมือน Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[จัดระเบียบบุคลากรของคุณ](hr-personnel-departments-jobs-positions.md)<br>
[ตั้งค่าส่วนประกอบของงาน](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
