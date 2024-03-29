---
title: (ตัวอย่าง) ทำให้สินค้าสำเร็จรูปพร้อมใช้จริงก่อนลงรายการบัญชีในสมุดรายวัน
description: เมื่อมีการรายงานการเสร็จงานของสินค้าที่ผลิต สินค้านั้นจะถูกลงทะเบียนเป็นพร้อมใช้งานเพื่อการประมวลผลทางกายภาพต่อไป และสมุดรายวันอย่างน้อยหนึ่งรายการถูกลงรายการบัญชี บทความนี้จะอธิบายวิธีการยืดเวลาการลงรายการบัญชีสมุดรายวัน โดยการเปิดใช้งานการลงรายการบัญชีสมุดรายวันเพื่อประมวลผลโดยชุดงานในคิวข้อความ
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689352"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>(ตัวอย่าง) ทำให้สินค้าสำเร็จรูปพร้อมใช้จริงก่อนลงรายการบัญชีในสมุดรายวัน

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

เมื่อผู้ปฏิบัติงานรายงานการเสร็จงานของสินค้าที่ผลิต ระบบจะลงทะเบียนสินค้านั้นเพื่อการประมวลผลทางกายภาพเพิ่มเติม (เช่น การจัดส่งสินค้าหรือการสำรองสินค้า) ในระหว่างกระบวนการนี้ สมุดรายวันหนึ่งรายการหรือมากกว่านั้นจะถูกลงรายการบัญชีด้วย (เช่น รายงานเป็นสมุดรายวันที่เสร็จสิ้น สมุดรายวันรายการเบิกสินค้า และสมุดรายวันบัตรกระบวนการผลิต) ถ้าคุณต้องการให้สินค้าของคุณพร้อมใช้งานจริงก่อนที่จะประมวลผลการลงรายการบัญชีทั้งหมดแล้ว คุณสามารถตั้งค่าระบบให้ยืดเวลาลงรายการบัญชีสมุดรายวันได้ จากนั้น การลงรายการบัญชีที่รอการตัดบัญชีจะมีการจัดการโดยชุดงานที่จะประมวลผลการลงรายการบัญชีเมื่อทรัพยากรระบบอนุญาต

ภาพประกอบต่อไปนี้แสดงวิธีการเรียกกระบวนการลงรายการบัญชีสมุดรายวันทั้งที่มีและไม่มีการลงรายการบัญชีที่รอการตัดบัญชี

![กระบวนการรายงานการเสร็จงานที่มีและไม่มีการลงรายการบัญชีสมุดรายวันที่รอการตัดบัญชี](media/deferred-posting-flowchart.png "กระบวนการรายงานการเสร็จงานที่มีและไม่มีการลงรายการบัญชีสมุดรายวันที่รอการตัดบัญชี")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>เปิดการลงรายการบัญชีสมุดรายวันที่รอการตัดบัญชีจากระบบของคุณ

ก่อนที่คุณจะสามารถใช้การลงรายการบัญชีสมุดรายวันที่รอการตัดบัญชี คุณต้องเปิดใช้งานในระบบของคุณ ผู้ดูแลระบบสามารถใช้พื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:

- **โมดูล:** *การควบคุมการผลิต*
- **ชื่อคุณลักษณะ:** *(ตัวอย่าง) ทำให้สินค้าสำเร็จรูปพร้อมใช้จริงก่อนลงรายการบัญชีในสมุดรายวัน*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>ตั้งค่าตัวเลือกการลงรายการบัญชีสมุดรายวันเพื่อการรายงานการเสร็จงาน

ผู้ปฏิบัติงานสามารถรายงานการเสร็จงานของสินค้าโดยใช้ไคลเอ็นต์ใดๆ ต่อไปนี้

- เว็บไคลเอ็นต์
- แอป Warehouse Management บนมือถือ
- อินเทอร์เฟสการดำเนินการของระบบการผลิต

เว็บไคลเอ็นต์ใช้การตั้งค่าคอนฟิกวิธีการลงรายการบัญชีแบบเดียวกันกับแอป Warehouse Management บนมือถือ อย่างไรก็ตาม วิธีการลงรายการบัญชีที่อินเทอร์เฟสการปฏิบัติการของการผลิตใช้ต้องมีการตั้งค่าคอนฟิกแยกต่างหาก

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>ตั้งค่าตัวเลือกการลงรายการบัญชีสมุดรายวันเกี่ยวกับเว็บไคลเอ็นต์และแอป Warehouse Management บนมือถือ

ในแอปบนมือถือ ผู้ปฏิบัติงานจะรายงานสินค้าเมื่อเสร็จสมบูรณ์โดยการเปิดรายการเมนูบนมือถือซึ่งค่า **กระบวนการสร้างงาน** คือ *รายงานการเสร็จงาน* หรือ *รายงานการเสร็จงานและการสำรองสินค้า* ในเว็บไคลเอ็นต์ ผู้ปฏิบัติงานจะรายงานการเสร็จงานของสินค้าจากหน้ารายการ **ใบสั่งผลิตทั้งหมด** หรือหน้า **ใบสั่งผลิต (รายละเอียด)** คุณสามารถตั้งค่าคอนฟิกวิธีการเริ่มต้นทั่วทั้งบริษัทและยังสามารถตั้งค่าการแทนที่เฉพาะคลังสินค้าได้ตามที่คุณต้องการ

ใช้ขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกวิธีการลงรายการบัญชีเริ่มต้นทั่วทั้งบริษัทเพื่อรายงานสินค้าเมื่อเสร็จสมบูรณ์จากเว็บไคลเอ็นต์หรือแอป Warehouse Management บนมือถือ

1. ไปที่ **การควบคุมการผลิตl \> การตั้งค่า \> พารามิเตอร์การควบคุมการผลิต**
1. บนแท็บ **สมุดรายวัน** ในส่วน **สมุดรายวันที่รายงานการเสร็จงาน** ให้ตั้งค่าฟิลด์ **วิธีการลงรายการบัญชี** เป็นหนึ่งในค่าต่อไปนี้:

    - *แบบทันที* – เมื่อสินค้ามีการรายงานการเสร็จงาน ระบบจะประมวลผลการลงรายการบัญชีสมุดรายวันที่เกี่ยวข้องทั้งหมดโดยสมบูรณ์ ก่อนที่จะเครื่องหมายสินค้าสำเร็จรูปเป็นพร้อมให้บริการ
    - *เลื่อนออกไป* – เมื่อสินค้ามีการรายงานการเสร็จงาน ระบบจะทำเครื่องหมายสินค้าสำเร็จรูปเป็นพร้อมให้บริการและเพิ่มการลงรายการบัญชีสมุดรายวันไปยังคิวข้อความ ระบบไม่รอจนกว่าจะมีการประมวลผลการลงรายการบัญชีทั้งหมดก่อนจะทำเครื่องหมายเลือกสินค้าสำเร็จรูปเป็นสินค้าพร้อมใช้งานจริง

ใช้ขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกการแทนที่เฉพาะคลังสินค้าในวิธีการลงรายการบัญชีเริ่มต้นที่ตั้งค่าคอนฟิกบนหน้า **พารามิเตอร์การควบคุมการผลิต**

1. ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การแบ่งสินค้าคงคลัง \> คลังสินค้า**
1. เลือกคลังสินค้าที่คุณต้องการตั้งค่า
1. บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**
1. บนแท็บด่วน **คลังสินค้า** ในส่วน **ใบสั่งผลิต** ให้ตั้งค่าฟิลด์ **วิธีการลงรายการบัญชี** เป็นหนึ่งในค่าต่อไปนี้:

    - *สืบทอด* – คลังสินค้าที่เลือกจะรับช่วงการตั้งค่าจากหน้า **พารามิเตอร์การควบคุมการผลิต**
    - *แบบทันที* – เมื่อสินค้ามีการรายงานการเสร็จงาน ระบบจะประมวลผลการลงรายการบัญชีสมุดรายวันที่เกี่ยวข้องทั้งหมดโดยสมบูรณ์ ก่อนที่จะเครื่องหมายสินค้าสำเร็จรูปเป็นพร้อมให้บริการ
    - *เลื่อนออกไป* – เมื่อสินค้ามีการรายงานการเสร็จงาน ระบบจะทำเครื่องหมายสินค้าสำเร็จรูปเป็นพร้อมให้บริการและเพิ่มการลงรายการบัญชีสมุดรายวันไปยังคิวข้อความ ระบบไม่รอจนกว่าจะมีการประมวลผลการลงรายการบัญชีทั้งหมดก่อนจะทำเครื่องหมายเลือกสินค้าสำเร็จรูปเป็นสินค้าพร้อมใช้งานจริง

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>ตั้งค่าตัวเลือกการลงรายการบัญชีสมุดรายวันสำหรับอินเทอร์เฟสการดำเนินการของระบบการผลิต

ใช้ขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกวิธีการลงรายการบัญชีที่ใช้เมื่อรายงานการเสร็จงานของสินค้าจากอินเทอร์เฟสการปฏิบัติการการผลิต

1. ไปที่ **การควบคุมการผลิต \> การตั้งค่า \> การดำเนินการผลิต \> รายละเอียดของใบสั่งผลิต**
1. บนแท็บ **รายงานการเสร็จงาน** ในส่วน **สมุดรายวันที่รายงานการเสร็จงาน** ให้ตั้งค่าฟิลด์ **วิธีการลงรายการบัญชี** เป็นหนึ่งในค่าต่อไปนี้:

    - *แบบทันที* – เมื่อสินค้ามีการรายงานการเสร็จงาน ระบบจะประมวลผลการลงรายการบัญชีสมุดรายวันที่เกี่ยวข้องทั้งหมดโดยสมบูรณ์ ก่อนที่จะเครื่องหมายสินค้าสำเร็จรูปเป็นพร้อมให้บริการ
    - *เลื่อนออกไป* – เมื่อสินค้ามีการรายงานการเสร็จงาน ระบบจะทำเครื่องหมายสินค้าสำเร็จรูปเป็นพร้อมให้บริการและเพิ่มการลงรายการบัญชีสมุดรายวันไปยังคิวข้อความ ระบบไม่รอจนกว่าจะมีการประมวลผลการลงรายการบัญชีทั้งหมดก่อนจะทำเครื่องหมายเลือกสินค้าสำเร็จรูปเป็นสินค้าพร้อมใช้งานจริง

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>จัดตารางการผลิตชุดงานตัวประมวลผลข้อความเพื่อประมวลผลการลงรายการบัญชีที่รอการตัดบัญชี

ชุดงานตัวประมวลผลข้อความจะรับผิดชอบการประมวลผลการลงรายการบัญชีสมุดรายวัน หลังจากที่จัดคิวแล้ว เพื่อให้แน่ใจว่ามีการประมวลผลการลงรายการบัญชีสมุดรายวันของคุณ คุณต้องตั้งค่าคอนฟิกงานนี้ให้รันในช่วงเวลาปกติ ใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าชุดงานที่ต้องการ

1. ไปที่ **การจัดการระบบ \>ตัวประมวลผลข้อความ \> ตัวประมวลผลข้อความ**
1. บนแท็บด่วน **พารามิเตอร์** ให้ตั้งค่าฟิลด์ **คิวข้อความ** เป็น *การผลิต*
1. บนแท็บด่วน **ทำงานในเบื้องหลัง** ให้ตั้งค่าตัวเลือก **การประมวลผลชุดงาน** เป็น *ใช่* จากนั้น ตั้งค่ากําหนดการที่เกิดพร้อมกัน และตั้งค่าคอนฟิกการตั้งค่าอื่นๆ ตามต้องการ การตั้งค่าจะทำงานเช่นเดียวกับทำให้ชนิด [งานพื้นหลัง](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) อื่นๆ ใน Microsoft Dynamics 365 Supply Chain Management

## <a name="track-the-progress-of-your-deferred-postings"></a>ติดตามความคืบหน้าของการลงรายการบัญชีที่รอการตัดบัญชีของคุณ

การลงรายการบัญชีสมุดรายวันที่รอการตัดบัญชีจะถูกจัดคิว *ข้อความตัวประมวลผลข้อความ* ที่รอจนกว่าการประมวลผลโดย *ตัวประมวลผลข้อความ* ควรมีการตั้งค่าตัวประมวลผลข้อความให้รันเป็นชุดงานที่จัดตารางการผลิตไว้ เมื่อต้องการดูข้อความการลงรายการบัญชีที่รอการตัดบัญชีที่ได้หรือจะถูกประมวลผลโดยตัวประมวลผลข้อความ ให้ไปที่ **การควบคุมการผลิต \> ใบสั่งผลิต \> การลงรายการบัญชีใบสั่งผลิตที่รอตัดบัญชี**

### <a name="message-grid-columns-and-filters"></a>คอลัมน์และตัวกรองกริดข้อความ

คุณสามารถใช้ฟิลด์ที่ด้านบนของหน้า **การลงรายการบัญชีใบสั่งผลิตที่รอตัดบัญชี** เพื่อช่วยค้นหาข้อความเฉพาะใดๆ ที่คุณกำลังค้นหา

โดยตัวกรองที่เลือกได้มีดังต่อไปนี้:

- **ชนิดข้อความ** – ระบุชนิดของข้อความที่แสดงในกริด
- **สถานะข้อความ** – ระบุสถานะของข้อความที่แสดงในกริด โดยมีสถานะต่อไปนี้

    - *จัดคิวแล้ว* – ข้อความพร้อมแล้วที่จะถูกประมวลผลโดยตัวประมวลผลข้อความ
    - *ประมวลผลแล้ว* – ข้อความถูกประมวลผลเสร็จเรียบร้อยแล้วโดยตัวประมวลผลข้อความ
    - *ยกเลิก* – ข้อความล้มเหลวที่จะประมวลผลในระหว่างความพยายามครั้งสุดท้ายและถูกยกเลิกโดยผู้ใช้
    - *ล้มเหลว* – ประมวลผลข้อความล้มเหลวในระหว่างความพยายามครั้งสุดท้าย ระบบจะลองใหม่ข้อความที่ล้มเหลวสามครั้ง จากนั้น จะยอมและปล่อยข้อความในสถานะ *ล้มเหลว* โปรดทราบว่าคุณไม่สามารถยกเลิกหรือแก้ไขข้อความได้ด้วยตนเองได้จนกว่าจะผ่านความพยายามครั้งสุดท้ายจากสามครั้งเหล่านี้

- **เนื้อหาข้อความ** – ตัวกรองนี้ทำการค้นหาข้อความแบบเต็มของเนื้อหาข้อความ (เนื้อหาข้อความไม่ถูกแสดงในกริด) ตัวกรองจะถือว่าสัญลักษณ์พิเศษส่วนใหญ่ (เช่น ยติภังค์) เป็นอักขระช่องว่าง และถือว่าอักขระพื้นที่ทั้งหมดเป็นตัวปฏิบัติการ OR แบบบูลีน ตัวอย่างเช่น หากคุณค้นหาค่า `journalid` เท่ากับ *USMF-123456* ระบบจะค้นหาข้อความทั้งหมดที่มี "USMF" หรือ "123456" ในกรณีนี้ รายการของผลลัพธ์อาจยาว ดังนั้น ควรป้อนเพียง *123456* อย่างเดียว เนื่องจากจะส่งคืนผลลัพธ์ที่เฉพาะเจาะจงมากขึ้น

คุณยังสามารถเรียงลำดับและกรองข้อมูลรายการด้วยการเลือกหัวข้อคอลัมน์ใดๆ และป้อนเงื่อนไขในกล่องโต้ตอบแบบหล่นลง

### <a name="view-the-message-log-message-content-and-details"></a>ดูล็อกข้อความ เนื้อหาข้อความ และรายละเอียด

คุณสามารถค้นหารายละเอียดเกี่ยวกับข้อความได้โดยเลือกข้อความนั้นในกริด แล้วจากนั้น เลือกแท็บ **ล็อก** หรือ **เนื้อหาดิบ** ภายใต้กริดข้อความ โดยที่เหตุการณ์การประมวลผลแต่ละเหตุการณ์จะแสดงขึ้น

แถบเครื่องมือบนแท็บ **ล็อก** จะรวมปุ่มต่อไปนี้:

- **ล็อก** – เลือกปุ่มนี้เพื่อแสดงผลลัพธ์การประมวลผล ปุ่มนี้มีประโยชน์โดยเฉพาะอย่างยิ่งเมื่อข้อความมีค่า **ผลลัพธ์ของการประมวลผล** ของ *ล้มเหลว* และคุณต้องการทราบเหตุผลของความล้มเหลวในการประมวลผล
- **กลุ่มงาน** – การดําเนินการประมวลผลข้อความหลายรายการสามารถเรียกใช้เป็นส่วนหนึ่งของกระบวนการชุดงานเดียวกันได้ เลือกปุ่มนี้เพื่อดูข้อมูลโดยละเอียดนี้ ตัวอย่างเช่น คุณสามารถดูว่ามีการอ้างอิงที่ต้องการลำดับการประมวลผลเฉพาะสำหรับบางข้อความ

### <a name="manually-process-or-cancel-a-message"></a>ประมวลผลหรือยกเลิกข้อความด้วยตนเอง

คุณสามารถประมวลผลหรือยกเลิกข้อความด้วยตนเองได้ตามต้องการ ตามสถานะปัจจุบัน ให้เลือกข้อความในกริด แล้วจากนั้น เลือก **กระบวนการ** หรือ **ยกเลิก** ในบานหน้าต่างการดำเนินการ

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>ตั้งค่าเหตุการณ์ทางธุรกิจเพื่อจัดส่งข้อความแจ้งเตือนสำหรับผลลัพธ์ของการประมวลผลที่ล้มเหลว

คุณสามารถตั้งค่า [เหตุการณ์ทางธุรกิจ](../../fin-ops-core/dev-itpro/business-events/home-page.md) ที่เตือนคุณเกียวกับผลลัพธ์ของการประมวลผลที่ล้มเหลว ไปที่ **การจัดการระบบ \> การตั้งค่า \> เหตุการณ์ทางธุรกิจ \> แค็ตตาล็อกเหตุการณ์ทางธุรกิจ** และให้เรียกใช้เหตุการณ์ทางธุรกิจที่ชื่อ *ข้อความของตัวประมวลผลข้อความที่ประมวลผล*

เนื่องจากเป็นส่วนหนึ่งของกระบวนการเรียกใช้ คุณจะได้รับพร้อมต์ให้ระบุว่าเหตุการณ์เป็นเหตุการณ์เฉพาะกับนิติบุคคลหนึ่งๆ หรือใช้กับนิติบุคคลทั้งหมดหรือไม่ นอกจากนี้ คุณยังได้รับพร้อมต์ให้ระบุค่า **ชื่อปลายทาง** ด้วย ต้องกำหนดค่านี้ก่อน

> [!NOTE]
> หาก **เมื่อเหตุการณ์ทางธุรกิจเกิดขึ้น** ถูกตั้งค่าเป็น *Microsoft Power Automate* (ตัวอย่างเช่น แทนที่จะเป็น *HTTPS*) ค่า **ชื่อปลายทาง** จะถูกสร้างขึ้นโดยอัตโนมัติใน Supply Chain Management ตามการตั้งค่า *Microsoft Power Automate*
