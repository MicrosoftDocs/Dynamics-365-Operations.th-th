---
title: การวางแผนหลักที่มีข้อตกลงทางการค้าของการซื้อ
description: หัวข้อนี้จะอธิบายถึงวิธีที่การเพิ่มประสิทธิภาพของการวางแผนจะถูกค้นหาโดยผู้จัดจำหน่ายและ/หรือระยะเวลารอคอยสินค้าสำหรับแผนการใบสั่ง ตามราคาที่ดีที่สุดหรือระยะเวลารอคอยสินค้าที่พบในข้อตกลงทางการค้าของการซื้อ
author: ChristianRytt
manager: tfehr
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e060f20b65153a7bbe70996e6ff4c3930468348a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992257"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>การวางแผนหลักที่มีข้อตกลงทางการค้าของการซื้อ

[!include [banner](../../includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีที่การเพิ่มประสิทธิภาพของการวางแผนจะถูกค้นหาโดยผู้จัดจำหน่ายและ/หรือระยะเวลารอคอยสินค้าสำหรับแผนการใบสั่ง ตามราคาที่ดีที่สุดหรือระยะเวลารอคอยสินค้าที่พบในข้อตกลงทางการค้าของการซื้อทั้งหมดที่ระบุโดยผลิตภัณฑ์ที่กำหนด

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>เปิดข้อตกลงทางการค้าของการซื้อสำหรับคุณลักษณะการเพิ่มประสิทธิภาพการวางแผน

ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:

- **โมดูล:** *การวางแผนหลัก*
- **ชื่อคุณลักษณะ:** *ข้อตกลงทางการค้าของการซื้อสำหรับการเพิ่มประสิทธิภาพการวางแผน*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>จัดเตรียมระบบของคุณเพื่อประเมินข้อตกลงทางการค้าของการซื้อในระหว่างการวางแผนหลัก

ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกระบบของคุณเพื่อใช้การเพิ่มประสิทธิภาพของการวางแผนซึ่งประเมินข้อตกลงทางการค้าของการซื้อ

1. ไปที่ **การวางแผนหลัก \> การตั้งค่า \> พารามิเตอร์การวางแผนหลัก** บนแท็บ **แผนการใบสั่ง** ในส่วน **ผู้จัดจำหน่าย** ให้ตั้งค่าต่อไปนี้:

    - **ค้นหาข้อตกลงทางการค้า** – กำหนดตัวเลือกนี้เป็น **ใช่** เพื่อรวมข้อตกลงทางการค้าของการซื้อในการวางแผนหลัก
    - **เงื่อนไขการค้นหา** – เลือกตัวคูณที่คุณต้องการจัดระดับความสำคัญสำหรับข้อตกลงทางการค้าของการซื้อแต่ละฉบับ: **ระยะเวลารอคอยสินค้าต่ำสุด** หรือ **ราคาต่อหน่วยต่ำสุด**

1. ไปที่ **การจัดซื้อและการจัดหา \> การตั้งค่า \> ราคาและส่วนลด \> เปิดใช้งานราคา/ส่วนลด** และตรวจสอบให้แน่ใจว่าตัวเลือก **ผู้จัดจำหน่าย** ตั้งค่าเป็น **ใช่**
1. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> กลุ่มตัวแปรและกลุ่มมิติ \> กลุ่มมิติการจัดเก็บ** และเลือกกลุ่มมิติการจัดเก็บที่ใช้กับผลิตภัณฑ์ที่การวางแผนหลักควรประเมินข้อตกลงทางการค้าของการซื้อ ตรวจสอบให้แน่ใจว่าแต่ละมิติการจัดเก็บที่เกี่ยวข้องในกลุ่มนี้มีเครื่องหมายถูกในฟิลด์ **สำหรับราคาซื้อ** ทำซ้ำขั้นตอนนี้สำหรับกลุ่มมิติการจัดเก็บที่เกี่ยวข้องอื่นๆ ทั้งหมด

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>จัดเตรียมผลิตภัณฑ์ที่นำออกใช้เพื่อประเมินข้อตกลงทางการค้าของการซื้อในระหว่างการวางแผนหลัก

หลังจากที่ระบบของคุณเตรียมไว้ตามที่อธิบายไว้ในหัวข้อก่อนหน้านี้ คุณควรปฏิบัติตามขั้นตอนต่อไปนี้เพื่อให้แน่ใจว่ามีการตั้งค่าแต่ละผลิตภัณฑ์ที่คุณต้องการใช้ด้วยคุณลักษณะนี้ไว้อย่างถูกต้อง

1. ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้** แล้วเปิดผลิตภัณฑ์เป้าหมาย
1. บนแท็บด่วน **การซื้อ** ให้ตรวจสอบให้แน่ใจว่าไม่มีการกำหนดผู้จัดจำหน่ายในฟิลด์ **ผู้จัดจำหน่าย**
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **แผน** ในกลุ่ม **ความครอบคลุม** เลือก **ความครอบคลุมสินค้า** เพื่อเปิดหน้า **ความครอบคลุมสินค้า** สำหรับผลิตภัณฑ์ที่เลือก ตรวจสอบการตั้งค่าดังต่อไปนี้:

    - บนแท็บ **ทั่วไป** คุณสามารถตั้งค่าการแทนที่ผู้จัดจำหน่ายได้ ถ้าคุณต้องการให้การเพิ่มประสิทธิภาพการวางแผนใช้ข้อตกลงทางการค้าของการซื้อเพื่อเลือกผู้จัดจำหน่าย คุณควรป้องกันการแทนที่ผู้จัดจำหน่ายด้วยการล้างกล่องกาเครื่องหมาย **ใช้การตั้งค่าเฉพาะ**
    - บนแท็บ **ระยะเวลารอคอยสินค้า** คุณสามารถตั้งค่าการแทนที่ระยะเวลารอคอยสินค้าได้ ถ้าคุณต้องการให้การเพิ่มประสิทธิภาพการวางแผนใช้ข้อตกลงทางการค้าของการซื้อเพื่อเลือกระยะเวลารอคอยสินค้า คุณควรป้องกันการแทนที่ระยะเวลารอคอยสินค้า ยกเลิกการเลือกกล่องกาเครื่องหมายสำหรับระยะเวลารอคอยสินค้าแต่ละชนิดที่คุณต้องการเลือกด้วยการใช้ข้อตกลงทางการค้าของการซื้อ (**การซื้อ** **การผลิต** และ/หรือ **การโอนย้าย**)

1. ปิดหน้า **ความครอบคลุมสินค้า** เพื่อกลับไปที่หน้ารายละเอียดสำหรับผลิตภัณฑ์ที่เลือก
1. บนบานหน้าต่างการดำเนินการบนแท็บ **แผน** ในกลุ่ม **การคาดการณ์** ให้เลือก **การคาดการณ์การจัดหาวัสดุ** เพื่อเปิดหน้า **การคาดการณ์การจัดหาวัสดุ** ตรวจสอบให้แน่ใจว่าไม่มีแถวที่จะแสดงที่นี่มีค่าในคอลัมน์ **บัญชีผู้จัดจำหน่าย**
1. ปิดหน้า **การคาดการณ์การจัดหาวัสดุ** เพื่อกลับไปที่หน้ารายละเอียดสำหรับผลิตภัณฑ์ที่เลือก
1. บนบานหน้าต่างการดำเนินการบนแท็บ **การซื้อ** ในกลุ่ม **ข้อตกลงทางการค้า** ให้เลือก **ดูข้อตกลงทางการค้า** ตรวจสอบให้แน่ใจว่ามีการแสดงรายการข้อตกลงทางการค้าของการซื้อที่เกี่ยวข้องทั้งหมด นอกจากนี้โปรดตรวจสอบให้แน่ใจว่ามีการตั้งค่าตัวเลือก **ไม่คำนึงถึงระยะเวลารอคอยสินค้า** เป็น **ไม่** ใช้สำหรับข้อตกลงแต่ละรายการที่คุณต้องการเพิ่มประสิทธิภาพการวางแผนให้ใช้ระยะเวลารอคอยสินค้าที่ระบุสำหรับข้อตกลง
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **แผน** ในกลุ่ม **การตั้งค่าใบสั่ง** เลือก **การตั้งค่าใบสั่งเริ่มต้น** เพื่อเปิดหน้า **การตั้งค่าใบสั่งเริ่มต้น** สำหรับผลิตภัณฑ์ที่เลือก บนแท็บด่วน **ใบสั่งซื้อ** ให้ดูที่ค่าของฟิลด์ **ระยะเวลารอคอยสินค้าซื้อ** ถ้าไม่มีการกำหนดการแทนที่ระยะเวลารอคอยสินค้าตามความครอบคลุมของสินค้า การเพิ่มประสิทธิภาพการวางแผนจะใช้ค่านี้เมื่อเลือกข้อตกลงทางการค้าของการซื้อที่มีการตั้งค่าตัวเลือก **ไม่คำนึงถึงระยะเวลารอคอยสินค้า** เป็น **ใช่** ดังนั้นคุณจึงควรปรับปรุงค่านี้ตามที่คุณต้องการ
1. ทำขั้นตอนนี้ซ้ำสำหรับผลิตภัณฑ์ที่เกี่ยวข้อง

> [!NOTE]
> สกุลเงินของรายการข้อตกลงทางการค้าของการซื้อต้องตรงกับสกุลเงินของผู้จัดจำหน่ายที่เลือก การวางแผนหลักจะรวมข้อมูลจากบรรทัดข้อตกลงทางการค้าของการซื้อซึ่งสกุลเงินตรงกับสกุลเงินของผู้จัดจำหน่ายเท่านั้น

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>ตัวอย่างของวิธีที่การเพิ่มประสิทธิภาพของการวางแผนค้นพบผู้จัดจำหน่ายและระยะเวลารอคอยสินค้า

ตารางต่อไปนี้แสดงตัวอย่างที่แสดงวิธีการตั้งค่าต่างๆ สำหรับผลิตภัณฑ์ที่นำออกใช้และข้อตกลงทางการค้าที่เกี่ยวข้องกับการซื้อจะมีผลกระทบต่อค่าที่พบสำหรับแผนการใบสั่งซื้อที่เป็นผลลัพธ์ ค่า **ตัวหนา** ในสองคอลัมน์ด้านขวาสุดคือค่าที่เลือกโดยการเพิ่มประสิทธิภาพการวางแผน ค่า **_ตัวหนาและตัวเอียง_** ในคอลัมน์อื่นๆ คือการตั้งค่าที่สร้างค่าที่เป็นผลลัพธ์สำหรับแต่ละแถว

| ผลิตภัณฑ์ที่นำออกใช้: ผู้จัดจำหน่าย | การตั้งค่าใบสั่งเริ่มต้น: ระยะเวลารอคอยสินค้า | ความครอบคลุมสินค้า: แทนที่ผู้จัดจำหน่าย | ความครอบคลุมสินค้า: แทนที่ระยะเวลารอคอยสินค้า | ข้อตกลงทางการค้า: ผู้จัดจำหน่าย | ข้อตกลงทางการค้า: ระยะเวลารอคอยสินค้า | ข้อตกลงทางการค้า: ไม่คำนึงถึงระยะเวลารอคอยสินค้า | ผู้จัดจำหน่ายที่เป็นผลลัพธ์ | ระยะเวลารอคอยสินค้าที่เป็นผลลัพธ์ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| _*_US001_*_ | _*_1_*_ | หมายเลข | หมายเลข | US003 | 3 | หมายเลข | **US001** | **1** |
| US001 | 1 | **_ใช่: US002_* _ | _*_ใช่: 2_*_ | US003 | 3 | หมายเลข | **US002** | **2** |
| *(ว่างเปล่า)* | 1 | หมายเลข | หมายเลข | ***US003** _ | _*_3_*_ | หมายเลข | **US003** | **3** |
| *(ว่างเปล่า)* | ***1** _ | หมายเลข | หมายเลข | _*_US003_*_ | 3 | ใช่ | **US003** | **1** |
| *(ว่างเปล่า)* | ***1** _ | _*_ใช่: US002_*_ | หมายเลข | US003 | 3 | หมายเลข | **US002** | **1** |
| *(ว่างเปล่า)* | ***1** _ | _*_ใช่: US002_*_ | หมายเลข | US003 | 3 | หมายเลข | **US002** | **1** |
| *(ว่างเปล่า)* | 1 | หมายเลข | ใช่: 2 | ***US003** _ | _*_3_*_ | หมายเลข | **US003** | **3** |
| *(ว่างเปล่า)* | 1 | หมายเลข | ***ใช่: 2** _ | _*_US003_*_ | 3 | ใช่ | **US003** | **2** |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ข้อตกลงการซื้อ](../../procurement/purchase-agreements.md)
