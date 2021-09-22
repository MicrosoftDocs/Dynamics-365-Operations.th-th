---
title: จํากัดการแก้ไขข้อมูลส่วนบุคคล
description: จํากัดพนักงานจากการแก้ไขรายละเอียดผู้ติดต่อใน Dynamics 365 Human Resources
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c4a13818103434df5005ad2805ac2ea7495bb767
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431424"
---
# <a name="restrict-editing-of-personal-information"></a>จํากัดการแก้ไขข้อมูลส่วนบุคคล

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

หัวข้อนี้อธิบายวิธีการจํากัดพนักงานจากการแก้ไขรายละเอียดผู้ติดต่อใน Dynamics 365 Human Resources คุณอาจต้องการป้องกันไม่ให้พนักงานแก้ไขรายละเอียดผู้ติดต่อบางอย่าง เช่น ที่ตั้งธุรกิจหรือที่อยู่อีเมลของพนักงาน

> [!NOTE]
> การใช้คุณลักษณะนี้ ก่อนอื่นคุณต้องเปิดใช้งาน **(พรีวิว) จํากัดพนักงานจากการเพิ่มหรือแก้ไขที่อยู่และข้อมูลผู้ติดต่อ เพื่อเลือกวัตถุประสงค์** ในการจัดการคุณลักษณะ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะรุ่นพรีวิว ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)<br><br>![เปิดใช้งานคุณลักษณะการแสดงตัวอย่าง](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>เลือกข้อมูลที่พนักงานสามารถเพิ่มหรือแก้ไขได้

1. ในทรัพยากรบุคคล ให้เลือก **การจัดการบุคลากร** เลือก **ลิงค์** แล้วจากนั้น เลือก **พารามิเตอร์ทรัพยากรบุคคล**

   ![ไปที่พารามิเตอร์ทรัพยากรบุคคล](./media/hr-employee-self-service-human-resources-parameters.png)

2. บนหน้า **พารามิเตอร์ทรัพยากรบุคคล** ให้เลือกแท็บ **ระบบบริการตนเองของพนักงาน**

   ![เลือก ระบบบริการตนเองของพนักงาน](./media/hr-employee-self-service-tab.png)

3. บนแท็บ **ระบบบริการตนเองของพนักงาน** ให้ยกเลิกการเลือกข้อมูลทั้งหมดในส่วน **ที่อยู่และข้อมูลการติดต่อ** ที่คุณไม่ต้องการให้พนักงานเพิ่มหรือแก้ไข ในตัวอย่างนี้ เราได้ยกเลิกการเลือกข้อมูลการติดต่อ **ธุรกิจ**

   ![จํากัดการแก้ไขข้อมูลการติดต่อทางธุรกิจ](./media/hr-employee-self-service-restrict-business.png)

4. เลือก **บันทึก**

   ![บันทึกการเปลี่ยนแปลง](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>ประสบการณ์พนักงาน

หลังจากที่คุณได้จำกัดพนักงานจากการเพิ่มหรือแก้ไขรายละเอียดผู้ติดต่อแล้ว พนักงานสามารถดูข้อมูลได้ แต่ไม่สามารถเปลี่ยนแปลงได้

ในตัวอย่างนี้ พนักงานที่ถูกจำกัดจากการแก้ไขรายละเอียดผู้ติดต่อ **ธุรกิจ** พนักงานยังคงสามารถดูข้อมูลใน **ระบบบริการตนเองของพนักงาน**:

![ดูรายละเอียดผู้ติดต่อทางธุรกิจ](./media/hr-employee-self-service-restrict-view.png)

อย่างไรก็ตาม เมื่อเลือกรายละเอียดผู้ติดต่อทางธุรกิจ บานหน้าต่าง **แก้ไขที่อยู่** จะปรากฏเป็นแบบอ่านอย่างเดียว และไม่สามารถเปลี่ยนแปลงฟิลด์ใดๆ ได้

![การแสดงรายละเอียดผู้ติดต่อทางธุรกิจเป็นแบบอ่านอย่างเดียว](./media/hr-employee-self-service-restrict-read-only.png)

นอกจากนี้ หากลูกค้าเลือก **เพิ่ม** เพื่อเพิ่มที่อยู่ใหม่ พวกเขาจะไม่สามารถเลือก **ธุรกิจ** จากกล่องรายการแบบหล่นลง **วัตถุประสงค์**

![พนักงานไม่สามารถเพิ่มที่อยู่ทางธุรกิจ](./media/hr-employee-self-service-restrict-add.png)

พนักงานได้รับประสบการณ์ที่เหมือนกัน เมื่อพวกเขาเลือก **รายละเอียดผู้ติดต่อ** บนหน้า **ข้อมูลส่วนตัว** และเพิ่มที่อยู่ใหม่ กล่องรายการแบบหล่นลง **วัตถุประสงค์** จะแสดงเฉพาะชนิดของข้อมูลที่ผู้ใช้สามารถเพิ่มได้เท่านั้น 

![พนักงานไม่สามารถเลือก ธุรกิจ ในรายการแบบหล่นลงของวัตถุประสงค์](./media/hr-employee-self-service-restrict-purpose.png)

ขณะนี้ **รายละเอียดผู้ติดต่อ** แสดง **วัตถุประสงค์** ในกริด

![วัตถุประสงค์แสดงในกริดรายละเอียดผู้ติดต่อ](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ภาพรวมของระบบบริการตนเองของพนักงานและผู้จัดการ](hr-employee-manager-self-service-overview.md)<br>
[ตั้งค่าคอนฟิกพารามิเตอร์ Human Resources](hr-setup-parameters.md)<br>
[แก้ไขข้อมูลส่วนตัว](hr-employee-manager-self-service-edit-personal-information.md)
