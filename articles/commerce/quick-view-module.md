---
title: โมดูลการแสดงผลแบบด่วน
description: บทความนี้ครอบคลุมถึงโมดูลมุมมองด่วน และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16f4b0aad803434f10a1c0ab8375552772ee534a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286876"
---
# <a name="quick-view-module"></a>โมดูลการแสดงผลแบบด่วน

[!include [banner](includes/banner.md)]

บทความนี้ครอบคลุมถึงโมดูลมุมมองด่วน และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce

โมดูลมุมมองด่วนช่วยให้ผู้ใช้ดูข้อมูลผลิตภัณฑ์ได้อย่างรวดเร็วเมื่อเลือกดูผลิตภัณฑ์ในหน้ารายการ และเพิ่มผลิตภัณฑ์หนึ่งรายการหรือมากกว่าในรถเข็นจากหน้ารายการ โดยไม่ต้องไปที่หน้ารายละเอียดผลิตภัณฑ์ (PDP) โมดูลมุมมองด่วนแสดงภาพรวมของข้อมูลผลิตภัณฑ์ที่ผู้ใช้ต้องมีในการตัดสินใจ "เพิ่มลงในรถเข็น" นอกจากนี้ ยังให้ลิงค์กับ PDP ด้วย เพื่อให้ผู้ใช้สามารถดูรายละเอียดผลิตภัณฑ์เพิ่มเติมและตัวเลือกการซื้อได้

โมดูลมุมมองด่วนได้รับการสนับสนุนโดยโมดูล [คอลเลกชันผลิตภัณฑ์](product-collection-module-overview.md) และ [ผลการค้นหา](search-result-module.md)

> [!IMPORTANT]
> โมดูลมุมมองด่วนพร้อมใช้งาน ณ การเริ่มใช้งาน Commerce รุ่น 10.0.17

ภาพประกอบต่อไปนี้แสดงตัวอย่างของโมดูลมุมมองด่วนบนหน้ารายการผลิตภัณฑ์

![ตัวอย่างของโมดูลมุมมองด่วนบนหน้ารายการผลิตภัณฑ์](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>คุณสมบัติของโมดูล

โมดูลมุมมองด่วนสนับสนุนฟังก์ชันบางอย่างเดียวกับโมดูลกล่องการซื้อ ดังนั้น คุณสมบัติของโมดูลมุมมองด่วนจะคล้ายกับคุณสมบัติของโมดูลกล่องการซื้อ

| คุณสมบัติ | มูลค่า | คำอธิบาย |
|----------------|--------|-------------|
| แท็กหัวเรื่อง | **H1**, **H2**, **H3**, **H4**, **H5**, or **H6** | คุณสมบัตินี้กำหนดป้ายชื่อเรื่องสำหรับชื่อผลิตภัณฑ์ ถ้าโมดูลมุมมองด่วนอยู่ที่ด้านบนของหน้าคุณสมบัตินี้ควรถูกตั้งค่าเป็น **H1** เพื่อให้เป็นไปตามมาตรฐานการเข้าถึง |
| อนุญาตราคาที่กำหนดเอง | **จริง** หรือ **เท็จ** | ถ้าตั้งค่าคุณสมบัตินี้เป็น **จริง** ผู้ใช้สามารถป้อนราคาแบบกำหนดเองได้ |
| ราคาต่ำสุด | เลขจำนวนเต็ม | คุณสมบัตินี้สามารถใช้ได้เฉพาะเมื่อตั้งค่าคุณสมบัติ **อนุญาตราคาแบบกำหนดเอง** เป็น **จริง** เท่านั้น ค่านี้จะกําหนดราคาต่ำสุดที่ผู้ใช้สามารถป้อนได้ ($1) |
| ราคาสูงสุด | เลขจำนวนเต็ม | คุณสมบัตินี้สามารถใช้ได้เฉพาะเมื่อตั้งค่าคุณสมบัติ **อนุญาตราคาแบบกำหนดเอง** เป็น **จริง** เท่านั้น ค่านี้จะกําหนดราคาสูงสุดที่ผู้ใช้สามารถป้อนได้ ($1,000) |

## <a name="commerce-site-builder-settings"></a>การตั้งค่าตัวสร้างไซต์ Commerce

เช่นเดียวกับโมดูลกล่องการซื้อ โมดูลมุมมองด่วนจะมีลักษณะการตั้งค่าที่ **การตั้งค่าไซต์ \> ส่วนขยาย \> เพิ่มผลิตภัณฑ์ลงในรถเข็น** อย่างไรก็ตาม การตั้งค่า **นําทางไปยังหน้ารถเข็น** จะถูกละเว้น เนื่องจากไม่สอดคล้องกันกับวัตถุประสงค์ของโมดูลมุมมองด่วน ซึ่งเป็นการอนุญาตให้ผู้ใช้เรียกดูผลิตภัณฑ์หลายรายการในหน้ารายการและเพิ่มผลิตภัณฑ์เหล่านั้นลงในรถเข็นโดยไม่ย้ายออกจากหน้ารายการ

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>เพิ่มโมดูลมุมมองด่วนไปยังโมดูลการรวบรวมผลิตภัณฑ์

โมดูลมุมมองด่วนสามารถเพิ่มไปโมดูลคอลเลกชันผลิตภัณฑ์และผลการค้นหา

เมื่อต้องการเพิ่มโมดูลมุมมองด่วนไปโมดูลคอลเลกชันผลิตภัณฑ์ในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **หน้า** แล้วเลือกโฮมเพจสำหรับไซต์ Fabrikam
1. ไปที่โมดูล **คอลเลกชันผลิตภัณฑ์** ใดๆ บนโฮมเพจ เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เลือกโมดูล** ให้เลือกโมดูล **มุมมองด่วน** แล้วเลือก **ตกลง**
1. ในบานหน้าต่างคุณสมบัติของโมดูล **มุมมองด่วน** ให้เลือก **หัวข้อ** ในกล่องโต้ตอบ **หัวข้อ** ให้ตั้งค่าฟิลด์ **ระดับหัวข้อ** เป็น **H2** แล้วเลือก **ตกลง**
1. เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของไลบรารีโมดูล](starter-kit-overview.md)

[โมดูลกล่องการซื้อ](add-buy-box.md)

[โมดูลการรวบรวมผลิตภัณฑ์](product-collection-module-overview.md)

[โมดูลผลการค้นหา](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
