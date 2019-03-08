---
title: การส่งสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด
description: ในขณะที่ลงทะเบียนสินค้าที่ส่งคืน กำหนดว่าควรจะส่งสินค้าไปตรวจสอบก่อนที่จะส่งคืนสินค้านั้นไปยังสินค้าคงคลัง หรือควรจะตัดจำหน่ายในวิธีอื่น
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70aafb752b2c847d5d48236fd5d201a73e088c24
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "334093"
---
# <a name="pass-returned-items-on-to-inspection"></a>การส่งสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด 

[!include [banner](../includes/banner.md)]


ในขณะที่ลงทะเบียนสินค้าที่ส่งคืน คุณอาจกำหนดว่าควรจะส่งสินค้าไปตรวจสอบก่อนที่จะส่งคืนสินค้านั้นไปยังสินค้าคงคลัง หรือควรจะตัดจำหน่ายในบางกรณี

1.  คลิก **การบริหารสินค้าคงคลัง** \> **สมุดรายวัน** \> **การมาถึงของสินค้า** \> **การมาถึงของสินค้า**
    
    \-หรือ-
    
    คลิก **การบริหารสินค้าคงคลัง** \> **สมุดรายวัน** \> **การมาถึงของสินค้า** \> **อินพุทการผลิต**

2.  ในแบบฟอร์ม **สมุดรายวันสถานที่เก็บ** ลงทะเบียนการรับสินค้าตามปกติ
    

    > [!NOTE]
    > <P>สำหรับข้อมูลเกี่ยวกับการลงทะเบียนการรับสินค้าส่งคืน ดู <A href="register-the-receipt-of-returned-items.md">ลงทะเบียนการรับสินค้าที่ส่งคืน</A></P>



3.  บนแท็บ **ค่าเริ่มต้น** ในพื้นที่ **โหมดของการจัดการ** เลือกกล่อง **การบริหารการตรวจสอบสินค้า**

การทำเช่นนี้จะทำให้ระบบสร้างใบสั่งตรวจสอบสินค้า และบุคคลหรือแผนกที่ทำการตรวจสอบจะตอบสนองต่อใบสั่งนี้โดยใช้แบบฟอร์ม **ใบสั่งตรวจสอบสินค้า**

## <a name="see-also"></a>ดูเพิ่มเติมที่

[การนำสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด](take-returned-items-through-inspection.md)

[การระบุวิธีการตัดจำหน่ายสินค้าที่ส่งคืน](specify-how-to-dispose-of-returned-items.md)

