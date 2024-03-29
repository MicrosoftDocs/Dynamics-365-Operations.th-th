---
title: การเชื่อมโยงคุณภาพ
description: บทความนี้จะอธิบายวิธีการที่คุณสามารถใช้การเชื่อมโยงคุณภาพใน Microsoft Dynamics 365 Supply Chain Management เพื่อสร้างใบสั่งตรวจสอบคุณภาพที่เกี่ยวข้องกับกระบวนการผลิตการขาย การซื้อ และกระบวนการผลิตของคุณโดยอัตโนมัติ
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e96f301d8dec255e57f0f0fbfa9c8e1a5922ae9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887528"
---
# <a name="quality-associations"></a>การเชื่อมโยงคุณภาพ

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการที่คุณสามารถใช้การเชื่อมโยงคุณภาพใน Microsoft Dynamics 365 Supply Chain Management เพื่อสร้างใบสั่งตรวจสอบคุณภาพที่เกี่ยวข้องกับกระบวนการผลิตการขาย การซื้อ และกระบวนการผลิตของคุณโดยอัตโนมัติ

ความสัมพันธ์ของคุณภาพกำหนดข้อมูลต่อไปนี้ทั้งหมดสำหรับใบสั่งตรวจสอบคุณภาพที่สร้างขึ้น:

- เหตุการณ์ธุรกรรม
- ชุดของการทดสอบที่ต้องดำเนินการบนสินค้า
- ระดับคุณภาพที่ยอมรับได้ (AQL)
- แผนการสุ่มตัวอย่าง

คุณต้องกำหนดคำความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจที่จำเป็นต้องมีการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ ตัวอย่างเช่น สามารถสร้างใบสั่งตรวจสอบคุณภาพในกระบวนการทางธุรกิจสำหรับใบสั่งซื้อ ใบสั่งตรวจสอบสินค้า ใบสั่งขาย และใบสั่งผลิต

## <a name="working-with-quality-associations"></a>การทำงานกับการเชื่อมโยงคุณภาพ

กระบวนการทางธุรกิจที่ใช้การเชื่อมโยงคุณภาพอาจเกี่ยวข้องกับเอกสารต้นทางต่าง ๆ เช่นใบสั่งซื้อ ใบสั่งขาย หรือใบสั่งผลิต

แต่ละเรกคอร์ดความสัมพันธ์ของคุณภาพกำหนดชุดของการทดสอบ AQL และแผนการสุ่มตัวอย่างที่ใช้กับใบสั่งตรวจสอบคุณภาพที่ถูกสร้างขึ้น คุณต้องกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจ ตัวอย่างเช่น คุณสามารถตั้งค่าการเชื่อมโยงคุณภาพที่สร้างใบสั่งตรวจสอบคุณภาพเมื่อมีการอัพเดตใบรับสินค้าตามใบสั่งซื้อ ทั้งนี้ขึ้นอยู่กับการตั้งค่าของแผนปฏิบัติการ คุณสามารถบล็อคกระบวนการทริกเกอร์ได้เองในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ หรือกระบวนการต่อมา เช่น การออกใบแจ้งหนี้ใบสั่งซื้อ สามารถบล็อคได้

> [!NOTE]
> ในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ ปริมาณสินค้าคงคลังจะถูกถูกบล็อคจากการออกใช้โดยอัตโนมัติ ขึ้นอยู่กับการตั้งค่าฟิลด์ **การบล็อคทั้งหมด** บนหน้า **การสุ่มตัวอย่างสินค้า** ปริมาณเป็นปริมาณในใบสั่งตรวจสอบคุณภาพ หรือปริมาณในรายการเอกสารต้นทาง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การสุ่มตัวอย่างสินค้าการจัดการคุณภาพ](quality-item-sampling.md)

สำหรับกระบวนการทางธุรกิจที่ระบุ เรกคอร์ดความสัมพันธ์ของคุณภาพจะระบุเหตุการณ์และเงื่อนไขที่มีการสร้างใบสั่งตรวจสอบคุณภาพ เงื่อนไขอาจเป็นเฉพาะสำหรับไซต์หรือนิติบุคคล สามารถสร้างใบสั่งตรวจสอบคุณภาพที่เกี่ยวข้องกับการทดสอบแบบทำลายเฉพาะเมื่อสินค้าคงคลังคงเหลือที่มีอยู่สำหรับเหตุการณ์

เมื่อต้องการใช้งานการเชื่อมโยงคุณภาพ ให้ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> การเชื่อมโยงคุณภาพ** ตัวอย่างต่อไปนี้อธิบายวิธีกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรในแต่ละกระบวนการทางธุรกิจ สำหรับแต่ละตัวอย่าง ตารางต่อไปนี้สรุปเหตุการณ์และเงื่อนไขที่กำหนดโดยเรกคอร์ดความสัมพันธ์ของคุณภาพ

<table>
<thead>
<tr>
<th>ชนิดการอ้างอิง</th>
<th>ชนิดเหตุการณ์</th>
<th>การดำเนินการ</th>
<th>การบล็อคเหตุการณ์</th>
<th>การอ้างอิงเอกสาร</th>
</tr>
</thead>
<tbody>
<tr>
<td>สินค้าคงคลัง</td>
<td>ใช้ไม่ได้</td>
<td>ใช้ไม่ได้</td>
<td>ไม่มี</td>
<td>ทั้งหมด</td>
</tr>
<tr>
<td rowspan="7">ใบสั่งขาย</td>
<td rowspan="4">กระบวนการเบิกสินค้าถูกจัดกำหนดการ</td>
<td rowspan="4">ก่อน</td>
<td>ไม่มี</td>
<td rowspan="22">รหัส กลุ่ม หรือทั้งหมด เฉพาะเท่านั้น</td>
</tr>
<tr>
<td>กระบวนการเบิกสินค้า</td>
</tr>
<tr>
<td>บันทึกการจัดส่ง</td>
</tr>
<tr>
<td>ใบแจ้งหนี้</td>
</tr>
<tr>
<td rowspan="3">บันทึกการจัดส่ง</td>
<td rowspan="3">ก่อน</td>
<td>ไม่มี</td>
</tr>
<tr>
<td>บันทึกการจัดส่ง</td>
</tr>
<tr>
<td>ใบแจ้งหนี้</td>
</tr>
<tr>
<td rowspan="15">การซื้อ</td>
<td rowspan="7">รายการรับสินค้า</td>
<td rowspan="4">ก่อน</td>
<td>ไม่มี</td>
</tr>
<tr>
<td>รายการรับสินค้า</td>
</tr>
<tr>
<td>ใบรับสินค้า</td>
</tr>
<tr>
<td>ใบแจ้งหนี้</td>
</tr>
<tr>
<td rowspan="3">หลัง</td>
<td>ไม่มี</td>
</tr>
<tr>
<td>ใบรับสินค้า</td>
</tr>
<tr>
<td>ใบแจ้งหนี้</td>
</tr>
<tr>
<td rowspan="3">การลงทะเบียน</td>
<td rowspan="3">ใช้ไม่ได้</td>
<td>ไม่มี</td>
</tr>
<tr>
<td>ใบรับสินค้า</td>
</tr>
<tr>
<td>ใบแจ้งหนี้</td>
</tr>
<tr>
<td rowspan="5">ใบรับสินค้า</td>
<td rowspan="3">ก่อน</td>
<td>ไม่มี</td>
</tr>
<tr>
<td>ใบรับสินค้า</td>
</tr>
<tr>
<td>ใบแจ้งหนี้</td>
</tr>
<tr>
<td rowspan="2">หลัง</td>
<td>ไม่มี</td>
</tr>
<tr>
<td>ใบแจ้งหนี้</td>
</tr>
<tr>
<td rowspan="8">การผลิต</td>
<td rowspan="3">การลงทะเบียน</td>
<td rowspan="3">ใช้ไม่ได้</td>
<td>ไม่มี</td>
<td rowspan="12">ทั้งหมด</td>
</tr>
<tr>
<td>รายงานเมื่อเสร็จสมบูรณ์</td>
</tr>
<tr>
<td>สิ้นสุด</td>
</tr>
<tr>
<td rowspan="5">รายงานเมื่อเสร็จสมบูรณ์</td>
<td rowspan="3">ก่อน</td>
<td>ไม่มี</td>
</tr>
<tr>
<td>รายงานเมื่อเสร็จสมบูรณ์</td>
</tr>
<tr>
<td>สิ้นสุด</td>
</tr>
<tr>
<td rowspan="2">หลัง</td>
<td>ไม่มี</td>
</tr>
<tr>
<td>สิ้นสุด</td>
</tr>
<tr>
<td rowspan="4">การตรวจสอบสินค้า</td>
<td rowspan="3">รายงานเมื่อเสร็จสมบูรณ์</td>
<td rowspan="2">ก่อน</td>
<td>รายงานเมื่อเสร็จสมบูรณ์</td>
</tr>
<tr>
<td>สิ้นสุด</td>
</tr>
<tr>
<td>หลัง</td>
<td>สิ้นสุด</td>
</tr>
<tr>
<td>สิ้นสุด</td>
<td>ก่อน</td>
<td>สิ้นสุด</td>
</tr>
<tr>
<td rowspan="3">ขั้นตอนของกระบวนการผลิต</td>
<td rowspan="3">รายงานเมื่อเสร็จสมบูรณ์</td>
<td rowspan="2">ก่อน</td>
<td>None</td>
<td rowspan="3">รหัส กลุ่ม หรือทั้งหมดเฉพาะ และระบุทรัพยากร กลุ่ม หรือทั้งหมด</td>
</tr>
<tr>
<td>รายงานเมื่อเสร็จสมบูรณ์</td>
</tr>
<tr>
<td>หลังจาก</td>
<td>None</td>
</tr>
<tr>
<td rowspan="3">การผลิตสินค้าร่วม</td>
<td>การลงทะเบียน</td>
<td>ใช้ไม่ได้</td>
<td rowspan="3">None</td>
<td rowspan="3">ทั้งหมด</td>
</tr>
<tr>
<td rowspan="2">รายงานเมื่อเสร็จสมบูรณ์</td>
<td>ก่อน</td>
</tr>
<tr>
<td>หลังจาก</td>
</tr>
</tbody>
</table>

> [!NOTE]
> คุณลักษณะ *การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า* เพิ่มความสามารถสำหรับการประมวลผลใบสั่งตรวจสอบคุณภาพสำหรับการผลิตที่มีการตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น *รายงานการเสร็จงาน* และมีการตั้งค่าฟิลด์ **การดำเนินการ** เป็น *ภายหลัง* และสำหรับการซื้อที่มีการตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น *การลงทะเบียน* สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า](quality-management-for-warehouses-processes.md)

ตารางต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างใบสั่งตรวจสอบคุณภาพสามารถสำหรับชนิดเฉพาะของกระบวนการ

<div class="tableSection">
<table>
<thead>
<tr>
<th>ชนิดของกระบวนการ</th>
<th>เมื่อใบสั่งตรวจสอบคุณภาพสามารถถูกสร้างขึ้นโดยอัตโนมัติ</th>
<th>เมื่อใบสั่งตรวจสอบคุณภาพสามารถสร้างหากการทดสอบแบบทำลายจำเป็น</th>
<th>ข้อมูลเงื่อนไข</th>
<th>ข้อมูลการสร้างด้วยตนเอง</th>
</tr>
</thead>
<tbody>
<tr>
<td>ใบสั่งซื้อ</td>
<td>ก่อนหรือหลังรายการรับสินค้าหรือใบรับสินค้าสำหรับวัสดุที่ได้รับจะมีการลงรายการบัญชี</td>
<td>หลังจากใบรับสินค้าสำหรับวัสดุที่ได้รับมีการลงรายการบัญชี เนื่องจากวัสดุต้องพร้อมใช้งานสำหรับการทดสอบแบบทำลาย</td>
<td>ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</td>
<td>ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</td>
</tr>
<tr>
<td>ใบสั่งตรวจสอบสินค้า</td>
<td>ก่อน หรือหลัง ใบสั่งตรวจสอบสินค้ามีการรายงานเสร็จสิ้นแล้วหรือสิ้นสุด</td>
<td>ใบสั่งตรวจสอบคุณภาพที่ต้องการการทดสอบแบบทำลายไม่สามารถที่จะสร้าง สมมติว่า ฟังก์ชันใบสั่งตรวจสอบสินค้าจัดการการโอนการครอบครองวัสดุที่ถูกทำลาย</td>
<td>ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</td>
<td>ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งตรวจสอบสินค้าสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</td>
</tr>
<tr>
<td>ใบสั่งขาย</td>
<td>ก่อนการจัดกำหนดการกระบวนการเบิกสินค้าหรืออัพเดตบันทึกสำหรับสินค้าที่กำลังจัดส่ง</td>
<td>ในขั้นตอนใดๆ</td>
<td>ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือลูกค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</td>
<td>ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</td>
</tr>
<tr>
<td>ใบสั่งผลิต</td>
<td>ก่อนหรือหลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</td>
<td>หลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</td>
<td>ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</td>
<td>ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</td>
</tr>
<tr>
<td>ใบสั่งผลิตที่มีขั้นตอนของกระบวนการผลิต</td>
<td>ก่อนหรือหลังจากรายงานการเสร็จสำหรับการดำเนินงาน</td>
<td>หลังจากการรายงานการผลิตเสร็จสิ้นแล้วสำหรับการดำเนินงานสุดท้าย</td>
<td>ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือทรัพยากรการดำเนินงาน หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</td>
<td>ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับขั้นตอนของกระบวนการผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</td>
</tr>
<tr>
<td>สินค้าคงคลัง</td>
<td>ใบสั่งตรวจสอบคุณภาพไม่สามารถถูกสร้างขึ้นโดยอัตโนมัติสำหรับธุรกรรมในสมุดรายวันสินค้าคงคลังหรือธุรกรรมใบสั่งโอนย้าย</td>
<td></td>
<td></td>
<td>ใบสั่งคุณภาพต้องถูกสร้างด้วยตนเองสำหรับปริมาณสินค้าคงคลังของสินค้า จำเป็นต้องมีปริมาณสินค้าคงคลังคงเหลือที่มีอยู่จริง</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>ตัวอย่างของการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ

### <a name="purchasing"></a>การซื้อ

ในการซื้อ หากคุณตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น *ใบรับสินค้า* และฟิลด์ **การดำเนินการ** เป็น *ภายหลัง* บนเพจ **การเชื่อมโยงคุณภาพ** คุณจะได้ผลลัพธ์ต่อไปนี้:

- หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น *ใช่* จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับทุกการรับสินค้าต่อใบสั่งซื้อ ตามปริมาณที่รับและการตั้งค่าในสินค้าตัวอย่าง ทุกครั้งที่มีการรับปริมาณต่อใบสั่งซื้อ จะมีการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่รับมาใหม่
- หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น *ไม่* จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับสินค้ารายการแรกต่อใบสั่งซื้อ ตามปริมาณที่รับ นอกจากนี้ จะมีการสร้างใบสั่งตรวจสอบคุณภาพอย่างน้อยหนึ่งรายการตามปริมาณคงเหลือ ขึ้นอยู่กับมิติการติดตาม ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับต่อใบสั่งซื้อหลังจากนี้

### <a name="production"></a>การใช้งานจริง

ในการผลิต หากคุณตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น *รายงานเป็นเสร็จสิ้น* และฟิลด์ **การดำเนินการ** เป็น *ภายหลัง* บนเพจ **การเชื่อมโยงคุณภาพ** คุณจะได้ผลลัพธ์ต่อไปนี้:

- หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น *ใช่* จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับทุกปริมาณที่เสร็จสิ้นและการตั้งค่าในสินค้าตัวอย่าง ทุกครั้งที่มีการรายงานปริมาณเป็นเสร็จสิ้นต่อใบสั่งผลิต จะมีการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่เพิ่งเสร็จสิ้น ตรรกะการสร้างนี้สอดคล้องกับการซื้อ
- หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น *ไม่* จะมีการสร้างใบสั่งตรวจสอบคุณภาพในครั้งแรกที่มีการรายงานปริมาณเป็นเสร็จสิ้น ตามปริมาณที่เสร็จสิ้น นอกจากนี้ จะมีการสร้างใบสั่งตรวจสอบคุณภาพอย่างน้อยหนึ่งรายการตามปริมาณคงเหลือ ขึ้นอยู่กับมิติการติดตามของสินค้าตัวอย่าง ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับปริมาณที่เสร็จสิ้นในเวลาต่อมา

<table>
<thead>
<tr>
<th>ข้อกำหนดเกี่ยวกับคุณภาพ</th>
<th>ต่อปริมาณที่อัพเดต</th>
<th>ต่อมิติการติดตาม</th>
<th>ผลลัพธ์</th>
</tr>
</thead>
<tbody>
<tr>
<td>เปอร์เซ็นต์: 10%</td>
<td>ใช่</td>
<td>
<p>หมายเลขชุดงาน: ไม่</p>
<p>รหัสหมายเลขลำดับประจำสินค้า: ไม่</p>
</td>
<td>
<p>ปริมาณการสั่ง: 100</p>
<ol>
<li>รายงานเมื่อเสร็จสิ้นสำหรับ 30
<ul>
<li>ใบสั่งตรวจสอบคุณภาพ 1 สำหรับ 3 (10% ของ 30)</li>
</ul>
</li>
<li>รายงานเมื่อเสร็จสิ้นสำหรับ 70
<ul>
<li>ใบสั่งตรวจสอบคุณภาพ 2 สำหรับ 7 (10% ของปริมาณในใบสั่งที่เหลืออยู่ซึ่งเท่ากับ 70 ในกรณีนี้)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>ปริมาณคงที่: 1</td>
<td>ไม่</td>
<td>
<p>หมายเลขชุดงาน: ไม่</p>
<p>รหัสหมายเลขลำดับประจำสินค้า: ไม่</p>
</td>
<td>ปริมาณการสั่ง: 100
<ol>
<li>รายงานเมื่อเสร็จสิ้นสำหรับ 30
<ul>
<li>ใบสั่งตรวจสอบคุณภาพ 1 ต่อ 1 (สำหรับปริมาณที่รายงานการเสร็จงานครั้งแรกซึ่งมีค่าคงที่เป็น 1)</li>
<li>ใบสั่งตรวจสอบคุณภาพ 2 ต่อ 1 (สำหรับปริมาณที่คงเหลือ ซึ่งยังมีค่าคงที่เป็น 1)</li>
</ul>
</li>
<li>รายงานเมื่อเสร็จสิ้นสำหรับ 10
<ul>
<li>ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</li>
</ul>
</li>
<li>รายงานเมื่อเสร็จสิ้นสำหรับ 60
<ul>
<li>ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>ปริมาณคงที่: 1</td>
<td>ใช่</td>
<td>
<p>หมายเลขชุดงาน: ใช่</p>
<p>หมายเลขลำดับประจำสินค้า: ใช่</p>
</td>
<td>
<p>ปริมาณการสั่ง: 10</p>
<ol>
<li>รายงานการเสร็จงานของ 3: 1 สำหรับหมายเลขชุดงาน b1 หมายเลขลำดับประจำสินค้า s1 1 สำหรับหมายเลขชุดงาน b2 หมายเลขลำดับประจำสินค้า s2 และ 1 สำหรับหมายเลขชุดงาน b3 หมายเลขลำดับประจำสินค้า s3
<ul>
<li>ใบสั่งตรวจสอบคุณภาพ 1 ต่อ 1 ของหมายเลขชุดงาน b1 หมายเลขลำดับประจำสินค้า s1</li>
<li>ใบสั่งตรวจสอบคุณภาพ 2 ต่อ 1 ของหมายเลขชุดงาน b2 หมายเลขลำดับประจำสินค้า s2</li>
<li>ใบสั่งตรวจสอบคุณภาพ 3 ต่อ 1 ของหมายเลขชุดงาน b3 หมายเลขลำดับประจำสินค้า s3</li>
</ul>
</li>
<li>รายงานการเสร็จงานของ 2: 1 สำหรับหมายเลขชุดงาน b4 หมายเลขลำดับประจำสินค้า s4 1 สำหรับหมายเลขชุดงาน b5 หมายเลขลำดับประจำสินค้า s5
<ul>
<li>ใบสั่งตรวจสอบคุณภาพ 4 ต่อ 1 ของหมายเลขชุดงาน b4 หมายเลขลำดับประจำสินค้า s4</li>
<li>ใบสั่งตรวจสอบคุณภาพ 5 ต่อ 1 ของหมายเลขชุดงาน b5 หมายเลขลำดับประจำสินค้า s5</li>
</ul>
</li>
</ol>
<p><strong>หมายเหตุ:</strong> : ชุดงานสามารถนำมาใช้ใหม่ได้</p>
</td>
</tr>
<tr>
<td>ปริมาณคงที่: 2</td>
<td>ไม่</td>
<td>
<p>หมายเลขชุดงาน: ใช่</p>
<p>หมายเลขลำดับประจำสินค้า: ใช่</p>
</td>
<td>
<p>ปริมาณการสั่ง: 10</p>
<ol>
<li>รายงานการเสร็จงานของ 3: 1 สำหรับหมายเลขชุดงาน b1 หมายเลขลำดับประจำสินค้า s1 1 สำหรับหมายเลขชุดงาน b2 หมายเลขลำดับประจำสินค้า s2 และ 1 สำหรับหมายเลขชุดงาน b3 หมายเลขลำดับประจำสินค้า s3 และ 1 สำหรับหมายเลขชุดงาน b4 หมายเลขลำดับประจำสินค้า s4
<ul>
<li>ใบสั่งตรวจสอบคุณภาพ 1 ต่อ 1 ของหมายเลขชุดงาน b1 หมายเลขลำดับประจำสินค้า s1</li>
<li>ใบสั่งตรวจสอบคุณภาพ 2 ต่อ 1 ของหมายเลขชุดงาน b2 หมายเลขลำดับประจำสินค้า s2</li>
<li>ใบสั่งตรวจสอบคุณภาพ 3 ต่อ 1 ของหมายเลขชุดงาน b3 หมายเลขลำดับประจำสินค้า s3</li>
<li>ใบสั่งตรวจสอบคุณภาพ 4 ต่อ 1 ของหมายเลขชุดงาน b4 หมายเลขลำดับประจำสินค้า s4</li>
</ul>
<ul>
<li>ใบสั่งตรวจสอบคุณภาพ 5 สำหรับ 2 โดยไม่มีการอ้างอิงถึงหมายเลขชุดงานและหมายเลขลำดับประจำสินค้า</li>
</ul>
</li>
<li>รายงานการเสร็จงานของ 6: 1 สำหรับหมายเลขชุดงาน b5 หมายเลขลำดับประจำสินค้า s5 1 สำหรับหมายเลขชุดงาน b6 หมายเลขลำดับประจำสินค้า s6 และ 1 สำหรับหมายเลขชุดงาน b7 หมายเลขลำดับประจำสินค้า s7 1 สำหรับหมายเลขชุดงาน b8 หมายเลขลำดับประจำสินค้า s8 สำหรับหมายเลขชุดงาน b9 หมายเลขลำดับประจำสินค้า s9 และ 1 สำหรับหมายเลขชุดงาน b10 หมายเลขลำดับประจำสินค้า s10
<ul>
<li>ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [กระบวนการการจัดการคุณภาพ](quality-management-processes.md)
- [เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน](enable-quality-management.md)
- [การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
