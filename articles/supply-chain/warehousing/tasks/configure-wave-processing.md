---
title: ตั้งค่าคอนฟิกตัวอย่างการประมวลผลเวฟ
description: บทความนี้อธิบายตัวอย่างวิธีการตั้งค่าเกณฑ์ที่กำหนดว่า งานใดถูกสร้างสำหรับคลังสินค้าเมื่อมีการประมวลผลเวฟ และเวฟถูกประมวลผลด้วยตนเองหรือโดยอัตโนมัติ
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a8c088f8726573e4b1fcad1944676547391a9bf
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219642"
---
# <a name="configure-wave-processing-example"></a>ตั้งค่าคอนฟิกตัวอย่างการประมวลผลเวฟ

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายตัวอย่างวิธีการตั้งค่าเกณฑ์ที่กำหนดว่า งานใดถูกสร้างสำหรับคลังสินค้าเมื่อมีการประมวลผลเวฟ และเวฟถูกประมวลผลด้วยตนเองหรือโดยอัตโนมัติ คุณกำหนดเกณฑ์โดยการตั้งค่าเท็มเพลตเวฟและการสอบถามที่ตรงกับเวฟ ที่มีรายการที่นำออกใช้ในใบสั่งขาย ใบสั่งผลิต หรือใบสั่งคัมบัง

## <a name="enable-sample-data"></a>เปิดใช้งานข้อมูลตัวอย่าง

เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องใช้ระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../../fin-ops-core/fin-ops/get-started/demo-data.md) มาตรฐาน นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น

## <a name="example-scenario-configure-wave-processing"></a>ตัวอย่างสถานการณ์จำลอง: ตั้งค่าคอนฟิกการประมวลผลเวฟ

สถานการณ์นี้จะแสดงผ่านการตั้งค่าต่างๆ ที่หลากหลาย ซึ่งมีผลกระทบต่อวิธีการสร้าง เติมข้อมูล ประมวลผล และออกใช้เวฟ

1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > เวฟ > เท็มเพลตเวฟ**
1. เลือก **ใหม่**
1. ในฟิลด์ **ชือเท็มเพลตเวฟ** ให้พิมพ์ค่า เมื่อคุณตั้งค่าเท็มเพลตเวฟ คุณระบุลำดับที่เท็มเพลตจะถูกจับคู่กับรายการในใบสั่งขาย ใบสั่งผลิต หรือคัมบัง  เมื่อรายการได้ถูกนำออกใช้ไปยังคลังสินค้า หรือไปยังการผลิต จะใช้เท็มเพลตเวฟแรกที่ตรงกับเกณฑ์ เราขอแนะนำให้คุณใส่เท็มเพลตที่มีเกณฑ์ที่เฉพาะเจาะจงที่สุดที่ด้านบนของรายการ ยิ่งเกณฑ์กว้างขึ้น เป็นไปได้มากขึ้นที่รายการจะตรงกับเกณฑ์ และนี่อาจทำให้รายการถูกกำหนดให้กับเวฟที่ไม่ถูกต้องได้  
1. ในฟิลด์ **คำอธิบายเท็มเพลตเวฟ** ให้พิมพ์ค่าใดค่าหนึ่ง
1. ในฟิลด์ **ไซต์** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกไซต์ 2 ได้  
1. ในฟิลด์ **คลังสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกคลังสินค้า 24 ได้  
1. ตั้งค่าฟิลด์ **การสร้างเวฟอัตโนมัติ** เป็น **ใช่** เลือกตัวเลือกนี้เพื่อสร้างเวฟโดยอัตโนมัติเมื่อใบสั่งขาย ใบสั่งผลิต หรือคัมบังมีการเผยแพร่ไปยังคลังสินค้า  
1. ตั้งค่าตัวเลือก **ประมวลผลเวฟเมื่อนำออกใช้ไปยังคลังสินค้า** เป็น **ใช่** เลือกตัวเลือกนี้เพื่อประมวลผลเวฟโดยอัตโนมัติ และสร้างงานเมื่อบรรทัดถูกนำออกใช้ไปยังคลังสินค้า  
1. ตั้งค่า **ตัวเลือกนำเวฟออกใช้อัตโนมัติ** เป็น **ใช่** เลือกตัวเลือกนี้จะนำออกใช้เวฟโดยอัตโนมัติ  งานการเบิกสินค้ามีสร้าง และทำงานได้บนอุปกรณ์เคลื่อนที่  
1. ตั้งค่า **ตัวเลือกกำหนดให้เปิดเวฟ** เป็น **ใช่** รายการมีการกำหนดให้กับเวฟที่ขึ้นอยู่กับตัวกรองข้อมูลการสอบถามสำหรับเท็มเพลตคลื่น  
1. ตั้งค่า **ตัวเลือกประมวลผลเวฟโดยอัตโนมัติที่ขีดจำกัด** เป็น **ใช่** เลือกตัวเลือกนี้เพื่อประมวลผลเวฟโดยอัตโนมัติเมื่อค่าถึงขีดจำกัดสำหรับน้ำหนัก การจัดส่ง และรายการที่ระบุในกลุ่มฟิลด์ **เกณฑ์เวฟ** ตัวเลือกนี้จะใช้ได้เฉพาะหาก **การจัดส่ง** เลือกในฟิลด์ **ชนิดแม่แบบเวฟ**  
1. ตั้งค่า **ตัวเลือกกำหนดให้การนำงานการเพิ่มเติมสินค้าออกใช้เป็นอัตโนมัติ** เป็น **ใช่** เลือกตัวเลือกนี้เพื่อสร้างงานการเติมสินค้าตามความต้องการ และนำออกใช้โดยอัตโนมัติ คุณต้องเพิ่มวิธีของเวฟการเพิ่มเติมสินค้าไปยังแม่แบบเวฟ และสร้างแม่แบบการเติมสินค้าโดยใช้ชนิด **ความต้องการเวฟ**  
1. ใช้การตั้งค่าในกลุ่มการยื่น **ค่าเริ่มต้น** เพื่อกําหนดแอตทริบิวต์เวฟ แอตทริบิวต์เวฟทำหน้าที่เป็นตัวกรอง เพื่อจำกัดชนิดของสินค้าที่สามารถใช้เวฟได้ ตัวอย่างเช่น คุณสามารถระบุกลุ่มสินค้าได้  
1. ขยายส่วน **วิธีการ** และตั้งค่าการกิจกรรมที่แม่แบบเวฟใช้ วิธีเท็มเพลตเวฟอนุญาตให้คุณควบคุมลำดับของกิจกรรมที่แต่ละเวฟต้องเจอเมื่อมีการประมวลผล ตัวอย่างเช่น คุณอาจมีวิธีสำหรับการเพิ่มเติมสินค้าของเวฟ เมื่อคุณเพิ่มวิธีการ มีการแสดงรายการโดยอัตโนมัติในตำแหน่งที่เหมาะสมในลำดับของขั้นตอน ถ้าคุณได้ตั้งค่าตัวเลือก **การกำหนดให้การนำงานการเพิ่มเติมสินค้าออกใช้เป็นอัตโนมัติ** เป็น **ใช่**, คุณต้องเพิ่มวิธีการเพิ่มเติมสินค้าที่นี่  
1. เลือก **บันทึก**
1. ปิดหน้า
1. ไปที่ **การจัดการคลังสินค้า > การตั้งค่า > พารามิเตอร์การจัดการคลังสินค้า**
1. ขยายส่วน **การประมวลผลเวฟ**
1. ในฟิลด์ **กลุ่มชุดงานการประมวลผลเวฟ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
1. ตั้งค่า **ตัวเลือกประมวลผลเวฟในชุดงาน** เป็น **ใช่**
1. ในฟิลด์ **คอยการล็อค (มิลลิวินาที)** ให้ป้อนตัวเลข ป้อนเวลา ในหน่วยมิลลิวินาที ที่มีขั้นตอนการปันส่วนจะรอทรัพยากรระบบที่ถูกล็อค โดยขั้นตอนอื่นที่ปันส่วน  เมื่อเกินเวลานี้ ไม่มีการประมวลผลคลื่น และข้อผิดพลาดจะแสดงขึ้น  
1. เลือก **บันทึก**
1. ปิดหน้า
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > การควบคุมการผลิต > การตั้งค่า > พารามิเตอร์การควบคุมการผลิต**
1. ในฟิลด์ **นำออกใช้ไปยังคลังสินค้า** ให้เลือกหนึ่งตัวเลือก

    สำหรับใบสั่งขายหรือใบสั่งคัมบัง สินค้าคงคลังต้องถูกจองก่อนที่จะนำใบสั่งออกใช้ไปยังคลังสินค้า  มิฉะนั้น สินค้าหรือรายการการปันส่วนไม่สามารถดำเนินการในเวฟ สำหรับใบสั่งผลิต คุณยังสามารถมีตัวเลือกของการเลือก **การอนุญาตให้จองบางส่วน** ได้ ตัวอย่างเช่น นี่จะมีประโยชน์ถ้าคุณมีวัสดุที่คุณต้องการเพื่อเริ่มต้นการผลิต และจากนั้นสามารถรอคอยจนกระทั่งวัสดุเพิ่มเติมพร้อมใช้งานเพื่อสิ้นสุดกระบวนการ ถ้าคุณเลือกตัวเลือกนี้ คุณต้องทำซ้ำการนำออกใช้ไปยังกระบวนการคลังสินค้าด้วยตัวเอง เมื่อวัสดุเพิ่มเติมพร้อมใช้งาน
1. ปิดหน้า

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [การสร้างและการประมวลผลเวฟ](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
