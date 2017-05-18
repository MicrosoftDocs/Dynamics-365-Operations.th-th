---
title: "ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services"
description: "หัวข้อนี้อธิบายวิธีการดาวน์โหลดการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Microsoft Dynamics Lifecycle Services (LCS)"
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e2f3a352ca70472de838271fdedfede575cb839d
ms.contentlocale: th-th
ms.lasthandoff: 04/25/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services

[!include[banner](../includes/banner.md)]


หัวข้อนี้อธิบายวิธีการดาวน์โหลดการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Microsoft Dynamics Lifecycle Services (LCS)

บทสอนนี้จะแนะนำให้คุณทราบถึงขั้นตอนการดาวน์โหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เวอร์ชั่นล่าสุดจาก Microsoft Dynamics Lifecycle Services (LCS)

1.  เข้าสู่ระบบ Dynamics 365 for Operations โดยใช้หนึ่งในบทบาทต่อไปนี้:
    -   นักพัฒนาการรายงานทางอิเล็กทรอนิกส์
    -   ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์
    -   ผู้ดูแลระบบ

2.  ไปที่ **การจัดการองค์กร** &gt; **การรายงานทางอิเล็กทรอนิกส์**
3.  ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือกไทล์ **Microsoft**
4.  บนไทล์ **Microsoft** คลิก **ที่เก็บ** [![อัพเดต ER จาก LCS สำหรับ MS - เปิดรายการที่เก็บ MS](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในกริด เลือกที่เก็บที่มีอยู่ของชนิด **LCS** ถ้าที่เก็บนี้ไม่ปรากฏในกริด ให้ทำตามขั้นตอนเหล่านี้:
    1.  คลิก **เพิ่ม** เพื่อเพิ่มที่เก็บใหม่
    2.  เลือก **LCS** เป็นชนิดที่เก็บ
    3.  คลิก **สร้างที่เก็บ**
    4. หากได้รับการแจ้ง ให้ทำตามคำแนะนำการตรวจสอบ
    5.  ป้อนชื่อและคำอธิบายสำหรับที่เก็บ
    6.  คลิก **ตกลง** เพื่อยืนยันรายการที่เก็บใหม่
    7.  ในกริด เลือกที่เก็บใหม่ของชนิด **LCS**

6.  คลิก **เปิด** เพื่อดูรายการของการตั้งค่าคอนฟิก ER สำหรับที่เก็บที่เลือก [![อัพเดต ER จาก LCS สำหรับ MS - สร้างที่เก็บ LCS](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่คุณต้องการ
8.  บน FastTab **เวอร์ชัน** เลือกเวอร์ชันที่กำหนดของการตั้งค่าคอนฟิก ER ที่เลือก
9.  คลิก **นำเข้า** เพื่อดาวน์โหลดเวอร์ชันที่เลือกจาก LCS ไปยังอินสแตนซ์ Dynamics 365 for Operations ปัจจุบัน **หมายเหตุ:** ปุ่ม **นำเข้า** ใช้งานไม่ได้กับเวอร์ชันการตั้งค่าคอนฟิก ER ที่อยู่ในอินสแตนซ์ Dynamics 365 for Operations ปัจจุบันอยู่แล้ว [![อัพเดต ER จาก LCS สำหรับ MS - ดาวน์โหลดการตั้งค่าคอนฟิก](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**หมายเหตุ:** การตั้งค่าคอนฟิกจะได้รับการตรวจสอบความถูกต้องหลังจากที่มีการนำเข้าแล้ว โดยขึ้นอยู่กับการตั้งค่า ER คุณอาจได้รับแจ้งเกี่ยวกับปัญหาความไม่สอดคล้องใด ๆ ที่พบ คุณจะต้องแก้ไขปัญหาเหล่านั้นก่อนที่คุณจะสามารถใช้เวอร์ชันการตั้งค่าคอนฟิกที่นำเข้าได้ สำหรับข้อมูลเพิ่มเติม ดูรายการของบทความที่เกี่ยวข้องของหัวข้อนี้

<a name="see-also"></a>ดูเพิ่มเติมที่
--------

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)




