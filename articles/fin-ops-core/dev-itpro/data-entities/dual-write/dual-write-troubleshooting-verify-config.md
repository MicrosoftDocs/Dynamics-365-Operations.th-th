---
title: ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และ Common Data Service
description: หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถกำหนดได้ว่า มีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และใน Common Data Service หรือไม่
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172656"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และ Common Data Service

[!include [banner](../../includes/banner.md)]



หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service กล่าวคือ จะอธิบายถึงวิธีการที่คุณสามารถกำหนดได้ว่า มีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations และใน Common Data Service หรือไม่

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางในแอป Finance and Operations

เมื่อต้องการตรวจสอบว่า ข้อผิดพลาดที่คุณเห็นเมื่อคุณพยายามบันทึกเรกคอร์ดสำหรับการปรับปรุงมาจากการรวมแบบสองทิศทางหรือไม่ ก่อนอื่นให้ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง

+ ถ้าคุณมีสิทธิ์ระดับผู้ดูแลระบบในแอป Finance and Operations ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือกไทล์ **การรวมแบบสองทิศทาง** ถ้ารายละเอียดของสภาพแวดล้อมที่มีการเชื่อมโยงและรายการของแผนผังเอนทิตี้ที่กำลังรันถูกแสดง จะมีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง

    ![การตรวจสอบความถูกต้องของการเชื่อมต่อแอป Finance and Operations เมื่อคุณมีสิทธิ์ระดับผู้ดูแลระบบ](media/verify_fin_ops_1.png)

+ ถ้าคุณไม่มีสิทธิ์ระดับผู้ดูแลระบบ คุณจะได้รับข้อความแสดงข้อผิดพลาด *ไม่สามารถเขียนข้อมูลไปยังเอนทิตี้ได้ \<ชื่อเอนทิตี้\>* ในตัวอย่างในภาพประกอบต่อไปนี้ คุณไม่สามารถสร้างเรกคอร์ดลูกค้าในแอป Finance and Operations ได้ เนื่องจากมีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง แต่กลุ่มลูกค้าและข้อมูลอ้างอิงเงื่อนไขการชำระเงินไม่มีอยู่ใน Common Data Service

    ![การตรวจสอบความถูกต้องของการเชื่อมต่อแอป Finance and Operations เมื่อคุณไม่มีสิทธิ์ระดับผู้ดูแลระบบ](media/verify_fin_ops_2.png)

สำหรับข้อมูลเกี่ยวกับวิธีการแก้ไขปัญหา เมื่อคุณสร้างข้อมูลในแอป Finance and Operations ให้ดูที่ [แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง](dual-write-troubleshooting-live-sync.md)

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>ตรวจสอบว่ามีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางใน Common Data Service

เมื่อคุณสร้างข้อมูล ถ้าคุณเห็นฟิลด์ **บริษัท** บนหน้าใน Common Data Service จะมีการตั้งค่าคอนฟิกการรวมแบบสองทิศทาง

![การตรวจสอบการเชื่อมต่อ Common Data Service](media/verify_cds.png)

สำหรับข้อมูลเกี่ยวกับวิธีการแก้ไขปัญหา เมื่อคุณสร้างข้อมูลใน Common Data Service ให้ดูที่ [แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง](dual-write-troubleshooting-live-sync.md)

สำหรับข้อมูลเกี่ยวกับวิธีการดูรายละเอียดข้อผิดพลาด ถ้าคุณพบข้อผิดพลาดใดๆ ในขณะที่คุณสร้างข้อมูลใน Common Data Service ให้ดูที่ให้ดูที่ [เปิดใช้งานและดูล็อกการติดตามปลั๊กอินใน Common Data Service เพื่อดูรายละเอียดข้อผิดพลาด](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details)
