---
title: ตรวจสอบการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และ Dataverse
description: หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถกำหนดได้ว่า มีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และใน Dataverse หรือไม่
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 074cfd5dc2d2877e83e7e65a8b2178ed954a288e
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416692"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>ตรวจสอบการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และ Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse กล่าวคือ จะอธิบายถึงวิธีการที่คุณสามารถกำหนดได้ว่า มีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และใน Dataverse หรือไม่

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations

เมื่อต้องการตรวจสอบว่า ข้อผิดพลาดที่คุณเห็นเมื่อคุณพยายามบันทึกแถวสำหรับการปรับปรุงมาจากการรวมแบบสองทิศทางหรือไม่ ก่อนอื่นให้ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง

+ ถ้าคุณมีสิทธิ์ระดับผู้ดูแลระบบในแอป Finance and Operations ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือกไทล์ **การรวมแบบสองทิศทาง** ถ้ารายละเอียดของสภาพแวดล้อมที่มีการเชื่อมโยงและรายการของแผนผังตารางที่กำลังรันถูกแสดง จะมีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง

    ![การตรวจสอบความถูกต้องของการเชื่อมต่อแอป Finance and Operations เมื่อคุณมีสิทธิ์ระดับผู้ดูแลระบบ](media/verify_fin_ops_1.png)

+ ถ้าคุณไม่มีสิทธิ์ของผู้ดูแลระบบ คุณจะได้รับข้อความแสดงข้อผิดพลาด *ไม่สามารถเขียนข้อมูลไปยังเอนทิตีได้ \<entity name\>* ในตัวอย่างในภาพประกอบต่อไปนี้ คุณไม่สามารถสร้างแถวลูกค้าในแอป Finance and Operations ได้ เนื่องจากมีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง แต่กลุ่มลูกค้าและข้อมูลอ้างอิงเงื่อนไขการชำระเงินไม่มีอยู่ใน Dataverse

    ![การตรวจสอบความถูกต้องของการเชื่อมต่อแอป Finance and Operations เมื่อคุณไม่มีสิทธิ์ระดับผู้ดูแลระบบ](media/verify_fin_ops_2.png)

สำหรับข้อมูลเกี่ยวกับวิธีการแก้ไขปัญหา เมื่อคุณสร้างข้อมูลในแอป Finance and Operations ให้ดูที่ [แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง](dual-write-troubleshooting-live-sync.md)

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางใน Dataverse

เมื่อคุณสร้างข้อมูล ถ้าคุณเห็นคอลัมน์ **บริษัท** บนหน้าใน Dataverse จะมีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง

![การตรวจสอบการเชื่อมต่อ Dataverse](media/verify_cds.png)

สำหรับข้อมูลเกี่ยวกับวิธีการแก้ไขปัญหา เมื่อคุณสร้างข้อมูลใน Dataverse ให้ดูที่ [แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง](dual-write-troubleshooting-live-sync.md)

สำหรับข้อมูลเกี่ยวกับวิธีการดูรายละเอียดข้อผิดพลาด ถ้าคุณพบข้อผิดพลาดใดๆ ในขณะที่คุณสร้างข้อมูลใน Dataverse ให้ดูที่ให้ดูที่ [เปิดใช้งานและดูล็อกการติดตามปลั๊กอินใน Dataverse เพื่อดูรายละเอียดข้อผิดพลาด](dual-write-troubleshooting.md#enable-view-trace)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]