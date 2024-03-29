---
title: ตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์เกี่ยวกับไซต์อีคอมเมิร์ซของ B2B
description: บทความนี้อธิบายวิธีการตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์สำหรับไซต์อีคอมเมิร์ซระหว่างธุรกิจ (B2B)
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: 76a7ad2c3095d1402ff214dbfee26b344b492681
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275690"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>ตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์เกี่ยวกับไซต์อีคอมเมิร์ซของ B2B

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายวิธีการตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์สำหรับไซต์อีคอมเมิร์ซระหว่างธุรกิจ (B2B)

ผลิตภัณฑ์ส่วนใหญ่มีหน่วยวัดที่กําหนดการจัดกลุ่มของผลิตภัณฑ์ การจัดกลุ่มจะมีผลต่อการขายผลิตภัณฑ์อย่างไร ผลิตภัณฑ์บางรายการอาจมีการจัดกลุ่มปริมาณเพิ่มเติม การจัดกลุ่มนี้จะระบุว่าผลิตภัณฑ์สามารถขายเป็นแต่ละหน่วยหรือหลายหน่วย และระบุว่าต้องมีขีดจํากัดปริมาณการสั่งต่สุดหรือสูงสุดที่ต้องปฏิบัติตาม

คุณลักษณะการใช้งานการกําหนดขีดจํากัดปริมาณช่วยให้มั่นใจว่าปริมาณต่ำสุด สูงสุด หลายรายการ และปริมาณมาตรฐาน ที่ตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce (ในการตั้งค่าใบสั่งเริ่มต้น หรือการตั้งค่าไซต์โปรแกรมสร้างไซต์ของ Commerce) จะใช้กับใบสั่งของลูกค้าที่จัดวางบนไซต์อีคอมเมิร์ซ ปัจจุบันไม่สนับสนุนขีดจํากัดปริมาณผลิตภัณฑ์ในการขายหน้าร้าน (POS) และศูนย์บริการ

ผู้ค้าปลีกหลายรายมีตัวเลือกสำหรับใบสั่งของลูกค้า (หรือใบสั่งพิเศษ) เพื่อให้ตรงกับผลิตภัณฑ์ที่หลากหลายและความต้องการในการเติมเต็ม ต่อไปนี้เป็นสถานการณ์ทั่วไปบางส่วน:

- ลูกค้าต้องการผลิตภัณฑ์ของผลิตภัณฑ์ย่อยเฉพาะเพื่อขายในหลายผลิตภัณฑ์
- ลูกค้าต้องการรับผลิตภัณฑ์จากร้านค้าหรือสถานที่ที่ไม่ใช่ร้านค้าหรือสถานที่ที่ลูกค้าสั่งซื้อผลิตภัณฑ์ดังกล่าว อย่างไรก็ตาม มาตรฐานการบรรจุของร้านค้าจะแตกต่างจากมาตรฐานการบรรจุในการกระจายการขายทางออนไลน์
- ลูกค้าต้องการซื้อผลิตภัณฑ์ที่มีข้อจํากัดที่มีขีดจํากัดปริมาณสูงสุดต่อสินค้าที่สามารถซื้อได้

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>เปิดคุณลักษณะการตั้งค่าใบสั่งเริ่มต้นใน Commerce headquarters

ก่อนที่คุณจะสามารถตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์ได้ ต้องเปิดคุณลักษณะการตั้งค่าใบสั่งเริ่มต้นใน Commerce headquarters

หากต้องการเปิดใช้งานคุณลักษณะการตั้งค่าใบสั่งเริ่มต้น ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การดูแลระบบ \> พื้นที่ทำงาน \> การจัดการคุณลักษณะ**
1. ค้นหาและเลือกคุณลักษณะ **สนับสนุนไซต์และการตั้งค่าใบสั่งเริ่มต้นในใบสั่งของลูกค้า**
1. ที่ด้านล่างของบานหน้าต่างด้านขวา ให้เลือก **เปิดใช้งานทันที** 

## <a name="define-quantity-settings"></a>กําหนดการตั้งค่าปริมาณ 

คุณสามารถกำหนดการตั้งค่าปริมาณในหน้า **การตั้งค่าใบสั่งเริ่มต้น**

ในการกําหนดการตั้งค่าปริมาณ ให้ปฏิบัติตามขั้นตอนต่อไปนี้ 

1. ไปที่ผลิตภัณฑ์ **Retail และ Commerce \> ผลิตภัณฑ์และประเภท \> ผลิตภัณฑ์ที่นำออกใช้ตามประเภท**
1. ค้นหาผลิตภัณฑ์ที่นำออกใช้
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดการสินค้างคงคลัง** ในกลุ่ม **การตั้งค่าใบสั่ง** ให้เลือก **การตั้งค่าใบสั่งเริ่มต้น** 
1. บนหน้า **การตั้งค่าใบสั่งเริ่มต้น** บนแท็บด่วน **ใบสั่งขาย** ในส่วน **ปริมาณการขาย** ให้ตั้งค่าปริมาณการขายของผลิตภัณฑ์ดังนี้

    - **หลากหลาย** - ปริมาณที่สามารถซื้อผลิตภัณฑ์ได้หลากหลาย
    - **ปริมาณการสั่งขั้นต่ำ** – จํานวนต่ำสุดของผลิตภัณฑ์ที่ต้องซื้อ
    - **ปริมาณการสั่งสูงสุด** – จํานวนสูงสุดของผลิตภัณฑ์ที่สามารถซื้อได้
    - **ปริมาณการสั่งมาตรฐาน** – ปริมาณเริ่มต้นที่จะป้อนโดยอัตโนมัติเมื่อเลือกผลิตภัณฑ์

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>เปิดคุณลักษณะขีดจํากัดปริมาณใบสั่ง B2B ของโปรแกรมสร้างไซต์ Commerce

หากต้องการเปิดคุณลักษณะขีดจํากัดปริมาณใบสั่ง B2B ของโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การตั้งค่าไซต์\> ส่วนขยาย**
1. ภายใต้ **เปิดใช้งานขีดจํากัดปริมาณการสั่ง** ให้เลือก **ที่เปิดใช้งานของลูกค้า B2B** ในเมนูแบบหล่นลง 

> [!NOTE] 
> การตั้งค่าโปรแกรมสร้างไซต์ที่อัปเดตจะมีผลเฉพาะหลังจากที่อัปเดตไฟล์ app.settings.json แล้วเท่านั้น สำหรับข้อมูลเพิ่มเติม โปรดดู [SDK และอัปเดตไลบรารีโมดูล](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าไซต์อีคอมเมิร์ซ B2B](set-up-b2b-site.md)

[จัดการคู่ค้าทางธุรกิจ B2B โดยใช้ลำดับชั้นของลูกค้า](partners-customer-hierarchies.md)

[จัดการผู้ใช้คู่ค้าทางธุรกิจบนไซต์อีคอมเมิร์ซ B2B](manage-b2b-users.md)

[ตั้งค่าคอนฟิกวิธีการชำระเงินด้วยบัญชีลูกค้าสำหรับไซต์อีคอมเมิร์ซของ B2B](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
