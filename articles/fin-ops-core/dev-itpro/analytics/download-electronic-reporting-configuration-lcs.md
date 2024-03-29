---
title: ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services
description: บทความนี้อธิบายวิธีการดาวน์โหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Microsoft Dynamics Lifecycle Services (LCS)
author: kfend
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace
ms.openlocfilehash: f48dd14bc3009550d78bd71db030c172d2ef6450
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277830"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการดาวน์โหลด [การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md#Configuration) รุ่นใหม่ล่าสุดจาก [ไลบรารีแอสเซทที่ใช้ร่วมกัน](../lifecycle-services/asset-library.md) ใน Microsoft Dynamics Lifecycle Services (LCS)

> [!IMPORTANT]
> การใช้ LCS เป็นที่เก็บหน่วยจัดเก็บเพื่อการตั้งค่าคอนฟิก ER [ไม่ได้รับการสนับสนุน](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release) สำหรับข้อมูลเพิ่มเติม ให้ดู [Regulatory Configuration Service (RCS) – การเลิกใช้ที่เก็บข้อมูล Lifecycle Services (LCS)](../../../finance/localizations/rcs-lcs-repo-dep-faq.md)

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
> โดยขึ้นอยู่กับการตั้งค่า ER การตั้งค่าคอนฟิกจะได้รับการตรวจสอบความถูกต้องหลังจากที่มีการนำเข้าแล้ว คุณอาจได้รับแจ้งเกี่ยวกับปัญหาความไม่สอดคล้องใด ๆ ที่พบ คุณจะต้องแก้ไขปัญหาเหล่านั้นก่อนที่คุณจะสามารถใช้เวอร์ชันการตั้งค่าคอนฟิกที่นำเข้าได้ สำหรับข้อมูลเพิ่มเติม ดูรายการของหัวข้อที่เกี่ยวข้องของบทความนี้

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md)

[ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
