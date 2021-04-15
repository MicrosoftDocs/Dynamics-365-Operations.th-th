---
title: การส่งสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด
description: ในขณะที่ลงทะเบียนสินค้าที่ส่งคืน กำหนดว่าควรจะส่งสินค้าไปตรวจสอบก่อนที่จะส่งคืนสินค้านั้นไปยังสินค้าคงคลัง หรือควรจะตัดจำหน่ายในวิธีอื่น
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdee1ed2c7e98843e5dcfe9669e6a7c1eb11173c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810689"
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]