---
title: ใบสั่งผลิตไม่แสดงอยู่บนหน้าการทำเครื่องหมาย
description: บางใบสั่งผลิตไม่แสดงอยู่บนหน้า การทำเครื่องหมาย หัวข้อนี้อธิบายการจัดโครงแบบผลิตภัณฑ์สามโครงแบบที่ไม่พร้อมให้มีการเลือก
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477686"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>ใบสั่งผลิตไม่แสดงอยู่บนหน้าการทำเครื่องหมาย

## <a name="symptoms"></a>อาการ

เมื่อใช้งานแต่ละการผลิต ใบสั่งผลิตบางใบจะไม่แสดงบนหน้า **การทำเครื่องหมาย**

## <a name="resolution"></a>การแก้ปัญหา

ผลิตภัณฑ์ที่มีการตั้งค่าคอนฟิกต่อไปนี้ไม่พร้อมใช้งานสำหรับการทำเครื่องหมาย ดังนั้นจึงไม่แสดงบนหน้า **การทำเครื่องหมาย**:

- ผลิตภัณฑ์ได้รับการกำหนดเป็นผลิตภัณฑ์ของชนิด *น้ำหนักจริง*
- มีการเปิดใช้งานสำหรับกระบวนการคลังสินค้าขั้นสูง
- มีการตั้งค่าคอนฟิกไว้เพื่อควบคุมโดยหลักการ *ต้นทุนมาตรฐาน*
