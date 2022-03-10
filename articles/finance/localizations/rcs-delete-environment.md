---
title: Regulatory Configuration Service (RCS) - ลบสภาพแวดล้อม RCS
description: หัวข้อนี้อธิบายวิธีการที่ผู้ดูแลระบบ Regulatory Configuration Service (RCS) สามารถลบสภาพแวดล้อม RCS และข้อมูลที่เกี่ยวข้องได้
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: f9073a14143423676f23f9bf8dc9c17dbae18a6c3ad0d2f6d1e33919fd9162bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759830"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) - ลบสภาพแวดล้อม RCS

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการที่ผู้ดูแลระบบ Regulatory Configuration Service (RCS) สามารถลบสภาพแวดล้อม RCS และข้อมูลที่เกี่ยวข้องได้

ก่อนที่คุณจะสามารถดำเนินการกระบวนงานต่างๆ ในหัวข้อนี้ให้เสร็จสมบูรณ์ ต้องตรงข้อกำหนดเบื้องต้นต่อไปนี้:

- คุณต้องได้รับมอบหมายบทบาท **ผู้ดูแลระบบ** ให้กับคุณให้กับสภาพแวดล้อม RCS
- บทบาท **ผู้ดูแลระบบ** ต้องมอบหมายบทบาท **RCSDeleteEnvironmentDuty** ให้กับสภาพแวดล้อม

## <a name="delete-an-rcs-environment"></a>ลบสภาพแวดล้อม RCS

1. เปิด RCS และให้เลือกไทล์พื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์**
2. ในส่วน **ลิงค์ที่เกี่ยวข้อง** ให้เลือก **ลบสภาพแวดล้อม RCS**

    ![ลบลิงค์สภาพแวดล้อม RCS ในส่วนลิงค์ที่เกี่ยวข้อง](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. ในกล่องโต้ตอบที่ปรากฏ ให้ทบทวนข้อความเกี่ยวกับขอบเขตของการลบสภาพแวดล้อม

    ![ข้อความในกล่องโต้ตอบลบสภาพแวดล้อม RCS](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > ไม่สามารถกลับรายการการลบสภาพแวดล้อม RCS
    >
    > การดําเนินงานจะลบสภาพแวดล้อม RCS ที่เลือกและข้อมูลที่เกี่ยวข้องใดๆ รวมถึงลักษณะการดําเนินการและการตั้งค่าคอนฟิกที่จัดเก็บอยู่ในที่เก็บส่วนกลาง คุณลักษณะและการตั้งค่าคอนฟิกที่ใช้ร่วมกันกับองค์กรอื่นๆ จะถูกยกเลิกและลบออกถ้าไม่มีการอ้างอิง คุณลักษณะและการตั้งค่าคอนฟิกที่ขึ้นต่อกันจะถูกเลือกเป็นถูกตัดออก

4. ในฟิลด์ที่ระบุ ให้ป้อนรหัสเฉพาะสากล (GUID) ของสภาพแวดล้อม RCS เพื่อยืนยันว่าคุณต้องการลบ GUID ของสภาพแวดล้อมรวมอยู่ในข้อความลบ
5. เลือก **ลบสภาพแวดล้อม**
    
ขณะนี้สภาพแวดล้อม RCS และข้อมูลที่เกี่ยวข้องใดๆ ของคุณถูกลบแล้ว

> [!IMPORTANT]
> หลังจากที่คุณลบสภาพแวดล้อม RCS แล้ว จะไม่มีวิธีกู้คืนข้อมูล คุณสามารถสร้างสภาพแวดล้อม RCS ใหม่ได้ในภูมิภาค RCS ที่พร้อมใช้งานใดๆ
