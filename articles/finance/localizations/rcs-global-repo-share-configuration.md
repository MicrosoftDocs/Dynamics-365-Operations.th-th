---
title: ใช้การตั้งค่าคอนฟิก ER ร่วมกันใน RCS/ที่เก็บส่วนกลางร่วมกับองค์กรภายนอก
description: บทความนี้จะอธิบายถึงวิธีการแชร์การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ใน Microsoft Regulatory Configuration Services (RCS) /ที่เก็บส่วนกลางกับองค์กรภายนอกโดยตรง
author: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
ms.openlocfilehash: d9400ffcede9924a01391a433b570651d3f0c5e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284829"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>แชร์การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ในที่เก็บส่วนกลาง Regulatory Configuration Services (RCS) กับองค์กรภายนอก

[!include [banner](../includes/banner.md)]

คุณสามารถใช้ Microsoft Regulatory Configuration Services (RCS) เพื่อแชร์การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) แล้วเผยแพร่ไปยังองค์กรภายนอก

ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ RCS สามารถใช้เวอร์ชันของการตั้งค่าคอนฟิก ER ที่ได้รับการตั้งค่าคอนฟิกในอินสแตนซ์ RCS กับองค์กรภายนอกร่วมกัน ก่อนที่คุณจะสามารถดำเนินกระบวนงานเหล่านั้นให้เสร็จสมบูรณ์ คุณจะต้องดำเนินการตามข้อกำหนดเบื้องต้นต่อไปนี้ให้เสร็จสมบูรณ์:

- เข้าถึงอินสแตนซ์ RCS
- สร้างผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)
- สร้างและอัปโหลดการตั้งค่าคอนฟิก ER เวอร์ชันใหม่ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างและอัปโหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เวอร์ชันใหม่](rcs-global-repo-upload.md)

นอกจากนี้คุณต้องตรวจสอบให้แน่ใจว่ามีการเตรียมใช้งานสภาพแวดล้อม RCS สำหรับบริษัทของคุณ

1. ในแอปการเงินและการดำเนินงาน ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**
2. ถ้าไม่มีสภาพแวดล้อม RCS ที่จัดเตรียมสำหรับบริษัทของคุณ ให้เลือก **Regulatory services – การตั้งค่าคอนฟิกภายนอก** และทำตามคำแนะนำเพื่อจัดเตรียมสภาพแวดล้อม

ถ้ามีการจัดเตรียมสภาพแวดล้อม RCS ให้กับบริษัทของคุณแล้ว ให้ใช้ URL ของหน้าเพื่อเข้าถึงโดยเลือกตัวเลือกการลงชื่อเข้าใช้

## <a name="verify-the-configuration-that-you-want-to-share"></a>ตรวจสอบการตั้งค่าคอนฟิกที่คุณต้องการใช้ร่วมกัน

ให้ทำตามขั้นตอนต่อไปนี้เพื่อตรวจสอบว่าการตั้งค่าคอนฟิกที่คุณต้องการใช้ร่วมกันถูกอัปโหลดไปยังที่เก็บส่วนกลางแล้ว

1. ในพื้นที่ทำงาน **การรายงานอิเล็กทรอนิกส์** ให้เลือก **ที่เก็บ** สำหรับผู้ให้บริการการตั้งค่าคอนฟิกของคุณ

    ![ผู้ให้บริการการตั้งค่าคอนฟิก](media/1_RCS_Repo_for_config_provider.JPG)

2. เลือก **ที่เก็บส่วนกลาง** \> **เปิด**
3. ค้นหาการตั้งค่าคอนฟิกที่คุณต้องการใช้ร่วมกัน คุณสามารถใช้ฟิลด์ตัวกรองเพื่อจำกัดการค้นหาของคุณให้แคบลง ถ้าคุณไม่พบการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง ให้ทำตามขั้นตอนใน [สร้างและอัปโหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เวอร์ชันใหม่](rcs-global-repo-upload.md)

## <a name="share-er-configurations-with-external-organizations"></a>ใช้การตั้งค่าคอนฟิก ER ในกับกับองค์กรภายนอก

หลังจากที่มีการสร้างการตั้งค่าคอนฟิกภายใต้ผู้ให้บริการการตั้งค่าคอนฟิกของคุณแล้ว คุณสามารถใช้ร่วมกันโดยตรงกับองค์กรภายนอกโดยใช้แท็บด่วน **ใช้ร่วมกันกับ** บนหน้า **ที่เก็บการตั้งค่าคอนฟิกส่วนกลาง**

1. ในพื้นที่ทำงาน **การรายงานอิเล็กทรอนิกส์** ให้เลือก **ที่เก็บ** สำหรับผู้ให้บริการการตั้งค่าคอนฟิกของคุณ
2. เลือก **ที่เก็บส่วนกลาง** \> **เปิด** 
3. เลือกการตั้งค่าคอนฟิกที่คุณต้องการใช้ร่วมกัน
4. บนแท็บด่วน **ใช้ร่วมกันกับ** ให้เลือก **องค์กร**

    ![FastTab ใช้ร่วมกันกับ](media/1_RCS_Repo_for_Share_with_org.JPG)

5. ในกล่องโต้ตอบ ให้ป้อนชื่อโดเมนสำหรับองค์กรภายนอก แล้วเลือก **ตกลง**

    ![กล่องโต้ตอบใช้รุ่นการตั้งค่าคอนฟิกร่วมกันกับองค์กรภายนอก](media/1_RCS_Repo_for_Share_with_form.JPG)

การตั้งค่าคอนฟิกที่ใช้ร่วมกันกับองค์กรภายนอกและพร้อมใช้งานสำหรับองค์กรนั้นในที่เก็บส่วนกลาง จากที่นั่น สามารถนำเข้าไปยังอินสแตนซ์ขององค์กรของ RCS หรืออินสแตนซ์ของแอปการเงินและการดำเนินงาน

6. เมื่อต้องการยกเลิกการใช้ร่วมกันของการตั้งค่าคอนฟิกร่วมกับองค์กรภายนอกก่อนหน้านี้ โปรดเลือกการตั้งค่าคอนฟิก แล้วคลิก **ยกเลิกการใช้ร่วมกัน** แล้วเลือก **ตกลง**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
