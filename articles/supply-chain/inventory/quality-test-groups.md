---
title: กลุ่มการทดสอบการจัดการคุณภาพ
description: บทความนี้จะอธิบายวิธีการสร้างกลุ่มทดสอบ เพื่อให้สามารถใช้การทดสอบหลายรายการกับใบสั่งตรวจสอบคุณภาพใน Microsoft Dynamics 365 Supply Chain Management
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7722bc92d8c2bf52d6a798a93f07af44037d4e0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857719"
---
# <a name="quality-management-test-groups"></a>กลุ่มการทดสอบการจัดการคุณภาพ

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการสร้างกลุ่มทดสอบ เพื่อให้สามารถใช้การทดสอบหลายรายการกับใบสั่งตรวจสอบคุณภาพใน Microsoft Dynamics 365 Supply Chain Management

คุณใช้หน้า **กลุ่มทดสอบ** เพื่อตั้งค่า แก้ไข และดูกลุ่มการทดสอบ ตลอดจนการทดสอบต่างๆ ที่กำหนดให้กับกลุ่มการทดสอบ ส่วนของหน้าด้านบนจะแสดงกลุ่มการทดสอบ และส่วนด้านล่างจะแสดงการทดสอบที่กำหนดให้กับกลุ่มการทดสอบที่เลือก

คุณกำหนดนโยบายต่างๆ ให้กับกลุ่มการทดสอบ เช่น แผนการสุ่มตัวอย่าง ระดับคุณภาพที่ยอมรับได้ (AQL) และความจำเป็นสำหรับการทดสอบแบบทำลาย จากนั้น เมื่อคุณกำหนดการทดสอบแต่ละรายการกับกลุ่มการทดสอบ คุณต้องกำหนดข้อมูลเพิ่มเติม เช่น ลำดับ เอกสาร และวันที่ที่มีผลใช้ สำหรับการทดสอบเชิงปริมาณ ข้อมูลที่คุณกำหนดจะประกอบด้วยค่าการประเมินที่ยอมรับได้ สำหรับการทดสอบเชิงคุณภาพ ข้อมูลนี้รวมถึงตัวแปรทดสอบและผลลัพธ์เริ่มต้น

กลุ่มการทดสอบที่กำหนดให้กับใบสั่งตรวจสอบคุณภาพกำหนดชุดค่าเริ่มต้นของการทดสอบที่ต้องดำเนินการกับสินค้าที่ระบุ อย่างไรก็ตาม คุณสามารถเพิ่ม ลบ หรือเปลี่ยนการทดสอบสำหรับใบสั่งตรวจสอบคุณภาพ ระบบจะรายงานผลการทดสอบสำหรับการทดสอบแต่ละรายการบนใบสั่งตรวจสอบคุณภาพ

เมื่อคุณกําหนดกลุ่มทดสอบ คุณสามารถเลือกที่จะระบุการสุ่มตัวอย่างสินค้าได้ การสุ่มตัวอย่างสินค้าใช้ในการกําหนดจํานวนของผลิตภัณฑ์ที่ต้องทดสอบ สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การสุ่มตัวอย่างสินค้าการจัดการคุณภาพ](quality-item-sampling.md) คุณยังสามารถระบุว่าการทดสอบในกลุ่มการทดสอบเป็นแบบทำลายหรือไม่ ในการทดสอบโดยการทำลาย การสุ่มตัวอย่างสินค้าจะถูกทำลายและปริมาณจะถูกลบออกจากปริมาณคงคลังคงเหลือ

## <a name="example-of-a-test-group"></a>ตัวอย่างของกลุ่มการทดสอบ

บริษัทผู้ผลิตแห่งหนึ่งกำหนดกลุ่มการทดสอบสำหรับความผันแปรต่างๆ ของคำแนะนำด้านคุณภาพ  กลุ่มการทดสอบต่าง ๆ สะท้อนถึงผลต่างในแผนการสุ่มตัวอย่าง ชุดของการทดสอบที่ต้องดำเนินการพร้อมกัน AQL และปัจจัยอื่น ๆ สำหรับการทดสอบเชิงปริมาณ ยังมความแตกต่างของค่าการประเมินที่ยอมรับได้ เพื่อบังคับใช้หลักเกณฑ์ด้านคุณภาพ บริษัทกําหนดกลุ่มการทดสอบให้กับกฎแต่ละกฎที่ใช้ในการสร้างใบสั่งตรวจสอบคุณภาพในหน้า **การเชื่อมโยงคุณภาพ** โดยอัตโนมัติ และกําหนดกลุ่มการทดสอบให้กับใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเอง

## <a name="create-a-test-group"></a>สร้างกลุ่มทดสอบ

เมื่อต้องการสร้างกลุ่มการทดสอบ ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> กลุ่มการทดสอบ**
1. ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริดในส่วนด้านบนของหน้า จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:

    - **กลุ่มการทดสอบ** – ป้อนรหัสหรือชื่อเฉพาะสำหรับกลุ่มการทดสอบ
    - **คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของกลุ่มการทดสอบ
    - **ระดับคุณภาพที่ยอมรับได้** – ป้อนเปอร์เซ็นต์รวมของผลการทดสอบที่ต้องผ่านเพื่อให้ถือว่ากลุ่มการทดสอบผ่าน
    - **การสุ่มตัวอย่างสินค้า** – เลือกการสุ่มตัวอย่างสินค้า สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การสุ่มตัวอย่างสินค้าการจัดการคุณภาพ](quality-item-sampling.md)
    - **แบบทำลาย** – เลือกกล่องกาเครื่องหมายนี้เพื่อบ่งชี้ว่ากลุ่มการทดสอบจะทำลายสินค้าที่มีการทดสอบ

1. ขณะที่ยังคงเลือกแถวใหม่อยู่ ให้เลือกแท็บ **ทั่วไป** ในส่วนบนของหน้า การตั้งค่าบางอย่างของกลุ่มทดสอบที่เลือกบนแท็บ **ภาพรวม** จะซ้ำกันที่นี่ นอกจากนี้ คุณสามารถตั้งค่าฟิลด์ต่อไปนี้สำหรับกลุ่ม:

    - **อัปเดตแอททริบิวต์ของชุดงานสินค้าคงคลัง** – เมื่อคุณตั้งค่าตัวเลือกนี้เป็น *ใช่* ที่นี่ จะมีการตั้งค่าแอททริบิวต์นี้เป็น *ใช่* โดยอัตโนมัติเฉพาะการทดสอบใหม่ทุกการทดสอบที่เพิ่มในกลุ่มการทดสอบในส่วนล่างของหน้า
    - **อัปเดตการโอนการครอบครองชุดงาน** – เมื่อคุณตั้งค่าตัวเลือกนี้เป็น *ใช่* ถ้าสินค้าที่ทดสอบเป็นการควบคุมชุดงาน การโอนการครอบครองชุดงานจะถูกอัปเดตโดยอัตโนมัติด้วยค่าที่เลือกไว้ในฟิลด์ **การโอนการครอบครองชุดงานของใบสั่งตรวจสอบคุณภาพที่ไม่ผ่าน** หรือฟิลด์ **การโอนการครอบครองชุดงานของใบสั่งตรวจสอบคุณภาพที่ผ่านแล้ว**
    - **การโอนการครอบครองชุดงานของใบสั่งตรวจสอบคุณภาพที่ไม่ผ่าน** – เลือกรหัสการโอนการครอบครองชุดงานที่ควรมอบหมายเมื่อใบสั่งตรวจสอบคุณภาพที่มีกลุ่มทดสอบนี้ล้มเหลว เนื่องจากรหัสดังกล่าวไม่ตรงกับ AQL
    - **การโอนการครอบครองชุดงานของใบสั่งตรวจสอบคุณภาพที่ผ่าน** – เลือกรหัสการโอนการครอบครองชุดงานที่ควรมอบหมายเมื่อใบสั่งตรวจสอบคุณภาพที่มีกลุ่มทดสอบนี้ผ่าน เนื่องจากรหัสดังกล่าวตรงกับ AQL
    - **อัปเดตสถานะสินค้าคงคลัง** – เมื่อคุณตั้งค่าตัวเลือกนี้เป็น *ใช่* ถ้า **สถานะสินค้าคงคลัง** เปิดใช้งานบนกลุ่มมิติการจัดเก็บของสินค้าที่มีการทดสอบ สถานะจะถูกอัปเดตโดยอัตโนมัติด้วยสถานะที่เลือกไว้ในฟิลด์ **สถานะใบสั่งตรวจสอบคุณภาพที่ล้มเหลว** หรือฟิลด์ **สถานะของใบสั่งตรวจสอบคุณภาพที่ผ่านแล้ว**
    - **สถานะใบสั่งตรวจสอบคุณภาพที่ไม่ผ่าน** – เลือกสถานะสินค้าคงคลังที่ควรมอบหมายแก่สินค้าเมื่อใบสั่งตรวจสอบคุณภาพที่มีกลุ่มทดสอบนี้ล้มเหลว เนื่องจากรหัสดังกล่าวไม่ตรงกับ AQL
    - **สถานะใบสั่งตรวจสอบคุณภาพที่ผ่าน** – เลือกสถานะสินค้าคงคลังที่ควรมอบหมายแก่สินค้าเมื่อใบสั่งตรวจสอบคุณภาพที่มีกลุ่มทดสอบนี้ผ่าน เนื่องจากรหัสดังกล่าวตรงกับ AQL

## <a name="add-a-qualitative-test-to-a-test-group"></a>เพิ่มการทดสอบเชิงคุณภาพลงในกลุ่มการทดสอบ

ในการเพิ่มการทดสอบเชิงคุณภาพเข้าในกลุ่มการทดสอบ ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> กลุ่มการทดสอบ**
1. บนแท็บ **ภาพรวม** ในส่วนบนของหน้า ให้เลือกกลุ่มการทดสอบที่คุณต้องการเพิ่มการทดสอบ
1. ในส่วนล่างของหน้า บนแท็บ **ภาพรวม** ให้เลือก **เพิ่ม** บนแถบเครื่องมือ เพื่อเพิ่มแถวที่กริด จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:

    - **หมายเลขลำดับ** – ป้อนเลขจํานวนเต็ม เพื่อระบุลำดับที่ควรปฏิบัติในการทดสอบ การทดสอบที่มีหมายเลขลำดับน้อยกว่าจะถูกรันก่อนการทดสอบที่มีหมายเลขลำดับที่มากกว่า

        > [!NOTE]
        > ขอแนะนาว่าคุณควรเว้นช่องว่างระหว่างหมายเลขลำดับ ตัวอย่างเช่น ตั้งค่าฟิลด์ **หมายเลขลำดับ** เป็น *10* ของการทดสอบแรกของคุณ แล้วเพิ่มค่านี้ทีละ 10 ในการทดสอบเพิ่มเติม ด้วยวิธีนี้ คุณสามารถเพิ่มการทดสอบใหม่ในภายหลังได้โดยไม่ต้องลบและสร้างรายการใหม่เพื่อวางการทดสอบเหล่านั้นในลำดับที่ต้องการ

    - **การทดสอบ** – เลือกการทดสอบที่คุณต้องการปฏิบัติ ในการทดสอบเชิงคุณภาพ ให้เลือกการทดสอบที่ฟิลด์ **ชนิด** ถูกตั้งค่าเป็น *ตัวเลือก*
    - **มีผลบังคับใช้** – เลือกวันที่เริ่มต้นที่การทดสอบมีผลบังคับใช้ หากคุณปล่อยฟิลด์นี้ว่างไว้ ก็จะไม่มีข้อจำกัด
    - **วันหมดอายุ** – เลือกวันที่สุดท้ายที่การทดสอบมีผลบังคับใช้ ถ้าคุณปล่อยฟิลด์นี้ว่างไว้หรือตั้งค่าเป็น *ไม่เคย* จะไม่มีขีดจํากัด
    - **การกำหนดค่าทดสอบ** – เลือกวิธีการที่ควรกําหนด AQL เมื่อบันทึกผลที่ได้หลายครั้งในการทดสอบเดียวกัน เพื่อการทดสอบเชิงคุณภาพ สามารถเลือก *ด้วยตนเอง* ได้เท่านั้น ถ้าคุณเลือกค่าใดค่าหนึ่ง (*ค่าเฉลี่ย* *ค่าต่ำสุด* หรือ *ค่าสูงสุด*) คุณจะได้รับข้อความแสดงข้อผิดพลาดเมื่อคุณบันทึกกลุ่มการทดสอบ
    - **แอททริบิวต์** – หากคุณต้องการบันทึกผลการทดสอบของแอททริบิวต์ของชุดงาน ให้เลือกแอททริบิวต์ที่นี่ และเลือกกล่องกาเครื่องหมาย **อัปเดตแอททริบิวต์ของชุดงานสินค้าคงคลัง**
    - **อัปเดตแอททริบิวต์ของชุดงานสินค้าคงคลัง** – ให้เลือกกล่องกาเครื่องหมายเพื่อบันทึกผลการทดสอบของแอททริบิวต์ของชุดงานที่เลือกในฟิลด์ **แอททริบิวต์**

1. ในส่วนล่างของหน้า ให้เลือกแท็บ **ทั่วไป** การตั้งค่าบางอย่างของการทดสอบที่เลือกบนแท็บ **ภาพรวม** จะซ้ำกันที่นี่ นอกจากนี้ คุณสามารถตั้งค่าฟิลด์ต่อไปนี้สำหรับการทดสอบ:

    - **รายงานใบรับรองการวิเคราะห์** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อบ่งชี้ว่าควรจะพิมพ์ผลการทดสอบบนใบรับรองการวิเคราะห์ (CoA) คุณสามารถสร้างรายงานนี้จากใบสั่งตรวจสอบคุณภาพ
    - **การดำเนินการล้มเหลว** – เลือก *ยอมรับ* หรือ *ล้มเหลว* เพื่อบ่งชี้ว่าการทดสอบควรผ่านหรือไม่ผ่านถ้า AQL ไม่ตรง
    - **ระดับคุณภาพที่ยอมรับได้** – ป้อนเปอร์เซ็นต์รวมของผลการทดสอบที่ต้องผ่านเพื่อให้ถือว่าการทดสอบผ่าน

1. ในส่วนล่างของหน้า บนแท็บ **การทดสอบ** ให้ตั้งค่าฟิลด์ต่อไปนี้:

    - **ตัวแปร** – เลือกหรือดูตัวแปรการทดสอบเพื่อบันทึกผลการทดสอบสำหรับการทดสอบเชิงคุณภาพ
    - **ผลที่ได้เริ่มต้น** – เลือกผลที่ได้เริ่มต้นที่ควรบันทึกไว้ในผลการทดสอบ
    - **เครื่องมือทดสอบ** – เลือกอุปกรณ์ที่ควรใช้ในการทดสอบ ถ้ามีการกําหนดเครื่องมือทดสอบ เครื่องมือทดสอบจะถูกป้อนโดยอัตโนมัติให้ทดสอบในกลุ่มการทดสอบ

1. ปิดหน้า

## <a name="add-a-quantitative-test-to-a-test-group"></a>เพิ่มการทดสอบเชิงคุณภาพลงในกลุ่มการทดสอบ

ในการเพิ่มการทดสอบเชิงคุณภาพเข้าในกลุ่มการทดสอบ ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> กลุ่มการทดสอบ**
1. บนแท็บ **ภาพรวม** ในส่วนบนของหน้า ให้เลือกกลุ่มการทดสอบที่คุณต้องการเพิ่มการทดสอบ
1. ในส่วนล่างของหน้า บนแท็บ **ภาพรวม** ให้เลือก **เพิ่ม** บนแถบเครื่องมือ เพื่อเพิ่มแถวที่กริด จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:

    - **หมายเลขลำดับ** – ป้อนเลขจํานวนเต็ม เพื่อระบุลำดับที่ควรปฏิบัติในการทดสอบ การทดสอบที่มีหมายเลขลำดับน้อยกว่าจะถูกรันก่อนการทดสอบที่มีหมายเลขลำดับที่มากกว่า

        > [!NOTE]
        > ขอแนะนาว่าคุณควรเว้นช่องว่างระหว่างหมายเลขลำดับ ตัวอย่างเช่น ตั้งค่าฟิลด์ **หมายเลขลำดับ** เป็น *10* ของการทดสอบแรกของคุณ แล้วเพิ่มค่านี้ทีละ 10 ในการทดสอบเพิ่มเติม ด้วยวิธีนี้ คุณสามารถเพิ่มการทดสอบใหม่ในภายหลังได้โดยไม่ต้องลบและสร้างรายการใหม่เพื่อวางการทดสอบเหล่านั้นในลำดับที่ต้องการ

    - **การทดสอบ** – เลือกการทดสอบที่คุณต้องการปฏิบัติ ในการทดสอบเชิงคุณภาพ ให้เลือกการทดสอบที่ฟิลด์ **ชนิด** ถูกตั้งค่าเป็น *เศษส่วน* หรือ *เลขจำนวนเต็ม*
    - **มีผลบังคับใช้** – เลือกวันที่เริ่มต้นที่การทดสอบมีผลบังคับใช้ หากคุณปล่อยฟิลด์นี้ว่างไว้ ก็จะไม่มีข้อจำกัด
    - **วันหมดอายุ** – เลือกวันที่สุดท้ายที่การทดสอบมีผลบังคับใช้ ถ้าคุณปล่อยฟิลด์นี้ว่างไว้หรือตั้งค่าเป็น *ไม่เคย* จะไม่มีขีดจํากัด
    - **การกำหนดค่าทดสอบ** – เลือกวิธีการที่ควรกําหนด AQL เมื่อบันทึกผลที่ได้หลายครั้งในการทดสอบเดียวกัน ตัวเลือกที่พร้อมใช้งานคือ *ค่าเฉลี่ย* *ค่าต่ำสุด* *ค่าสูงสุด* และ *ด้วยตนเอง*
    - **แอททริบิวต์** – หากคุณต้องการบันทึกผลการทดสอบของแอททริบิวต์ของชุดงาน ให้เลือกแอททริบิวต์ที่นี่ และเลือกกล่องกาเครื่องหมาย **อัปเดตแอททริบิวต์ของชุดงานสินค้าคงคลัง**
    - **อัปเดตแอททริบิวต์ของชุดงานสินค้าคงคลัง** – ให้เลือกกล่องกาเครื่องหมายเพื่อบันทึกผลการทดสอบของแอททริบิวต์ของชุดงานที่เลือกในฟิลด์ **แอททริบิวต์**

1. ในส่วนล่างของหน้า ให้เลือกแท็บ **ทั่วไป** การตั้งค่าบางอย่างของการทดสอบที่เลือกบนแท็บ **ภาพรวม** จะซ้ำกันที่นี่ นอกจากนี้ คุณสามารถตั้งค่าฟิลด์ต่อไปนี้สำหรับการทดสอบ:

    - **รายงานใบรับรองการวิเคราะห์** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อบ่งชี้ว่าควรจะพิมพ์ผลการทดสอบบน CoA คุณสามารถสร้างรายงานนี้จากใบสั่งตรวจสอบคุณภาพ
    - **การดำเนินการล้มเหลว** – เลือก *ยอมรับ* หรือ *ล้มเหลว* เพื่อบ่งชี้ว่าการทดสอบควรผ่านหรือไม่ผ่านถ้า AQL ไม่ตรง
    - **ระดับคุณภาพที่ยอมรับได้** – ป้อนเปอร์เซ็นต์รวมของผลการทดสอบที่ต้องผ่านเพื่อให้ถือว่าการทดสอบผ่าน

1. ในส่วนล่างของหน้า บนแท็บ **การทดสอบ** ให้ตั้งค่าฟิลด์ต่อไปนี้:

    - **มาตรฐาน** – ป้อนจํานวนเงิน (จํานวนเต็มหรือเศษส่วน) ที่คาดไว้เพื่อให้ผลการทดสอบ ค่าที่คุณป้อนจะถูกป้อนโดยค่าเริ่มต้นในผลการทดสอบ นอกจากนี้ ฟิลด์จะถูกป้อนโดยอัตโนมัติเป็นค่าเริ่มต้นในฟิลด์ **ต่ำสุด** และ **สูงสุด**
    - **ค่าต่ำสุด** – ป้อนค่าต่ำสุดที่อนุญาตในผลการทดสอบ ค่าที่คุณป้อนต้องน้อยกว่ายอดเงินที่ตั้งค่าไว้ในฟิลด์ **มาตรฐาน** เมื่อคุณอัปเดตฟิลด์ **ต่ำสุด** ฟิลด์ **การยอมรับต่ำสุด (%)** จะอัปเดตโดยอัตโนมัติ เช่นเดียวกัน เมื่อคุณอัปเดตฟิลด์ **การยอมรับต่ำสุด (%)** ฟิลด์ **ต่ำสุด** จะอัปเดตโดยอัตโนมัติ
    - **ค่าสูงสุด** – ป้อนค่าสูงสุดที่อนุญาตในผลการทดสอบ ค่าที่คุณป้อนต้องมากกว่ายอดเงินที่ตั้งค่าไว้ในฟิลด์ **มาตรฐาน** เมื่อคุณอัปเดตฟิลด์ **สูงสุด** ฟิลด์ **การยอมรับสูงสุด (%)** จะอัปเดตโดยอัตโนมัติ เช่นเดียวกัน เมื่อคุณอัปเดตฟิลด์ **การยอมรับสูงสุด (%)** ฟิลด์ **สูงสุด** จะอัปเดตโดยอัตโนมัติ
    - **เครื่องมือทดสอบ** – เลือกอุปกรณ์ที่ควรใช้ในการทดสอบ ถ้ามีการกําหนดเครื่องมือทดสอบ เครื่องมือทดสอบจะถูกป้อนโดยอัตโนมัติให้ทดสอบในกลุ่มการทดสอบ

1. ปิดหน้า

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [เครื่องมือการทดสอบการจัดการคุณภาพ](quality-management-processes.md)
- [การทดสอบการจัดการคุณภาพ](quality-management-processes.md)
- [ตัวแปรการทดสอบการจัดการคุณภาพ](quality-management-processes.md)
- [ความสัมพันธ์ของคุณภาพ](quality-management-processes.md)
- [แอททริบิวต์ของชุดงาน](../production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
