---
title: การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างสภาพแวดล้อม Finance and Operations ใหม่ และสภาพแวดล้อม Common Data Service ใหม่จาก Microsoft Dynamics Lifecycle Services (LCS)
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f49eba1748861af6ee3353a6c58005ee84ccae23
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998119"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

หัวข้อนี้อธิบายวิธีการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างสภาพแวดล้อม Finance and Operations ใหม่ และสภาพแวดล้อม Common Data Service ใหม่จาก Microsoft Dynamics Lifecycle Services (LCS)

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

คุณต้องเป็นผู้ดูแลระบบจึงจะสามารถตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางได้

+ คุณต้องมีการเข้าถึงผู้เช่า
+ คุณต้องเป็นผู้ดูแลระบบทั้งในสภาพแวดล้อม Finance and Operations และสภาพแวดล้อม Common Data Service

## <a name="set-up-a-dual-write-connection"></a>ตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง

ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง

1. ใน LCS ไปที่โครงการของคุณ
2. เลือก **ตั้งค่าคอนฟิก** เพื่อปรับใช้สภาพแวดล้อมใหม่
3. เลือกรุ่น 
4. เลือกโทโพโลยี ถ้ามีหนึ่งโทโพโลยีเท่านั้นที่พร้อมใช้งาน จะมีการเลือกโดยอัตโนมัติ
5. ปฏิบัติตามขั้นตอนแรกในวิซาร์ด **การตั้งค่าการปรับใช้** ให้เสร็จสมบูรณ์
6. บนแท็บ **Common Data Service** ทำตามหนึ่งในขั้นตอนเหล่านี้:

    - ถ้ามีการเตรียมใช้งานสภาพแวดล้อม Common Data Service สำหรับผู้เช่าของคุณแล้ว คุณสามารถเลือกสภาพแวดล้อมได้

        1. ตั้งค่าตัวเลือก **ตั้งค่าคอนฟิก Common Data Service** เป็น **ใช่**
        2. ในฟิลด์ **สภาพแวดล้อมที่พร้อมใช้งาน** ให้เลือกสภาพแวดล้อมที่จะรวมกับข้อมูล Finance and Operations ของคุณ รายการนี้รวมถึงสภาพแวดล้อมทั้งหมดที่ซึ่งคุณมีสิทธิ์ของผู้ดูแลระบบ
        3. เลือกกล่องกาเครื่องหมาย **ยินยอม** เพื่อระบุว่าคุณยอมรับข้อกำหนดและเงื่อนไข

        ![แท็บ Common Data Service เมื่อมีการเตรียมใช้งานสภาพแวดล้อม Common Data Service สำหรับผู้เช่าของคุณแล้ว](../dual-write/media/lcs_setup_1.png)

    - ถ้าผู้เช่าของคุณไม่มีสภาพแวดล้อม Common Data Service สภาพแวดล้อมใหม่จะถูกเตรียมใช้งาน

        1. ตั้งค่าตัวเลือก **ตั้งค่าคอนฟิก Common Data Service** เป็น **ใช่**
        2. ป้อนชื่อสำหรับสภาพแวดล้อม Common Data Service
        3. เลือกภูมิภาคที่จะปรับใช้สภาพแวดล้อม
        4. เลือกภาษาและสกุลเงินเริ่มต้นสำหรับสภาพแวดล้อม

            > [!NOTE]
            > คุณไม่สามารถเปลี่ยนภาษาและสกุลเงินในภายหลังได้

        5. เลือกกล่องกาเครื่องหมาย **ยินยอม** เพื่อระบุว่าคุณยอมรับข้อกำหนดและเงื่อนไข

        ![แท็บ Common Data Service เมื่อผู้เช่าของคุณไม่มีสภาพแวดล้อม Common Data Service อยู่แล้ว](../dual-write/media/lcs_setup_2.png)

7. ปฏิบัติตามขั้นตอนที่เหลือในวิซาร์ด **การตั้งค่าการปรับใช้** ให้เสร็จสมบูรณ์
8. หลังจากที่สภาพแวดล้อมมีสถานะเป็น **ปรับใช้แล้ว** ให้เปิดหน้ารายละเอียดของสภาพแวดล้อม ส่วน **ข้อมูลสภาพแวดล้อม Common Data Service** แสดงชื่อของสภาพแวดล้อม Finance and Operations และสภาพแวดล้อม Common Data Service ที่มีการเชื่อมโยง

    ![ส่วนข้อมูลสภาพแวดล้อมของ Common Data Service](../dual-write/media/lcs_setup_3.png)

9. ผู้ดูแลระบบของสภาพแวดล้อม Finance and Operations ต้องลงชื่อเข้าใช้ใน LCS และเลือก **ลิงค์ไปยัง CDS for Apps** เพื่อทำให้การเชื่อมโยงเสร็จสมบูรณ์ หน้ารายละเอียดของสภาพแวดล้อมจะแสดงข้อมูลผู้ติดต่อของผู้ดูแลระบบ

    หลังจากเสร็จสิ้นการเชื่อมโยง สถานะจะได้รับการอัพเดตเป็น **การเชื่อมโยงสภาพแวดล้อมเสร็จเรียบร้อยแล้ว**

10. เมื่อต้องการเปิดพื้นที่ทำงาน **การรวมข้อมูล** ในสภาพแวดล้อม Finance and Operations และควบคุมเท็มเพลตที่พร้อมใช้งาน เลือก **เชื่อมโยงกับ CDS for Apps**

    ![ปุ่มลิงค์ไปยัง CDS for Apps ในส่วนข้อมูลสภาพแวดล้อมของ Common Data Service](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> คุณไม่สามารถยกเลิกการเชื่อมโยงสภาพแวดล้อมได้โดยใช้ LCS เมื่อต้องการยกเลิกการเชื่อมโยงสภาพแวดล้อม ให้เปิดพื้นที่ทำงาน **การรวมข้อมูล** ในสภาพแวดล้อม Finance and Operations และจากนั้น เลือก **ยกเลิกการเชื่อมโยง**
