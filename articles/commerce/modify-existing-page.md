---
title: ปรับเปลี่ยนหน้าไซต์ที่มีอยู่
description: บทความนี้อธิบายวิธีการปรับเปลี่ยนหน้าไซต์ที่มีอยู่ใน Microsoft Dynamics 365 Commerce
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fb5348c2f29625647f06e48233f877a847677486
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286930"
---
# <a name="modify-an-existing-site-page"></a>ปรับเปลี่ยนหน้าไซต์ที่มีอยู่

[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีการปรับเปลี่ยนหน้าไซต์ที่มีอยู่ใน Microsoft Dynamics 365 Commerce

เมื่อคุณต้องปรับเปลี่ยนหน้า ขั้นตอนแรกคือการเปิดขึ้นในโปรแกรมแก้ไขหน้า ไปที่ไซต์ที่มีหน้าของคุณ จากนั้นในรายการของหน้าให้ค้นหาหน้าที่คุณต้องการ ถ้าคุณไม่พบหน้า คุณสามารถใช้ฟังก์ชันการค้นหาที่สมบูรณ์ของเครื่องมือการสร้าง พิมพ์ชื่อหน้าที่ถูกต้องหรือพิมพ์ตัวอักษรสองสามตัวแรกและเครื่องหมายดอกจัน (\*) รายการที่ถูกกรองของหน้าจะปรากฏขึ้น คุณสามารถใช้รายการนี้เพื่อค้นหาหน้าที่คุณต้องการ หลังจากที่คุณพบหน้าที่ถูกต้องแล้ว ให้เลือกชื่อหน้าเพื่อเปิดหน้าในโปรแกรมแก้ไขหน้า

> [!TIP]
> ถ้าหน้าของคุณสามารถมองเห็นได้ในตัวตรวจสอบหน้า คุณสามารถเลือก **แก้ไข** และตรวจสอบหน้า ก่อนที่คุณจะเปิดในโปรแกรมแก้ไขหน้า ด้วยวิธีนี้คุณสามารถตรวจสอบหลายหน้าในเวลาเดียวกันได้

หลังจากที่หน้าเปิดอยู่ในโปรแกรมแก้ไขหน้า คุณต้องตรวจสอบให้แน่ใจว่าได้เช็คเอาท์ไปยังคุณแล้ว แถบคำสั่งในเครื่องมือการสร้างเป็นแบบไดนามิก มีความไวของบริบท และความไวของสถานะ ดังนั้น จะแสดงเฉพาะการดำเนินการที่คุณสามารถดำเนินการบนหน้าในขณะนี้เท่านั้น ตัวอย่างเช่น ถ้าหน้าไม่ได้เช็คเอาท์ไปยังคุณ จะไม่มีปุ่ม **บันทึก** และ **แก้ไขให้เสร็จสิ้น** บนแถบคำสั่ง สถานะของหน้าจะปรากฏขึ้นทางด้านขวาของหน้าต่าง

ถ้าหน้ายังไม่ได้เช็คเอาท์ไปยังคุณ ให้เลือก **แก้ไข** บนแถบคำสั่ง แถบคำสั่งจะเปลี่ยนไปเพื่อให้สะท้อนถึงสถานะใหม่ของหน้า นอกจากนี้คุณยังได้รับการแจ้งเตือนที่ระบุว่าหน้าถูกเช็คเอาท์ไปยังคุณ

ขั้นตอนต่อไปคือทำการเปลี่ยนแปลงจริงของคุณ บ่อยครั้งคุณจะใช้แผนภูมิเค้าร่างของหน้าทางด้านซ้ายเพื่อค้นหาและเลือกโมดูลที่คุณต้องการเปลี่ยนแปลง แล้วทำการเปลี่ยนแปลงในบานหน้าต่างคุณสมบัติทางด้านขวา 

อย่างไรก็ตาม การเปลี่ยนแปลงในบางครั้งอาจเกี่ยวข้องกับการเพิ่มหรือลบแบบจำลองหรือส่วนต่างๆ เมื่อต้องการเพิ่มส่วนหรือโมดูล ให้ใช้แผนภูมิเค้าร่างของหน้าเพื่อค้นหาช่องที่คุณต้องการเพิ่มโมดูลหรือส่วนต่างๆ แล้วเลือกปุ่มจุดไข่ปลา (**...**) สำหรับช่องเสียบดังกล่าว เมนูจะปรากฏขึ้นซึ่งรวมคำสั่งสำหรับการเพิ่มโมดูลหรือส่วน เมื่อต้องการลบโมดูลหรือส่วน ให้ค้นหาและเลือกตัวเลือกในแผนภูมิเค้าร่างของหน้า เลือกปุ่มจุดไข่ปลา แล้วเลือกคำสั่งเพื่อลบโมดูลหรือส่วน

> [!TIP]
> นอกจากนี้คุณยังสามารถดูและแก้ไขคุณสมบัติสำหรับโมดูลใดๆ ที่สามารถมองเห็นได้ในการแสดงตัวอย่างตัวสร้างหน้าการแสดงผลด้วยภาพโดยการเลือกโดยตรง

หลังจากที่คุณทำการเปลี่ยนแปลงและการแสดงตัวอย่างผลกระทบของคุณเสร็จแล้ว คุณควรตรวจสอบในหน้าด้วยการเลือก **แก้ไขให้เสร็จสิ้น** บนแถบคำสั่ง 

เมื่อต้องการเผยแพร่การเปลี่ยนแปลงในทันที ให้เลือก **เผยแพร่** บนแถบคำสั่ง เวอร์ชันที่มีการเช็คอินล่าสุดของหน้าที่คุณแก้ไขได้รับการเผยแพร่และจะพร้อมใช้งานสำหรับผู้ใช้ภายนอกที่ดูไซต์ของคุณ 

## <a name="example-change-the-video-on-the-home-page"></a>ตัวอย่าง: เปลี่ยนวิดีโอบนโฮมเพจ

ตัวอย่างต่อไปนี้แสดงวิธีการปรับเปลี่ยนโฮมเพจโดยการเปลี่ยนวิดีโอที่ปรากฏขึ้นในโมดูลของโปรแกรมเล่นวิดีโอ

1. ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)
1. ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **หน้า**
1. ค้นหาและเลือกหน้าหลัก เพื่อเปิดในโปรแกรมแก้ไขหน้า
1. บนแถบคำสั่ง ให้เลือก **แก้ไข**
1. ในเค้าร่างหน้าให้เลือกช่อง **หลัก**
1. ภายใต้ช่อง **หลัก** ให้ขยายโมดูลคอนเทนเนอร์ของเหลวทั้งหมด
1. ค้นหาและเลือกโมดูลของโปรแกรมเล่นวิดีโอ
1. ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกคุณสมบัติ **วิดีโอ** ตัวเลือกสินทรัพย์จะปรากฏขึ้น
1. ในตัวเลือกสินทรัพย์ ให้เลือกสินทรัพย์วิดีโอที่มีอยู่ หรือเลือก **อัพโหลดสินทรัพย์ใหม่** เพื่ออัพโหลดสินทรัพย์วิดีโอใหม่
1. เลือก **ตกลง**
1. เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**
1. ในฟิลด์ **ข้อคิดเห็น** ป้อน **เปลี่ยนวิดีโอ** แล้วเลือก **ตกลง**
1. เลือก **แสดงตัวอย่าง** เพื่อเเสดงตัวอย่างหน้าที่อัพเดต เมื่อเสร็จสิ้นแล้ว ให้ปิดแท็บการแสดงตัวอย่า งเพื่อกลับไปที่เครื่องมือการสร้าง
1. เลือก **เผยแพร่**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[เพิ่มหน้าไซต์ใหม่](add-new-page.md)

[เลือกเค้าโครงหน้า](select-page-layouts.md)

[จัดการข้อมูลเมตา SEO](manage-seo-metadata.md)

[บันทึก แสดงตัวอย่าง และเผยแพร่หน้า](save-preview-publish-page.md)

[ทำให้หน้าผลิตภัณฑ์สมบูรณ์](enrich-product-page.md)

[เพิ่มข้อมูลหน้าเริ่มต้นของประเภท](enrich-category-page.md)

[ตรวจสอบการเข้าถึงเนื้อหาของหน้า](verify-accessibility.md)

[สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์บน URL](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
