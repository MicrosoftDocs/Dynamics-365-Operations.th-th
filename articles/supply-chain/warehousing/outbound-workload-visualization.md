---
title: การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก
description: บทความนี้มีข้อมูลเกี่ยวกับการจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก ฟังก์ชันนี้ทำให้ผู้จัดการคลังสินค้าและผู้บังคับบัญชาสร้างแผนภูมิปริมาณงานที่กำหนดเองซึ่งสามารถใช้เพื่อตรวจสอบความคืบหน้าของงานปัจจุบันและจำนวนเงินที่เหลืออยู่ ผู้จัดการคลังสินค้าสามารถสร้างหลายมุมมอง และตั้งค่าการรีเฟรชโดยอัตโนมัติได้ตามต้องการ
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78d0d81095bb52a314936dd7590a5690d94ecb15
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334429"
---
# <a name="outbound-workload-visualization"></a>การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก

[!include [banner](../includes/banner.md)]

ความสามารถในการตั้งค่าขั้นสูงที่สามารถเข้าถึงได้จากหน้า **การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก** ช่วยให้ผู้จัดการคลังสินค้าและผู้บังคับบัญชาสร้างแผนภูมิปริมาณงานที่กำหนดเองซึ่งสามารถใช้เพื่อตรวจสอบความคืบหน้าของงานปัจจุบันและจำนวนเงินที่เหลืออยู่ ผู้จัดการคลังสินค้าสามารถสร้างหลายมุมมอง และตั้งค่าการรีเฟรชโดยอัตโนมัติได้ตามต้องการ การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออกเหมาะสำหรับแสดงบนหน้าประสิทธิภาพของคลังสินค้า

ฟังก์ชันนี้สามารถใช้ในการติดตามความคืบหน้าของงานการเบิกสินค้า ลักษณะการทำงานที่ถูกรวมเข้ากับการจัดการแรงงาน และถ้ามีการตั้งค่าการจัดการแรงงานแสดงการจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออกสามารถแสดงการคำนวณจำนวนชั่วโมงที่ยังคงอยู่สำหรับงานการเบิกสินค้าที่แสดง (ถูกกรอง)

## <a name="turn-the-outbound-workload-visualization-feature-on-or-off"></a>เปิดหรือปิดคุณลักษณะการจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก

การใช้คุณลักษณะนี้ ต้องเปิดคุณลักษณะนี้ในระบบของคุณก่อน เริ่มจาก Supply Chain Management รุ่น 10.0.25 คุณลักษณะนี้จะเปิดไว้ ตามค่าเริ่มต้น เริ่มจาก Supply Chain Management เวอร์ชัน 10.0.29 คุณลักษณะนี้เป็นแบบบังคับ และไม่สามารถปิดได้ ถ้าคุณเรียกใช้รุ่นที่เก่ากว่า 10.0.29 ผู้ดูแลระบบสามารถเปิดหรือปิดฟังก์ชันนี้ได้โดยค้นหาคุณลักษณะ *การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก* ในพื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="set-up-outbound-workload-visualizations"></a>ตั้งค่าการจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก

เมื่อต้องการตั้งค่าการจัดรูปแบบการแสดงข้อมูลของคุณ คุณสร้างชุดของตัวกรองข้อมูล (มุมมอง) และการออกแบบแต่ละตัวกรองเพื่อให้แสดงชนิดการวิเคราะห์ที่แตกต่างกัน คุณสามารถใช้หน้า **ตั้งค่าคอนฟิกตัวกรอง** เพื่อออกแบบตัวกรอง

หากต้องการตั้งค่าการจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก ให้ปฏิบัติดังนี้

1. ไปที่ **การจัดการคลังสินค้า \> รายการการตรวจสอบความถูกต้องของคลังสินค้า \> การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก**

    หน้า **การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก** จะปรากฏขึ้น หลังจากที่คุณสร้างตัวกรองข้อมูลแล้ว หน้านี้จะแสดงการจัดรูปแบบการแสดงข้อมูลของคุณ คุณสามารถสร้างตัวกรองได้ตามต้องการ ตัวกรองทั้งหมดที่คุณสร้างจะได้รับการบันทึกไว้ภายใต้บัญชีผู้ใช้ของคุณ เพื่อให้คุณสามารถใช้ตัวกรองข้อมูลเหล่านี้ในภายหลังได้ กล่าวอีกอย่างหนึ่งคือ ผู้ใช้แต่ละรายจะมีชุดตัวกรองของตนเองที่สร้างขึ้น ตัวกรองข้อมูลดังกล่าวจะไม่มีการใช้ร่วมกับผู้ใช้อื่น

1. บนหน้า **การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก** ในบานหน้าต่างการดำเนินการ บนแท็บ **ตัวกรอง** ให้เลือก **ตั้งค่าคอนฟิกตัวกรอง**
1. บนหน้า **ตั้งค่าคอนฟิกตัวกรอง** ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มตัวกรองแล้วตั้งค่าฟิลด์ต่อไปนี้:

    - **ตารางกลุ่ม X** – เลือกตารางที่มีฟิลด์ที่ควรใช้ในการจัดกลุ่มค่าแกน X
    - **ฟิลด์กลุ่มแกน X** – จากระหว่างฟิลด์ของตารางที่คุณเลือกไว้ในฟิลด์ **ตารางกลุ่มแกน X** ให้เลือกฟิลด์ที่ควรใช้ในการจัดกลุ่มค่าแกน X
    - **ตารางค่า X** – เลือกตารางที่มีฟิลด์ที่ควรใช้ในการวิเคราะห์กลุ่มเพิ่มเติม
    - **ฟิลด์ค่าแกน X** – จากระหว่างฟิลด์ของตารางที่คุณเลือกไว้ในฟิลด์ **ตารางค่าแกน X** ให้เลือกฟิลด์ที่ให้ค่าที่ควรใช้ในการวิเคราะห์แต่ละกลุ่ม
    - **รีเฟรชอัตโนมัติ** – เลือกว่าควรรีเฟรชการจัดรูปแบบการแสดงข้อมูลอัตโนมัติหรือไม่
    - **ช่วงเวลารีเฟรช (นาที)** – ป้อนจำนวนนาทีระหว่างการรีเฟรชอัตโนมัติ
    - **ระดับการแสดง** – เลือกว่าแผนภูมิควรแสดงบรรทัดเปิดหรือการตรวจนับส่วนหัวที่เปิด
    - **ชนิดการเบิกสินค้า** – ถ้าคุณตั้งค่าฟิลด์ **ระดับการแสดงผล** เป็น _เปิดบรรทัด_ ให้เลือกว่าจำนวนของบรรทัดการทำงานที่เปิดค้างไว้ในแผนภูมิควรมีการเบิกสินค้าเริ่มต้น การเบิกสินค้าตามระยะ หรือทั้งการเบิกสินค้าเริ่มต้นและการเบิกสินค้าครั้งแรก
    - **ไซต์** – เลือกไซต์ที่จะโหลดแผนภูมิสำหรับ
    - **คลังสินค้า** – เลือกคลังสินค้าที่จะโหลดแผนภูมิสำหรับ
    - **จำนวนวันที่จะรวม** – ป้อนจำนวนวันในอดีตที่ควรสร้างแผนภูมิสำหรับ
    - **ชนิดของใบสั่งงาน** – เลือกชนิดใบสั่งงานขาออกเพื่อกรองข้อมูล

    ![หน้าตั้งค่าคอนฟิกตัวกรอง](media/work-viz-filters-1.png "ตั้งค่าคอนฟิกหน้าตัวกรอง")

1. ปิดหน้า **ตั้งค่าคอนฟิกตัวกรอง** เพื่อย้อนกลับไปที่หน้า **การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก**

    หน้า **การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออก** ในขณะนี้แสดงข้อมูล ตามการตั้งค่าตัวกรองข้อมูลใหม่ของคุณ ขณะนี้ตัวกรองข้อมูลใหม่ของคุณพร้อมใช้งานแล้วและเลือกไว้ในฟิลด์ **ตัวกรอง** ฟิลด์ต่อไปนี้จะพร้อมใช้งานที่ด้านบนของแผนภูมิ:

    - **ตัวกรอง** – ฟิลด์นี้จะมีตัวกรองทั้งหมดที่คุณสร้างขึ้นจนถึงขณะนี้ เลือกตัวกรองข้อมูลเพื่อดูข้อมูลในแผนภูมิ
    - **รีเฟรชครั้งล่าสุด** – ฟิลด์นี้แสดงวันที่และเวลาเมื่อมีการอัปเดตข้อมูลในแผนภูมิครั้งล่าสุด
    - **เวลาที่ประเมิน/จริง** – ถ้ามาตรฐานแรงงานมีการตั้งค่าในระบบของคุณ ให้กำหนดตัวเลือกนี้เป็น *ใช่* เพื่อแสดงเวลาการเบิกสินค้าโดยประมาณสะสมที่ด้านบนของแต่ละคอลัมน์ในแผนภูมิ ถ้าคุณไม่ได้ใช้มาตรฐานแรงงาน ตัวเลือกนี้จะไม่พร้อมใช้งาน

    ![การจัดรูปแบบการแสดงข้อมูลตัวอย่าง](media/work-viz-chart.png "การจัดรูปแบบการแสดงข้อมูลตัวอย่าง")

1. เลือกแถบใดก็ได้ในแผนภูมิเพื่อดูรายละเอียดของรายการงานที่เชื่อมโยง

    ![รายละเอียดรายการงาน](media/work-viz-work-details.png "รายละเอียดรายการงาน")

## <a name="example-outbound-workload-visualization-for-zones"></a>ตัวอย่าง: การจัดรูปแบบการแสดงข้อมูลปริมาณงานขาออกสำหรับโซน

สำหรับตัวอย่างนี้ คุณต้องการตั้งค่าการจัดรูปแบบการแสดงข้อมูลซึ่งแสดงรายการงานสำหรับแต่ละโซนและสถานะของบรรทัดงานแต่ละบรรทัด (_เปิด_ _ปิด_ หรือ _ยกเลิก_) ในกรณีนี้ คุณสามารถตั้งค่าตัวกรองข้อมูลที่มีการตั้งค่าต่อไปนี้

- **ชื่อตัวกรอง** – ป้อนชื่อสำหรับตัวกรองข้อมูลนี้ (เช่น _โซนเทียบกับสถานะของงาน_)
- **คำอธิบาย** – ป้อนคำอธิบายสั้น ๆ สำหรับตัวกรองข้อมูลนี้ (เช่น _โซนเทียบกับสถานะของงาน_)
- **ตารางกลุ่มแกน X** – เลือก _สถานที่เก็บ_
- **กลุ่มแกน X** – เลือก _รหัสโซน_
- **ตารางค่าแกน X** – เลือก _งาน_ เนื่องจากคุณต้องการดูงานสำหรับแต่ละโซน
- **ฟิลด์ค่าแกน X** – เลือก _สถานะงาน_ เนื่องจากคุณต้องการดูสถานะงาน
- **รีเฟรชอัตโนมัติ** – เลือกว่าควรรีเฟรชการจัดรูปแบบการแสดงข้อมูลอัตโนมัติหรือไม่
- **ชนิดการเบิกสินค้า** – เลือก _การเบิกสินค้าเริ่มต้นและการเบิกสินค้าตามระยะ_ เนื่องจากคุณต้องการรวมทั้งการเบิกสินค้าเริ่มต้นและการเบิกสินค้าจากสถานที่เป็นระยะ กล่าวอีกอย่างหนึ่งคือ คุณต้องการรวมรายการงานการเบิกสินค้าทั้งหมดที่คุณมีไว้เป็นหลัก
- **ระดับการแสดง** – เลือก _เปิดบรรทัด_ เนื่องจากคุณต้องการดูข้อมูลสำหรับแต่ละบรรทัดไม่ใช่ส่วนหัวของงาน

ภาพประกอบต่อไปนี้แสดงตัวอย่างของแผนภูมิผลลัพธ์

![การจัดรูปแบบการแสดงข้อมูลสถานะของงานเทียบกับโซน](media/work-viz-chart.png "การจัดรูปแบบการแสดงข้อมูลสถานะของงานเทียบกับโซน")

แผนภูมินี้แสดงสองโซนที่มีการตั้งชื่อว่า **ชั้น** และ **จำนวนมาก** บวกโซนที่ชื่อ **ว่างเปล่า** โซน **ว่างเปล่า** แสดงรายการงานทั้งหมดที่ไม่ได้เป็นสมาชิกของโซนใดก็ แผนภูมิจะแสดงข้อมูลที่ถูกกรองทั้งหมดที่ไม่เกี่ยวข้องทั้งหมดเป็น **ว่างเปล่า** เพื่อให้สามารถมองเห็นได้มากที่สุดเท่าที่จะเป็นไปได้ ในโซน **ชั้น** แผนภูมิจะแสดงบรรทัดที่ปิด 3 บรรทัดและมีบรรทัดเปิดสี่บรรทัด ในโซน **จำนวนมาก** แผนภูมิจะแสดงบรรทัดที่ปิดสี่บรรทัด มีบรรทัดเปิดหนึ่งบรรทัด และ 24 บรรทัดยกเลิก ในขั้นสุดท้าย แผนภูมิจะแสดงบรรทัดที่ปิดอยู่แปดบรรทัดที่ไม่ได้เป็นส่วนหนึ่งของโซนใดก็ตาม ดังนั้นจึงแสดงรายการเป็น **ว่างเปล่า**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]