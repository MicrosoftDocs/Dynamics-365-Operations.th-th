---
title: ข้อความที่ถูกเขียนทับเมื่อมีการตั้งค่าคอนฟิกสินค้าในบรรทัดใบสั่งขาย
description: เมื่อมีการตั้งค่าคอนฟิกผลิตภัณฑ์ในบรรทัดใบสั่งขาย ข้อความที่แก้ไขจะถูกเขียนทับด้วยข้อความมาตรฐาน เปลี่ยนข้อความหลังจากที่คุณตั้งค่าคอนฟิกบรรทัด ไม่ใช่ก่อนหน้า
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477694"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>ข้อความสินค้าจะถูกเขียนทับ เมื่อมีการตั้งค่าคอนฟิกผลิตภัณฑ์ในบรรทัดใบสั่งขาย

## <a name="symptoms"></a>อาการ

ปัญหานี้เกิดขึ้นเมื่อคุณสร้างบรรทัดใบสั่งขายสำหรับสินค้าที่จัดโครงแบบแล้วจึงปรับเปลี่ยนข้อความของสินค้า เมื่อคุณตั้งค่าคอนฟิกสินค้า และเลือก **ตกลง** ข้อความจะถูกเขียนทับด้วยข้อความมาตรฐาน

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานนี้คาดการณ์ไว้ ฟิลด์ข้อความประกอบด้วยชื่อตัวแปร ซึ่งจะถูกกรอกเฉพาะหลังจากที่คุณตั้งค่าคอนฟิกบรรทัด ดังนั้น คุณต้องเปลี่ยนข้อความหลังจากที่คุณได้ตั้งค่าคอนฟิกบรรทัดแล้ว ไม่ใช่ก่อน
