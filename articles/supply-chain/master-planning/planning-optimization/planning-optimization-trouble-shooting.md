---
title: แก้ไขปัญหาการเพิ่มประสิทธิภาพการวางแผน
description: บทความนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับการเพิ่มประสิทธิภาพของการวางแผน
author: t-benebo
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 37c38ab9cec8ae3c9d4decf8043b43ea2251083e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739741"
---
# <a name="troubleshoot-planning-optimization"></a>แก้ไขปัญหาการเพิ่มประสิทธิภาพการวางแผน 

[!include [banner](../../includes/banner.md)]

บทความนี้จะอธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบขณะทำงานกับการเพิ่มประสิทธิภาพของการวางแผน

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>การติดตั้ง Add-in ของการเพิ่มประสิทธิภาพการวางแผนไม่สมบูรณ์

การเพิ่มประสิทธิภาพของการวางแผนต้องมีการเปิดใช้งาน Lifecycle Services (LCS) สภาพแวดล้อมที่มีความพร้อมใช้งานสูง ระดับ 2 หรือสูงกว่า (ไม่ใช่สภาพแวดล้อม OneBox) โดยมี Dynamics 365 Supply Chain Management รุ่น 10.0.7 หรือใหม่กว่า ถ้าคุณพยายามติดตั้ง Add-in บนสภาพแวดล้อม OneBox การติดตั้งจะไม่เสร็จสมบูรณ์

**การแก้ไข**: ยกเลิกการติดตั้งและใช้สภาพแวดล้อมความพร้อมใช้งานสูงระดับ 2 หรือสูงกว่า (ไม่ใช่สภาพแวดล้อม OneBox)

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>การวางแผนชุดงานล้มเหลวเมื่อเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน

เมื่อคุณเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน กลไกจัดการการวางแผนหลักที่ไม่สนับสนุนที่มีอยู่แล้วจะถูกปิดใช้งานโดยอัตโนมัติ ชุดงานการวางแผนหลักที่มีอยู่ที่สร้างไว้สำหรับกลไกจัดการการวางแผนหลักที่ไม่สนับสนุนจะล้มเหลวถ้าถูกทริกเกอร์ในขณะที่การเพิ่มประสิทธิภาพการวางแผนถูกเปิดใช้งาน งานเหล่านั้นจะล้มเหลว คุณอาจได้รับข้อความแสดงข้อผิดพลาด เช่น *การดำเนินงานนี้จะทริกเกอร์การวางแผนหลักที่ไม่ได้รับการสนับสนุนเมื่อเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน*

**การแก้ไข**: ยกเลิกชุดงานการวางแผนหลักทั้งหมดที่สร้างขึ้นสำหรับกลไกจัดการการวางแผนหลักที่ไม่สนับสนุน

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>ผลการเพิ่มประสิทธิภาพการวางแผนแตกต่างจากผลลัพธ์ก่อนหน้านี้

การเพิ่มประสิทธิภาพการวางแผนแตกต่างจากการออกแบบกลไกจัดการการวางแผนหลักที่ไม่สนับสนุนในบางพื้นที่ ลักษณะเช่นนี้อาจเกิดจากคุณลักษณะการทำงานที่ค้างอยู่

**การแก้ไข**: รันการวิเคราะห์การเพิ่มประสิทธิภาพของการวางแผนแล้ววิเคราะห์ผลลัพธ์ขณะอ้างอิงถึงเอกสารที่เกี่ยวข้องเพื่อให้เข้าใจถึงผลกระทบ สำหรับข้อมูลเพิ่มเติมให้ดูที่ [การวิเคราะห์การปรับการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-fit-analysis.md)

## <a name="cant-enable-planning-optimization"></a>ไม่สามารถเปิดใช้การเพิ่มประสิทธิภาพการวางแผนได้

**สถานะการเชื่อมต่อ** ต้องเป็น **เชื่อมต่อ** ก่อนที่คุณจะสามารถตั้งค่า **ใช้การเพิ่มประสิทธิภาพการวางแผน** เป็น **ใช่** สำหรับข้อมูลเพิ่มเติมให้ดูที่ [การเริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน](get-started.md)

**การแก้ไข**: ตรวจสอบให้แน่ใจว่าได้ติดตั้ง Add-in การเพิ่มประสิทธิภาพการวางแผนเสร็จเรียบร้อยแล้ว

## <a name="error-message-is-shown-during-ctp"></a>แสดงข้อความแสดงข้อผิดพลาดในระหว่าง CTP

ถ้าคุณพยายามที่จะรันปริมาณที่สามารถสัญญาได้ (CTP) จากใบสั่งขายเมื่อมีการเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: *การดำเนินการนี้จะทริกเกอร์การวางแผนหลักที่ไม่ได้รับการสนับสนุนเมื่อเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน*

ซึ่งนี่เกี่ยวข้องกับลักษณะการทำงานที่ค้างอยู่ซึ่งวางแผนไว้เป็นส่วนหนึ่งของการสนับสนุนสำหรับใบสั่งผลิต

**การแก้ไข:** หลีกเลี่ยงการคำนวณ CTP เมื่อเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผนจนกว่าจะมีการสนับสนุน CTP

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [เริ่มต้นใช้งานการวางแผนหลัก](get-started.md)
- [การวิเคราะห์ความเหมาะสมของการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]