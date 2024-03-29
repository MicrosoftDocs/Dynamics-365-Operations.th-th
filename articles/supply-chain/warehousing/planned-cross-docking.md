---
title: การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้
description: บทความนี้จะอธิบายถึงการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้า ซึ่งปริมาณสินค้าคงคลังที่จำเป็นสำหรับใบสั่งจะถูกส่งตรงจากการรับสินค้าหรือการสร้างไปยังท่าออกที่ถูกต้องหรือพื้นที่ที่จัดเตรียม สินค้าคงคลังที่เหลือทั้งหมดจากต้นทางขาเข้าจะถูกส่งไปยังสถานที่เก็บสินค้าที่ถูกต้องโดยผ่านกระบวนการสำรองสินค้าปกติ
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: b530cc1403458775fd330e826a32417d3b03bf25
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334579"
---
# <a name="planned-cross-docking"></a>การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายถึงการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้า การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าคือกระบวนการของคลังสินค้าซึ่งปริมาณสินค้าคงคลังที่จำเป็นสำหรับใบสั่งจะถูกส่งตรงจากการรับสินค้าหรือการสร้างไปยังท่าออกที่ถูกต้องหรือพื้นที่ที่จัดเตรียม สินค้าคงคลังที่เหลือทั้งหมดจากต้นทางขาเข้าจะถูกส่งไปยังสถานที่เก็บสินค้าที่ถูกต้องโดยผ่านกระบวนการสำรองสินค้าปกติ

การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าช่วยให้ผู้ปฏิบัติงานข้ามการสำรองสินค้าขาเข้าและการเบิกสิค้าขาออกของสินค้าคงคลังที่มีการทำเครื่องหมายสำหรับใบสั่งขาออกอยู่แล้ว ดังนั้นจำนวนครั้งที่สินค้าคงคลังถูกสัมผัสจะถูกย่อให้เล็กที่สุดเท่าที่จะเป็นไปได้ นอกจากนี้เนื่องจากมีการโต้ตอบกับระบบน้อยลง การประหยัดเวลาและพื้นที่บนชั้นร้านค้าของคลังสินค้าจะเพิ่มขึ้น

ก่อนที่คุณจะสามารถรันการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าได้ คุณต้องตั้งค่าคอนฟิกเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าใหม่ ซึ่งจะมีการระบุแหล่งที่มาของการจัดหาวัสดุและชุดอื่นๆ ของความต้องการสำหรับการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า เมื่อสร้างใบสั่งขาออกจะต้องมีการทำเครื่องหมายรายการสำหรับใบสั่งขาเข้าที่มีสินค้าเดียวกัน คุณสามารถเลือกฟิลด์รหัสสั่งบนแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าได้ ในลักษณะเดียวกับที่คุณตั้งค่าการเพิ่มเติมสินค้าและใบสั่งซื้อ

ในขณะรับใบสั่งขาเข้า การตั้งค่าการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าจะระบุความต้องการของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและสร้างงานการเคลื่อนย้ายสำหรับปริมาณที่ต้องการโดยขึ้นอยู่กับการตั้งค่าของคำสั่งสถานที่โดยอัตโนมัติ

> [!NOTE]
> รายการความเคลื่อนไหวของสินค้าคงคลังจะ *ไม่* ลงทะเบียนเมื่อมีการยกเลิกการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า ถึงแม้ว่าจะมีการเปิดใช้การตั้งค่าสำหรับความสามารถนี้ในพารามิเตอร์การจัดการคลังสินค้า

## <a name="turn-on-the-planned-cross-docking-features"></a>เปิดใช้งานลักษณะการทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้

ถ้าคุณรัน Supply Chain Management เวอร์ชัน 10.0.28 หรือก่อนหน้านั้น คุณอาจต้องเปิดใช้งานกระบวนการส่งสินค้าผ่านศูนย์เปลี่ยนวัสดุที่วางแผนไว้ก่อนที่คุณจะสามารถใช้ระบบได้ ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดใช้งานคุณลักษณะต่อไปนี้ในลำดับต่อไปนี้:

1. *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้*<br>(เริ่มจาก Supply Chain Management เวอร์ชัน 10.0.29 คุณลักษณะนี้เป็นแบบบังคับ และไม่สามารถปิดได้)
1. *เท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่มีคำสั่งสถานที่*<br>(เริ่มจาก Supply Chain Management เวอร์ชัน 10.0.29 คุณลักษณะนี้จะเปิดตามค่าเริ่มต้น)
    > [!NOTE]
    > คุณลักษณะนี้ช่วยให้สามารถระบุฟิลด์ **รหัสคำสั่ง** บนแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าได้คล้ายกับวิธีการตั้งค่าแม่แบบการเติมสินค้า การเปิดใช้งานคุณลักษณะนี้จะป้องกันคุณไม่ให้เพิ่มรหัสข้อควบคุมบนรายการแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าสำหรับรายการ *เบิกสินค้า* สุดท้าย ซึ่งช่วยให้มั่นใจว่าจะสามารถกําหนดสถานที่ส่งครั้งสุดท้ายระหว่างการสร้างงานก่อนที่จะพิจารณาแม่แบบงาน

## <a name="setup"></a>ตั้งค่า

### <a name="regenerate-load-posting-methods"></a>สร้างวิธีการลงรายการบัญชีการบรรทุกใหม่

การใช้การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้าจะถูกนำมาใช้เป็นวิธีการลงรายการบัญชีการบรรทุก หลังจากที่คุณเปิดใช้งานลักษณะการทำงานแล้ว คุณต้องสร้างวิธีการใหม่

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> วิธีการลงรายการบัญชีการบรรทุก**
1. บนบานหน้าต่างการดำเนินการ เลือก **สร้างวิธีการใหม่**

    เมื่อการดำเนินการเสร็จสมบูรณ์แล้ว คุณควรจะเห็นวิธีการที่มีค่า **ชื่อวิธีการ** *planCrossDocking*

1. ปิดหน้า

### <a name="create-a-cross-docking-template"></a>สร้างเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า**
1. ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างเท็มเพลต
1. บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:

    - **ลำดับ:** *1*

        ฟิลด์นี้จะกำหนดใบสั่งที่จะมีการประเมินเท็มเพลต

    - **รหัสเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า:** *51*
    - **คำอธิบาย:** *คลังสินค้า 51*
    - **นโยบายการนำออกใช้ความต้องการ** *ก่อนใบรับการจัดหาสินค้า*
    - **คลังสินค้า:** *51*

1. การตั้งค่าบนแท็บด่วน **การวางแผน** ควบคุมวิธีการทำงานของเท็มเพลต ตั้งค่าดังต่อไปนี้:

    - **ข้อกำหนดของความต้องการ:** *ไม่มี*

        ฟิลด์นี้จะกำหนดความต้องการของสินค้าคงคลังที่ต้องการ ถ้าต้องการให้มีการเชื่อมโยงความต้องการกับการจัดหาวัสดุก่อนการนำออกใช้ ให้เลือก *การทำเครื่องหมาย* ถ้าต้องการให้มีการจองสินค้าตามความต้องการกับการจัดหาวัสดุก่อนการนำออกใช้ ให้เลือกการ *การจองสินค้าสำหรับใบสั่ง*

    - **ชนิดของการระบุตำแหน่ง:** *สถานที่จัดส่ง*

        ฟิลด์นี้กำหนดว่างานการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าควรใช้สถานที่ที่จัดเตรียม/การบรรทุกจากการจัดส่งหรือไม่ และควรใช้คำสั่งของสถานที่ในการค้นหาสถานที่การจัดเตรียม/การบรรทุกของตนเองหรือไม่

    - **เท็มเพลตงาน** ปล่อยฟิลด์นี้ว่างไว้ได้

        ฟิลด์นี้จะกำหนดเท็มเพลตงานที่ควรใช้เมื่อมีการสร้างงานการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า

    - **ตรวจสอบความถูกต้องของใบรับการจัดหาสินค้าซ้ำ:** *ไม่*

        ตัวเลือกนี้กำหนดว่าควรตรวจสอบความถูกต้องของการจัดหาวัสดุในระหว่างการรับสินค้าหรือไม่ ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ทั้งหน้าต่างเวลาสูงสุดและช่วงวันหมดอายุจะถูกตรวจสอบ

    - **รหัสคำสั่ง:** ให้ปล่อยฟิลด์นี้ว่างไว้

        ตัวเลือกนี้เปิดใช้งานโดยคุณลักษณะ *เทมเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่มีคำสั่งสถานที่* (เริ่มเมื่อ Supply Chain Management เวอร์ชัน 10.0.29 คุณลักษณะจะเปิดไว้ตามค่าเริ่มต้น) ระบบใช้ใบสั่งสถานที่เพื่อช่วยระบุสถานที่ที่ดีที่สุดที่จะย้ายสินค้าคงคลังในการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า คุณสามารถตั้งค่าโดยการกําหนดรหัสข้อกําหนดให้กับแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่เกี่ยวข้องแต่ละแม่แบบ ถ้ามีการกำหนดรหัสสถานที่ ระบบจะไม่ค้นหาคำสั่งสถานที่ตามรหัสสถานที่เมื่อต้องสร้างงาน ด้วยวิธีนี้ คุณสามารถจํากัดข้อความของสถานที่ที่จะใช้กับแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเฉพาะได้

    - **ตรวจสอบความถูกต้องของหน้าต่างเวลา:** *ใช่*

        ตัวเลือกนี้กำหนดว่าควรประเมินหน้าต่างเวลาสูงสุดเมื่อมีการเลือกแหล่งที่มาของการจัดหาวัสดุหรือไม่ ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ฟิลด์ที่เกี่ยวข้องกับหน้าต่างเวลาสูงสุดและหน้าต่างเวลาต่ำสุดจะพร้อมใช้งาน

    - **หน้าต่างเวลาสูงสุด:** *5*

        ฟิลด์นี้กำหนดระยะเวลาสูงสุดที่อนุญาตระหว่างการมาถึงของการจัดหาวัสดุและความต้องการ

    - **หน่วยของหน้าต่างเวลาสูงสุด:** *วัน*
    - **หน้าต่างเวลาต่ำสุด:** *0*

        ฟิลด์นี้กำหนดระยะเวลาต่ำสุดที่อนุญาตระหว่างการมาถึงของการจัดหาวัสดุและความต้องการ

    - **หน่วยของหน้าต่างเวลาต่ำสุด:** *วัน*
    - **ช่วงวันหมดอายุ:** *0*

        *เงื่อนไขที่หมดอายุแรกออกก่อน (FEFO):* ฟิลด์นี้จะกำหนดจำนวนวันสูงสุดระหว่างวันหมดอายุของชุดงานที่หมดอายุแรกที่ปัจจุบันอยู่ในคลังสินค้าและชุดงานที่ได้รับ

1. บนแท็บด่วน **แหล่งที่มาของการจัดหาสินค้า** คุณสามารถระบุชนิดของการจัดหาวัสดุที่มีผลบังคับใช้สำหรับเท็มเพลตนี้ เลือก **สร้าง** แล้วตั้งค่าค่าต่อไปนี้:

    - **หมายเลขลำดับ:** *1*
    - **แหล่งที่มาของการจัดหาสินค้า:** *ใบสั่งซื้อ*

> [!NOTE]
> คุณสามารถตั้งค่าการสอบถามเพื่อควบคุมเมื่อเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าโดยเฉพาะนั้นถูกใช้ การสอบถามเกี่ยวกับเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้ามีเพียง *InventTable* (สินค้า) และ *WHSInventTable* (สินค้า WMS) ที่มีข้อมูลเชื่อมกัน ถ้าคุณต้องการเพิ่มตารางอื่นๆ ในการสอบถาม คุณสามารถเชื่อมต่อโดยใช้เพียง *ตัวเชื่อมที่มีอยู่* หรือ *ตัวเชื่อมที่ไม่มีอยู่*  เมื่อคุณกรองข้อมูลในตารางที่รวม ข้อมูลเรกคอร์ดจากตารางหลักจะถูกดึงมาให้กับแต่ละเรกคอร์ดที่ตรงกันในตารางที่รวม ถ้าชนิดการเชื่อมต่อ *ตัวเชื่อมที่มีอยู่* การค้นหาจะสิ้นสุดหลังจากที่พบการจับคู่ครั้งแรก ตัวอย่างเช่น ถ้าคุณรวมตารางบรรทัดใบสั่งขายกับตารางสินค้า ระบบจะตรวจสอบความถูกต้องและส่งคืนสินค้า ซึ่งมีบรรทัดใบสั่งขายอย่างน้อยหนึ่งบรรทัดที่มีเงื่อนไขที่กําหนด ที่สำคัญคือ ข้อมูลจะถูกดึงมาจากตารางหลัก (สินค้า) ไม่ใช่จากตารางรอง (รายการใบสั่งขาย) ดังนั้น การกรองข้อมูลตามเอกสารต้นทาง เช่น รายการใบสั่งขาย หรือจากลูกค้า จะไม่สามารถทำนอกกรอบได้

### <a name="create-a-work-class"></a>สร้างคลาสงาน

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> คลาสงาน**
1. ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างคลาสงาน
1. ตั้งค่าดังต่อไปนี้:

    - **รหัสคลาสงาน:** *CrossDock*
    - **คำอธิบาย:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*
    - **ชนิดของใบสั่งงาน:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*

### <a name="create-a-work-template"></a>สร้างเท็มเพลตงาน

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**
1. ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังแท็บ **ภาพรวม**
1. บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:

    - **หมายเลขลำดับ:** *1*
    - **เท็มเพลตงาน:** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*
    - **คำอธิบายเท็มเพลตงาน:** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*

1. เลือก **บันทึก** เพื่อให้แท็บด่วน **รายละเอียดเท็มเพลตงาน** พร้อมใช้งาน
1. บนแท็บด่วน **รายละเอียดเท็มเพลตงาน** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด
1. บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:

    - **ชนิดงาน:** *เบิกสินค้า*
    - **รหัสคลาสงาน:** *CrossDock*

1. เลือก **สร้าง** เพื่อเพิ่มบรรทัดอื่นและตั้งค่าค่าดังต่อไปนี้:

    - **ชนิดงาน:** *ส่งสินค้า*
    - **รหัสคลาสงาน:** *CrossDock*

1. เลือก **บันทึก** และยืนยันว่ามีการเลือกกล่องกาเครื่องหมาย **ที่ถูกต้อง** สำหรับเท็มเพลต *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*
1. ไม่บังคับ: เลือก **แก้ไขการสอบถาม** ถ้าคุณต้องการตั้งค่าเงื่อนไขเพื่อควบคุมว่าจะใช้เท็มเพลตเมื่อไรและที่ไหน

    คุณสามารถตั้งค่าการสอบถามเพื่อควบคุมเมื่อเท็มเพลตโดยเฉพาะนั้นถูกใช้ ตัวอย่างเช่น คุณสามารถระบุว่าสามารถใช้เท็มเพลตเพื่องานเฉพาะที่สถานที่ที่ระบุเท่านั้น หากคุณต้องการเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่สถานที่เฉพาะ คุณต้องกรองข้อมูลฟิลด์ **สถานที่เก็บเริ่มต้น** ไม่ใช่ฟิลด์ **สถานที่เก็บ** เนื่องจากการสร้างงานของกระบวนการขาเข้า (การซื้อ การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า และการเติมสินค้า) จะเริ่มต้นจากใส่รายการสินค้า เมื่อสร้างงานขึ้น ผู้ควบคุมสถานที่จะตั้งค่าฟิลด์ **สถานที่** เป็นสถานที่ส่งสินค้า อย่างไนก็ตาม สถานที่เบิกสินค้าจะจัดเก็บอยู่ในฟิลด์ **สถานที่เก็บเริ่มต้น**

> [!NOTE]
> รหัสคลาสงานสำหรับชนิดงาน *การเบิกสินค้า* และ *การวาง* ต้องเหมือนกัน

### <a name="create-location-directives"></a>สร้างคำสั่งสถานที่

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**
1. ในบานหน้าต่างด้านซ้าย ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*
1. ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** แล้วตั้งค่าค่าต่อไปนี้:

    - **หมายเลขลำดับ:** *1*
    - **ชื่อ:** *การวางส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*
    - **ชนิดงาน:** *ส่งสินค้า*
    - **ไซต์:** *5*
    - **คลังสินค้า:** *51*

1. เลือก **บันทึก** เพื่อให้แท็บด่วน **รายการ** พร้อมใช้งาน
1. บนแท็บด่วน **บรรทัด** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด
1. บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:

    - **ปริมาณเริ่มต้น:** *1*
    - **ปริมาณสิ้นสุด:** *1000000*

1. เลือก **บันทึก** เพื่อให้แท็บด่วน **การดำเนินคำสั่งสถานที่** พร้อมใช้งาน
1. บนแท็บด่วน **การดำเนินการของคำสั่งสถานที่** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด
1. บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:

    - **ชื่อ:** *Baydoor*
    - **การใช้สถานที่คงที่:** *สถานที่คงที่และไม่คงที่*

1. เลือก **บันทึก** เพื่อให้ปุ่ม **แก้ไขการสอบถาม** บน **การดำเนินการคำสั่งสถานที่** พร้อมใช้งาน
1. เลือก **แก้ไขการสอบถาม** เพื่อเปิดตัวแก้ไขการสอบถาม
1. บนแท็บ **ช่วง** ให้ตรวจสอบให้แน่ใจว่ามีการตั้งค่าคอนฟิกสองบรรทัดต่อไปนี้:

    - บรรทัดที่ 1:

        - **ตาราง:** *สถานที่*
        - **ตารางที่ได้รับมา:** *สถานที่ตั้ง*
        - **ฟิลด์:** *คลังสินค้า*
        - **เงื่อนไข:** *51*

    - บรรทัดที่ 2:

        - **ตาราง:** *สถานที่*
        - **ตารางที่ได้รับมา:** *สถานที่ตั้ง*
        - **ฟิลด์:** *สถานที่ตั้ง*
        - **เงื่อนไข:** *Baydoor*

1. เลือก **ตกลง** เพื่อปิดตัวแก้ไขการสอบถาม

### <a name="create-a-mobile-device-menu-item"></a>สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**
1. ในรายการเมนูในบานหน้าต่างด้านซ้าย ให้เลือก **การสำรองการซื้อ**
1. เลือก **แก้ไข**
1. บนแท็บด่วน **คลาสงาน** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด
1. บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:

    - **รหัสคลาสงาน:** *CrossDock*
    - **ชนิดของใบสั่งงาน:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*

1. เลือก **บันทึก**

## <a name="scenario"></a>สถานการณ์

### <a name="create-a-purchase-order"></a>สร้างใบสั่งซื้อ

ทำตามขั้นตอนต่อไปนี้เพื่อสร้างใบสั่งซื้อเป็นแหล่งที่มาของการจัดหาวัสดุ

1. ไปที่ **การจัดซื้อและการจัดหา \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**
1. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
1. ในกล่องโต้ตอบ **สร้างใบสั่งซื้อ** ให้ตั้งค่าต่อไปนี้:

    - **บัญชีผู้จัดจำหน่าย:** *104*
    - **คลังสินค้า:** *51*

1. เลือก **ตกลง** แล้วจดบันทึกหมายเลขใบสั่ง
1. มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งซื้อ** บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:

    - **หมายเลขสินค้า:** *A0001*
    - **ปริมาณ:** *5*

### <a name="create-a-sales-order"></a>สร้างใบสั่งขาย

ทำตามขั้นตอนต่อไปนี้เพื่อสร้างใบสั่งขายเป็นแหล่งที่มาของความต้องการ

1. ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**
1. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
1. ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:

    - **บัญชีลูกค้า:** *US-002*
    - **คลังสินค้า:** *51*

1. เลือก **ตกลง**
1. มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งขาย** บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:

    - **หมายเลขสินค้า:** *A0001*
    - **ปริมาณ:** *3*

### <a name="create-planned-cross-docking"></a>สร้างการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้

ทำตามขั้นตอนต่อไปนี้เพื่อสร้างการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้จากใบสั่งขาย

1. ในหน้า **รายละเอียดใบสั่งขาย** สำหรับใบสั่งขายที่คุณเพิ่งสร้างขึ้นในบานหน้าต่างการดำเนินการบนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**

    การดำเนินการนำออกใช้ไปยังคลังสินค้าจะสร้างบรรทัดการจัดส่งและการบรรทุกสำหรับบรรทัดใบสั่งขายและพยายามปันส่วนสินค้าคงคลัง
    
    คุณได้รับข้อความแสดงข้อมูล คุณได้รับข้อความแจ้งเตือนต่อไปนี้: "ไม่มีการสร้างงานสำหรับเวฟ XXXX ดูล็อกประวัติการสร้างงานสำหรับรายละเอียด " ลักษณะการทำงานนี้คาดไว้ เนื่องจากไม่มีสินค้าคงคลังในคลังสินค้า

1. บนแท็บด่วน **รายการใบสั่งขาย** บนเมนู **คลังสินค้า** เลือก **รายละเอียดการจัดส่ง**

    หน้า **รายละเอียดการจัดส่ง** จะปรากฏขึ้นและแสดงการจัดส่งที่สร้างขึ้นสำหรับใบสั่งขาย

1. บนแท็บด่วน **รายการการบรรทุก** โปรดสังเกตว่าฟิลด์ **ปริมาณการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้** ถูกตั้งค่าเป็น *3* เนื่องจากไม่มีสินค้าคงคลังที่มีอยู่ในคลังสินค้า แต่แหล่งที่มาของการจัดหาวัสดุที่ถูกต้องจะมาถึงภายในหน้าต่างเวลาที่กำหนดไว้ในเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า ปริมาณการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่ถูกสร้างขึ้น
1. บนแท็บด่วน **รายการการบรรทุก** ให้เลือก **การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้** เพื่อดูรายละเอียดของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่สร้างขึ้น

## <a name="process-the-cross-docking"></a>ประมวลผลการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>การรับใบสั่งซื้อบนแอปคลังสินค้าบนอุปกรณ์เคลื่อนที่

ระบบจะได้รับปริมาณ 5 จากใบสั่งซื้อไปยังสถานที่รับสินค้าและสร้างงานสองชิ้น

รหัสงานแรกที่สร้างขึ้นมีค่า **ชนิดของใบสั่งงาน** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า* และเชื่อมโยงกับใบสั่งขาย มีปริมาณ 3 และส่งไปยังสถานที่จัดส่งขั้นสุดท้ายเพื่อให้สามารถจัดส่งสินค้าได้ทันที

รหัสงานที่สองที่สร้างขึ้นมีค่า **ชนิดของใบสั่งงาน** *ใบสั่งซื้อ* และเชื่อมโยงกับใบสั่งซื้อ มีปริมาณที่เหลืออยู่ของ 2 ซึ่งไม่ใช่การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและถูกส่งตรงไปยังการสำรองสินค้าไปที่การจัดเก็บ

1. ลงชื่อเข้าใช้อุปกรณ์เคลื่อนที่ในฐานะผู้ใช้ในคลังสินค้า *51*
1. ไปที่ **ขาเข้า \> รับการซื้อ**
1. ในฟิลด์ **PONum** ให้ป้อนหมายเลขใบสั่งซื้อของคุณ
1. ในฟิลด์ **ปริมาณ** ให้ป้อน *5*
1. เลือก **ตกลง**
1. บนหน้าถัดไปให้ตั้งค่าฟิลด์ **สินค้า** เป็น *A0001*
1. เลือก **ตกลง**
1. บนหน้าถัดไปให้ยืนยันค่า **PONum** **สินค้า** และ **ปริมาณ** โดยเลือก **ตกลง**

    คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"

1. เลือก **ยกเลิก** เพื่อออก

### <a name="put-away-to-cross-docking-and-bulk"></a>สำรองสินค้าไปยังการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและจำนวนมาก

ในปัจจุบันรหัสงานทั้งสองจะมีป้ายทะเบียนเป้าหมายเดียวกัน เมื่อต้องการดำเนินการขั้นตอนต่อไปให้เสร็จสมบูรณ์ คุณต้องได้รับรหัสงานและรหัสป้ายทะเบียนเป้าหมาย คุณจะได้รับข้อมูลนี้จากรายละเอียดงานสำหรับบรรทัดใบสั่งซื้อและบรรทัดใบสั่งขาย อีกทางหนึ่งคือคุณสามารถไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน** และกรองข้อมูลสำหรับงานที่มีค่า **คลังสินค้า** เป็น *51*

1. บนอุปกรณ์เคลื่อนที่ ให้ไปที่ **ขาเข้า \> การสำรองการซื้อ** แล้วป้อนป้ายทะเบียนเป้าหมายจากงาน
1. ในฟิลด์ **รหัส** ให้ป้อนรหัสป้ายทะเบียนเป้าหมายจากรายละเอียดงาน

    หน้าการเบิกสินค้าของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าจะแสดงสถานที่เบิกสินค้า (*RECV*) ป้ายทะเบียนเป้าหมาย (*ป้ายทะเบียน*) สินค้า (*A0001*) และปริมาณ (*3*)

1. เลือก **ตกลง**
1. ในฟิลด์ **LP เป้าหมาย** ให้ป้อนป้ายทะเบียนเป้าหมายสำหรับรหัสป้ายทะเบียนที่ควรจะวาง (ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า) ไปยังสถานที่จัดส่ง คุณสามารถเลือกรหัสป้ายทะเบียนใดๆ ที่คุณต้องการ
1. เลือก **ตกลง**
1. บนหน้าถัดไป ในฟิลด์ **รหัส** ให้ป้อนรหัสป้ายทะเบียนเป้าหมาย
1. เลือก **ตกลง**
1. ยืนยันงานสำหรับการเบิกปริมาณ 2 ที่เหลือ แล้วเลือก **ตกลง**
1. บนหน้าถัดไป ให้เลือก **เสร็จสิ้น** เพื่อจบกระบวนการเบิกสินค้าและเริ่มกระบวนการสำรองสินค้า

    แอปบนอุปกรณ์เคลื่อนที่จะนำเสนอที่ตั้งและป้ายทะเบียนที่จะนำสินค้าไปวาง

1. ยืนยันการจัดเก็บจำนวนมากของ **การวาง** โดยการเลือก **ตกลง**
1. บนหน้าถัดไปให้ยืนยัน **การวาง** การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าโดยเลือก **ตกลง**

    คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"

1. เลือก **ยกเลิก** เพื่อออก

ภาพประกอบต่อไปนี้แสดงวิธีการทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่เสร็จสมบูรณ์ที่อาจปรากฏใน Microsoft Dynamics 365 Supply Chain Management

![งานการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเสร็จสมบูรณ์แล้ว](media/PlannedCrossDockingWork.png "การทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเสร็จสมบูรณ์แล้ว")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
