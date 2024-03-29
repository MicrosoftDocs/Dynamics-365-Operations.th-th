---
title: การปรับปรุงมูลค่าต้นทุนปริมาณคงคลังคงเหลือ
description: ใช้หน้าการปรับปรุงปริมาณสินค้าคงคลังคงเหลือเพื่อปรับปรุงมูลค่าต้นทุนของปริมาณสินค้าคงคลังคงเหลือหลังจากกระบวนการปิดบัญชีสินค้าคงคลังได้ถูกรัน
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62122454b2fe0f6a9f04f073057156603e66bb22
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673311"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>การปรับปรุงมูลค่าต้นทุนปริมาณคงคลังคงเหลือ

[!include [banner](../includes/banner.md)]

ใช้หน้าการปรับปรุงปริมาณสินค้าคงคลังคงเหลือเพื่อปรับปรุงมูลค่าต้นทุนของปริมาณสินค้าคงคลังคงเหลือหลังจากกระบวนการปิดบัญชีสินค้าคงคลังได้ถูกรัน

คุณสามารถใช้หน้า **การปรับปรุงปริมาณสินค้าคงคลังคงเหลือ** เพื่อปรับปรุงมูลค่าต้นทุนของปริมาณสินค้าคงคลังคงเหลือหลังจากกระบวนการปิดบัญชีสินค้าคงคลังได้ถูกรัน **หมายเหตุ:** เพื่อเปิดหน้า **การปรับปรุงสินค้าคงคลังคงเหลือ** ในหน้า **การปิดและการปรับปรุง** เลือกเรกคอร์ดของกระบวนการปิดสินค้าคงคลังที่สมบูรณ์ และจากนั้น คลิก **การปรับปรุง** &gt; **คงเหลือ** **ตัวอย่าง:** คุณมีธุรกรรมต่อไปนี้ในเดือนกุมภาพันธ์:

-   1 กุมภาพันธ์: ใบเสร็จรับเงินสินค้าคงคลังในปริมาณเท่ากับ 2 หน่วย ในราคาต้นทุน USD 10.00
-   5 กุมภาพันธ์: ใบเสร็จรับเงินสินค้าคงคลังในปริมาณเท่ากับ 1 หน่วย ในราคาต้นทุน USD 13.00
-   19 กุมภาพันธ์: นำสินค้าคงคลังทางการเงินออกใช้ในปริมาณ 1 หน่วย ที่ต้นทุนเฉลี่ยต่อเนื่อง USD 11.00

สินค้านี้มีการตั้งค่าโดยใช้แบบจำลองสินค้าคงคลังแบบเข้าก่อนออกก่อน (FIFO) และมีการปิดบัญชีสินค้าคงคลัง ณ วันที่ 28 กุมภาพันธ์ ธุรกรรมการออกใช้ทางการเงินมูลค่า USD 11.00 จะถูกจับคู่กับใบเสร็จรับเงินลงวันที่ 1 กุมภาพันธ์ และจะมีการปรับปรุง USD 1.00 การรับสินค้าคงคลังต่อไปนี้จะมีปริมาณสินค้าคงคลังที่เปิดไว้:

-   1 กุมภาพันธ์: ปริมาณ 1 หน่วย ที่ต้นทุน USD 10.00
-   5 กุมภาพันธ์: ปริมาณ 1 หน่วย ที่ต้นทุน USD 13.00

ในการตั้งค่าต้นทุนของสินค้าทั้งสองนี้เป็น USD 15.00 ให้ใช้ตัวเลือกการปรับปรุงคงเหลือเพื่อปรับปรุงปริมาณคงเหลือที่เปิด ณ รอบระยะเวลาการปิดบัญชีสินค้าคงคลังล่าสุด **หมายเหตุ:** วันที่ลงรายการบัญชีของธุรกรรมการปรับปรุงคงเหลือจะเป็นวันที่ปิดบัญชีสินค้าคงคลังล่าสุด วันที่นี้ไม่สามารถแก้ไขได้


[!INCLUDE[footer-include](../../includes/footer-banner.md)]