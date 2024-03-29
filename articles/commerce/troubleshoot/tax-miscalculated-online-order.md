---
title: การคํานวณภาษีในใบสั่งออนไลน์ไม่ถูกต้อง
description: บทความนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการคํานวณภาษีในใบสั่งออนไลน์ที่ไม่ถูกต้อง หรือเมื่อตั้งค่ากลุ่มภาษีบนรายการขายไม่ถูกต้อง
author: Reza-Assadi
ms.date: 02/16/2022
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: a85b03cb6245c7c2e3622abc61a7887030927432
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285590"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>การคํานวณภาษีในใบสั่งออนไลน์ไม่ถูกต้อง

[!include [banner](../../includes/banner.md)]

บทความนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการคํานวณภาษีในใบสั่งออนไลน์ที่ไม่ถูกต้อง หรือเมื่อตั้งค่ากลุ่มภาษีบนรายการขายไม่ถูกต้อง

## <a name="description"></a>คำอธิบาย

เมื่อวางใบสั่งอีคอมเมิร์ซ ภาษีจะคํานวณไม่ถูกต้อง หรือกลุ่มภาษีบนรายการขายจะตั้งค่าไม่ถูกต้อง

## <a name="resolution"></a>การแก้ปัญหา

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>ตั้งค่าคอนฟิกกลุ่มภาษีขายทั่วไปใน Commerce headquarters

หากต้องการตั้งค่าคอนฟิกกลุ่มภาษีขายทั่วไปใน Commerce headquarters ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีขาย \> กลุ่มภาษีขาย**
1. ในบานหน้าต่างการนําทางด้านซ้าย ให้เลือกกลุ่มภาษีที่จะตั้งค่าคอนฟิก
1. บนแท็บด่วน **ภาษีตามปลายทางการขายปลีก** ให้ตั้งค่าคอนฟิกภาษีของกลุ่มภาษีขาย

> [!NOTE]
> การจัดส่งที่ไม่รวมภาษีขายในที่กำหนดโดยที่อยู่ของลูกค้า ที่อยู่ที่จัดส่งในบรรทัดและภาษีฐานปลายทางซึ่งตั้งค่าคอนฟิกไว้สำหรับกลุ่มภาษีจะกําหนดกลุ่มภาษี สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าภาษีสำหรับร้านค้าออนไลน์ตามปลายทาง](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>ตั้งค่าคอนฟิกภาษีขายจากร้านค้าปลีกใน Commerce headquarters

ในการตั้งค่าคอนฟิกภาษีขายจากร้านค้าปลีกใน Commerce headquarters ให้ทำตามขั้นตอนต่อไปนี้

1. ไปยัง **Retail และ Commerce \> ช่องทาง \> ร้านค้าทั้งหมด**
1. เลือกร้านค้าที่จะตั้งค่าคอนฟิกภาษีขาย
1. บนแท็บด่วน **ทั่วไป** ในส่วน **ภาษีขาย** ให้ตั้งค่าคอนฟิกข้อมูลภาษีขายของร้านค้า

> [!NOTE]
> สำหรับการเบิกสินค้าจากร้านค้า กลุ่มภาษีจะมาจากร้านค้าที่เลือกเพื่อเบิกสินค้า ดูข้อมูลเพิ่มเติมที่ [ตั้งค่าตัวเลือกภาษีอื่นๆ สำหรับร้านค้า](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>ตั้งค่าคอนฟิกภาษีขายสำหรับที่อยู่ของลูกค้าใน Commerce headquarters

ในการตั้งค่าคอนฟิกภาษีขายจากที่อยู่ของลูกค้าใน Commerce headquarters ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**
1. เลือกลูกค้าเพื่อกำหนดค่าคอนฟิกที่จะสร้างใบสั่งขายให้
1. บนแท็บด่วน **ที่อยู่** ให้เลือกที่อยู่ที่จะตั้งค่าคอนฟิกภาษีขาย ให้เลือก **ตัวเลือกเพิ่มเติม** แล้วเลือก **ขั้นสูง**
1. บนแท็บด่วน **ทั่วไป** ให้เลือก **กลุ่มภาษี**
1. ในฟิลด์ **ภาษีขาย** ให้เลือกค่าที่เหมาะสม:

> [!NOTE]
> การจัดส่งที่เกี่ยวข้องกับภาษีขายตามที่อยู่ของลูกค้า ที่อยู่ที่จัดส่งของบรรทัดจะระบุกลุ่มภาษีสำหรับรายการ หากลูกค้าได้รับการจัดส่งไปยังที่อยู่ที่มีอยู่ ซึ่งมีกลุ่มภาษีที่ตั้งค่าคอนฟิกไว้แล้ว ระบบจะใช้กลุ่มภาษีที่มีอยู่ ตามค่าเริ่มต้น ที่อยู่จะไม่มีกลุ่มภาษีเมื่อสร้างที่อยู่

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าคอนฟิกภาษีขายสำหรับใบสั่งออนไลน์](../sales-tax-config.md)
