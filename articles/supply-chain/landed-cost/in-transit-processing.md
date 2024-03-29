---
title: การประมวลผลสินค้าที่อยู่ระหว่างส่งต่อ
description: บทความนี้อธิบายวิธีการทำงานกับใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ เมื่อตั้งค่าใบสั่งหรือการเดินทางให้ใช้การประมวลผลสินค้าที่อยู่ระหว่างการส่งต่อ คุณสามารถออกใบแจ้งหนี้สินค้าก่อนที่จะได้รับสินค้าในคลังสินค้าเพื่อปริมาณการใช้ได้
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 47e5ef2ef99fcf23af73cfdb6ec57b92ad62f18c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854397"
---
# <a name="goods-in-transit-processing"></a>การประมวลผลสินค้าที่อยู่ระหว่างส่งต่อ

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายวิธีการทำงานกับใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ ใบสั่งชนิดนี้จะใช้โดยโมดูล **ต้นทุนแฝง** เท่านั้น เมื่อตั้งค่าใบสั่งหรือการเดินทางให้ใช้การประมวลผลสินค้าที่อยู่ระหว่างการส่งต่อ คุณไม่ต้องรอจนได้รับสินค้าในคลังสินค้าก่อนที่จะสามารถออกใบเจ้งหนี้ได้ แต่สินค้าจะถูกออกใบแจ้งหนี้เมื่อออกจากคลังสินค้าหรือพอร์ตต้นทางของผู้จัดจำหน่าย และรับรู้ต้นทุนทางการเงินเมื่อการเดินทางเริ่มต้น ฟังก์ชันนี้ช่วยให้คุณสามารถเป็นเจ้าของสินค้าคงคลังได้อย่างถูกต้อง เนื่องจากสินค้ามักกลายเป็นคุณสมบัติขององค์กรเมื่อออกจากพอร์ตการจัดส่ง

เมื่อมีการใช้ใบสั่งสินค้าที่อยู่ระหว่างการส่งต่อ จะได้รับรายการที่อัปเดตทางการเงินในคลังสินค้าระหว่างกาล ซึ่งเรียกอีกอย่างว่าคลังสินค้าที่อยู่ระหว่างการส่งต่อ จากนั้นสินค้าจะอยู่ในคลังสินค้านี้จนกว่าจะได้รับสินค้าที่คลังสินค้าปลายทางสุดท้าย (นั่นคือ คลังสินค้าที่กําหนดไว้ในรายการซื้อ) ไม่สามารถลบออกด้วยตัวเองได้

หากสินค้าอยู่ระหว่างการส่งต่อ สินค้านั้นจะไม่พร้อมใช้งานในสินค้าคงคลัง และไม่สามารถเบิกจากสินค้าคงคลังเพื่อจัดส่งได้ อย่างไรก็ตาม คุณสามารถดูสินค้าคงคลังที่อยู่ระหว่างการส่งต่อได้ คุณยังสามารถใช้สินค้าเพื่อวางแผนหลักได้ ในกรณีนี้ ให้ใช้วันที่จัดส่งที่ยืนยันในบรรทัดใบสั่งซื้อเป็นวันที่คาดไว้ เมื่อสินค้าคงคลังจะพร้อมใช้งาน

ส่วนต่อไปนี้จะอธิบายการตั้งค่าที่ต้องใช้ในการประมวลผลสินค้าคงคลังและการเดินทาง โดยใช้แนวคิดและฟังก์ชันของสินค้าที่อยู่ระหว่างการส่งต่อ

## <a name="terms-of-delivery"></a>เงื่อนไขการจัดส่ง

เมื่อคุณเปิดใช้งานโมดูล **ต้นทุนแฝง** เอนทิตี้ *เงื่อนไขการจัดส่ง* มาตรฐานจะถูกปรับปรุงเพื่อสนับสนุนคุณลักษณะสินค้าที่อยู่ระหว่างการส่งต่อ

เมื่อตั้งค่าตัวเลือก **การจัดการสินค้าที่อยู่ระหว่างส่งต่อ** เป็น *ใช่* สำหรับเรกคอร์ดเงื่อนไขการจัดส่งที่ใช้ได้ สินค้าจะถูกวางลงในคลังสินค้าที่อยู่ระหว่างการส่งต่อ การดำเนินการนี้จะทริกเกอร์เฉพาะเมื่อการรับสินค้าคงคลังไม่มีการประมวลผลก่อนที่จะมีการประมวลผลใบแจ้งหนี้ เมื่อเงื่อนไขการจัดส่งของใบสั่งได้รับการตั้งค่าเพื่อใช้สินค้าที่อยู่ระหว่างการส่งต่อ ผู้ใช้จะไม่สามารถลงรายการบัญชีใบรับสินค้าของใบสั่งซื้อได้อีกต่อไป หากพวกเขาพยายาม จะเกิดข้อผิดพลาดขึ้น ข้อความแสดงข้อผิดพลาดระบุว่าต้องใช้ฟังก์ชันสินค้าที่อยู่ระหว่างการส่งต่อเพื่อดําเนินการต่อ

เมื่อต้องการใช้งานข้อมูลเงื่อนไขการจัดส่งเกี่ยวกับสินค้าที่อยู่ระหว่างส่งต่อ ให้ไปที่ **การจัดซื้อและการจัดหา \> ตั้งค่า \> การกระจายสินค้า \> เงื่อนไขการจัดส่ง** ตารางต่อไปนี้อธิบายฟิลด์ที่โมดูล **ต้นทุนแฝง** เพิ่มที่หน้า **เงื่อนไขการจัดส่ง** เพื่อสนับสนุนฟังก์ชันสินค้าที่อยู่ระหว่างส่งต่อ ทั้งสองฟิลด์อยู่บนแท็บด่วน **ทั่วไป** สำหรับข้อมูลเพิ่มเติมเกี่ยวกับฟิลด์อื่นๆ บนหน้านี้ โปรดดู [เงื่อนไขการจัดส่ง (ฟอร์ม)](/dynamicsax-2012//terms-of-delivery-form)

| ฟิลด์ | คำอธิบาย |
|---|---|
| จำเป็นต้องมีท่าเรือขนส่งสินค้า | ตั้งค่าตัวเลือกนี้เป็น *ใช่* ถ้าพอร์ตการจัดส่งเป็นพอร์ตบังคับ เมื่อเงื่อนไขการจัดส่งมีผลบังคับ |
| การจัดการสินค้าที่อยู่ระหว่างส่งต่อ | ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อใช้การจัดการสินค้าที่อยู่ระหว่างส่งต่อ เมื่อเงื่อนไขการจัดส่งมีผลบังคับ |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>คลังสินค้าสำหรับสินค้าที่อยู่ระหว่างส่งต่อ และขีดจำกัดการรับสินค้าต่ำกว่าปริมาณการสั่ง

เมื่อคุณเปิดใช้งานโมดูล **ต้นทุนแฝง** เอนทิตี้ *คลังสินค้า* มาตรฐาน จะได้รับการปรับปรุงเพื่อเปิดใช้งานใบสั่งซื้อที่จะออกใบแจ้งหนี้ ในขณะที่สินค้าอยู่ใน คลังสินค้าที่อยู่ระหว่างการส่งต่อ

ต้นทุนแฝงจะเพิ่มคลังสินค้าใหม่สองชนิด: *สินค้าที่อยู่ระหว่างส่งต่อ* และ *การจัดส่งน้อยกว่าปริมาณที่สั่ง* คุณสามารถเลือกคลังสินค้าทั้งสองชนิดเป็นคลังสินค้าเริ่มต้นได้ การประมวลผลใบสั่งสินค้าที่อยู่ระหว่างส่งต่อที่เสร็จเรียบร้อยแล้วนั้น กําหนดให้ต้องตั้งค่าคอนฟิกทั้งคลังสินค้าที่อยู่ระหว่างส่งต่อและคลังสินค้าที่การจัดส่งน้อยกว่าปริมาณที่สั่ง บนหน้า **คลังสินค้า** จากนั้น คลังสินค้าเริ่มต้นแต่ละรายการจะใช้กับต้นทนแฝงและสินค้าที่อยู่ระหว่างการส่งต่อ คุณต้องเลือกคลังสินค้าที่อยู่ระหว่างส่งต่อและคลังสินค้าที่การจัดส่งน้อยกว่าปริมาณที่สั่งที่พร้อมใช้งานแต่ละชนิด

ชนิดคลังสินค้า *สินค้าที่อยู่ระหว่างส่งต่อ* จะเชื่อมโยงกับคลังสินค้าที่อยู่ระหว่างส่งต่อของคุณ และคลังสินค้าดังกล่าวจะใช้ในการประมวลผลสินค้าในใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ ก่อนที่จะได้รับสินค้าที่คลังสินค้าปลายทางสุดท้าย โดยทั่วไปแล้ว คลังสินค้าที่อยู่ระหว่างส่งต่อหนึ่งรายการจะเพียงพอเฉพาะกับแต่ละไซต์ หากไซต์และคลังสินค้าเป็นมิติสินค้าคงคลังเพียงมิติเดียวที่ใช้ในการจัดการสินค้าคงคลัง ถ้ามีการใช้มิติสินค้าคงคลังของสถานที่เก็บด้วย ต้องตั้งค่าคลังสินค้าที่อยู่ระหว่างส่งต่อในแต่ละชุดของไซต์และคลังสินค้า จึงสามารถระบุสถานที่เก็บเริ่มต้นได้

หากต้องการใช้งานการตั้งค่าสินค้าที่อยู่ระหว่างส่งต่อของคลังสินค้าของคุณ ให้ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การแบ่งสินค้าคงคลัง \> คลังสินค้า** ตารางต่อไปนี้อธิบายฟิลด์ที่โมดูล **ต้นทุนแฝง** เพิ่มที่หน้า **คลังสินค้า** เพื่อสนับสนุนฟังก์ชันสินค้าที่อยู่ระหว่างส่งต่อ ทั้งสองฟิลด์จะปรากฎบนแท็บด่วน **ทั่วไป** สำหรับข้อมูลเพิ่มเติมเกี่ยวกับฟิลด์อื่นๆ บนหน้า โปรดดู [คลังสินค้า (ฟอร์ม)](/dynamicsax-2012//warehouses-form)

| ฟิลด์ | คำอธิบาย |
|---|---|
| คลังสินค้าของสินค้าที่อยู่ระหว่างส่งต่อ | ระบุคลังสินค้าที่อยู่ระหว่างส่งต่อที่เกี่ยวข้องกับคลังสินค้าหลัก |
| คลังสินค้าที่อยู่ระหว่างการจัดส่ง | ระบุคลังสินค้าการจัดส่งน้อยกว่าปริมาณที่สั่งที่เกี่ยวข้องกับคลังสินค้าหลัก |

## <a name="posting-rules-for-landed-cost"></a>กฎการลงรายการบัญชีของต้นทุนแฝง

ต้นทุนแฝงจะเพิ่มกฎการลงรายการบัญชีใหม่สองกฎ ที่คุณสามารถตั้งค่าคอนฟิกได้ กฎการลงรายการบัญชีเหล่านี้ใช้เพื่อลงรายการบัญชีจำนวนเงินในใบแจ้งหนี้ของใบสั่งซื้อโดยตรง เพื่อระบุความเป็นเจ้าของของสินค้าเมื่อออกจากต้นทาง กระบวนการนี้แทนที่แนวคิด *สินค้าที่ได้รับแล้วแต่ยังไม่ได้ออกใบแจ้งหนี้* เนื่องจากสินค้าได้รับการออกใบแจ้งหนี้ก่อนที่จะได้รับ <!-- KFM: Add a link to the related scenario when available. -->

เมื่อต้องการใช้งานโพรไฟล์การลงรายการบัญชี ให้ไปที่ **การจัดการสินค้าคงคลัง \> การตั้งค่า \> การลงรายการบัญชี \> การลงรายการบัญชี** บนแท็บ **ใบสั่งซื้อ** กฎการลงรายการบัญชีใหม่ต่อไปนี้จะพร้อมใช้งาน

- **ต้นทุนแฝง สินค้าที่อยู่ระหว่างส่งต่อ** – ระบุกฎการลงรายการบัญชีของการจัดการสินค้าที่อยู่ระหว่างส่งต่อ
- **ต้นทุนแฝง การรับรู้ค่าธรรมเนียมต้นทุน** – ระบุกฎการลงรายการบัญชีสำหรับการรับรู้บัญชีค่าธรรมเนียม

## <a name="goods-in-transit-orders"></a>ใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ

คุณสามารถตรวจทานและจัดการใบสั่งสินค้าที่อยู่ระหว่างการส่งต่อได้โดยตรงในโมดูล **ต้นทุนแฝง** คุณสามารถประมวลผลใบสั่งสินค้าที่อยู่ระหว่างส่งต่อได้โดยตรงจากหน้า **ใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ** หรือคุณสามารถไปที่การเดินทางที่สัมพันธ์กับใบสั่งสินค้าที่อยู่ระหว่างการส่งต่อ และประมวลผลการเดินทาง คอนเทนเนอร์จัดส่ง หรือใบแจ้งรายการทั้งหมด เมื่อคุณออกใบแจ้งกนี้การเดินทางและสร้างใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ ใบสั่งสินค้าที่อยู่ระหว่างส่งต่อใหม่จะถูกสร้างขึ้นในแต่ละชุดของสินค้าคงคลังและมิติสินค้าคงคลังที่สัมพันธ์กับบรรทัดใบสั่งซื้อ

การจัดการสินค้าที่อยู่ระหว่างการส่งต่อ ต้นทุนแฝง จะใช้กระบวนงานสองขั้นตอน ดังนี้:

1. ได้รับสินค้าเมื่อมีการประมวลผลใบแจ้งหนี้สินค้าคงคลัง และมอบหมายสถานะของ *อยู่ระหว่างการส่งต่อ*
1. ใบสั่งสินค้าที่อยู่ระหว่างส่งต่อจะถูกประมวลผลบนหน้า **ใบสั่งสินค้าที่อยู่ระหว่างการส่งต่อ** แล้วได้รับในคลังสินค้าที่ระบุไว้ในใบสั่งซื้อ ณ จุดนั้น สถานะจะเปลี่ยนเป็น *ได้รับแล้ว*

เมื่อต้องการใช้งานใบสั่งสินค้าที่อยู่ระหว่างการส่งต่อ ให้ไปที่ **ต้นทุนแฝง \> งานประจำงวด \> ใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ**

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>การรับสินค้าคงคลังจากคลังสินค้าที่อยู่ระหว่างส่งต่อ

คุณสามารถรับสินค้าจากใบสั่งสินค้าที่อยู่ระหว่างการส่งต่อได้หลายวิธี ขึ้นอยู่กับการตั้งค่าระบบของคุณ

### <a name="in-transit-receiving"></a>การรับสินค้าที่อยู่ระหว่างส่งต่อ

คุณสามารถรับสินค้าแบบส่งต่อจากหน้าใดๆ ต่อไปนี้:

- บนหน้า **ใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ** ให้เลือกบรรทัด แล้วในบานหน้าต่างการดำเนินการ ให้เลือก **รับ**
- ในหน้า **การเดินทางทั้งหมด** ให้เลือกหรือเปิดการเดินทาง จากนั้น ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดการ** ในกลุ่ม **สินค้าที่อยู่ระหว่างส่งต่อ** ให้เลือก **รับสินค้าที่อยู่ระหว่างส่งต่อ**
- บนหน้า **คอนเทนเนอร์จัดส่งทั้งหมด** ให้เลือกหรือเปิดคอนเทนเนอร์จัดส่ง จากนั้น ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดการ** ในกลุ่ม **สินค้าที่อยู่ระหว่างส่งต่อ** ให้เลือก **รับสินค้าที่อยู่ระหว่างส่งต่อ**
- ในหน้า **ใบแจ้งรายการทั้งหมด** ให้เลือกหรือเปิดใบแจ้งรายการ จากนั้น ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดการ** ในกลุ่ม **สินค้าที่อยู่ระหว่างส่งต่อ** ให้เลือก **รับสินค้าที่อยู่ระหว่างส่งต่อ**

> [!NOTE]
> การรับสินค้าที่อยู่ระหว่างส่งต่อ มักใช้ในสถานการณ์ที่ไม่ได้ใช้สถานที่และการติดตามชุดงาน/หมายเลข

### <a name="arrival-journal"></a>สมุดรายวันการมาถึง

คุณยังสามารถรับสินค้าโดยการสร้างสมุดรายวันการมาถึงได้ด้วย คุณสามารถสร้างสมุดรายวันการมาถึงได้โดยตรงจากหน้าการเดินทาง แนวทางปฏิบัติที่องค์กรของคุณสร้างขึ้นเพื่อกำหนดว่ามีการใช้สมุดรายวันการมาถึงในการรับสินค้าหรือไม่

1. เปิดการเดินทาง คอนเทนเนอร์ หรือใบแจ้งรายการ
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดการ** ในกลุ่ม **ฟังก์ชัน** ให้เลือก **สร้างสมุดรายวันการมาถึง**
1. ในกล่องโต้ตอบ **สร้างสมุดรายวันการมาถึง** ให้ตั้งค่าต่อไปนี้:

    - **เริ่มต้นปริมาณ** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อตั้งค่าปริมาณจากปริมาณการส่งต่อ ถ้าตั้งค่าตัวเลือกนี้ เป็น *ไม่* จะไม่มีการตั้งค่าปริมาณเริ่มต้นจากบรรทัดสินค้าที่อยู่ระหว่างส่งต่อ
    - **สร้างจากสินค้าที่อยู่ระหว่างส่งต่อ** - ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อยกปริมาณจากบรรทัดการส่งต่อที่เลือกให้กับการเดินทาง คอนเทนเนอร์ หรือใบแจ้งรายการที่เลือก
    - **สร้างจากบรรทัดใบสั่ง** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อตั้งค่าปริมาณเริ่มต้นในสมุดรายวันการมาถึงจากบรรทัดใบสั่งซื้อ สามารถตั้งค่าปริมาณเริ่มต้นในสมุดรายวันการมาถึงได้ด้วยวิธีนี้ เฉพาะเมื่อปริมาณในบรรทัดใบสั่งซื้อตรงกับปริมาณในใบสั่งสินค้าที่อยู่ระหว่างส่งต่อเท่านั้น

1. ประมวลผลสมุดรายวันการมาถึง ตามที่อธิบายไว้ใน [ลงทะเบียนการรับสินค้าด้วยสมุดรายวันการมาถึงของสินค้า](/dynamicsax-2012/appuser-itpro/register-item-receipts-with-an-item-arrival-journal)

> [!NOTE]
> โดยทั่วไป สมุดรายวันการมาถึงจะใช้ในสถานการณ์ที่มีการใช้สถานที่และการติดตามชุดงาน/หมายเลขลำดับ แต่ไม่ได้ใช้การจัดการคลังสินค้า
>
> ไม่ควรระบุสถานที่รับสินค้าเริ่มต้นบนบรรทัดใบสั่ง ถ้าจะระบุสถานที่รับสินค้าในสมุดรายวันการมาถึง

## <a name="warehouse-management"></a>การจัดการคลังสินค้า

เมื่อคุณเปิดใช้งานโมดูล **ต้นทุนแฝง** จะมีการแก้ไขหน้าหลายหน้าในโมดูล **การจัดการคลังสินค้า** เพื่อให้การประมวลผลใบสั่ง (โดยเฉพาะ การประมวลผลสินค้าที่อยู่ระหว่างส่งต่อ) สามารถเกิดขึ้นได้ผ่านโมดูล **ต้นทุนแฝง** โครงร่างส่วนนี้ฟิลด์และกระบวนการที่เพิ่มในโมดูล **การจัดการคลังสินค้า**

### <a name="mobile-device-menu-items"></a>รายการเมนูของอุปกรณ์เคลื่อนที่

สินค้าสามารถได้รับโดยใช้อุปกรณ์เคลื่อนที่ หากได้ตั้งค่าเมนูอุปกรณ์เคลื่อนที่ และโมดูล **การจัดการคลังสินค้า** ให้รับสินค้าในใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ ส่วนนี้อธิบายการตั้งค่าที่เกี่ยวข้องกับการรับสินค้าที่อยู่ระหว่างส่งต่อ

การตั้งค่าอุปกรณ์เคลื่อนที่ให้กับการประมวลผลสินค้าที่อยู่ระหว่างส่งต่อ ให้ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูอุปกรณ์เคลื่อนที่**

ต้นทุนแฝงเพิ่มกระบวนการสร้างงานต่อไปนี้ลงในรายการเมนูของอุปกรณ์เคลื่อนที่ เพื่อสนับสนุนการประมวลผลสินค้าที่อยู่ระหว่างส่งต่อ:

- การรับสินค้าสำหรับสินค้าที่อยู่ระหว่างส่งต่อ
- การรับสินค้าและการสำรองสินค้าที่อยู่ระหว่างส่งต่อ

การตั้งค่าคอนฟิกของกระบวนการเหล่านี้มีลักษณะคล้ายกับการตั้งค่าของ [กระบวนการสร้างงานการรับและสำรองใบสั่งซื้อ](/dynamicsax-2012/appuser-itpro/configure-mobile-devices-for-warehouse-work) อย่างไรก็ตาม กระบวนการ *การรับสินค้าและสำรองสินค้าที่อยู่ระหว่างส่งต่อ* ยังเพิ่มฟิลด์ต่อไปนี้ด้วย

- **เปิดใช้งานคอนเทนเนอร์การจัดส่งเสร็จสมบูรณ์** – ถ้าตัวเลือกนี้ถูกตั้งค่าเป็น *ใช่* เมื่องานการสำรองสินค้าเสร็จสมบูรณ์ แอป Warehouse Management บนมือถือจะแสดงตัวเลือกเพิ่มเติมชื่อ **คอนเทนเนอร์จัดส่งเสร็จสมบูรณ์** เมื่อเลือกตัวเลือกนี้ ผู้ปฏิบัติงานจะถูกขอให้ยืนยันว่าคอนเทนเนอร์นั้นสมบูรณ์ ในจุดนั้น การรับสินค้าสั้นๆ ทั้งหมดจะถูกประมวลผลเป็นภายใต้ธุรกรรม

### <a name="location-directives"></a>คำสั่งสถานที่

ต้นทุนแฝงเพิ่มชนิดใบสั่งงานใหม่ที่ชื่อ *สินค้าอยู่ระหว่างส่งต่อ* ไปยังหน้า **คำสั่งสถานที่** ควรตั้งค่าคอนฟิกชนิดใบสั่งงานนี้ในลักษณะเดียวกับ [ชนิดใบสั่งงานของใบสั่งซื้อ](/dynamicsax-2012/appuser-itpro/create-a-work-template)

### <a name="work-templates"></a>เท็มเพลตงาน

ส่วนนี้อธิบายลักษณะต่างๆที่โมดูล **ต้นทุนแฝง** จะเพิ่มไปในแม่แบบงาน

#### <a name="goods-in-transit-work-order-type"></a>ชนิดใบสั่งงานของสินค้าที่อยู่ระหว่างส่งต่อ

ต้นทุนแฝงเพิ่มชนิดใบสั่งงานใหม่ที่ชื่อ *สินค้าอยู่ระหว่างส่งต่อ* ไปยังหน้า **เท็มเพลตงาน** ควรตั้งค่าคอนฟิกชนิดใบสั่งงานนี้ในลักษณะเดียวกับ [เท็มเพลตงานของใบสั่งซื้อ](/dynamicsax-2012/appuser-itpro/create-a-work-template)

#### <a name="work-header-breaks"></a>การแบ่งส่วนหัวของงาน

แม่แบบงานที่มีชนิดใบสั่งงานเป็น *สินค้าที่อยู่ระหว่างการส่งต่อ* สามารถตั้งค่าคอนฟิกให้แบ่งหัวข้องานได้ ในหน้า **แม่แบบงาน** ให้ทำตามหนึ่งในขั้นตอนเหล่านี้

- บนแท็บ **ทั่วไป** ของแม่แบบ ให้ตั้งค่าหัวข้องานสูงสุด ค่าสูงสุดเหล่านี้ใช้ได้ในลักษณะเดียวกันกับค่าสูงสุดของแม่แบบใบสั่งซื้อ (สำหรับข้อมูลเพิ่มเติม ดูที่ [แม่แบบใบสั่งซื้อ](/dynamicsax-2012/appuser-itpro/create-a-work-template))
- ใช้ปุ่ม **แบ่งส่วนหัวของงาน** เพื่อกำหนดว่าระบบควรสร้างส่วนหัวของงานใหม่เมื่อไร ตามฟิลด์ที่ถูกใช้ในการเรียงลำดับ ตัวอย่างเช่น ถ้าต้องการสร้างส่วนหัวของงานสำหรับแต่ละรหัสคอนเทนเนอร์ ให้เลือก **แก้ไขการสอบถาม** บนแถบคำสั่ง แล้วเพิ่มฟิลด์ **รหัสคอนเทนเนอร์** ไปยังแท็บ **การเรียงลำดับ** ของตัวแก้ไขการสอบถาม ฟิลด์ที่มีการเพิ่มลงในแท็บ **การเรียงลำดับ** จะพร้อมใช้งานสำหรับการเลือกเป็น *ฟิลด์การจัดกลุ่ม* เมื่อต้องการตั้งค่าฟิลด์การจัดกลุ่ม ให้เลือก **ตัวแบ่งส่วนหัวของงาน** ในแถบคำสั่ง จากนั้น สำหรับแต่ละฟิลด์ที่คุณต้องการใช้เป็นฟิลด์การจัดกลุ่ม ให้เลือกที่มีเครื่องหมายถูกในคอลัมน์ **จัดกลุ่มตามฟิลด์นี้**

ต้นทุนแฝง [จะก่อให้เกิดการทำธุรกรรมเกิน](over-under-transactions.md) ถ้าปริมาณที่ลงทะเบียนเกินกว่าปริมาณในใบสั่งต้นฉบับ เมื่อหัวข้องานเสร็จสมบูรณ์แล้ว ระบบจะอัพเดตสถานะของธุรกรรมสินค้าคงคลังสำหรับปริมาณการสั่งซื้อหลัก อย่างไรก็ตาม ในครั้งแรกจะอัพเดตปริมาณที่เชื่อมโยงกับธุรกรรมที่เกิน หลังจากที่สินค้าหลักได้ถูกซื้อนั้นอย่างสมบูรณ์แล้ว

ถ้าคุณยกเลิกหัวข้องานในธุรกรรมที่เกินที่มีการลงทะเบียนแล้ว อันดับแรกธุรกรรมที่เกินจะถูกลดลงด้วยปริมาณที่ยกเลิก หลังจากธุรกรรมที่เกินถูกลดเป็นปริมาณเป็น 0 (ศูนย์) เรกคอร์ดจะถูกลบออก และปริมาณเพิ่มเติมใดๆ จะถูกยกเลิกการลงทะเบียนตามปริมาณในใบสั่งหลัก
