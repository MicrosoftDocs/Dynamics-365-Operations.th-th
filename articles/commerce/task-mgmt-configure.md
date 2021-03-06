---
title: ตั้งค่าคอนฟิกการจัดการงาน
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกคุณลักษณะการจัดการงานใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e880305d02fd9f10464fe3f65a2774a44da258c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006246"
---
# <a name="configure-task-management"></a>ตั้งค่าคอนฟิกการจัดการงาน

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกคุณลักษณะการจัดการงานใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

ก่อนที่ผู้จัดการและพนักงาน Dynamics 365 Commerce จะสามารถใช้คุณลักษณะการจัดการงานใน Commerce ได้ ต้องมีการตั้งค่าคอนฟิกการจัดการงาน ขั้นตอนการตั้งค่าคอนฟิกรวมถึงการให้สิทธิ์กับผู้จัดการและพนักงาน การกระจายสิทธิ์ไปยังไคลเอนต์ของการขายหน้าร้าน (POS) การตั้งค่าการแจ้งเตือน POS และการตั้งค่าไทล์ **งาน** บนโฮมเพจของแอปพลิเคชัน POS

## <a name="configure-permissions-for-store-managers"></a>ตั้งค่าคอนฟิกสิทธิ์สำหรับผู้จัดการร้านค้า

ผู้ปฏิบัติงานทุกคนในร้านค้าที่กำหนดสามารถดูงานทั้งหมดที่กำหนดให้กับร้านค้าดังกล่าวได้ นอกจากนี้ คุณยังสามารถอัปเดตสถานะของงานที่กำหนดให้กับผู้ใช้เหล่านั้นได้ด้วย อย่างไรก็ตาม บทบาท เช่น ผู้จัดการร้านค้า ต้องมีสิทธ์ในการจัดการงานที่ได้รับมอบหมายให้กับร้านค้าและเพื่อสร้างงานวัตถุประสงค์เดียว

เมื่อต้องการตั้งค่าคอนฟิกสิทธิ์การจัดการงานสำหรับผู้จัดการร้านค้า ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การขายปลีกและการค้า \> พนักงาน \> กลุ่มสิทธิ์**
1. เลือกกลุ่มสิทธิ์เฉพาะ (ตัวอย่างเช่น **ผู้จัดการ**) แล้วเลือก **แก้ไข**
1. บนแท็บด่วน **สิทธิ์** ให้ตั้งค่าตัวเลือก **อนุญาตการจัดการงาน** เป็น **ใช่**
1. บนแท็บด่วน **การแจ้งเตือน** ให้เพิ่มการดำเนินงาน **การจัดการงาน** และป้อนค่าในฟิลด์ **ลำดับการแสดงผล** ตัวอย่างเช่น ป้อน **2** ถ้าการดำเนินงาน **การเติมสินค้าของใบสั่ง** มีค่า **ลำดับการแสดงผล** เป็น **1** อยู่แล้ว
    
> [!NOTE]
> ถ้าบทบาทที่ไม่ใช่ผู้จัดการต้องมีสิทธิ์ในการจัดการงานใน POS คุณสามารถให้สิทธิ์สำหรับแต่ละบุคคล อีกทางหนึ่งคือ คุณสามารถสร้างกลุ่มสิทธิ์ใหม่สำหรับผู้ที่ไม่ใช่ผู้จัดการและตั้งค่าตัวเลือก **อนุญาตการจัดการงาน** เป็น **ใช่**

แผนภาพต่อไปนี้แสดงวิธีตั้งค่าคอนฟิกสิทธิ์การจัดการงานสำหรับผู้จัดการร้านค้า

![การตั้งค่าคอนฟิกสิทธิ์การจัดการงานสำหรับผู้จัดการร้านค้า](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>ตั้งค่าคอนฟิกสิทธิ์สำหรับพนักงาน

พนักงานต้องมีสิทธิ์ในการสร้างรายการงาน จัดการเงื่อนไขการกำหนด และตั้งค่าคอนฟิกการเกิดซ้ำของรายการงานใดๆ เมื่อต้องการตั้งค่าคอนฟิกสิทธิ์เหล่านี้ คุณสามารถกำหนดพนักงานให้กับบทบาท **จัดการงานขายปลีก**

ในการตั้งค่าคอนฟิกสิทธิ์สำหรับพนักงาน ให้ทำตามขั้นตอนเหล่านี้

1. ไปยัง **การขายปลีกและการค้า \> พนักงาน \> ผู้ใช้**
1. เลือกพนักงาน
1. บนแท็บด่วน **บทบาทของผู้ใช้** ให้เลือก **กำหนดบทบาท**
1. ในกล่องโต้ตอบ **กำหนดบทบาทให้กับผู้ใช้** ให้เลือกบทบาทของ **ผู้จัดการงานขายปลีก** แล้วเลือก **ตกลง**

## <a name="distribute-permissions-to-pos-clients"></a>กระจายสิทธิ์ไปยังไคลเอนต์ POS

ก่อนที่พนักงานสามารถใช้ไคลเอนต์ POS ต้องมีการกระจายสิทธิ์และซิงค์กับไคลเอนต์เหล่านั้น

เมื่อต้องการกระจายสิทธิ์ไปยังไคลเอนต์ POS ให้ทำตามขั้นตอนต่อไปนี้

1. ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**
1. เลือกตารางการหระจาย **1060** (**พนักงาน**) แล้วเลือก **เรียกใช้เดี๋ยวนี้**
1. เลือกตารางการกระจาย **1070** (**การตั้งค่าคอนฟิกช่องทาง**) แล้วเลือก **เรียกใช้เดี๋ยวนี้**

## <a name="configure-pos-notifications-for-tasks"></a>ตั้งค่าคอนฟิกการแจ้งเตือน POS สำหรับงาน

ต้องมีการตั้งค่าคอนฟิกการจัดการงานเพื่อให้การแจ้งเตือนพร้อมใช้งานในแอปพลิเคชัน POS

ในการตั้งค่าคอนฟิกการแจ้งเตือน POS สำหรับงาน ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> POS \> การดำเนินการ POS**
1. ค้นหาการดำเนินงาน **1400** (**การจัดการงาน**) และเลือกกล่องกาเครื่องหมาย **เปิดใช้งานการแจ้งเตือน**

ภาพประกอบต่อไปนี้จะแสดงการดำเนินงานของ **การจัดการงาน** ในหน้า **การดำเนินงาน POS**

![การดำเนินงานการจัดการงานในหน้าการดำเนินงาน POS](media/HQ-POS-Tasks-Notifications.png)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกการแจ้งเตือน POS ให้ดูที่ [แสดงการแจ้งเตือนใบสั่งในการขายหน้าร้าน (POS)](notifications-pos.md)

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>ตั้งค่าคอนฟิกไทล์งานบนโฮมเพจของแอปพลิเคชัน POS

ก่อนที่คุณจะตั้งค่าคอนฟิกไทล์ **งาน** บนโฮมเพจของแอปพลิเคชัน POS ให้ดูที่ [โครงร่างหน้าจอสำหรับการขายหน้าร้าน (POS)](pos-screen-layouts.md) สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกและเพิ่มปุ่มใหม่ลงในโครงร่างหน้าจอ POS

หากต้องการตั้งค่าคอนฟิกไทล์ **งาน** บนโฮมเพจของแอปพลิเคชัน POS ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า \> POS \> โครงร่างหน้าจอ**
1. เลือกโครงร่างหน้าจอ เลือกขนาดโครงร่าง และเลือกกริดปุ่ม
1. บนแท็บด่วน **กริดปุ่ม** ให้เลือก **ผู้ออกแบบ** เพื่อแก้ไขกริดปุ่มที่เลือก
1. เพิ่มไทล์ **งาน** ไปยังส่วนที่เหมาะสมของโฮมเพจ

ภาพประกอบต่อไปนี้แสดงตัวอย่างของไทล์ **งาน** บนโฮมเพจ POS

![ไทล์งานบนโฮมเพจของ POS](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของการจัดการงาน](task-mgmt-overview.md)

[สร้างรายการงานและเพิ่มงาน](task-mgmt-create-lists.md)

[กำหนดรายการงานให้กับร้านค้าหรือพนักงาน](task-mgmt-assign-lists.md)

[การจัดการงานใน POS](task-mgmt-POS.md)
