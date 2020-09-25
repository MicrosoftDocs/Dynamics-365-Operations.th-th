---
title: ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการดาวน์โหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Microsoft Dynamics Lifecycle Services (LCS)
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a18427114bddb7c72024a8d96d33f3fbf8dbe17
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810630"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการดาวน์โหลด [การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md#Configuration) รุ่นใหม่ล่าสุดจาก [ไลบรารีแอสเซทที่ใช้ร่วมกัน](../lifecycle-services/asset-library.md) ใน Microsoft Dynamics Lifecycle Services (LCS)

1. ลงชื่อเข้าใช้ในแอพลิเคชันโดยใช้หนึ่งในบทบาทต่อไปนี้:

    - นักพัฒนาการรายงานทางอิเล็กทรอนิกส์
    - ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์
    - ผู้ดูแลระบบ

2. ไปที่ **การจัดการองค์กร** &gt; **พื้นที่ทำงาน** &gt; **การรายงานทางอิเล็กทรอนิกส์**
3. ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือกไทล์ **Microsoft**
4. บนไทล์ **Microsoft** เลือก **ที่เก็บ**

    [![ไทล์ Microsoft บนหน้าการตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในกริด เลือกที่เก็บที่มีอยู่ของชนิด **LCS** ถ้าที่เก็บนี้ไม่ปรากฏในกริด ให้ทำตามขั้นตอนเหล่านี้:

    1. เลือก **เพิ่ม** เพื่อเพิ่มที่เก็บ
    2. เลือก **LCS** เป็นชนิดที่เก็บ
    3. เลือก **สร้างที่เก็บ**
    4. ถ้าคุณได้รับข้อความแจ้งเกี่ยวกับการอนุมัติ ให้ทำตามคำแนะนำบนหน้าจอ
    5. ป้อนชื่อและคำอธิบายสำหรับที่เก็บ
    6. เลือก **ตกลง** เพื่อยืนยันรายการที่เก็บใหม่
    7. ในกริด เลือกที่เก็บใหม่ของชนิด **LCS**

6. เลือก **เปิด** เพื่อดูรายการของการตั้งค่าคอนฟิก ER สำหรับที่เก็บที่เลือก

    [![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > ถ้าคุณมีปัญหาในการเข้าถึงที่เก็บ LCS เพื่อดาวน์โหลดการตั้งค่าคอนฟิกจากไลบรารีแอสเซทที่ใช้ร่วมกันใน LCS คุณสามารถดาวน์โหลดการตั้งค่าคอนฟิกจาก [ที่เก็บส่วนกลาง](er-download-configurations-global-repo.md) แทน

7. ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่ต้องการ
8. บน FastTab **เวอร์ชัน** เลือกเวอร์ชันที่กำหนดของการตั้งค่าคอนฟิก ER ที่เลือก
9. เลือก **นำเข้า** เพื่อดาวน์โหลดเวอร์ชันที่เลือกจาก LCS ไปยังอินสแตนซ์ปัจจุบัน

    > [!NOTE]
    > ปุ่ม **นำเข้า** ใช้งานไม่ได้กับเวอร์ชันการตั้งค่าคอนฟิก ER ที่อยู่ในอินสแตนซ์ปัจจุบันอยู่แล้ว

    [![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> โดยขึ้นอยู่กับการตั้งค่า ER การตั้งค่าคอนฟิกจะได้รับการตรวจสอบความถูกต้องหลังจากที่มีการนำเข้าแล้ว คุณอาจได้รับแจ้งเกี่ยวกับปัญหาความไม่สอดคล้องใด ๆ ที่พบ คุณจะต้องแก้ไขปัญหาเหล่านั้นก่อนที่คุณจะสามารถใช้เวอร์ชันการตั้งค่าคอนฟิกที่นำเข้าได้ สำหรับข้อมูลเพิ่มเติม ดูรายการของหัวข้อที่เกี่ยวข้องของหัวข้อนี้

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md)

[ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก](er-download-configurations-global-repo.md)
