---
title: ประมวลผลการเบิกสินค้าตามใบสั่งของลูกค้าใน POS
description: บทความนี้อธิบายฟังก์ชันที่พร้อมใช้งานในแอปพลิเคชันการขายหน้าร้าน (POS) เพื่อประมวลผลการเบิกสินค้าตามใบสั่งของลูกค้า
author: hhainesms
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 7fd7d08ac59f6fe7381b79d854160188ef1c325a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286369"
---
# <a name="process-customer-order-pickups-in-pos"></a>ประมวลผลการเบิกสินค้าตามใบสั่งของลูกค้าใน POS

[!include [banner](includes/banner.md)]

เมื่อสร้าง [ใบสั่งของลูกค้า](customer-orders-overview.md) เพื่อเบิกสินค้าจากร้านค้า ผู้ใช้ร้านค้าสามารถใช้แอปพลิเคชันการขายหน้าร้าน (POS) เพื่อเริ่มต้นการเบิกสินค้าคงคลัง POS จะรันการรวบรวมข้อมูลการจ่ายเงินขั้นสุดท้ายตามที่ต้องการ นอกจากนี้ สินค้าคงคลังและการลงรายการบัญชีทางการเงินยังจะเสร็จสิ้นตามปริมาณที่เบิกสินค้าด้วย

หากคุณเป็นผู้ใช้ร้านค้า คุณสามารถดําเนินการเบิกสินค้าได้โดยใช้การดําเนินการ **เรียกคืนใบสั่ง** หรือการดําเนินการ **การเติมสินค้าตามใบสั่ง** ใน POS หากร้องการให้การดําเนินการ **เบิกสินค้า** พร้อมใช้งาน คุณต้องดําเนินการตามขั้นตอนใดขั้นตอนหนึ่งต่อไปนี้ก่อน

- เมื่อต้องการใช้การดําเนินการ **เรียกคืนใบสั่ง** ให้ค้นหาและเลือกใบสั่งที่จะถูกเบิกสินค้า
- เมื่อต้องการใช้การดําเนินการ **การเติมสินค้าตามใบสั่ง** ให้ค้นหาและเลือกบรรทัดใบสั่งหนึ่งบรรทัดหรือมากกว่า

ถ้าใบสั่งหรือรายการใบสั่งที่เลือกไม่ได้รับการตั้งค่าคอนฟิกให้เบิกสินค้าที่ร้านค้าที่ระบุ หรือถ้ามีการเบิกสินค้าตามใบสั่งครบแล้ว การดําเนินการ **เบิกสินค้า** จะไม่พร้อมใช้งาน

![การดำเนินงานเบิกสินค้า](media/pickupoperation.png)

ใน Microsoft Dynamics 365 Commerce รุ่น 10.0.17 และใหม่กว่า คุณลักษณะ **ประสบการณ์ของผู้ใช้ที่ปรับปรุงเพื่อการประมวลผลใบสั่งในการขายหน้าร้าน** สามารถเปิดผ่านการจัดการคุณลักษณะใน Commerce headquarters ถ้าคุณลักษณะนี้ปิดอยู่ ผู้ใช้จะเลือกปริมาณการเบิกสินค้าไม่ได้ ตามค่าเริ่มต้น ปริมาณทั้งหมดที่สั่งไว้ของบรรทัดคือปริมาณที่จะเบิกสินค้า ประสบการณ์นี้อาจเป็นปัญหา เนื่องจากผู้ใช้อาจลืมที่จะเลือกสินค้าบางรายการเพื่อเบิกสินค้าเมื่อเบิกสินค้าผ่านการเติมสินค้าตามใบสั่ง

คุณลักษณะ **ประสบการณ์ของผู้ใช้ที่ปรับปรุงเพื่อการประมวลผลใบสั่งในอยู่ในการขายหน้าร้าน** ช่วยให้ผู้ใช้สามารถควบคุมการเลือกผลิตภัณฑ์ที่จะเบิกสินค้าได้มากกว่า และปริมาณของผลิตภัณฑ์เหล่านั้นที่จะเบิก ผู้ใช้ไม่ต้องเลือกทุกบรรทัดของใบสั่งขายในหน้าการเติมสินค้าตามใบสั่งก่อนที่จะเลือก **เบิกสินค้า** สินค้าทั้งหมดที่สามารถเบิกสินค้าได้จะแสดงขึ้น ผู้ใช้สามารถระบุการเบิกสินค้าได้หลายบรรทัดแม้ว่าจะเลือกรายการผลิตภัณฑ์เพียงรายการเดียว

คุณลักษณะ **ประสบการณ์ของผู้ใช้ที่ปรับปรุงเพื่อการประมวลผลใบสั่งในอยู่ในการขายหน้าร้าน** เปิด และคุณเลือกการดำเนินการ **เบิกสินค้า** กล่องโต้ตอบ **การเบิกสินค้า** จะปรากฏขึ้น คุณสามารถเลือกสินค้าและปริมาณที่จะเบิกสินค้าได้ ตามค่าเริ่มต้น ปริมาณที่สั่งใด ๆ ที่มีสินค้าคงคลังในสถานะเบิกสินค้าหรือที่บรรจุจะถือว่ามีสิทธิ์เบิกสินค้า โดยค่าเริ่มต้น ปริมาณจะถูกตั้งค่าเป็นปริมาณการเบิกสินค้า คุณสามารถเปลี่ยนปริมาณที่ป้อนได้ ถ้าปริมาณไม่ใช่ 0 (ศูนย์) และไม่เกินปริมาณเปิดรวม (นั่นคือยังไม่ได้ออกใบแจ้งหนี้) ของบรรทัดที่เลือก

![กล่องโต้ตอบการเบิกสินค้า](media/pickupselect.png)

หลังจากที่คุณเลือกปริมาณที่จะเบิกสินค้าแล้วเลือก **เบิกสินค้า** หน้าธุรกรรมจะปรากฏขึ้น หากเปิดคุณลักษณะ [การชำระเงินช่องทาง omni](omni-channel-payments.md) และมีบัตรเครดิตที่ได้รับอนุญาตล่วงหน้าในไฟล์ คุณจะต้องใช้การชำระเงิน

ในหน้าธุรกรรม ระบบจะคํานวณจํานวนเงินที่ครบกําหนดโดยการคํานวณยอดรวมที่ครบกําหนดของสินค้าในการเบิกสินค้าที่เลือก แล้วหักเงินฝากใด ๆ ที่ใช้ก่อนหน้านี้ หรือการจ่ายผ่านบัตรเครดิตที่ได้รับอนุญาต คุณต้องประมวลผลการเบิกสินค้าเพื่อประมวลผลธุรกรรมการเบิกสินค้าให้เสร็จสมบูรณ์ หาก [โครงร่างหน้าจอ](pos-screen-layouts.md) ของหน้าธุรกรรมมีการตั้งค่าคอนฟิกเพื่อให้รวมการดําเนินการ **ธุรกรรมสรุป** และไม่มียอดเงินครบกําหนด คุณสามารถดําเนินธุรกรรมให้เสร็จสมบูรณ์ และไม่มียอดเงินครบกําหนดโดยไม่ได้เลือกวิธีการจ่ายเงิน ถ้าการดําเนินการ **ธุรกรรมสรุป** ไม่พร้อมใช้งาน คุณสามารถเลือกลิงค์ **จำนวนเงินที่ครบกำหนดชำระ $0.00** ในบานหน้าต่าง **ผลรวม** เพื่อสรุปธุรกรรมได้โดยไม่ต้องเลือกวิธีการจ่ายเงิน

![หน้าธุรกรรมสำหรับธุรกรรมการเบิกสินค้าตามใบสั่งของลูกค้า](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>การเปลี่ยนรายการหรือปริมาณการเบิกสินค้า

ถ้าคุณต้องเปลี่ยนปริมาณการเบิกสินค้า หลังจากที่คุณได้เลือกสินค้าที่จะเบิกสินค้าแล้ว คุณสามารถเลือก **ตั้งค่าปริมาณ** คุณไม่สามารถตั้งค่าปริมาณการเบิกสินค้าเป็น **0** (ศูนย์) หรือเพิ่มปริมาณนี้เป็นค่าที่เกินปริมาณที่ยังไม่ได้ออกใบแจ้งหนี้คงเหลือของบรรทัดที่สั่ง เมื่อต้องการลบรายการเบิกสินค้าออกจากรถเข็นธุรกรรม ให้เลือก **ยกเลิกธุรกรรม** ธุรกรรมปัจจุบันจะถูกหยุด และขั้นตอนการดําเนินการ **การเบิกสินค้า** จะถูกเริ่มต้นใหม่

ถ้าเปิดคุณลักษณะ **ประสบการณ์ของผู้ใช้ที่ปรับปรุงเพื่อการประมวลผลใบสั่งในอยู่ในการขายหน้าร้าน** องค์กรสามารถเพิ่มปุ่มสำหรับการดำเนินการ **เปลี่ยนรายการเบิกสินค้า** ไปยังโครงร่างของหน้าธุรกรรมได้ หลังจากที่คุณสร้างรถเข็นธุรกรรมการเบิกสินค้าใน POS และเลือกสินค้าแล้ว คุณสามารถเลือก **เปลี่ยนรายการเบิกสินค้า** ได้หากคุณต้องเปลี่ยนสินค้าเบิกสินค้า แต่ไม่ต้องการยกเลิกธุรกรรมทั้งหมด ในกล่องโต้ตอบ **เปลี่ยนรายการเบิกสินค้า** ที่ปรากฏ คุณสามารถเปลี่ยนสินค้าและปริมาณการเบิกสินค้าได้ จากนั้นรถเข็นธุรกรรมจะถูกอัปเดตเพื่อสะท้อนการเปลี่ยนแปลงของคุณ

![กล่องโต้ตอบการเปลี่ยนรายการเบิกสินค้า](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
