---
title: แผนการบำรุงรักษา
description: บทความนี้อธิบายถึงแผนการบำรุงรักษาในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectType, EntAssetCounterType, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6303af9a9d4d4565deba9ca8893535554d03c274
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335030"
---
# <a name="maintenance-plans"></a>แผนการบำรุงรักษา

[!include [banner](../../includes/banner.md)]

แผนการบำรุงรักษาจะกำหนดเวลาที่จะมีการดำเนินงานบำรุงรักษาเชิงป้องกันที่วางแผนไว้ล่วงหน้าในสินทรัพย์ แผนการบำรุงรักษาอาจเกี่ยวข้องกับสินทรัพย์ ชนิดสินทรัพย์ ตำแหน่งที่ทำงาน หรือชนิดของตำแหน่งที่ทำงาน แต่ก่อนอื่นคุณต้องสร้างแผนการบำรุงรักษาที่จะใช้ในบริษัทของคุณ

แผนการบำรุงรักษาอาจมีรายการแผนการบำรุงรักษาหลายรายการ มีการระบุชนิดของงานการบำรุงรักษาและช่วงอยู่บนรายการแผนการบำรุงรักษา มีชนิดของรายการแผนการบำรุงรักษาสองชนิด:

- เวลา
- ตัวนับ

รายการแผนการบำรุงรักษาของชนิด "เวลา" ถูกใช้สำหรับการบำรุงรักษาตามแผนที่เกิดซ้ำตามช่วงเวลาคงที่ รายการแผนการบำรุงรักษาของชนิด "ตัวนับ" ถูกใช้สำหรับการบำรุงรักษาที่วางแผนไว้ หรือการบำรุงรักษาเชิงรับ ตามการลงทะเบียนของตัวนับสินทรัพย์ แผนการบำรุงรักษาอาจรวมถึงรายการแผนการบำรุงรักษาต่างๆ ของทั้งสองชนิด

>[!NOTE]
>ถ้าไม่มีการลงทะเบียนค่าตัวนับสำหรับชนิดตัวนับในสินทรัพย์ รายการแผนการบำรุงรักษาจะถูกเว้นไว้

ขั้นแรก คุณสร้างแผนการบำรุงรักษาที่จำเป็นสำหรับงานบำรุงรักษาเชิงป้องกันของคุณ และเลือกชนิดสินทรัพย์ สินทรัพย์ ชนิดตำแหน่งที่ทำงาน และตำแหน่งที่ทำงานที่ควรเกี่ยวข้องกับแผนการบำรุงรักษาแต่ละแผน หลังจากนั้น ถ้าต้องการ คุณยังสามารถเพิ่มแผนการบำรุงรักษาไปยังสินทรัพย์ หรือตำแหน่งที่ทำงานซึ่งทำในแท็บด่วน **สินทรัพย์ทั้งหมด** \> เลือกสินทรัพย์ \> **แผนการบำรุงรักษาสินทรัพย์** หรือแท็บด่วน **ตำแหน่งที่ทำงานทั้งหมด** \> เลือกตำแหน่งที่ทำงาน \> **แผนการบำรุงรักษา**

ถ้าคุณเพิ่มแผนการบำรุงรักษาไปยังชนิดสินทรัพย์หรือชนิดตำแหน่งที่ทำงาน หมายความว่าเมื่อคุณสร้างสินทรัพย์ใหม่หรือตำแหน่งที่ทำงานใหม่ที่มีชนิดสินทรัพย์หรือชนิดตำแหน่งที่ทำงานเหล่านั้น จะมีการเพิ่มสินทรัพย์หรือตำแหน่งที่ทำงานไปยังแผนการบำรุงรักษาโดยอัตโนมัติ วันที่เริ่มต้นของความสัมพันธ์กับแผนการบำรุงรักษาจะเป็นวันที่ปัจจุบัน ซึ่งอาจจำเป็นต้องมีการปรับปรุง

## <a name="set-up-maintenance-plans"></a>ตั้งค่าแผนการบำรุงรักษา

ส่วนนี้จะอธิบายวิธีการตั้งค่ารายการแผนการบำรุงรักษา และแสดงตัวอย่างของวิธีการใช้งาน

1. ไปที่ **การจัดการสินทรัพย์ \> การตั้งค่า \> การบำรุงรักษาเชิงป้องกัน \> แผนการบำรุงรักษา**

1. เลือก **ใหม่** เพื่อสร้างลำดับใหม่

1. ใส่รหัสลงในฟิลด์ **ลำดับการบำรุงรักษา** และชื่อในฟิลด์ **ชื่อ**

1. ในฟิลด์ **วันที่วางแผน** ให้ป้อนวันที่เริ่มต้นซึ่งสามารถทำการวางแผนบนแผนการบำรุงรักษาได้ โปรดทราบว่ารายการแผนการบำรุงรักษาตามเวลาอาจมีวันที่วางแผนอื่นๆ

1. เลือก "ใช่" ในปุ่มสลับ **ที่ใช้งานอยู่** เพื่อเรียกใช้งานแผนการบำรุงรักษา

    >[!NOTE]
    >ถ้าคุณปิดใช้งานแผนการบำรุงรักษา จะไม่มีการสร้างการลงรายการบัญชีของกำหนดการในกำหนดการบำรุงรักษา เมื่อคุณรันงานแผนการบำรุงรักษาของกำหนดการ

1. ฟิลด์ **วันที่ยอมรับได้ก่อนหน้า** และ **วันที่ยอมรับได้หลังจาก** เกี่ยวข้องกับรายการแผนการบำรุงรักษาที่มีการเลือกกล่องกาเครื่องหมาย **ระงับงานการบำรุงรักษาที่ทับซ้อนกัน** (อ้างถึงขั้นตอนที่ 17) ฟิลด์ "ค่าเผื่อ" ถูกใช้ในการขยายช่วงเวลาเป็นจำนวนวัน ซึ่งถ้าแผนการบำรุงรักษาต่างๆ ทับซ้อนกัน งานที่ครอบคลุม/ใหญ่ที่สุด จะถูกสร้างเป็นรายการกำหนดการบำรุงรักษาในระหว่างการจัดกำหนดการบำรุงรักษา ในขณะที่มีการข้ามงานที่ทับซ้อนกันที่บ่อยที่สุดในระหว่างการจัดกำหนดการวางแผนการบำรุงรักษา แทรกจำนวนของวันในฟิลด์ **วันที่ยอมรับได้ก่อนหน้า** ตัวอย่างเช่น "2"

1. ถ้าคุณได้แทรกค่าใน **วันที่ยอมรับได้ก่อนหน้า** นอกจากนี้ ให้แทรกจำนวนวันในฟิลด์ **วันที่ยอมรับได้หลังจาก** ตัวอย่างเช่น "2"

    >[!NOTE]
    >ตัวอย่างที่อธิบายไว้ในขั้นตอนนี้และขั้นตอนก่อนหน้านี้หมายความว่า ถ้ารายการแผนการบำรุงรักษาต่างๆ ซ้อนทับกัน และมีการเลือก **ระงับงานการบำรุงรักษาที่ทับซ้อน** สำหรับหนึ่งรายการขึ้นไป รอบระยะเวลาของการละเว้นรายการกำหนดการบำรุงรักษาถูกขยายเป็นทั้งหมดห้าวัน (วันที่เริ่มต้นที่คาดไว้ในรายการกำหนดการบำรุงรักษา *และ* สองวันก่อนหน้า *และ* สองวันหลังจากวันที่ดังกล่าว)

1. ฟิลด์ในกลุ่ม **รายละเอียด** บน FastTab **รายละเอียด** แสดงจำนวนของรายการแผนการบำรุงรักษาที่ตั้งค่าไว้ในแผนการบำรุงรักษา และจำนวนของสินทรัพย์และตำแหน่งที่ทำงานที่เกี่ยวข้องกับแผนการบำรุงรักษา

1. บนแท็บด่วน **รายการ** เลือก **เพิ่มรายการเวลา** หรือ **เพิ่มรายการตัวนับสินทรัพย์** เพื่อสร้างรายการแผนการบำรุงรักษาใหม่

1. แทรกคำอธิบายสำหรับรายการในฟิลด์ **คำอธิบายใบสั่งงาน** คำอธิบายจะถูกโอนย้ายไปยังใบสั่งงานที่เกี่ยวข้อง

1. ในฟิลด์ **ชนิดงานบำรุงรักษา** ให้เลือกชนิดงานที่สัมพันธ์กับรายการแผนการบำรุงรักษา

1. ในฟิลด์ **ตัวแปรชนิดงานบำรุงรักษา** และฟิลด์ **การค้า** ให้เลือกตัวแปรและการค้าที่เกี่ยวข้องกับชนิดงานบำรุงรักษา

1. ในฟิลด์ **เสร็จสิ้นภายในวัน** และฟิลด์ **เสร็จสิ้นภายในชั่วโมง** คุณสามารถแทรกวันที่สิ้นสุดที่คาดไว้เป็นวันหรือชั่วโมง วันที่สิ้นสุดที่คาดไว้จะถูกแทรกให้สอดคล้องกับวันที่เริ่มต้นที่คาดไว้ ซึ่งจะถูกคำนวณเมื่อมีการสร้างรายการกำหนดการบำรุงรักษา ตัวอย่างเช่น คุณสามารถแทรก "7" ในฟิลด์ **เสร็จสิ้นภายในวัน** เพื่อบ่งชี้ว่างานที่เกี่ยวข้องควรมีการดำเนินการให้เสร็จสมบูรณ์ภายในหนึ่งสัปดาห์ ตั้งแต่วันที่เริ่มต้นที่คาดไว้

1. ในฟิลด์ **ชนิดช่วงเวลา** ให้เลือกชนิดของช่วงเวลาที่จะใช้ในรายการแผนการบำรุงรักษา ตัวอย่างเช่น "ทำซ้ำ..." หรือ "เมื่อ..." อ้างอิงถึงตาราง [ภาพรวมของชนิดช่วงเวลา](#interval-types) ข้างล่างนี้ สำหรับคำอธิบายของความสัมพันธ์ระหว่างชนิดของช่วงและชนิดของรายการ

1. ฟิลด์ **รอบระยะเวลา** เกี่ยวข้องกับชนิดรายการตามเวลาเท่านั้น เลือกชนิดของรอบระยะเวลาที่เกี่ยวข้องกับความถี่ของรอบระยะเวลา

1. ในฟิลด์ **ความถี่ของรอบระยะเวลา** ให้แทรกจำนวนครั้งที่รายการควรถูกใช้สำหรับการวางแผนงานบำรุงรักษาเชิงป้องกัน ตัวอย่าง: ถ้าคุณได้สร้างรายการของชนิด "ตัวนับ" และตัวนับของคุณเป็นปริมาณการผลิต และคุณแทรกหมายเลข "20000" ในฟิลด์นี้ รายการลำดับการบำรุงรักษาใหม่จะถูกสร้างขึ้นระหว่างการจัดกำหนดการบำรุงรักษาเชิงป้องกัน ทุกครั้งที่คุณถูกคาดหวังว่าจะผลิตสินค้าเพิ่ม 20,000 รายการ

1. กล่องกาเครื่องหมาย **ระงับงานบำรุงรักษาที่ทับซ้อนกัน** เกี่ยวข้องกับชนิดรายการตามเวลา เช่นเดียวกับตามตัวนับ เลือกกล่องกาเครื่องหมายเพื่อลบรายการกำหนดการบำรุงรักษาที่สร้างขึ้นในวันที่เดียวกัน ตัวอย่างเช่น การดำเนินการนี้จะเกี่ยวข้อง ถ้าคุณได้สร้างรายการการตรวจสอบ 1 เดือน รายการการตรวจสอบ 6 เดือน และรายการการตรวจสอบ 1 ปี สำหรับการตรวจสอบ 1 ปี คุณต้องการให้เฉพาะการตรวจสอบนั้นเสร็จสิ้น ไม่ใช่การตรวจสอบอีกสองรายการ ซึ่งยังอาจทำให้พอดีกับกรอบเวลา เมื่อต้องการตั้งค่าตัวอย่างนี้อย่างถูกต้อง คุณตั้งค่ารายการการตรวจสอบ 1 ปีเป็นรายการแรก รายการ 6 เดือนเป็นรายการที่สอง และรายการ 1 เดือนเป็นรายการที่สาม และคุณเลือกกล่องกาเครื่องหมาย **ระงับงานบำรุงรักษาที่ทับซ้อนกัน** สำหรับรายการ 1 เดือน และ 6 เดือน ด้วยวิธีการนั้น คุณตรวจสอบให้แน่ใจว่าเมื่อคุณไปถึงเครื่องหมาย 1 ปี การตรวจสอบสำหรับหนึ่งเดือนและหกเดือนจะถูกละเว้น และมีการสร้างเฉพาะรายการกำหนดการบำรุงรักษาสำหรับรายการการตรวจสอบ 1 ปีเท่านั้น

    >[!NOTE]
    >ตัวอย่างที่อธิบายไว้ในขั้นตอนนี้แสดงให้เห็นว่างานที่ครอบคลุมมากที่สุด ซึ่งประกอบด้วยจำนวนงานที่มากที่สุด และไม่มีการดำเนินการบ่อยครั้ง ควรมีการแทรกเป็นรายการแรกเสมอ จากนั้น งานที่ใช้บ่อยมากกว่าจะถูกแทรกเป็นรายการแยกต่างหากตามลำดับของความถี่ ซึ่งวางงานที่ใช้บ่อยที่สุดที่ด้านล่างของรายการ

1. ฟิลด์ **ตัวนับ** เกี่ยวข้องกับชนิดรายการตามตัวนับเท่านั้น เลือกชนิดตัวนับที่จะใช้ในรายการ ถ้าชนิดตัวนับไม่ได้ใช้งานอยู่ในสินทรัพย์ที่เกี่ยวข้อง จะมีการละเว้นรายการแผนการบำรุงรักษา

1. ฟิลด์ **กรอบเวลาของตัวนับสินทรัพย์ในจำนวนวัน** เกี่ยวข้องกับชนิดของรายการตามตัวนับเท่านั้น แทรกหมายเลขที่กำหนดจำนวนวันการลงทะเบียนตัวนับย้อนหลังของจำนวนวันที่จะมีการเลือก เมื่อจัดกำหนดการบำรุงรักษาให้เสร็จสมบูรณ์ นี่หมายความว่า ระยะเวลาที่ข้อมูลย้อนกลับไปซึ่งใช้เป็นพื้นฐานสำหรับการคำนวณแนวโน้ม ซึ่งจะกำหนดจำนวนรายการของกำหนดการบำรุงรักษาที่จะมีการสร้าง

    >*ตัวอย่าง:* ถ้าคาดว่าจะมีการทำการลงทะเบียนตัวนับเดือนละครั้ง คุณอาจแทรกหมายเลข '365' ในฟิลด์นี้ เนื่องจากการจัดกำหนดการแผนการบำรุงรักษาจะขึ้นอยู่กับ 12 เดือนที่ผ่านมาเสมอ ดังนั้นจึงสร้างรายการกำหนดการบำรุงรักษาตามแนวโน้มของปีที่ผ่านมา ในทางตรงกันข้าม ถ้าคุณแทรกหมายเลข '10' ในฟิลด์นี้ คุณคาดว่าจะมีการทำการลงทะเบียนตัวนับบ่อยครั้งมากขึ้น ตัวอย่างเช่น รายวัน นี่หมายความว่า เมื่อคุณจัดกำหนดการแผนบำรุงรักษา การลงทะเบียนตัวนับสำหรับ 10 วันสุดท้าย จะใช้เป็นข้อมูลพื้นฐานสำหรับการจัดกำหนดการของรายการกำหนดการบำรุงรักษา

1. ฟิลด์ **วันที่วางแผน** เกี่ยวข้องกับชนิดรายการตามเวลาเท่านั้น ถ้ารายการแผนการบำรุงรักษามีวันที่วางแผนอื่น นอกเหนือจากแผนการบำรุงรักษาทั้งหมด ให้เลือกวันที่ในฟิลด์ **วันที่วางแผน** บนรายการ

1. ในฟิลด์ **ระดับบริการ** คุณสามารถเลือกระดับบริการของใบสั่งงานเป็นการกำหนดเขตเพิ่มเติมในรายการแผนการบำรุงรักษา - ที่จะใช้เป็นระดับบริการในใบสั่งงาน

1. เลือกกล่องกาเครื่องหมาย **สร้างอัตโนมัติ** ถ้าคุณต้องการให้มีการสร้างใบสั่งงานโดยอัตโนมัติตามรายการแผนการบำรุงรักษาที่เลือก เมื่อจัดกำหนดการแผนการบำรุงรักษา

1. ถ้าคุณเลือกกล่องกาเครื่องหมาย **สร้างโดยอัตโนมัติ** คุณสามารถเลือกชนิดของใบสั่งงานสำหรับใบสั่งงานที่สร้างขึ้นโดยอัตโนมัติในฟิลด์ **ชนิดใบสั่งงาน** ถ้าคุณเลือกกล่องกาเครื่องหมาย **สร้างอัตโนมัติ** และคุณไม่ได้เลือกชนิดใบสั่งงานในฟิลด์นี้ ชนิดของใบสั่งงานที่เลือกในลิงค์ **การจัดการสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การจัดการสินทรัพย์ \> ใบสั่งงาน** ฟิลด์ \> **ชนิดของใบสั่งงานเชิงป้องกัน** จะถูกใช้

1. ใช้ฟิลด์ **ตั้งแต่ฤดูกาล** และ **ถึงฤดูกาล** เพื่อสร้างรายการแผนการบำรุงรักษาตามเวลาที่ทำซ้ำภายในรอบระยะเวลา 12 เดือน *ตัวอย่าง :* อุปกรณ์ที่ใช้ในการรักษาพื้นที่สีเขียวต้องมีบริการในฤดูใบไม้ผลิแต่ละครั้ง ภายในรอบระยะเวลาที่กำหนดไว้ล่วงหน้า แทรกวันที่เริ่มต้นของรอบระยะเวลาที่จะทำซ้ำในฟิลด์ **ตั้งแต่ฤดูกาล**

1. แทรกวันที่สิ้นสุดของรอบระยะเวลาที่จะทำซ้ำในฟิลด์ **ถึงฤดูกาล**

1. ในฟิลด์ **รอบระยะเวลาที่เป็นผลลัพธ์** จะมีการแสดงรอบระยะเวลาปัจจุบันที่จะทำซ้ำ เมื่อมีการส่งผ่านรอบระยะเวลาปัจจุบัน และคุณเริ่มต้นปีใหม่ รอบระยะเวลาที่แสดงในฟิลด์นี้จะถูกปรับปรุงเพื่อให้สะท้อนถึงรอบระยะเวลาถัดไปในลำดับที่ซ้ำกัน

1. บน FastTab **สินทรัพย์** ให้เลือกสินทรัพย์ที่ควรเกี่ยวข้องกับแผนการบำรุงรักษา

1. บน FastTab **ชนิดสินทรัพย์** ให้เลือกชนิดสินทรัพย์ที่ควรเกี่ยวข้องกับแผนการบำรุงรักษา

1. บน FastTab **ตำแหน่งที่ทำงาน** ให้เลือกตำแหน่งที่ทำงานที่ควรเกี่ยวข้องกับแผนการบำรุงรักษา ถ้าจำเป็น คุณสามารถทำให้การตั้งค่าเป็นแบบเฉพาะเจาะจงมากขึ้นโดยการเลือกชนิดสินทรัพย์ ผู้ผลิต และแบบจำลองที่เกี่ยวข้อง

1. บน FastTab **ชนิดตำแหน่งที่ทำงาน** ให้เลือกชนิดตำแหน่งที่ทำงานที่ควรเกี่ยวข้องกับแผนการบำรุงรักษา

>[!NOTE]
>เมื่อมีการสร้างใบสั่งงานด้วยตนเองในสินทรัพย์ที่ครอบคลุมโดยการรับประกันของผู้จัดจำหน่าย กล่องโต้ตอบจะแสดงขึ้นเพื่อให้ผู้ใช้ทราบถึงการรับประกัน จากนั้น การสร้างของใบสั่งงานสามารถถูกยกเลิกได้ มีการละเว้นการตรวจสอบความสัมพันธ์ของการรับประกันสำหรับใบสั่งงานที่สร้างขึ้นโดยอัตโนมัติ

<a id="interval-types"></a>

## <a name="interval-types-overview"></a>ภาพรวมของชนิดช่วงเวลา

| ชนิดและคำอธิบายของช่วงเวลา | ชนิดรายการ: เวลา | ชนิดรายการ: ตัวนับ |
|---|---|---|
| **ชนิดของช่วง: เกิดซ้ำตั้งแต่วันที่วางแผน** การตรวจนับจะเริ่มต้นจากวันที่วางแผนใช้ เมื่อคุณจัดกำหนดการแผนการบำรุงรักษา รายการกำหนดการบำรุงรักษาจะถูกสร้างขึ้นเมื่อถึงช่วงเวลา | มีการใช้ **วันที่วางแผน** บนรายการแผนการบำรุงรักษา ถ้าไม่ได้เลือกวันที่วางแผนไว้ในรายการ **วันที่วางแผน** สำหรับแผนการบำรุงรักษาจะถูกใช้ ตัวอย่าง: ถ้ามีการแทรกตัวเลข "3" ในฟิลด์ **ความถี่ของรอบระยะเวลา** และ "ปี" ถูกเลือกในฟิลด์ **รอบระยะเวลา** รายการกำหนดการบำรุงรักษาใหม่จะถูกสร้างขึ้นทุกๆ 3 ปี | มีการใช้ **วันที่วางแผน** สำหรับแผนการบำรุงรักษา ถ้าตัวนับได้ถูกแทนที่ จะมีการใช้วันที่เปลี่ยนทดแทนล่าสุดเป็นวันที่วางแผน |
| **ชนิดของช่วง: ทำซ้ำตั้งแต่วันที่เริ่มต้น** การตรวจนับจะเริ่มต้นจากวันที่เริ่มต้นในความสัมพันธ์ของสินทรัพย์ มีการเลือกวันที่ในฟิลด์ **สินทรัพย์ทั้งหมด** มุมมองรายละเอียด \> **แผนการบำรุงรักษาสินทรัพย์** แท็บด่วน \> **วันที่เริ่มต้น** หรือ ในฟิลด์ **ตำแหน่งที่ทำงานทั้งหมด** มุมมองรายละเอียด \> **แผนการบำรุงรักษา** แท็บด่วน \> **วันที่เริ่มต้น** เมื่อคุณจัดกำหนดการแผนการบำรุงรักษา รายการกำหนดการบำรุงรักษาจะถูกสร้างขึ้น เมื่อถึงช่วงเวลา | วันที่เริ่มต้นของรายการแผนการบำรุงรักษาในสินทรัพย์ หรือตำแหน่งที่ทำงาน จะถูกใช้ ถ้าฟิลด์นี้ว่างเปล่า จะมีการใช้ **วันที่วางแผน** สำหรับแผนการบำรุงรักษา | วันที่เริ่มต้นของรายการแผนการบำรุงรักษาในสินทรัพย์ หรือตำแหน่งที่ทำงาน จะถูกใช้ ถ้าฟิลด์นี้ว่างเปล่า จะมีการใช้ **วันที่วางแผน** สำหรับแผนการบำรุงรักษา |
| **ชนิดของช่วง: ทำซ้ำตั้งแต่ใบสั่งงานล่าสุด** การตรวจนับจะเริ่มต้นจากวันที่และเวลาสิ้นสุดจริงของใบสั่งงานล่าสุดที่ดำเนินการเสร็จสมบูรณ์แล้วในสินทรัพย์ด้วยชนิดงานบำรุงรักษาเฉพาะนั้น / ตัวแปรชนิดงานบำรุงรักษา / ชุดการค้า วันที่และเวลาดังกล่าวจะปรากฏในฟิลด์ **สิ้นสุดจริง** ในมุมมองรายละเอียด **ใบสั่งงานทั้งหมด** | วันที่และเวลาสิ้นสุดจริงของใบสั่งงานที่เสร็จสมบูรณ์ในสินทรัพย์ด้วยชนิดงานบำรุงรักษาเฉพาะนั้น / ตัวแปรชนิดงานบำรุงรักษา / ชุดการค้า ถ้าไม่พบใบสั่งงานที่เสร็จสมบูรณ์ จะมีการใช้หนึ่งในวันที่ที่ใช้ในชนิดช่วงเวลา "ทำซ้ำตั้งแต่วันที่เริ่มต้น" ที่อธิบายไว้ข้างต้นแทน | วันที่และเวลาสิ้นสุดจริงของใบสั่งงานที่เสร็จสมบูรณ์ในสินทรัพย์ *และ* ชนิดงานบำรุงรักษา / ตัวแปรชนิดงานบำรุงรักษา / ชุดการค้า ถูกใช้ ถ้าวันที่และเวลาสิ้นสุดถูกปล่อยให้ว่างเปล่าในใบสั่งงาน จะมีการใช้หนึ่งในวันที่ที่ใช้ในชนิดช่วงเวลา "ทำซ้ำตั้งแต่วันที่เริ่มต้น" ที่อธิบายไว้ข้างต้นแทน |
| **ชนิดของช่วงเวลา: หลังจากวันที่วางแผน** ดูคำอธิบายสำหรับชนิดช่วงเวลา "ทำซ้ำตั้งแต่วันที่วางแผน" ด้านบน ความแตกต่างเดียวเท่านั้นคือ จะมีการใช้ชนิดของช่วงเวลานี้เพียงครั้งเดียว | ดูที่คำอธิบายสำหรับชนิดช่วงเวลาของ "ทำซ้ำตั้งแต่วันที่วางแผน" ด้านบน โดยทั่วไปจะมีการใช้ช่วงเวลานี้สำหรับการบำรุงรักษาหรืองานการให้บริการแบบครั้งเดียว | ดูที่คำอธิบายสำหรับชนิดช่วงเวลาของ "ทำซ้ำตั้งแต่วันที่วางแผน" ด้านบน โดยทั่วไปจะมีการใช้ช่วงเวลานี้สำหรับการบำรุงรักษาหรืองานการให้บริการแบบครั้งเดียว **หมายเหตุ 1:** ชนิดของช่วงเวลานี้มีความเกี่ยวข้อง เฉพาะเมื่อมีการแทนที่ตัวนับทุกครั้งที่คุณดำเนินการบำรุงรักษาหรืองานบริการ ถ้า สำหรับเหตุผลบางประการ ตัวนับได้ถูกแทนที่ก่อนสิ้นสุดช่วงเวลาที่วางแผนไว้ จะมีการคำนวณเวลาใหม่สำหรับงานนี้ตั้งแต่เวลาของการแทนที่ตัวนับ **หมายเหตุ 2:** ถ้าตัวนับถูกแทนที่ เมื่อดำเนินการบำรุงรักษาหรืองานบริการเสร็จสมบูรณ์ ชนิดของช่วงเวลานี้ทำหน้าที่เป็น "ทำซ้ำตั้งแต่วันที่วางแผน" ด้านบน |
| **ชนิดของช่วงเวลา: หลังจากวันที่เริ่มต้น** ดูคำอธิบายสำหรับชนิดช่วงเวลา "ทำซ้ำตั้งแต่วันที่เริ่มต้น" ด้านบน ความแตกต่างเดียวเท่านั้นคือ จะมีการใช้ชนิดของช่วงเวลานี้เพียงครั้งเดียว | ดูที่คำอธิบายสำหรับชนิดช่วงเวลาของ "ทำซ้ำตั้งแต่วันที่เริ่มต้น" ด้านบน โดยทั่วไปจะมีการใช้ช่วงเวลานี้สำหรับการบำรุงรักษาหรืองานการให้บริการแบบครั้งเดียว | ดูที่คำอธิบายสำหรับชนิดช่วงเวลาของ "ทำซ้ำตั้งแต่วันที่เริ่มต้น" ด้านบน โดยทั่วไปจะมีการใช้ช่วงเวลานี้สำหรับการบำรุงรักษาหรืองานการให้บริการแบบครั้งเดียว **หมายเหตุ 1** นอกจากนี้ รายการข้างต้นยังใช้กับชนิดช่วงเวลานี้ด้วย **หมายเหตุ 3:** ถ้าตัวนับถูกแทนที่ เมื่อดำเนินการบำรุงรักษาหรืองานบริการเสร็จสมบูรณ์ ชนิดของช่วงเวลานี้ทำหน้าที่เป็น "ทำซ้ำตั้งแต่วันที่เริ่มต้น" ด้านบน |
| **ชนิดของช่วงเวลา: เมื่อไปถึงด้านบน** ชนิดของช่วงเวลานี้เกี่ยวข้องกับตัวนับเท่านั้น และมีการใช้สำหรับการบ่งชี้การตั้งค่าขีดจำกัดสูงสุดบนรายการแผนการบำรุงรักษา รายการกำหนดการบำรุงรักษาจะมีวันที่และเวลาเริ่มต้นที่คาดไว้ของการลงทะเบียนตัวนับ ซึ่งหมายความว่ารายการเหล่านี้จะถูกสร้างขึ้นด้วยวันที่เริ่มต้นที่คาดไว้ เท่ากับหรือก่อนหน้าวันที่ของระบบ | ใช้ไม่ได้ | ช่วงตัวนับบ่งชี้ถึงขีดจำกัดด้านบน ถ้ามีการเกินวงเงินดังกล่าว เมื่อคุณสร้างการลงทะเบียนตัวนับ จะมีการสร้างรายการกำหนดการบำรุงรักษา เมื่อคุณจัดกำหนดการบำรุงรักษาเชิงป้องกัน |
| **ชนิดของช่วงเวลา: เมื่อไปถึงด้านล่าง** ชนิดของช่วงเวลานี้เกี่ยวข้องกับตัวนับเท่านั้น และมีการใช้สำหรับการบ่งชี้การตั้งค่าขีดจำกัดต่ำสุดบนรายการแผนการบำรุงรักษา รายการกำหนดการบำรุงรักษาจะมีวันที่และเวลาเริ่มต้นที่คาดไว้ของการลงทะเบียนตัวนับ ซึ่งหมายความว่ารายการเหล่านี้จะถูกสร้างขึ้นด้วยวันที่เริ่มต้นที่คาดไว้ เท่ากับหรือก่อนหน้าวันที่ของระบบ | ใช้ไม่ได้ | ช่วงตัวนับบ่งชี้ถึงขีดจำกัดด้านล่าง ถ้ามีการผ่านขีดจำกัดดังกล่าว เมื่อคุณสร้างการลงทะเบียนตัวนับ จะมีการสร้างรายการกำหนดการบำรุงรักษา เมื่อคุณจัดกำหนดการบำรุงรักษาเชิงป้องกัน |
| **ชนิดของช่วง: เชื่อมโยงจากวันที่เริ่มต้น** ชนิดของช่วงเวลานี้จะสร้างบรรทัดกำหนดการบำรุงรักษาหนึ่งครั้งเท่านั้น แผนการบำรุงรักษาอาจประกอบด้วยรายการแผนการบำรุงรักษาเพิ่มเติมที่ใช้ชนิดของช่วงเวลานี้ และรายการเหล่านั้นจะถูกเชื่อมโยง โดยทั่วไป คุณจะสร้างแผนการบำรุงรักษาที่มีรายการของชนิดช่วงเวลานี้เท่านั้น รายการกำหนดการบำรุงรักษาถูกสร้างขึ้นโดยการระบุรายการแผนการบำรุงรักษาที่มีวันที่และเวลาเริ่มต้นที่คาดไว้ครั้งแรก | ดูที่คำอธิบายสำหรับ "เมื่อมาจากวันที่เริ่มต้น" ด้านบน ตัวอย่าง: คุณสร้างรายการสองรายการในแผนการบำรุงรักษาสำหรับงานบริการบนรถยนต์: รายการที่ใช้ครั้งเดียวที่มีรอบระยะเวลา 1 ปี และรายการตามตัวนับที่มีขีดจำกัด 25,000 กม. รายการกำหนดการบำรุงรักษาถูกสร้างขึ้นสำหรับขีดจำกัดที่จะถึงเป็นอันดับแรก สำหรับชนิดรายการนี้ คุณสร้างรายการที่มีรอบระยะเวลา 1 ปี | ดูที่คำอธิบายสำหรับ "เมื่อมาจากวันที่เริ่มต้น" ด้านบน ตัวอย่าง: คุณสร้างรายการสองรายการในแผนการบำรุงรักษาสำหรับงานบริการบนรถยนต์: รายการที่ใช้ครั้งเดียวที่มีรอบระยะเวลา 1 ปี และรายการตามตัวนับที่มีขีดจำกัด 25,000 กม. รายการกำหนดการบำรุงรักษาถูกสร้างขึ้นสำหรับขีดจำกัดที่จะถึงเป็นอันดับแรก สำหรับชนิดรายการนี้ คุณสร้างรายการที่มีขีดจำกัด 25,000 กม. ตัวอย่างเช่น การสร้างรายการการตรวจนับสองรายการ: นอกจากนี้ คุณยังสามารถตั้งค่าแผนการบำรุงรักษาด้วยรายการตามตัวนับที่มีการเชื่อมโยงสองรายการ ซึ่งรายการแรกมีขีดจำกัดของปริมาณสินค้าผลิต 10,000 รายการ และรายการที่สองเกี่ยวข้องกับเครื่องจักรหรือศูนย์การผลิตที่จำเป็นต้องใช้บริการหลังจากการรัน 3,000 ชั่วโมง |
| **ชนิดของช่วงเวลา: ลิงค์จากใบสั่งงานล่าสุด** ชนิดของช่วงนี้สร้างรายการกำหนดการบำรุงรักษาใหม่หลังจากใบสั่งงานที่เสร็จสิ้นแล้วทุกครั้ง แผนการบำรุงรักษาอาจประกอบด้วยรายการเพิ่มเติมที่ใช้ชนิดของช่วงเวลานี้ และรายการเหล่านั้นจะถูกเชื่อมโยง โดยทั่วไป คุณจะสร้างแผนการบำรุงรักษาที่มีรายการแผนการบำรุงรักษาของชนิดช่วงเวลานี้เท่านั้น รายการกำหนดการบำรุงรักษาถูกสร้างขึ้นโดยการระบุรายการแผนการบำรุงรักษาที่มีวันที่และเวลาเริ่มต้นที่คาดไว้ครั้งแรก | ชนิดของช่วงเวลานี้โดยทั่วไปจะทำงานเป็น "เชื่อมโยงตั้งแต่วันที่เริ่มต้น" ที่อธิบายไว้ข้างต้น ความแตกต่างเดียวเท่านั้นคือ วันที่ซึ่งใช้ชนิดของช่วงเวลา วันที่ที่ใช้คือ วันที่และเวลาสิ้นสุดจริงในใบสั่งงานล่าสุดที่เสร็จสมบูรณ์ในสินทรัพย์ *และ* ชนิดงานบำรุงรักษา / ตัวแปรชนิดงานบำรุงรักษา / ชุดการค้า | ชนิดของช่วงเวลานี้โดยทั่วไปจะทำงานเป็น "เชื่อมโยงตั้งแต่วันที่เริ่มต้น" ที่อธิบายไว้ข้างต้น ความแตกต่างเดียวเท่านั้นคือ วันที่ซึ่งใช้ชนิดของช่วงเวลา วันที่ที่ใช้คือ วันที่และเวลาสิ้นสุดจริงในใบสั่งงานล่าสุดที่เสร็จสมบูรณ์ในสินทรัพย์ *และ* ชนิดงานบำรุงรักษา / ตัวแปรชนิดงานบำรุงรักษา / ชุดการค้า |
| **ชนิดของช่วง: ซ้ํากับค่ารวม (ตัวนับเท่านั้น)** เมื่อรันแผนการบำรุงรักษา รายการการบำรุงรักษาตามกำหนดเวลาจะมีการสร้างไว้ทุกครั้ง ที่มูลค่าสะสมของตัวนับสินทรัพย์ถึงความถี่ของรอบระยะเวลา หรือความถี่ของรอบระยะเวลาหลายรอบ (ความถี่ของรอบระยะเวลาถูกกำหนดไว้บนรายการแผนการบำรุงรักษา)<p>สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเปิดใช้งานและการใช้ฟังก์ชันนี้ ให้ดูที่ส่วน [การปรับปรุงการบํารุงรักษาที่ขึ้นอยู่กับตัวนับ](#counter-based-maintenance) ในตอนท้ายของบทความนี้ | ใช้ไม่ได้ | **ตัวอย่าง:** ตัวนับชั่วโมงมีการตั้งค่าไว้สำหรับ สินทรัพย์ AK-101 รายการแผนสินทรัพย์มีการตั้งค่าไว้สำหรับสินทรัพย์ด้วย ชนิดช่วงเวลาของรายการนี้ *ซ้ำกับค่ารวม (ตัวนับเท่านั้น)* และความถี่ของรอบระยะเวลา คือ *1000* เมื่อรันแผนการบํารุงรักษา รายการบํารุงรักษาตามกำหนดการ จะถูกสร้างขึ้นเมื่อค่ารวมสำหรับตัวนับ เกิน 1,000 ชั่วโมง จากนั้น เมื่อค่ารวมสำหรับตัวนับ เกิน 2,000 ชั่วโมง รายการการบํารุงรักษาตามกำหนดการอื่นจะถูกสร้างขึ้น และทุกๆ 1,000 ชั่วโมง ที่เพิ่มเติม |
| **ชนิดของช่วง: เมื่อค่ารวม (ตัวนับเท่านั้น)** เมื่อรันแผนการบำรุงรักษา รายการการบำรุงรักษาตามกำหนดเวลาจะมีการสร้าง เมื่อมูลค่าสะสมของตัวนับสินทรัพย์ถึงความถี่ของรอบระยะเวลาที่กำหนดไว้ในรายการแผนการบำรุงรักษา<p>สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเปิดใช้งานและการใช้ฟังก์ชันนี้ ให้ดูที่ส่วน [การปรับปรุงการบํารุงรักษาที่ขึ้นอยู่กับตัวนับ](#counter-based-maintenance) | ใช้ไม่ได้ | **ตัวอย่าง:** ตัวนับชั่วโมงมีการตั้งค่าไว้สำหรับ สินทรัพย์ AK-101 รายการแผนสินทรัพย์มีการตั้งค่าไว้สำหรับสินทรัพย์ด้วย ชนิดช่วงเวลาของรายการนี้ *เมื่อค่ารวม (ตัวนับเท่านั้น)* และความถี่ของรอบระยะเวลา คือ *1000* เมื่อรันแผนการบํารุงรักษา รายการบํารุงรักษาตามกำหนดการ จะถูกสร้างขึ้นเมื่อค่ารวมสำหรับตัวนับ เกิน 1,000 ชั่วโมง |

>[!NOTE]
>เมื่อมีการสร้างรายการกำหนดการบำรุงรักษาสำหรับรายการแผนการบำรุงรักษาตามเวลา เวลาที่คาดหวังจะอยู่ที่จุดเริ่มต้นของวันเสมอ สำหรับรายการแผนการบำรุงรักษาตามตัวนับ เวลาที่คาดไว้อาจเป็นเวลาในระหว่างวัน

ด้านล่างคุณจะพบตัวอย่างของการตั้งค่าของรายการแผนการบำรุงรักษาตามเวลาและตามตัวนับ:

**ตัวอย่างที่ 1 - รายการแผนการบำรุงรักษาตามเวลา:** งานการหล่อลื่นอาจมีการตั้งค่าในช่วงเวลาคงที่ ที่เกิดขึ้นสัปดาห์ละครั้ง สำหรับวัตถุประสงค์ดังกล่าว ให้เลือก "ทำซ้ำตั้งแต่วันที่วางแผน" ในฟิลด์ **ชนิดช่วงเวลา** ดูตัวอย่างในภาพประกอบต่อไปนี้

![งานบริการที่ตั้งค่าในช่วงเวลาคงที่ ซึ่งเกิดขึ้นสัปดาห์ละครั้ง](media/02-preventive-maintenance.png "งานบริการที่ตั้งค่าในช่วงเวลาคงที่ ซึ่งเกิดขึ้นสัปดาห์ละครั้ง")

**ตัวอย่างที่ 2 - รายการแผนการบำรุงรักษาตามเวลา:** งานการตรวจสอบอาจได้รับการตั้งค่าให้ดำเนินการประมาณหนึ่งครั้งต่อสัปดาห์ สำหรับวัตถุประสงค์ดังกล่าว ให้เลือก "ทำซ้ำจากใบสั่งงานล่าสุด" ในฟิลด์  **ชนิดช่วงเวลา** ดูตัวอย่างในภาพประกอบต่อไปนี้

![งานการตรวจสอบที่ตั้งค่าให้มีการดำเนินการประมาณสัปดาห์ละครั้ง](media/03-preventive-maintenance.png "งานการตรวจสอบที่ตั้งค่าให้เสร็จสิ้นประมาณสัปดาห์ละครั้ง")

**ตัวอย่างที่ 3 - รายการแผนการบำรุงรักษาตามตัวนับ** ภาพประกอบแบบกราฟิกแสดงตัวนับชั่วโมงซึ่งรายการกำหนดการบำรุงรักษาใหม่จะถูกสร้างขึ้นทุกครั้งที่ครบ 250 ชั่วโมง ชนิดของช่วงสำหรับรายการตามตัวนับนี้เป็น "ทำซ้ำตั้งแต่วันที่เริ่มต้น" วันที่เริ่มต้นคือ วันที่เริ่มต้นของสินทรัพย์ที่เกี่ยวข้องในฟิลด์ **สินทรัพย์ทั้งหมด** มุมมองรายละเอียด \> **แผนการบำรุงรักษาสินทรัพย์** แท็บด่วน \> **วันที่เริ่มต้น** หรือในฟิลด์ **ตำแหน่งที่ทำงาน** มุมมองรายละเอียด \> **แผนการบำรุงรักษา** แท็บด่วน \> **วันที่เริ่มต้น** นี่เป็นตัวอย่างของแผนการบำรุงรักษา *เชิงป้องกัน* เนื่องจากมีการสร้างรายการกำหนดการบำรุงรักษาโดยอัตโนมัติในแต่ละครั้งที่ไปถึงขีดจำกัด (+ 250)

![ตัวนับชั่วโมงที่สร้างรายการกำหนดการการรบํารุงรักษาเป็นระยะ](media/04-preventive-maintenance.png "ตัวนับชั่วโมงที่สร้างรายการกำหนดการการรบํารุงรักษาเป็นระยะ")

**ตัวอย่างที่ 4 - รายการแผนการบำรุงรักษาตามตัวนับ:** ภาพประกอบแบบกราฟิกแสดงการลดลงในมูลค่าของตัวนับ ซึ่งวัดการสึกหรอของแผ่นเบรค รายการกำหนดการบำรุงรักษาจะถูกสร้างขึ้น เมื่อมีการสร้างการลงทะเบียนตัวนับที่ต่ำกว่า 20 มม. บนแผ่นเบรก ชนิดของช่วงสำหรับรายการตามตัวนับนี้คือ "เมื่อถึงด้านล่าง" หรือ "เมื่อมาจากวันที่เริ่มต้นล่าสุด" นี่เป็นตัวอย่างของแผนการบำรุงรักษา *เชิงรับ* เนื่องจากไม่ได้สร้างรายการกำหนดการบำรุงรักษา จนกว่าจะมีการลงทะเบียนการวัดที่ต่ำกว่า 20 มม.

![การลดค่าตัวนับ ซึ่งวัดการสึกหรอของแผ่นเบรค](media/05-preventive-maintenance.png "การลดค่าตัวนับ ซึ่งวัดการสึกหรอของแผ่นเบรค")

**ตัวอย่างที่ 5 - รายการแผนการบำรุงรักษาตามตัวนับ:** ภาพประกอบแบบกราฟิกแสดงตัวนับที่มีขีดจำกัด -18 องศาเซลเซียส รายการกำหนดการบำรุงรักษาจะถูกสร้างขึ้น เมื่อมีการทำการลงทะเบียนตัวนับที่สูงกว่า -18° องศาเซลเซียส ชนิดของช่วงสำหรับรายการตามตัวนับนี้เป็น "เมื่อถึงด้านบน" นี่เป็นตัวอย่างของแผนการบำรุงรักษา *เชิงรับ* เนื่องจากไม่ได้สร้างรายการกำหนดการบำรุงรักษาจนกว่าจะมีการลงทะเบียนการวัดที่สูงกว่า -18° องศาเซลเซียส

![ตัวนับที่มีขีดจำกัด -18° องศาเซลเซียส](media/06-preventive-maintenance.png "ตัวนับที่มีขีดจำกัด -18 องศาเซลเซียส")

- เมื่อคุณสร้างสินทรัพย์ใหม่ และสินทรัพย์นั้นใช้ชนิดสินทรัพย์ที่เกี่ยวข้องกับแผนการบำรุงรักษา แผนการบำรุงรักษาจะถูกแทรกโดยอัตโนมัติใน แท็บด่วน **ออบเจ็กต์ทั้งหมด \> แผนการบำรุงรักษาสินทรัพย์** นอกจากนี้ ใน **ค่าเริ่มต้นของชนิดสินทรัพย์** บน FastTab **แผนการบำรุงรักษา** จะมีการแทรกแผนการบำรุงรักษาที่เกี่ยวข้องโดยอัตโนมัติ
- ถ้าคุณเพิ่มหรือลบชนิดสินทรัพย์หรือชนิดตำแหน่งที่ทำงานใน **แผนการบำรุงรักษา** การเปลี่ยนแปลงดังกล่าวจะสะท้อนเฉพาะในสินทรัพย์ใหม่ที่สร้างขึ้นหลังจากที่คุณทำการเปลี่ยนแปลง
- ถ้าคุณเพิ่มหรือลบสินทรัพย์ หรือตำแหน่งที่ทำงานใน **แผนการบำรุงรักษา** ที่จะปรับปรุงการเปลี่ยนแปลงโดยอัตโนมัติใน แท็บด่วน **สินทรัพย์ทั้งหมด \> แผนการบำรุงรักษาสินทรัพย์** หรือในแท็บด่วน **ตำแหน่งที่ทำงานทั้งหมด \> แผนการบำรุงรักษา**

ภาพประกอบต่อไปนี้แสดงตัวอย่างของ "บริการรถบรรทุก" แผนการบำรุงรักษา บนหน้า **แผนการบำรุงรักษา**

![ตัวอย่างของแผนการบำรุงรักษาบริการรถบรรทุก](media/07-preventive-maintenance.png "ตัวอย่างของแผนการบำรุงรักษาบริการรถบรรทุก")

## <a name="add-a-maintenance-plan-to-an-asset"></a>เพิ่มแผนการบำรุงรักษาให้กับสินทรัพย์

1. ไปที่ **การจัดการสินทรัพย์ \> ทั่วไป \> สินทรัพย์ \> สินทรัพย์ทั้งหมด** หรือ **สินทรัพย์ที่ใช้งานอยู่**

1. เลือกสินทรัพย์ที่คุณต้องการตั้งค่าแผนการบำรุงรักษา และเลือก **แก้ไข**

1. บนแท็บด่วน **แผนการบำรุงรักษาสินทรัพย์** เลือก **เพิ่มรายการ** เพื่อเพิ่มแผนการบำรุงรักษาไปยังสินทรัพย์

1. ในฟิลด์ **แผนการบำรุงรักษา** ให้เลือกแผนบำรุงรักษาที่เกี่ยวข้อง

1. ในฟิลด์ **วันที่เริ่มต้น** ให้เลือกวันที่จากการวางแผนของงานบำรุงรักษาที่สามารถทำได้ 

1. เลือก **บันทึก** ฟิลด์ **ใช้งานอยู่** มีการปรับปรุงโดยอัตโนมัติ

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการตั้งค่าแผนการบำรุงรักษาในสินทรัพย์บนหน้า **สินทรัพย์ทั้งหมด**

![ตัวอย่างของการตั้งค่าแผนการบำรุงรักษาในสินทรัพย์](media/08-preventive-maintenance.png "ตัวอย่างของการตั้งค่าแผนการบำรุงรักษาในสินทรัพย์")

<a id="counter-based-maintenance"></a>

## <a name="counter-based-maintenance-enhancements"></a>การปรับปรุงการบำรุงรักษาตามตัวนับ

คุณลักษณะ *การปรับปรุงการบํารุงรักษาตามตัวนับ* มีฟังก์ชันดังต่อไปนี้:

- ตัวเลือกในการแทรกตัวนับที่มีค่าเป็น *0* (ศูนย์) โดยอัตโนมัติ เมื่อสร้างสินทรัพย์ ตัวเลือกนี้มีประโยชน์เมื่อคุณใช้การบำรุงรักษาที่คาดการณ์ไว้ ซึ่งขึ้นอยู่กับตัวนับ เมื่อไม่ได้ใช้คุณลักษณะ *การปรับปรุงการบํารุงรักษาตามตัวนับ* ต้องแทรกตัวนับที่มีค่าเป็น *0* (ศูนย์) ด้วยตนเอง
- ความสามารถในการตั้งค่าคอนฟิกตัวนับเพื่อให้รีเซ็ตโดยอัตโนมัติ เมื่อใบสั่งงานเสร็จสมบูรณ์ ฟังก์ชันนี้มีประโยชน์เมื่อคุณต้องการจัดกำหนดการการบํารุงรักษาตามค่ารวม เมื่อใบสั่งงานล่าสุดเสร็จสมบูรณ์
- ชนิดของช่วงของแผนการบำรุงรักษาใหม่ ที่มีชื่อว่า *ซ้ำกับค่ารวม (ตัวนับเท่านั้น)* ชนิดนี้จะทริกเกอร์การบํารุงรักษาทุกครั้งที่ตัวนับรวมถึงค่าตัวนับหลายค่าที่ระบุ ตัวอย่างเช่น สามารถทริกเกอร์การบํารุงรักษาทุกๆ 10,000 ชั่วโมง สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [ภาพรวมของชนิดช่วงเวลา](#interval-types) ที่กล่าวถึงก่อนหน้าในบทความนี้
- ชนิดของช่วงของแผนการบำรุงรักษาใหม่อื่นๆ ที่มีชื่อว่า *เมื่อค่ารวม (ตัวนับเท่านั้น)* ชนิดนี้จะทริกเกอร์การบํารุงรักษาเมื่อตัวนับรวมถึงค่าที่ระบุ เช่น 8,000 ชั่วโมง สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [ภาพรวมของชนิดช่วงเวลา](#interval-types)

### <a name="turn-on-the-counter-based-maintenance-enhancements-feature"></a>เปิดคุณลักษณะการปรับปรุงการบำรุงรักษาตามตัวนับ

ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดคุณลักษณะนี้ในระบบของคุณก่อน ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:

- **โมดูล:** *การจัดการสินทรัพย์*
- **ชื่อคุณลักษณะ:** *การปรับปรุงการบำรุงรักษาตามตัวนับ*

### <a name="create-and-initialize-counters-when-an-asset-is-created"></a>สร้างและเริ่มต้นตัวนับเมื่อสร้างสินทรัพย์

ในแต่ละครั้งที่คุณสร้างสินทรัพย์ ตัวนับสินทรัพย์ที่เกี่ยวข้อง ซึ่งเริ่มต้นค่าเป็น *0* (ศูนย์) จะถูกสร้างขึ้นโดยอัตโนมัติ หากคุณตั้งค่าระบบของคุณ และสร้างสินทรัพย์นั้นอย่างถูกต้อง

1. ไปที่ **การจัดการสินทรัพย์ \> การตั้งค่า \> ชนิดสินทรัพย์**
1. ตรวจสอบให้แน่ใจว่าคุณมีชนิดสินทรัพย์ที่ใช้ได้กับสินทรัพย์ใหม่ที่วางแผนไว้ของคุณ สร้างชนิดสินทรัพย์ตามที่ต้องการ ตรวจสอบให้แน่ใจว่ามีการเลือกตัวนับที่เกี่ยวข้องทั้งหมด บนแท็บด่วน **ตัวนับ**
1. ไปที่ **การจัดการสินทรัพย์ \> การตั้งค่า \> ชนิดสินทรัพย์ \> ตัวนับ**
1. สำหรับตัวนับที่เกี่ยวข้องแต่ละตัว ให้ตรวจสอบให้แน่ใจว่า ฟิลด์ **ผลรวมทั้งหมด** ถูกตั้งเป็น *ผลรวม*
1. บนหน้า **สินทรัพย์ทั้งหมด** ให้สร้างสินทรัพย์
1. ตั้งค่าฟิลด์ **ชนิดสินทรัพย์** เป็นชนิดสินทรัพย์ที่คุณระบุ หรือสร้างขึ้นในขั้นตอนที่ 2
1. เสร็จสิ้นการตั้งค่าสินทรัพย์ใหม่ตามที่ต้องการ
1. ไปที่ **การจัดการสินทรัพย์ \> การสอบถาม \> สินทรัพย์ \> ตัวนับ** คุณควรจะสามารถค้นหาตัวนับที่เริ่มต้นซึ่งตั้งค่าไว้ให้กับสินทรัพย์ใหม่ของคุณ

> [!NOTE]
> เมื่อสร้างตัวนับสินทรัพย์เริ่มต้น สมมติฐานคือ ไม่เคยมีการใช้สินทรัพย์ก่อนที่จะเพิ่มเข้าในระบบ เมื่อรันการจัดกำหนดการการบํารุงรักษาในครั้งแรก การคํานวณจะใช้ค่าวันที่ และค่าตัวนับ *0* (ศูนย์) เป็นข้อมูลพื้นฐานสําหรับการคํานวณการบํารุงรักษาในอนาคต ถ้าสินทรัพย์ไม่ใช่สินทรัพย์ใหม่ เมื่อเพิ่มเข้าในระบบ คุณสามารถปรับปรุงค่าตัวนับด้วยตนเอง เพื่อให้ตรงกับค่าตัวนับจริงได้ เมื่อต้องการปรับปรุงค่าตัวนับ ให้เปิดสินทรัพย์ที่เกี่ยวข้อง บนหน้า **สินทรัพย์ทั้งหมด** จากนั้น ในบานหน้าต่างการดำเนินการ บนแท็บ **สินทรัพย์** ในกลุ่ม **เชิงป้องกัน** ให้เลือก **ตัวนับ** บนหน้า **ตัวนับสินทรัพย์** ของสินทรัพย์ที่เลือก ให้ปรับปรุงค่าในคอลัมน์ **ค่า** ในเรกคอร์ดตัววนับเริ่มต้น ตามที่ต้องการ

### <a name="automatically-reset-a-counter-value"></a>รีเซ็ตค่าตัวนับโดยอัตโนมัติ

คุณสามารถตั้งค่าคอนฟิกระบบให้รีเซ็ตตัวนับโดยอัตโนมัติ ทุกครั้งที่ใบสั่งงานที่เกี่ยวข้องถึงค่าสถานะที่เลือก

1. ไปที่ **การจัดการสินทรัพย์ \> การตั้งค่า \> การบำรุงรักษาเชิงป้องกัน \> แผนการบำรุงรักษา**
1. ในบานหน้าต่างรายการ เลือกแผนการบำรุงรักษา การรีเซ็ตตัวนับจะใช้กับสินทรัพย์ทั้งหมดที่ใช้แผนนี้
1. ในส่วน **รายการ** ให้ค้นหารายการตัวนับสินทรัพย์ที่คุณต้องการรีเซ็ต และเลือกกล่องกาเครื่องหมาย **รีเซ็ตตัวนับ** ของรายการนั้น (รายการตัวนับสินทรัพย์มีค่าอยู่ในคอลัมน์ **ตัวนับ** ตัวนับที่ระบุในคอลัมน์นั้น คือตัวนับที่จะรีเซ็ตเป็นสินทรัพย์ที่เกี่ยวข้อง)
1. ไปที่ **การจัดการสินทรัพย์ \> การตั้งค่า \> ใบสั่งงาน \> สถานะวงจรชีวิต**
1. ในบานหน้าต่างรายการ ให้เลือกสถานะวงจรชีวิตของใบสั่งงานที่ควรรีเซ็ตตัวนับที่เกี่ยวข้อง
1. บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **รีเซ็ตตัวนับ** เป็น *ใช่*


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]