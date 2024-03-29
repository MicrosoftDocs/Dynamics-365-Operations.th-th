---
title: ตั้งค่าคอนฟิกแสดงเฉพาะชุดงานภายในคลังสินค้าบนอุปกรณ์เคลื่อนที่
description: บทความนี้อธิบายวิธีการตั้งค่าอุปกรณ์เคลื่อนที่เพื่อแสดงรายการของที่ตั้งที่มีชุดงานที่เก่ากว่าที่ตั้งปัจจุบันของรายการงาน
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5788b42483f2c3046b0d20f45115b98d62cce213
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900548"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>ตั้งค่าคอนฟิกแสดงเฉพาะชุดงานภายในคลังสินค้าบนอุปกรณ์เคลื่อนที่

[!include [banner](../includes/banner.md)]

การตั้งค่าคอนฟิก **แสดงเฉพาะชุดงานภายในคลังสินค้า** ช่วยให้คุณสามารถแสดงรายการของที่ตั้งที่มีชุดงานที่เก่ากว่าที่ตั้งปัจจุบันของรายการงาน รายการของสถานที่เก็บที่จะแสดงขึ้นรวมถึงข้อมูลเกี่ยวกับชุดงานที่เก่ากว่าในสถานที่เก็บนั้น ๆ ที่มีวันหมดอายุและสินค้าคงคลังทางกายภาพของแต่ละชุดงาน คุณสามารถเลือกที่จะเบิกสินค้าจากสถานที่เก็บใหม่หรือเบิกสินค้าจากสถานที่เก็บปัจจุบันต่อไปได้ 
- เบิกสินค้าจากสถานที่เก็บใหม่ - ถ้าคุณเลือกที่จะเบิกสินค้าจากสถานที่เก็บใหม่ รายการงานปัจจุบันจะถูกอัพเดตเพื่อใช้สถานที่เก็บใหม่และงานจะดำเนินต่อไปตามปกติกับสถานที่เก็บใหม่ เพื่อให้สถานที่เก็บใหม่ใช้ได้ จะต้องมีปริมาณที่พร้อมใช้งานที่เพียงพอสำหรับรายการงานทั้งหมด ถ้าไม่มีปริมาณที่กำหนด รายการงานจะไม่ถูกอัพเดตและรายการจะแสดงขึ้น 
- ทำการเบิกสินค้าจากสถานที่เก็บปัจจุบัน - ถ้าคุณดำเนินการต่อกับสถานที่เก็บรายการงานปัจจุบัน ปริมาณสำหรับรายการงานจะดำเนินการเบิกสินค้าจากสถานที่เก็บเดิมต่อไป

## <a name="where-it-applies"></a>ตำแหน่งที่ใช้
แสดงชุดงานที่เก่ากว่าภายในคลังสินค้า ถูกตั้งค่าคอนฟิกบนรายการเมนูของอุปกรณ์เคลื่อนที่ และส่งผลต่อการเลือกชุดงานด้านล่างรายการ

## <a name="set-up-display-older-batches-within-warehouse"></a>ตั้งค่า แสดงผลชุดงานที่เก่ากว่าภายในคลังสินค้า
การตั้งค่าคอนฟิก **แสดงชุดงานที่เก่ากว่าภายในคลังสินค้า** จะพร้อมใช้งานบนรายการเมนูอุปกรณ์เคลื่อนที่เมื่อตัวเลือก **เลือกชุดงานที่เก่าที่สุด** ถูกตั้งค่าเป็น **เตือน**

- ภายใต้ **การบริหารคลังสินค้า** > **การตั้งค่า** > **อุปกรณ์เคลื่อนที่** > **รายการเมนูบนอุปกรณ์เคลื่อนที่** ตั้งค่า **ใช้งานที่มีอยู่** เป็น **ใช่** สำหรับรายการเมนู และเลือก **เตือน** ในฟิลด์ **เลือกชุดงานที่เก่าที่สุด** 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]