---
title: กำหนดการการเปลี่ยนแปลงปริมาณคงเหลือของการมองเห็นสินค้าคงคลังและปริมาณที่ให้สัญญาได้
description: บทความนี้อธิบายวิธีการจัดกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือในอนาคตและคํานวณปริมาณของปริมาณที่ให้สัญญาได้ (ATP)
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: f831c5d5719bbbd72c7cff37b8b35826f48ce6e4
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719320"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>กำหนดการการเปลี่ยนแปลงปริมาณคงเหลือของการมองเห็นสินค้าคงคลังและปริมาณที่ให้สัญญาได้

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการตั้งค่าคุณลักษณะ *กำหนดการการเปลี่ยนแปลงปริมาณคงเหลือ* เพื่อจัดกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือในอนาคตและคํานวณปริมาณของปริมาณที่ให้สัญญาได้ (ATP) ATP คือปริมาณของสินค้าที่พร้อมใช้งานและสามารถสัญญากับลูกค้าในรอบเวลาถัดไป การใช้การคํานวณนี้จะเพิ่มความสามารถในการเติมสินค้าตามใบสั่งของคุณมากขึ้น

สำหรับผู้ผลิต ผู้ค้าปลีก หรือผู้ขายหลายๆ ราย การรู้ว่าปัจจุบันมีอะไรอยู่บ้างยังไม่เพียงพอ พวกเขาต้องสามารถมองเห็นทั้งหมดสำหรับความพร้อมให้บริการในอนาคต ความพร้อมให้บริการในอนาคตนี้ควรพิจารณาถึงการจัดหาในอนาคต ความต้องการในอนาคต และ ATP

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>เปิดใช้งานและตั้งค่าคุณลักษณะ

ก่อนที่คุณจะสามารถใช้ ATP ได้ คุณต้องตั้งค่าการวัดที่คํานวณได้หนึ่งรายการขึ้นไปเพื่อคํานวณปริมาณ ATP คุณต้องเปิดคุณลักษณะและตั้งค่าคอนฟิกการตั้งค่า ATP ใน Microsoft Power Apps ด้วย

### <a name="set-up-calculated-measures-for-atp-quantities"></a>ตั้งค่าการวัดที่คํานวณได้เกี่ยวกับปริมาณ ATP

*การวัดที่คํานวณได้ของ ATP* เป็นการวัดที่คํานวณล่วงหน้าซึ่งโดยปกติจะใช้ในการค้นหาปริมาณคงเหลือที่พร้อมใช้งานในปัจจุบัน *ปริมาณการจัดหา* คือผลรวมของปริมาณสำหรับการวัดทางกายภาพที่มีชนิดตัวแก้ไข *การเพิ่ม* และ *ปริมาณความต้องการ* คือผลรวมของปริมาณสำหรับการวัดทางกายภาพที่มีชนิดตัวแก้ไข *การลบ*

คุณสามารถเพิ่มการวัดที่คํานวณได้หลายรายการเพื่อคํานวณหลายปริมาณ ATP อย่างไรก็ตาม จํานวนรวมของการวัดทางกายภาพที่ไม่ซ้ำระหว่างการวัดที่คํานวณได้ของ ATP ทั้งหมดควรน้อยกว่าเก้า

> [!IMPORTANT]
> การวัดที่คํานวณได้คือองค์ประกอบของการวัดทางกายภาพ สูตรสามารถรวมได้เฉพาะการวัดทางกายภาพโดยไม่มีข้อมูลใหม่ไม่มีการคํานวณหน่วยวัด

ตัวอย่างเช่น คุณสามารถตั้งค่าการวัดที่คำนวณได้ต่อไปนี้:

**ปริมาณคงเหลือที่มีอยู่** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

ผลรวม (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) แสดงถึงการจัดหา และผลรวม (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) แสดงถึงความต้องการ ด้วยเหตุนี้ จึงสามารถเข้าใจการวัดที่คํานวณได้ในลักษณะต่อไปนี้

**ปริมาณคงเหลือที่มีอยู่** = *การจัดหา* – *ความต้องการ*

คุณสามารถเพิ่มการวัดที่คํานวณได้อื่นเพื่อคํานวณปริมาณ ATP **คงเหลือที่มีอยู่จริง**

**ปริมาณคงเหลือที่มีอยู่** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

มีการวัดทางกายภาพที่แตกต่างกันแปดแบบระหว่างการวัดที่คํานวณได้ของ ATP สองรายการได้แก่: *PhysicalInvent*, *OnHand*, *Unrestricted*, *QualityInspection*, *Inbound*, *ReservPhysical*, *SoftReservePhysical* และ *Outbound*

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการวัดที่คำนวณได้ ดูที่ [การวัดที่คำนวณได้](inventory-visibility-configuration.md#calculated-measures)

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>เปิดคุณลักษณะกําหนดการการเปลี่ยนแปลงปริมาณคงเหลือและตั้งค่าคอนฟิกการตั้งค่า ATP

ปฏิบัติตามขั้นตอนเหล่านี้เพื่อเปิดคุณลักษณะ *กําหนดการการเปลี่ยนแปลงปริมาณคงเหลือ* ใน Power Apps ตั้งค่าคอนฟิกการตั้งค่า ATP

1. ลงชื่อเข้าใช้ Power Apps และเปิดการมองเห็นสินค้าคงคลัง
1. เปิดหน้า **การตั้งค่าคอนฟิก**
1. บนแท็บ **การจัดการคุณลักษณะ** ให้เปิดคุณลักษณะ *OnhandChangeSchedule*
1. เลือกแท็บ **การตั้งค่า ATP**
1. เมื่อคุณสอบถามการมองเห็นสินค้าคงคลัง จะมีผลลัพธ์ที่มีการวัดที่คํานวณได้แต่ละรายการที่คุณเพิ่มที่นี่ เลือก **เพิ่ม** เพื่อเพิ่มการวัดที่คํานวณใหม่สำหรับ ATP
1. ตั้งค่าฟิลด์เหล่านี้:

    - **แหล่งข้อมูล** – เลือกแหล่งข้อมูลที่สัมพันธ์กับการวัดที่คํานวณได้
    - **การวัดที่คํานวณได้** – เลือกการวัดที่คํานวณได้ที่สัมพันธ์กับแหล่งข้อมูลที่เลือก และที่คุณต้องการใช้เพื่อค้นหาปริมาณคงเหลือที่พร้อมใช้งานในปัจจุบัน
    - **รอบระยะเวลากำหนดการ** – ป้อนจํานวนวันที่ผู้ใช้สามารถดูและส่งกำหนดการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการเมื่อมีการใช้การวัดที่คํานวณได้ที่เลือก ผู้ใช้ที่สอบถามข้อมูลสินค้าคงคลังจะได้รับปริมาณคงเหลือ การเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการ และ ATP ของแต่ละวันในรอบระยะเวลานี้ ซึ่งเริ่มต้นด้วยวันที่ปัจจุบัน เลือกจํานวนเต็มระหว่าง 1 ถึง 7

    > [!IMPORTANT]
    > รอบระยะเวลากำหนดการมีวันที่ปัจจุบัน ดังนั้น ผู้ใช้สามารถจัดกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือที่จะเกิดขึ้นในเวลาใดๆ จากวันที่ปัจจุบัน (วันที่ที่ส่งการเปลี่ยนแปลง) จนถึง (รอบระยะเวลาตามกำหนดการ – 1) วันในอนาคต

1. เลือก **บันทึก**
1. ทำซ้ำขั้นตอนที่ 5 ถึง 7 จนกว่าคุณจะเพิ่มการวัดที่คํานวณได้ที่คุณต้องการสำหรับ ATP
1. เมื่อคุณตั้งค่าคอนฟิกการตั้งค่าที่กําหนดทั้งหมดเสร็จสิ้นแล้ว ให้เลือก **อัปเดตการตั้งค่าคอนฟิก**

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ทำการตั้งค่าคอนฟิกให้เสร็จสมบูรณ์และอัปเดต](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>วิธีการทำงานของกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือและการคํานวณ ATP

*กำหนดการการเปลี่ยนแปลงปริมาณคงเหลือ* จะสร้างวันที่และปริมาณที่คาดหวังของการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการ คุณสามารถส่งกําหนดการการเปลี่ยนแปลงปริมาณคงเหลือไปยังการมองเห็นสินค้าคงคลังหากวันที่อยู่ภายในรอบระยะเวลาที่กําหนดโดยการตั้งค่า **รอบระยะเวลากําหนดการ** (ดูที่ส่วน [เปิดใช้งานและตั้งค่าคุณลักษณะ](#setup)) ผู้ใช้ที่สอบถามข้อมูลสินค้าคงคลังจะได้รับปริมาณคงเหลือ การเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการ และ ATP ของแต่ละวันในรอบระยะเวลานั้น

การเปลี่ยนแปลงตามกำหนดการไม่มีข้อผูกมัดในขั้นต้น ดังนั้นจึงไม่ส่งผลต่อปริมาณคงเหลือจริงของคุณในระบบ เมื่อต้องการยืนยันการเปลี่ยนแปลง คุณต้องส่ง *เหตุการณ์การเปลี่ยนแปลงปริมาณคงเหลือ* ซึ่งอัปเดตปริมาณคงเหลือที่มีอยู่จริง จากนั้นคุณต้องแปลงกลับการเปลี่ยนแปลงตามกำหนดการโดยการส่งกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือสำหรับปริมาณค่าลบที่ตรงกัน

ตัวอย่างเช่น คุณส่งใบสั่งสำหรับจักรยาน 10 คันและคาดว่าใบสั่งนั้นจะมาถึงในวันพรุ่งนี้ ดังนั้นคุณจึงส่งกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือที่มีปริมาณสินค้าขาเข้าเท่ากับ 10 และลงวันที่ในวันพรุ่งนี้ เมื่อใบสั่งมาถึงในวันถัดไป คุณเพิ่มจักรยานในสินค้าคงคลังคงเหลือที่มีอยู่จริงของคุณ จากนั้นคุณต้องยืนยันการเปลี่ยนแปลงกับระบบของคุณเพื่ออัปเดตปริมาณคงเหลือจริง เมื่อต้องการยืนยันการเปลี่ยนแปลง คุณส่งเหตุการณ์การเปลี่ยนแปลงปริมาณคงเหลือที่มีปริมาณขาเข้าเป็น 10 จากนั้นคุณแปลงกลับการเปลี่ยนแปลงตามกำหนดการโดยการส่งกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือที่เป็นปริมาณขาเข้าที่ -10

เมื่อคุณสอบถามการมองเห็นสินค้าคงคลังสำหรับปริมาณคงเหลือและปริมาณ ATP จะมีการส่งคืนข้อมูลต่อไปนี้ของแต่ละวันในรอบระยะเวลาตามกำหนดการ

- **วันที่** – วันที่ที่จะใช้ผลลัพธ์ โซนเวลาคือเวลามาตรฐานสากล (UTC)
- **ปริมาณคงเหลือ** – ปริมาณคงเหลือจริงของวันที่ที่ระบุ การคํานวณนี้จะเป็นไปตามการวัดที่คํานวณได้ของ ATP ซึ่งตั้งค่าคอนฟิกไว้สำหรับการมองเห็นสินค้าคงคลัง
- **การจัดหาตามกำหนดการ** – ผลรวมของปริมาณขาเข้าซึ่งยังไม่ได้พร้อมใช้งานตามจริงกับปริมาณการใช้วัสดุทันทีหรือการจัดส่งในวันที่ที่ระบุ
- **ความต้องการตามกำหนดการ** – ผลรวมของปริมาณขาออกตามกำหนดการทั้งหมดซึ่งยังไม่ได้ใช้หรือจัดส่งในวันที่ที่ระบุ
- **ปริมาณ ATP** – ปริมาณคงเหลือที่ประมาณการขั้นต่ำที่พร้อมใช้งาน นับจากวันที่ที่ระบุจนถึงวันที่สิ้นสุดรอบระยะเวลาของกำหนดการ ปริมาณนี้รวมการปรับปรุงปริมาณตามกำหนดการทั้งหมด ปริมาณสูงสุดที่สามารถสัญญาได้ในวันที่ปัจจุบันสำหรับการจัดส่งหรือปริมาณการใช้วัสดุในวันนั้น

ตัวอย่างเช่น ถ้าวันที่ปัจจุบันคือ 1 กุมภาพันธ์ 2022 และรอบระยะเวลาของกำหนดการคือ 7 ผู้ใช้สามารถส่งการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการ ซึ่งคาดว่าจะเกิดขึ้นตั้งแต่วันที่ 1 กุมภาพันธ์ จนถึงวันที่ 7 กุมภาพันธ์ 2022 ในกรณีนี้ ปริมาณ ATP ของวันที่ 3 กุมภาพันธ์ จะคํานวณตามปริมาณคงเหลือของวันนั้นและปริมาณตามกำหนดการตั้งแต่วันที่ 3 กุมภาพันธ์ ถึงวันที่ 7 กุมภาพันธ์

## <a name="example"></a>ตัวอย่าง

ตัวอย่างต่อไปนี้แสดงให้เห็นว่าชุดการเปลี่ยนแปลงปริมาณตามกำหนดการจะมีผลกระทบต่อปริมาณคงเหลือและปริมาณ ATP ที่การมองเห็นสินค้าคงคลังรายงานอย่างไร และยังแสดงวิธีการยืนยันการเปลี่ยนแปลงตามกำหนดการ วิธีการที่การเปลี่ยนแปลงกำหนดการที่ยืนยันมีผลกับผลลัพธ์ และสิ่งที่อาจเกิดขึ้นถ้าคุณไม่ได้ยืนยันการเปลี่ยนแปลงกำหนดการ

ผลลัพธ์ในตัวอย่างนี้แสดงค่าของ *ปริมาณคงเหลือที่คาดการณ์* ค่านี้รวมการอัปเดตตามกำหนดการทั้งหมดเพื่อวัตถุประสงค์ในการอธิบาย แต่ไม่ได้รายงานจริงเมื่อคุณสอบถามในการมองเห็นสินค้าคงคลัง

1. ระบบจะตั้งค่าคอนฟิกการตั้งค่าต่อไปนี้ให้ระบบของคุณในหน้า **การตั้งค่า ATP** ใน Power Apps:

    - **การวัดที่คํานวณได้ของ ATP** – คุณมีการวัดที่คํานวณได้ที่ชื่อ *ปริมาณคงเหลือ* ซึ่งจะคํานวณเป็น *ปริมาณคงเหลือ = การจัดหา – ความต้องการ* คุณเลือกหน่วยวัดนั้นที่นี่
    - **รอบระยะเวลาของกำหนดการ** – คุณเลือก *7*

1. โดยมีเงื่อนไขดังนี้ร่วมด้วย:

    - วันที่ปัจจุบันคือ 1 กุมภาพันธ์ 2022
    - ปริมาณคงเหลือปัจจุบันคือ 20

1. สำหรับวันที่ปัจจุบัน (1 กุมภาพันธ์ 2022) คุณส่งปริมาณความต้องการตามกำหนดการเท่ากับ 3 ไปยังการมองเห็นสินค้าคงคลัง ดังนั้น ปริมาณคงเหลือที่คาดการณ์คือ 17 ตารางต่อไปนี้แสดงผลลัพธ์

    | วันที่ | ปริมาณคงคลังคงเหลือ | การจัดหาตามกำหนดการ | ความต้องการตามกำหนดการ | ปริมาณคงเหลือที่คาดการณ์ | ATP |
    | --- | --- | --- | --- | --- | --- |
    | วันที่ 2022-02-01 | 20 | | 3 | 17 | 17 |
    | วันที่ 2022-02-02 | 20 | | | 17 | 17 |
    | วันที่ 2022-02-03 | 20 | | | 17 | 17 |
    | วันที่ 2022-02-04 | 20 | | | 17 | 17 |
    | วันที่ 2022-02-05 | 20 | | | 17 | 17 |
    | วันที่ 2022-02-06 | 20 | | | 17 | 17 |
    | วันที่ 2022-02-07 | 20 | | | 17 | 17 |

1. สำหรับวันที่ปัจจุบัน (1 กุมภาพันธ์ 2022) คุณส่งปริมาณการจัดหาตามกำหนดการเป็น 10 สำหรับวันที่ 3 กุมภาพันธ์ 2022 ตารางต่อไปนี้แสดงผลลัพธ์

    | วันที่ | ปริมาณคงคลังคงเหลือ | การจัดหาตามกำหนดการ | ความต้องการตามกำหนดการ | ปริมาณคงเหลือที่คาดการณ์ | ATP |
    | --- | --- | --- | --- | --- | --- |
    | วันที่ 2022-02-01 | 20 | | 3 | 17 | 17 |
    | วันที่ 2022-02-02 | 20 | | | 17 | 17 |
    | วันที่ 2022-02-03 | 20 | 10 | | 27 | 27 |
    | วันที่ 2022-02-04 | 20 | | | 27 | 27 |
    | วันที่ 2022-02-05 | 20 | | | 27 | 27 |
    | วันที่ 2022-02-06 | 20 | | | 27 | 27 |
    | วันที่ 2022-02-07 | 20 | | | 27 | 27 |

1. ในวันที่ปัจจุบัน (1 กุมภาพันธ์ 2022) คุณส่งการเปลี่ยนแปลงปริมาณตามกำหนดการต่อไปนี้:

    - ปริมาณความต้องการ 15 สำหรับวันที่ 4 กุมภาพันธ์ 2022
    - ปริมาณการจัดหา 1 สำหรับวันที่ 5 กุมภาพันธ์ 2022
    - ปริมาณการจัดหา 3 สำหรับวันที่ 6 กุมภาพันธ์ 2022

    ตารางต่อไปนี้แสดงผลลัพธ์

    | วันที่ | ปริมาณคงคลังคงเหลือ | การจัดหาตามกำหนดการ | ความต้องการตามกำหนดการ | ปริมาณคงเหลือที่คาดการณ์ | ATP |
    | --- | --- | --- | --- | --- | --- |
    | วันที่ 2022-02-01 | 20 | | 3 | 17 | 12 |
    | วันที่ 2022-02-02 | 20 | | | 17 | 12 |
    | วันที่ 2022-02-03 | 20 | 10 | | 27 | 12 |
    | วันที่ 2022-02-04 | 20 | | วันที่ 15 ก.ย. | 12 | 12 |
    | วันที่ 2022-02-05 | 20 | 1 | | 13 | 13 |
    | วันที่ 2022-02-06 | 20 | 3 | | 16 | 16 |
    | วันที่ 2022-02-07 | 20 | | | 16 | 16 |

1. ในวันที่ปัจจุบัน (1 กุมภาพันธ์ 2022) คุณจัดส่งปริมาณความต้องการตามกำหนดการที่ 3 ดังนั้น คุณจึงต้องยืนยันการเปลี่ยนแปลงนี้เพื่อให้สะท้อนให้เห็นในปริมาณคงเหลือจริงของคุณ เมื่อต้องการยืนยันการเปลี่ยนแปลง คุณส่งเหตุการณ์การเปลี่ยนแปลงปริมาณคงเหลือที่มีปริมาณขาออกเป็น 3 จากนั้นคุณแปลงกลับการเปลี่ยนแปลงตามกำหนดการโดยการส่งกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือที่เป็นปริมาณขาออกที่ -3 ตารางต่อไปนี้แสดงผลลัพธ์

    | วันที่ | ปริมาณคงคลังคงเหลือ | การจัดหาตามกำหนดการ | ความต้องการตามกำหนดการ | ปริมาณคงเหลือที่คาดการณ์ | ATP |
    | --- | --- | --- | --- | --- | --- |
    | วันที่ 2022-02-01 | 17 | | 0 | 17 | 12 |
    | วันที่ 2022-02-02 | 17 | | | 17 | 12 |
    | วันที่ 2022-02-03 | 17 | 10 | | 27 | 12 |
    | วันที่ 2022-02-04 | 17 | | วันที่ 15 ก.ย. | 12 | 12 |
    | วันที่ 2022-02-05 | 17 | 1 | | 13 | 13 |
    | วันที่ 2022-02-06 | 17 | 3 | | 16 | 16 |
    | วันที่ 2022-02-07 | 17 | | | 16 | 16 |

1. ในวันถัดไป (2 กุมภาพันธ์ 2022) รอบระยะเวลาการจัดกำหนดการจะเลื่อนไปข้างหน้าหนึ่งวัน ตารางต่อไปนี้แสดงผลลัพธ์

    | วันที่ | ปริมาณคงคลังคงเหลือ | การจัดหาตามกำหนดการ | ความต้องการตามกำหนดการ | ปริมาณคงเหลือที่คาดการณ์ | ATP |
    | --- | --- | --- | --- | --- | --- |
    | วันที่ 2022-02-02 | 17 | | | 17 | 12 |
    | วันที่ 2022-02-03 | 17 | 10 | | 27 | 12 |
    | วันที่ 2022-02-04 | 17 | | วันที่ 15 ก.ย. | 12 | 12 |
    | วันที่ 2022-02-05 | 17 | 1 | | 13 | 13 |
    | วันที่ 2022-02-06 | 17 | 3 | | 16 | 16 |
    | วันที่ 2022-02-07 | 17 | | | 16 | 16 |
    | วันที่ 2022-02-08 | 17 | | | 16 | 16 |

1. อย่างไรก็ตาม สองวันต่อมา (4 กุมภาพันธ์ 2022) ปริมาณการจัดหาเท่ากับ 10 ที่จัดกำหนดการสำหรับวันที่ 3 กุมภาพันธ์ยังไม่มาถึง ตารางต่อไปนี้แสดงผลลัพธ์

    | วันที่ | ปริมาณคงคลังคงเหลือ | การจัดหาตามกำหนดการ | ความต้องการตามกำหนดการ | ปริมาณคงเหลือที่คาดการณ์ | ATP |
    | --- | --- | --- | --- | --- | --- |
    | วันที่ 2022-02-04 | 17 | | วันที่ 15 ก.ย. | 2 | 2 |
    | วันที่ 2022-02-05 | 17 | 1 | | 3 | 3 |
    | วันที่ 2022-02-06 | 17 | 3 | | 6 | 6 |
    | วันที่ 2022-02-07 | 17 | | | 6 | 6 |
    | วันที่ 2022-02-08 | 17 | | | 6 | 6 |
    | วันที่ 2022-02-09 | 17 | | | 6 | 6 |
    | วันที่ 2022-02-10 | 17 | | | 6 | 6 |

    ตามที่คุณเห็น การเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการ (แต่ไม่ได้ยืนยัน) จะไม่มีผลกระทบต่อปริมาณคงเหลือจริง

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>ส่งกำหนดการการเปลี่ยนแปลง เหตุการณ์การเปลี่ยนแปลง และการสอบถาม ATP ผ่าน API

คุณสามารถใช้ URL ของ Application Program Interface (API) ต่อไปนี้เพื่อส่งกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือ เหตุการณ์การเปลี่ยนแปลง และการสอบถาม

| พาธ | วิธีการ | คำอธิบาย |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | สร้างการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการหนึ่งเหตุการณ์ |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | สร้างการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการหลายเหตุการณ์ |
| `/api/environment/{environmentId}/onhand` | `POST` | สร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือหนึ่งเหตุการณ์ |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | สร้างเหตุการณ์การเปลี่ยนแปลงหลายเหตุการณ์ |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | การสอบถามโดยใช้วิธีการ `POST` |
| `/api/environment/{environmentId}/onhand` | `GET` | การสอบถามโดยใช้วิธีการ `GET` |
| `/api/environment/{environmentId}/onhand/exactquery` | `POST` | แยกการสอบถามโดยใช้วิธีการ `POST` |

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [API สาธารณะของการมองเห็นสินค้าคงคลัง](inventory-visibility-api.md)

### <a name="create-one-on-hand-change-schedule"></a>สร้างการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการหนึ่งเหตุการณ์

สร้างกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือโดยการส่งคำขอ `POST` ไปยัง URL ของบริการการมองเห็นสินค้าคงคลังที่เกี่ยวข้อง (ดูที่ส่วน [ส่งกำหนดการการเปลี่ยนแปลง เหตุการณ์การเปลี่ยนแปลง และการสอบถาม ATP ผ่าน API](#api-urls)) คุณยังสามารถส่งคำขอจำนวนมากได้เช่นกัน

กำหนดการการเปลี่ยนแปลงปริมาณคงเหลือสามารถสร้างก็ต่อเมื่อวันที่ตามกำหนดการอยู่ระหว่างวันที่ปัจจุบันและการสิ้นสุดรอบระยะเวลาของกำหนดการปัจจุบัน รูปแบบวันที่เวลาควรเป็น *ปี-เดือน-วัน* (ตัวอย่างเช่น **2022-02-01**) รูปแบบเวลาต้องถูกต้องเฉพาะวันเท่านั้น

API นี้จะสร้างกำหนดการการเปลี่ยนแปลงปริมาณคงคลังคงเหลือกำหนดการเดียว

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่างโดยไม่มี `dimensionDataSource`

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>สร้างกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือหลายกำหนดการ

API นี้สามารถสร้างเรกคอร์ดหลายรายการพร้อมกันได้ ความแตกต่างระหว่าง API นี้และ API เหตุการณ์เดียว ได้แก่ ค่า `Path` และค่า `Body` สำหรับ API นี้ `Body` จะมีแถวลำดับของเรกคอร์ด จำนวนเรกคอร์ดสูงสุดคือ 512 ดังนั้น API กลุ่มกำหนดการการเปลี่ยนแปลงปริมาณคงคลังคงเหลือสามารถสนับสนุนการเปลี่ยนแปลงกำหนดการได้มากถึง 512 การเปลี่ยนแปลงในคราวเดียว

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
                },
            },
        },
        ...
    ]
```

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง

```json
[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>สร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ

กำหนดเหตุการณ์การเปลี่ยนแปลงปริมาณคงเหลือโดยการส่งคำขอ `POST` ไปยัง URL ของบริการการมองเห็นสินค้าคงคลังที่เกี่ยวข้อง (ดูที่ส่วน [ส่งกำหนดการการเปลี่ยนแปลง เหตุการณ์การเปลี่ยนแปลง และการสอบถาม ATP ผ่าน API](#api-urls)) คุณยังสามารถส่งคำขอจำนวนมากได้เช่นกัน

> [!NOTE]
> เหตุการณ์การเปลี่ยนแปลงปริมาณคงเหลือซ้ำกับฟังก์ชัน ATP แต่เป็นส่วนหนึ่งของ API การมองเห็นสินค้าคงคลังมาตรฐาน ตัวอย่างนี้มีการรวมไว้เนื่องจากเหตุการณ์เกี่ยวข้องเมื่อคุณใช้งาน ATP เหตุการณ์การเปลี่ยนแปลงปริมาณคงเหลือจะคล้ายกับการจองการเปลี่ยนแปลงปริมาณคงเหลือ แต่ข้อความเหตุการณ์ต้องถูกส่งไปยัง API URL อื่น และเหตุการณ์จะใช้ `quantities` แทน `quantityByDate` ในเนื้อหาของข้อความ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเหตุการณ์การเปลี่ยนแปลงปริมาณคงเหลือและคุณลักษณะอื่นๆ ของ API ของการมองเห็นสินค้าคงคลัง ดูที่ [API สาธารณะสำหรับการมองเห็นสินค้าคงคลัง](inventory-visibility-api.md#create-one-onhand-change-event)

ตัวอย่างต่อไปนี้แสดงเนื้อหาคำขอที่มีเหตุการณ์การเปลี่ยนแปลงปริมาณคงเหลือครั้งเดียว

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>สอบถามเกี่ยวกับการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการและผลลัพธ์ ATP

คุณสามารถสอบถามเกี่ยวกับการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการและผลลัพธ์ ATP โดยการส่งคำขอ `POST` หรือคำขอ `GET` ไปยัง URL API ที่เหมาะสม ( ดูที่ส่วน [ส่งกำหนดการการเปลี่ยนแปลง เหตุการณ์การเปลี่ยนแปลง และการสอบถาม ATP ผ่าน API](#api-urls))

ในคำขอของคุณ ให้ตั้งค่า `QueryATP` เป็น *จริง* ถ้าคุณต้องการสอบถามเกี่ยวกับการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการและผลลัพธ์ ATP

- หากคุณส่งคำขอโดยใช้วิธีการ `GET` ให้ตั้งค่าพารามิเตอร์ใน URL
- หากคุณส่งคำขอโดยใช้วิธีการ `POST` ให้ตั้งค่าพารามิเตอร์ในเนื้อหาคำขอ

> [!NOTE]
> ไม่ว่าพารามิเตอร์ `returnNegative` จะถูกตั้งค่าเป็น *จริง* หรือ *เท็จ* ในเนื้อหาคำขอ ผลลัพธ์จะรวมค่าลบเมื่อคุณสอบถามการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการและผลลัพธ์ ATP ค่าลบเหล่านี้จะถูกรวมไว้ด้วยเนื่องจากหากมีการจัดกำหนดการเฉพาะใบสั่งความต้องการเท่านั้น หรือถ้าปริมาณการจัดหาน้อยกว่าปริมาณความต้องการ ปริมาณของการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการจะเป็นค่าลบ หากไม่รวมค่าลบ ผลลัพธ์อาจสร้างความสับสน สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวเลือกนี้และวิธีใช้งานการสอบถามอื่นๆ ดูที่ [API สาธารณะสำหรับการมองเห็นสินค้าคงคลัง](inventory-visibility-api.md#query-with-post-method)

### <a name="query-by-using-the-post-method"></a>สอบถามโดยใช้วิธีการ POST

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

ตัวอย่างต่อไปนี้แสดงวิธีการสร้างเนื้อหาคำขอการสอบถามดัชนีที่สามารถส่งไปยังการมองเห็นสินค้าคงคลังโดยใช้วิธีการ `POST`

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "SiteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-by-using-the-get-method"></a>สอบถามโดยใช้วิธีการ GET

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

ตัวอย่างต่อไปนี้แสดงวิธีการสร้าง URL คำขอการสอบถามดัชนีเป็นคำขอ `GET`

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

ผลลัพธ์ของคำขอ `GET` นี้จะเหมือนกับผลลัพธ์ของคำขอ `POST` ในตัวอย่างก่อนหน้านี้ทั้งหมด

### <a name="exact-query-by-using-the-post-method"></a>แยกการสอบถามโดยใช้วิธีการ POST

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

ตัวอย่างต่อไปนี้แสดงวิธีการสร้างเนื้อหาคำขอการสอบถามที่แน่ชัดที่สามารถส่งไปยังการมองเห็นสินค้าคงคลังโดยใช้วิธีการ `POST`

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "dimensions": ["SiteId", "LocationId"],
        "values": [
            ["1", "11"]
        ]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-result-example"></a>ตัวอย่างผลลัพธ์การสอบถาม

ตัวอย่างการสอบถามก่อนหน้าอาจทำให้เกิดการตอบกลับต่อไปนี้ ในตัวอย่างนี้ ระบบจะตั้งค่าคอนฟิกด้วยการตั้งค่าต่อไปนี้

- **การวัดที่คํานวณได้ของ ATP:** *iv.onhand = pos.inbound – pos.outbound*
- **รอบระยะเวลากำหนดการ:** *7*

ตัวอย่างของเนื้อหาการตอบกลับเป็นดังนี้

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
