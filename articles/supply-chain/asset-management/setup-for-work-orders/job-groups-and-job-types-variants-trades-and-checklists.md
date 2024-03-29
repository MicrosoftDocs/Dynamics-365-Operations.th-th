---
title: ชนิดงานการบํารุงรักษา ประเภท ตัวแปร การค้า และรายการตรวจสอบ
description: บทความนี้อธิบายประเภทของชนิดงานบำรุงรักษาและชนิดงานบำรุงรักษา ตัวแปรชนิดงานบำรุงรักษา และการค้าของชนิดงานบำรุงรักษา และรายการตรวจสอบการบำรุงรักษา ในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetJobTypeDefaultForecast, EntAssetJobTrade, EntAssetJobTypeDefaultCopy, EntAssetChecklistVariableValueLookup, EntAssetChecklistTemplateCreate, EntAssetJobVariant, EntAssetJobTypeDefaultReference, EntAssetJobTypeDefaultChecklist, EntAssetJobTypeDefault, EntAssetJobType, EntAssetJobTypeDefaultChecklistCopy, EntAssetChecklistTemplate, EntAssetJobTypeDefaultDescription, EntAssetJobTypeLookup, EntAssetJobTypeDefaultToolCopy, EntAssetJobTypePreviewPart, EntAssetJobTypeDefaultTool, EntAssetJobTypeDefaultForecastCopy, EntAssetChecklistTemplateLookup, EntAssetJobGroup, EntAssetChecklistVariable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d4385fdd3e94d48a65baf195efa1d687fbf95c3
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016781"
---
# <a name="maintenance-job-types-categories-variants-trades-and-checklists"></a>ชนิดงานการบํารุงรักษา ประเภท ตัวแปร การค้า และรายการตรวจสอบ

[!include [banner](../../includes/banner.md)]

มีการแนบชนิดสินทรัพย์กับสินทรัพย์ทุกรายการ ชนิดสินทรัพย์จะกำหนดชนิดของงานบำรุงรักษา (และดังนั้น งานบำรุงรักษา) ที่สามารถดำเนินการกับสินทรัพย์ได้ เมื่อคุณสร้างใบสั่งงาน คุณต้องเลือกชนิดของงานบำรุงรักษา คุณสามารถเลือกได้เฉพาะชนิดงานบำรุงรักษาที่เกี่ยวข้องกับการตั้งค่าของชนิดสินทรัพย์ที่ใช้สำหรับสินทรัพย์เท่านั้น

สำหรับภาพรวมกราฟิกของสินทรัพย์และชนิดของงานบำรุงรักษา และการเชื่อมต่อกับใบสั่งงาน ให้ดูที่ [ตำแหน่งที่ทำงานและสินทรัพย์](../overview/functional-locations-and-objects.md)

สามารถตั้งค่าตัวแปรชนิดงานบำรุงรักษาบนชนิดงานบำรุงรักษาได้ ชนิดของงานบำรุงรักษากำหนดความแตกต่างของชนิดงาน เช่น ขนาด (เล็ก กลาง หรือใหญ่) รอบระยะเวลา (รายสัปดาห์ รายสองสัปดาห์ หนึ่งเดือน หรือสามเดือน) และการตั้งค่าคอนฟิก (มาตรฐานต่ำ มีความยืดหยุ่น หรือประสิทธิภาพสูง)

การค้าของงานบำรุงรักษาจะให้ข้อมูลเกี่ยวกับการค้าด้านอาชีพ เช่น การค้าทางเครื่องกล ทางไฟฟ้า และไฮดรอลิค สามารถตั้งค่าความต้องการของความสามารถในการค้างานบำรุงรักษา การค้างานบำรุงรักษาทั้งหมดสามารถใช้ได้โดยสัมพันธ์กับชนิดงานบำรุงรักษาทั้งหมด การเลือกของตัวแปรของชนิดงานบำรุงรักษาและ/หรือการค้างานบำรุงรักษาบนใบสั่งงานนั้นไม่จำเป็น

สำหรับชนิดของงานบำรุงรักษาแต่ละชนิด จะสามารถสร้างความแตกต่างของการตั้งค่าชนิดงานบำรุงรักษาได้ ตัวอย่างเช่นถ้า คุณมีชนิดงานบำรุงรักษาที่มีชื่อว่า **บริการ** คุณสามารถสร้างความเปลี่ยนแปลงดังต่อไปนี้สำหรับชนิดงานบำรุงรักษานั้น: **รถบรรทุก 30,000 กม.** **รถยนต์ 30,000 กม.** และ **รถตู้ 30,000 กม.**

ประเภทชนิดของงานบำรุงรักษาถูกใช้เพื่อรวบรวมกลุ่มของชนิดงานบำรุงรักษาสำหรับวัตถุประสงค์ของภาพรวม ตัวอย่างของประเภทชนิดของงานบำรุงรักษาอาจรวมถึง **การสอบเทียบ** **การตรวจสอบ** **การซ่อมใหญ่** **การรายงานข้อมูลระบบ**

เท็มเพลตรายการตรวจสอบการบำรุงรักษาและตัวแปรรายการตรวจสอบการบำรุงรักษา จะถูกใช้สำหรับการตั้งค่ารายการตรวจสอบการบำรุงรักษา รายการตรวจสอบการบำรุงรักษาถูกตั้งค่าไว้ในชนิดของงานบำรุงรักษาและถูกใช้ในใบสั่งงาน

ก่อนอื่นคุณต้องตั้งค่าประเภทของชนิดงานบำรุงรักษา ตัวแปรชนิดงานบำรุงรักษา และการค้าของชนิดงานบำรุงรักษาที่ต้องการ จากนั้น คุณจะสร้างชนิดงานบำรุงรักษา ในตอนท้าย บนหน้า **ค่าเริ่มต้นของชนิดงานบำรุงรักษา** คุณสามารถสร้างความแตกต่างของชนิดงานบำรุงรักษาทั้งหมดที่จำเป็นสำหรับอุปกรณ์ของคุณ ในหน้าดังกล่าว คุณยังสามารถตั้งค่าการคาดการณ์ รายการตรวจสอบการบำรุงรักษา และเครื่องมือ สำหรับชุดของชนิดงานบำรุงรักษาได้ด้วย

> [!NOTE]
> ชนิดงานบำรุงรักษาอาจเกี่ยวข้องกับประเภทชนิดของงานบำรุงรักษาประเภทเดียวเท่านั้น

## <a name="create-a-maintenance-job-type-category"></a>สร้างประเภทชนิดของงานบำรุงรักษา

1. เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **งาน** \> **ประเภทชนิดของงานบำรุงรักษา**
2. เลือก **ใหม่**
3. ในฟิลด์ **ประเภทชนิดของงานบำรุงรักษา** ให้ป้อนรหัสสำหรับประเภทชนิดของงานบำรุงรักษา
4. ในฟิลด์ **ชื่อ** ป้อนชื่อ

    หลังจากที่คุณเชื่อมโยงประเภทชนิดของงานการบำรุงรักษากับชนิดงานบำรุงรักษา ฟิลด์ **ชนิดงาน** จะแสดงจำนวนของชนิดงานบำรุงรักษาที่เกี่ยวข้องกับประเภทชนิดงานบำรุงรักษานี้

![หน้าประเภทของชนิดงานการบำรุงรักษา](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>สร้างตัวแปรชนิดของงานบำรุงรักษา

1. เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **งาน** \> **ตัวแปรชนิดของงานบำรุงรักษา**
2. เลือก **ใหม่**
3. ในฟิลด์ **ตัวแปรชนิดงานบำรุงรักษา** ให้ป้อนรหัสสำหรับตัวแปรชนิดงานบำรุงรักษา
4. ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
5. บนแท็บด่วน **ชนิดงานบำรุงรักษา** เลือก **เพิ่ม** เพื่อเพิ่มชนิดงานบำรุงรักษา
6. ในฟิลด์ **ชนิดงานบำรุงรักษา** ให้เลือกชนิดงานบำรุงรักษา
7. ทำซ้ำขั้นตอนที่ 5 ถึง 6 เพื่อเพิ่มชนิดงานบำรุงรักษาเพิ่มเติมให้กับตัวแปรชนิดงานบำรุงรักษา

    บนแท็บด่วน **รายละเอียด** ฟิลด์ **ชนิดงาน** จะแสดงจำนวนของชนิดงานบำรุงรักษาที่ถูกเพิ่มเข้าไปในตัวแปรชนิดงานบำรุงรักษานี้

![หน้าตัวแปรชนิดงานการบำรุงรักษา](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>สร้างการค้าของงานบำรุงรักษา

1. เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **งาน** \> **การค้าของชนิดงานบำรุงรักษา**
2. เลือก **ใหม่**
3. ในฟิลด์ **การค้า** ให้ป้อนรหัสสำหรับการค้าของชนิดงานบำรุงรักษา
4. ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
5. บนแท็บด่วน **ทักษะ** ให้เลือก **เพิ่ม** เพื่อเพิ่มทักษะใหม่ที่ควรเกี่ยวข้องกับการค้าของงานบำรุงรักษา
6. ในฟิลด์ **ทักษะ** เลือกทักษะ
7. ในฟิลด์ **ระดับ** เลือกระดับทักษะ
8. ทำซ้ำขั้นตอนที่ 5 ถึง 7 เพื่อเพิ่มทักษะเพิ่มเติมไปยังการค้าของงานบำรุงรักษา

    บนแท็บด่วน **รายละเอียด** ฟิลด์ **ทักษะ** จะแสดงจำนวนของทักษะที่ถูกเพิ่มเข้าไปยังการค้าของงานบำรุงรักษานี้

9. บนแท็บด่วน **ใบรับรอง** ให้เลือก **เพิ่ม** เพื่อเพิ่มใบรับรองไปยังการค้าของงานบำรุงรักษา
10. ในฟิลด์ **ชนิดของใบรับรอง** ให้เลือกใบรับรอง
11. ทำซ้ำขั้นตอนที่ 9 ถึง 10 เพื่อเพิ่มใบรับรองเพิ่มเติมไปยังการค้าของงานบำรุงรักษา

    บนแท็บด่วน **รายละเอียด** ฟิลด์ **ใบรับรอง** จะแสดงจำนวนของใบรับรองที่ถูกเพิ่มเข้าไปยังการค้าของงานบำรุงรักษานี้

![หน้าการค้าของงานบำรุงรักษา](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>สร้างตัวแปรของรายการตรวจสอบการบำรุงรักษา

เมื่อคุณสร้างรายการของรายการตรวจสอบการบำรุงรักษาในค่าเริ่มต้นชนิดงานบำรุงรักษา คุณต้องเลือกชนิดรายการตรวจสอบการบำรุงรักษา **ตัวแปร** เป็นชนิดรายการตรวจสอบการบำรุงรักษาหนึ่งชนิด มีการใช้เพื่อกำหนดผลลัพธ์ที่เป็นไปได้ในช่วงบนรายการของรายการตรวจสอบการบำรุงรักษาที่เกี่ยวข้องกับรายการใบสั่งงาน ตัวแปรช่วยให้คุณสามารถสร้างชุดของผลลัพธ์ที่กำหนดไว้ล่วงหน้าได้โดยไม่ต้องทำการวัดที่แน่นอน

**ตัวอย่างที่ 1:** คุณสามารถวัดระดับน้ำมันโดยการกำหนดค่าสามค่า: **ระดับสูงเกินไป** **ระดับต่ำเกินไป** และ **ระดับภายในช่วง** สำหรับแต่ละค่า คุณกำหนดว่าผลลัพธ์ของค่าคือ **ผ่าน** **ล้มเหลว** หรือ **ไม่มี**

**ตัวอย่างที่ 2:** คุณทำการตรวจสอบภาพของอุปกรณ์ในการประเมินการสึกหรอและการฉีกขาด

1. เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **รายการตรวจสอบการบำรุงรักษา** \> **ตัวแปรรายการตรวจสอบการบำรุงรักษา**
2. เลือก **ใหม่**
3. ในฟิลด์ **ตัวแปร** ให้ป้อนรหัสสำหรับตัวแปรรายการตรวจสอบการบำรุงรักษา
4. ในฟิลด์ **ชื่อ** ป้อนชื่อ
5. บนแท็บด่วน **ทั่วไป** ให้เลือก **เพิ่ม** เพื่อเพิ่มรายการสำหรับตัวแปร

    มีการป้อนหมายเลขรายการตามลำดับโดยอัตโนมัติในฟิลด์ **หมายเลขรายการ** หลังจากที่คุณได้เพิ่มรายการทั้งหมดแล้ว คุณก็สามารถเปลี่ยนหมายเลขรายการได้ตามที่คุณต้องการ เมื่อคุณเลือกรายการ แล้วจากนั้น กดคีย์ **ลูกศรลง** หมายเลขถัดไปในลำดับจะถูกป้อนโดยอัตโนมัติในรายการถัดไป

6. ในฟิลด์ **ค่า** ให้ป้อนคำอธิบายค่า
7. ในฟิลด์ **ผลลัพธ์** เลือกผลลัพธ์สำหรับรายการ

![หน้าตัวแปรของรายการตรวจสอบการบำรุงรักษา](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>สร้างเท็มเพลตของรายการตรวจสอบการบำรุงรักษา

เท็มเพลตรายการตรวจสอบการบำรุงรักษาสามารถใช้เป็นชุดทั่วไปของงานที่ผู้ปฏิบัติงานต้องทำเพื่อทำใบสั่งงานให้เสร็จสมบูรณ์ได้อย่างถูกต้อง เท็มเพลตจะอ้างอิงจากรายการในรายการตรวจสอบการบำรุงรักษาบนค่าเริ่มต้นชนิดงานบำรุงรักษา เท็มเพลตอาจอ้างอิงไปยังรายการเริ่มต้นสำหรับชนิดงานบำรุงรักษาต่างๆ ดังนั้น คุณจึงสามารถนำชุดของงานรายการตรวจสอบการบำรุงรักษาทั่วไปมาใช้ใหม่ได้ง่าย ตัวอย่างของเท็มเพลตรายการตรวจสอบการบำรุงรักษามีคำแนะนำด้านความปลอดภัยทั่วไป และรายการของสินค้าและเงื่อนไขที่ต้องมีการตรวจสอบในปั๊มเฉพาะหรือแบบจำลองที่คล้ายกันของสายพานลำเลียง

1. เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **รายการตรวจสอบการบำรุงรักษา** \> **เท็มเพลตรายการตรวจสอบการบำรุงรักษา**
2. เลือก **ใหม่**

    รหัสเท็มเพลตจะถูกป้อนโดยอัตโนมัติในฟิลด์ **เท็มเพลตรายการตรวจสอบการบำรุงรักษา**

3. ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับเท็มเพลตรายการตรวจสอบการบำรุงรักษา
4. บนแท็บด่วน **รายการของรายการตรวจสอบการบำรุงรักษา** เลือก **เพิ่ม** เพื่อเพิ่มรายการเท็มเพลต

    มีการป้อนหมายเลขรายการตามลำดับโดยอัตโนมัติในฟิลด์ **หมายเลขรายการ** หลังจากที่คุณได้เพิ่มรายการทั้งหมดแล้ว คุณก็สามารถเปลี่ยนหมายเลขรายการได้ตามที่คุณต้องการ เมื่อคุณเลือกรายการ แล้วจากนั้น กดคีย์ **ลูกศรลง** หมายเลขถัดไปในลำดับจะถูกป้อนโดยอัตโนมัติในรายการถัดไป

5. ในฟิลด์ **ชนิด** ให้เลือกชนิดสำหรับรายการของรายการตรวจสอบการบำรุงรักษา สำหรับชนิดของรายการตรวจสอบการบำรุงรักษาแต่ละชนิด FastTab **รายละเอียดรายการ** จะแสดงฟิลด์ที่เกี่ยวข้อง ค่าที่พร้อมใช้งานมีดังต่อไปนี้

    - **ข้อความ** – รายการมีข้อความที่อธิบายถึงสิ่งที่ต้องทำ ใช้ชนิดของรายการตรวจสอบการบำรุงรักษานี้ หากคุณต้องการให้ผู้ปฏิบัติงานเช็คเหรือตรวจสอบบางอย่าง แต่คุณไม่ต้องคาดหวังถึงผลลัพธ์เฉพาะ (ที่วัดได้) หลังจากที่คุณเลือกชนิดนี้แล้ว ให้ป้อนชื่อหรือส่วนหัวในฟิลด์ **ชื่อ** ในฟิลด์ **คำแนะนำ** ให้ป้อนคำอธิบายของสิ่งที่ต้องทำ ถ้าขั้นตอนนี้เป็นแบบบังคับสำหรับรายการตรวจสอบการบำรุงรักษา ตั้งค่าตัวเลือก **แบบบังคับ** เป็น **ใช่**
    - **ส่วนหัว** – มีการใช้รายการเป็นส่วนหัวเพื่อจัดกลุ่มรายการของรายการตรวจสอบการบำรุงรักษาที่ปรากฏอยู่ด้านล่าง ชนิดนี้มีประโยชน์ ถ้าคุณมีรายการของรายการตรวจสอบการบำรุงรักษาหลายรายการที่สามารถแบ่งออกเป็นพื้นที่เฉพาะได้ ส่วนหัวแสดงภาพรวมสำหรับผู้ปฏิบัติงานที่จะดำเนินรายการตรวจสอบการบำรุงรักษาให้เสร็จสมบูรณ์ ซึ่งมีบรายการของรายการตรวจสอบการบำรุงรักษาจำนวนมาก หลังจากที่คุณเลือกชนิดนี้แล้ว ให้ป้อนชื่อที่เป็นคำอธิบายในฟิลด์ **ชื่อ**
    - **เท็มเพลต** – มีการใช้รายการเพื่อทำการอ้างอิงถึงเท็มเพลตที่มีอยู่ หลังจากที่คุณเลือกชนิดนี้แล้ว ให้ป้อนชื่อสำหรับเท็มเพลตในฟิลด์ **ชื่อ** ในฟิลด์ **เท็มเพลต** ให้เลือกเท็มเพลต
    - **ตัวแปร** – มีการใช้รายการเพื่อกำหนดผลลัพธ์ที่เป็นไปได้ในช่วง สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าตัวแปรรายการตรวจสอบการบำรุงรักษา ให้ดูที่ส่วน [สร้างตัวแปรของรายการตรวจสอบการบำรุงรักษา](#create-a-maintenance-checklist-variable) หลังจากที่คุณเลือกชนิดนี้แล้ว ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับตัวแปรในฟิลด์ **ชื่อ** ในฟิลด์ **ตัวแปร** เลือกตัวแปร ในฟิลด์ **คำแนะนำ** ให้ป้อนคำอธิบายของสิ่งที่ต้องทำ ถ้าขั้นตอนนี้เป็นแบบบังคับสำหรับรายการตรวจสอบการบำรุงรักษา ตั้งค่าตัวเลือก **แบบบังคับ** เป็น **ใช่**
    - **การวัด** – มีการใช้รายการเพื่อบันทึกการวัดที่ระบุ คุณสามารถตั้งค่าการวัดที่ควรเกี่ยวข้องกับตัวนับที่กำหนดไว้ล่วงหน้า หลังจากที่คุณเลือกชนิดนี้แล้ว ให้ป้อนชื่อสำหรับเท็มเพลตในฟิลด์ **ชื่อ** ถ้าขั้นตอนนี้เป็นแบบบังคับสำหรับรายการตรวจสอบการบำรุงรักษา ตั้งค่าตัวเลือก **แบบบังคับ** เป็น **ใช่** ถ้าคุณต้องการใช้รายการของการวัดเป็นการลงทะเบียนตัวนับ ให้เลือกตัวนับในฟิลด์ **ตัวนับ** จากนั้น ฟิลด์ **หน่วย** ที่เกี่ยวข้องจะถูกปรับปรุงโดยอัตโนมัติ ถ้าคุณเลือกตัวนับแล้ว ให้เลือกวิธีการปรับปรุงในฟิลด์ **ค่า** ในฟิลด์ **ค่าต่ำสุด** และ **ค่าสูงสุด** ป้อนช่วงของค่าที่อนุญาต ในฟิลด์ **คำแนะนำ** ให้ป้อนคำอธิบายของสิ่งที่ต้องทำ

        > [!NOTE]
        > รายการใดๆ ของชนิด **การวัด** ที่ไม่มีการตั้งค่าตัวนับ จะถือว่าเป็นการลงทะเบียนการวัดอิสระที่ไม่มีการติดตามผลแบบอัตโนมัติสำหรับในการจัดการสินทรัพย์ ในทำนองเดียวกัน ถ้าชนิดของตัวนับที่เลือกไม่มีอยู่ในสินทรัพย์ที่เกี่ยวข้องกับใบสั่งงาน งานรายการตรวจสอบการบำรุงรักษาจะถือว่าเป็นการวัดอิสระ ค่าตัวนับสามารถเปลี่ยนแปลงได้หลายครั้ง จะไม่มีการลงรายการบัญชีจนกว่า [สถานะของวงจรการใช้ของใบสั่งงาน](work-order-lifecycle-states.md) จะมีการเปลี่ยนแปลงเป็นสถานะที่ตัวเลือก **ประมวลผลรายการตรวจสอบการบำรุงรักษา** ถูกตั้งค่าเป็น **ใช่**

    บนแท็บด่วน **รายละเอียด** ฟิลด์ **ตรวจสอบ** จะแสดงจำนวนรวมของรายการของรายการตรวจสอบในเท็มเพลตของคุณ หมายเลขนี้รวมถึงรายการที่ซ้อนกันในเท็มเพลตที่มีอยู่ใดๆ ซึ่งคุณได้อ้างอิงในเท็มเพลตของคุณ

![หน้าเท็มเพลตของรายการตรวจสอบการบำรุงรักษา](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>สร้างชนิดของงานบำรุงรักษา

1. เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **งาน** \> **ชนิดของงานบำรุงรักษา**
2. เลือก **ใหม่**
3. ในฟิลด์ **ชนิดงานบำรุงรักษา** ให้ป้อนรหัสสำหรับชนิดงานบำรุงรักษา
4. ในฟิลด์ **ชื่อ** ป้อนชื่อ

    FastTab **รายละเอียด** จะแสดงภาพรวมของจำนวนของตัวแปรชนิดของงานบำรุงรักษา ทักษะ ใบรับรอง งานที่ประสบความสำเร็จ และชนิดสินทรัพย์ที่ถูกสร้างขึ้นบนชนิดงานบำรุงรักษานี้ ฟิลด์ **การตั้งค่ารายการ** จะแสดงจำนวนของรายการเริ่มต้นของชนิดงานการบำรุงรักษาที่มีการตั้งค่าไว้ในชนิดงานการบำรุงรักษานี้ ฟิลด์ **สินทรัพย์** แสดงจำนวนของสินทรัพย์ที่ใช้งานอยู่ซึ่งใช้ชนิดงานการบำรุงรักษานี้ในขณะนี้

5. บนแท็บด่วน **ทั่วไป** ในฟิลด์ **ประเภทชนิดของงานบำรุงรักษา** เลือกชนิดงานการบำรุงรักษา
6. ตั้งค่าตัวเลือก **กิจกรรมการหยุดทำงานของการบำรุงรักษา** เป็น **ใช่** ถ้าชนิดงานบำรุงรักษาจำเป็นต้องมีการหยุดการบำรุงรักษาของอุปกรณ์ ก่อนที่จะสามารถดำเนินการงานได้
7. บนแท็บด่วน **คำอธิบาย** ป้อนคำอธิบายของชนิดงานบำรุงรักษา
8. บนแท็บด่วน **ตัวแปรชนิดงานบำรุงรักษา** คุณสามารถเพิ่มตัวแปรไปยังชนิดงานบำรุงรักษา
9. บนแท็บด่วน **ทักษะที่จำเป็น** และ **ใบรับรองที่จำเป็น** คุณสามารถเพิ่มทักษะและข้อกำหนดใบรับรองสำหรับชนิดงานบำรุงรักษา
10. ถ้าต้องมีการดำเนินการชนิดงานบำรุงรักษาเฉพาะถัดไป ให้เพิ่มบนแท็บด่วน **งานที่ประสบความสำเร็จ** นอกจากนี้ คุณยังสามารถตั้งค่าตัวแปรชนิดงานการบำรุงรักษา และการค้าที่เกี่ยวข้องกับชนิดงานบำรุงรักษาได้ด้วย ถ้างานที่ประสบความสำเร็จควรเริ่มต้นจำนวนของวันเฉพาะ ก่อนหรือหลังจากงานที่ใช้ชนิดงานบำรุงรักษานี้ ได้เริ่มต้นแล้ว ป้อนจำนวนของวันในฟิลด์ **ความล่าช้าตามวัน** ตัวเลขค่าบวกแสดงวันหลังจากวันที่เริ่มต้นงานที่เกี่ยวข้อง และตัวเลขค่าลบแสดงถึงจำนวนวันก่อนการเริ่มต้นที่มีการจัดกำหนดการไว้ของงานที่เกี่ยวข้อง ตัวอย่างเช่น ถ้าคุณป้อน **5** งานที่ประสบความสำเร็จจะเริ่มต้นในห้าวัน หลังจากการเริ่มต้นของงานที่เกี่ยวข้องกับชนิดงานบำรุงรักษา ถ้าคุณป้อน **-3** งานที่ประสบความสำเร็จจะเริ่มต้นในสามวัน ก่อนการเริ่มต้นที่จัดกำหนดการของงานที่เกี่ยวข้องกับชนิดงานบำรุงรักษา

    > [!NOTE]
    > ถ้าคุณเพิ่มรายการของชนิดงานบำรุงรักษามากกว่าหนึ่งรายการ ลำดับของรายการจะบ่งชี้ลำดับที่ควรมีการดำเนินการ ลำดับจะเริ่มต้นที่ด้านบนของรายการ

11. บนแท็บด่วน **ชนิดสินทรัพย์** คุณสามารถเพิ่มชนิดสินทรัพย์ไปยังชนิดงานบำรุงรักษาได้

![หน้าชนิดของงานบำรุงรักษา](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>สร้างรายการเริ่มต้นของชนิดงานบำรุงรักษาและการคาดการณ์ที่เกี่ยวข้อง รายการตรวจสอบการบำรุงรักษา เครื่องมือ คำอธิบาย และเอกสารแนบ

1. เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **งาน** \> **ค่าเริ่มต้นชนิดของงานบำรุงรักษา**

    หรือ

    เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **งาน** \> **ชนิดงานบำรุงรักษา** เลือกชนิดงานบำรุงรักษา และจากนั้น เลือก **ค่าเริ่มต้นชนิดงานบำรุงรักษา**

2. เลือก **ใหม่**
3. ในฟิลด์ **ตำแหน่งที่ทำงาน** **ชนิดสินทรัพย์** **ผู้ผลิต** **แบบจำลอง** และ **สินทรัพย์** ให้เลือกค่าที่เหมาะสม โดยขึ้นอยู่กับความเฉพาะเจาะจงของค่าเริ่มต้นของชนิดงานบำรุงรักษา ที่ควรจะเป็น
4. ในฟิลด์ **ชนิดงานบำรุงรักษา** ให้เลือกชนิดงานบำรุงรักษา ถ้าไม่ได้เลือกโดยอัตโนมัติ
5. ในฟิลด์ **ตัวแปรชนิดงานบำรุงรักษา** และฟิลด์ **การค้า** ให้เลือกตัวแปรชนิดงานบำรุงรักษาและการค้างานบำรุงรักษา ตามที่คุณต้องการ
6. เลือก **การคาดการณ์**
7. บนหน้า **การคาดการณ์ค่าเริ่มต้นของชนิดงานบำรุงรักษา** คุณสามารถทำการคาดการณ์ในชั่วโมง สินค้า และค่าใช้จ่ายได้ บนแท็บที่เกี่ยวข้อง ให้เลือก **เพิ่ม** และทำการเลือกเพื่อสร้างการคาดการณ์ที่จำเป็นสำหรับชนิดงานบำรุงรักษา
8. บนแท็บ **การคาดการณ์สินค้า** คุณสามารถเลือกมิติสินค้าคงคลังที่ควรแสดงบนรายการสินค้าได้ เลือก **สินค้าคงคลัง** \> **มิติ** เลือกมิติที่จะแสดง ตั้งค่าตัวเลือก **บันทึกการตั้งค่า** เป็น **ใช่** แล้วจากนั้น เลือก **ตกลง**
9. บนแท็บ **การคาดการณ์สินค้า** เลือก **สินค้าที่ใช้** เพื่อดูภาพรวมของตำแหน่งที่สินค้าในรายการที่เลือกถูกใช้ในการจัดการสินทรัพย์ โดยสัมพันธ์กับสินทรัพย์ ค่าเริ่มต้นของชนิดงานบำรุงรักษา อะไหล่สำรอง และใบสั่งงาน 

    FastTab **ยอดรวมการคาดการณ์ในการบำรุงรักษา** แสดงภาพรวมของผลรวมการคาดการณ์ ภาพรวมนี้มีจำนวนรวมของชั่วโมงและรายการของการคาดการณ์ที่ถูกสร้างขึ้น

    > [!NOTE]
    > เมื่อต้องการคัดลอกการตั้งค่าการคาดการณ์จากชนิดงานบำรุงรักษาอื่น เลือก **คัดลอกการคาดการณ์** แล้วจากนั้น เลือกชนิดงานบำรุงรักษาเพื่อคัดลอกการตั้งค่ามา

11. เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ
12. ปิดหน้า **การคาดการณ์ค่าเริ่มต้นของชนิดงานบำรุงรักษา** เพื่อกลับไปยังหน้า **ค่าเริ่มต้นของชนิดงานบำรุงรักษา**
13. เลือก **รายการตรวจสอบการบำรุงรักษา**
14. ในหน้า **รายการตรวจสอบค่าเริ่มต้นของชนิดงานบำรุงรักษา** คุณสามารถเพิ่มรายการของรายการตรวจสอบการบำรุงรักษาไปยังค่าเริ่มต้นของชนิดงานบำรุงรักษาที่เลือกได้ บนแท็บด่วน **รายการของการตรวจสอบการบำรุงรักษา** เลือก **สร้าง** เพื่อเพิ่มรายการของรายการตรวจสอบการบำรุงรักษา

    จะมีการป้อนหมายเลขรายการโดยอัตโนมัติในฟิลด์ **หมายเลขรายการ** เพื่อระบุลำดับของรายการของรายการตรวจสอบการบำรุงรักษา คุณสามารถแก้ไขหมายเลขรายการได้ตามที่คุณต้องการ หลังจากที่คุณได้สร้างรายการของรายการตรวจสอบการบำรุงรักษาครั้งแรก แล้วจากนั้น ให้กดคีย์ **ลูกศรลง** เพื่อเพิ่มรายการด้านล่าง อีกทางหนึ่งคือ คุณสามารถเลือกรายการของรายการตรวจสอบการบำรุงรักษา และจากนั้น เลือก **สร้าง** ในกรณีนี้ รายการใหม่จะถูกเพิ่มเหนือรายการของรายการตรวจสอบการบำรุงรักษาที่เลือก

15. ในฟิลด์ **ชนิด** ให้เลือกชนิดของรายการ แล้วจากนั้น เพิ่มข้อมูลที่เกี่ยวข้องกับชนิดรายการตรวจสอบการบำรุงรักษา สำหรับคำอธิบายเกี่ยวกับชนิดที่พร้อมใช้งานและฟิลด์ที่เกี่ยวข้อง ให้ดูที่ส่วน [สร้างเท็มเพลตรายการตรวจสอบการบำรุงรักษา](#create-a-maintenance-checklist-template)

    > [!NOTE]
    > เมื่อต้องการคัดลอกการตั้งค่ารายการตรวจสอบการบำรุงรักษาจากชนิดงานบำรุงรักษาอื่น เลือก **คัดลอกรายการตรวจสอบการบำรุงรักษา** แล้วจากนั้น เลือกชนิดงานบำรุงรักษาเพื่อคัดลอกการตั้งค่ามา
    >
    > คุณสามารถสร้างเท็มเพลตได้จากรายการตรวจสอบการบำรุงรักษาที่มีอยู่ จากนั้น คุณสามารถใช้ซ้ำเท็มเพลตในรายการตรวจสอบการบำรุงรักษาหลายรายการได้ เท็มเพลตใหม่จะเป็นสำเนาที่เหมือนกันของรายการตรวจสอบการบำรุงรักษาที่ใช้งานอยู่ เลือก **สร้างเท็มเพลต** และจากนั้น ป้อนชื่อสำหรับเท็มเพลต เมื่อต้องการแทนที่รายการตรวจสอบการบำรุงรักษาที่มีอยู่ด้วยรายการเดียวที่อ้างอิงถึงเท็มเพลตใหม่ ให้ตั้งค่าตัวเลือก **แทนที่** เป็น **ใช่** คุณสามารถดูเนื้อหาของเท็มเพลตในหน้ารายละเอียด **เท็มเพลตการตรวจสอบการบำรุงรักษา**

16. เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ
17. กลับไปที่หน้า **ค่าเริ่มต้นของชนิดงานบำรุงรักษา**
18. เลือก **เครื่องมือ**
19. บนหน้า **เครื่องมือเริ่มต้นของชนิดงานบำรุงรักษา** คุณสามารถเพิ่มเครื่องมือ (ทรัพยากร) ที่ควรใช้สำหรับชนิดงานบำรุงรักษา เลือก **สร้าง** แล้วจากนั้น เลือกเครื่องมือในฟิลด์ **ทรัพยากร**

    > [!NOTE]
    > เมื่อต้องการคัดลอกการตั้งค่าเครื่องมือจากชนิดงานบำรุงรักษาอื่น เลือก **คัดลอกเครื่องมือ** แล้วจากนั้น เลือกชนิดงานบำรุงรักษาเพื่อคัดลอกการตั้งค่ามา

20. เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ
21. กลับไปที่หน้า **ค่าเริ่มต้นของชนิดงานบำรุงรักษา**
22. เลือก **คำอธิบายงาน**
23. บนหน้า **คำอธิบายงาน** ให้เลือก **แก้ไข** แล้วจากนั้น เพิ่มคำอธิบายที่เกี่ยวข้องกับค่าเริ่มต้นของชนิดของงานบำรุงรักษาที่เลือก ตามที่คุณต้องการ
24. เลือก **บันทึก** เพื่อบันทึกคำอธิบาย

    ถ้าคุณเพิ่มคำอธิบายงานไว้ที่นี่ จะแทนที่คำอธิบายใดๆ ที่ตั้งค่าไว้สำหรับชนิดงานบำรุงรักษาบนหน้า **ชนิดงานบำรุงรักษา** ถ้าคุณไม่ได้เพิ่มคำอธิบายงานไว้ที่นี่ จะมีการใช้คำอธิบายใดๆ ที่ตั้งค่าไว้สำหรับชนิดงานบำรุงรักษา คำอธิบายจะถูกโอนย้ายไปยังใบสั่งงานที่ใช้ชนิดงานบำรุงรักษา หรือค่าเริ่มต้นของชนิดงานบำรุงรักษาโดยอัตโนมัติ

25. กลับไปที่หน้า **ค่าเริ่มต้นของชนิดงานบำรุงรักษา**
26. เมื่อต้องการตั้งค่าเอกสารแนบบนรายการเริ่มต้นของชนิดงานบำรุงรักษาที่เลือก ให้เลือก **แนบเอกสาร** เอกสารแนบที่มีการตั้งค่าในรายการเริ่มต้นของชนิดงานบำรุงรักษาจะรวมอยู่ในรายการใบสั่งงานที่ใช้รายการเริ่มต้นของชนิดงานบำรุงรักษาโดยอัตโนมัติ
27. เลือก **สร้าง** และจากนั้น เลือกชนิดเอกสาร
28. อัปโหลดเอกสารหรือไฟล์
29. ตั้งค่าฟิลด์บนหน้า **เอกสารแนบ** การตั้งค่าเอกสารแนบใช้ฟังก์ชันการตั้งค่าเอกสารมาตรฐาน
30. เลือก **บันทึก** เพื่อบันทึกเอกสารแนบ

    > [!NOTE]
    > จะมีการพิมพ์เอกสารแนบบนชนิดงานบำรุงรักษาพร้อมกับรายงานใบสั่งงาน เฉพาะเมื่อมีการเลือกชนิดเอกสารของเอกสารแนบบนแท็บ **ชนิดเอกสาร** ของหน้า **พารามิเตอร์การจัดการสินทรัพย์** (**การจัดการสินทรัพย์** \> **การตั้งค่า** \> **พารามิเตอร์การจัดการสินทรัพย์**) ตัวอย่างของเอกสารแนบรวมถึงแนวทางที่อธิบายวิธีการทำให้งานที่ระบุหรือรายการตรวจสอบการบำรุงรักษาที่กำหนดไว้ล่วงหน้าเสร็จสมบูรณ์ (ถ้าคุณไม่ได้ใช้ฟังก์ชันรายการตรวจสอบการบำรุงรักษาสำหรับรายการเริ่มต้นของชนิดงานบำรุงรักษา)

    บนหน้า **ค่าเริ่มต้นของชนิดงานบำรุงรักษา** แต่ละรายการจะแสดงจำนวนชั่วโมงที่คาดการณ์ และจำนวนของรายการที่ได้ถูกสร้างขึ้นสำหรับสินค้า ค่าใช้จ่าย รายการตรวจสอบการบำรุงรักษา และเครื่องมือ ฟิลด์ **สินทรัพย์** แสดงจำนวนของสินทรัพย์ที่ใช้งานอยู่ซึ่งเกี่ยวข้องกับรายการเริ่มต้นของชนิดงานบำรุงรักษา

31. เมื่อต้องการคัดลอกค่าเริ่มต้นของชนิดงานบำรุงรักษาไปยังค่าเริ่มต้นของชนิดงานบำรุงรักษาอีกค่าหนึ่ง ให้เลือกรายการเริ่มต้นของชนิดงานบำรุงรักษาเพื่อคัดลอกการตั้งค่าอื่น ให้เลือก **คัดลอกการตั้งค่า** แล้วจากนั้น เลือกค่าเริ่มต้นของชนิดงานบำรุงรักษาที่จะคัดลอก
32. เมื่อต้องการดูรายการของสินทรัพย์ แผนการบำรุงรักษา หรือรอบการบำรุงรักษา ที่ใช้รายการเริ่มต้นชนิดงานบำรุงรักษาในปัจจุบัน และจากนั้น เลือก **ใช้โดย**

![หน้าค่าเริ่มต้นของชนิดงานการบำรุงรักษา](media/07-setup-for-work-orders.png)

เมื่อระบบเลือกค่าเริ่มต้นของชนิดงานบำรุงรักษาที่พร้อมใช้งานซึ่งควรใช้ในรายการใบสั่งงาน การเลือกจะขึ้นอยู่กับสินทรัพย์ และการตั้งค่าชนิดของสินทรัพย์ที่เกี่ยวข้อง การจัดการสินทรัพย์จะผ่านเรกคอร์ดค่าเริ่มต้นของชนิดงานบำรุงรักษาทั้งหมดที่เกี่ยวข้องกับชนิดของงานบำรุงรักษาที่เกี่ยวข้องกับชนิดสินทรัพย์ เพื่อตรวจสอบการจับคู่ที่เป็นไปได้ ซึ่งจะตรวจสอบชุดที่เฉพาะเจาะจงมากที่สุดก่อน กล่าวอีกอย่างหนึ่งคือ ถ้าต้องการค้นหาชุดข้อมูลที่เฉพาะเจาะจงที่สุด การจัดการสินทรัพย์ตรวจสอบการจับคู่ที่เป็นไปได้สำหรับฟิลด์ **การค้า** เป็นอันดับแรก ถ้าไม่พบการจับคู่ จะตรวจสอบการจับคู่สำหรับฟิลด์ **ตัวแปรชนิดงานบำรุงรักษา** ถ้าไม่พบข้อมูลที่ตรงกัน จะมีการตรวจสอบการจับคู่สำหรับฟิลด์ **ชนิดงานบำรุงรักษา** และอื่นๆ (**การค้า** จากนั้น **ตัวแปรของชนิดงานบำรุงรักษา** จากนั้น **ชนิดงานบำรุงรักษา** จากนั้น **สินทรัพย์** จากนั้น **แบบจำลอง** จากนั้น **ผู้ผลิต** และจากนั้น **ชนิดสินทรัพย์**) ถ้าไม่พบรายการที่ตรงกัน จะมีการใช้เรกคอร์ดเริ่มต้นที่มีการเลือกชนิดงานบำรุงรักษาเท่านั้น

รหัสกิจกรรมโครงการมีความเกี่ยวข้องโดยอัตโนมัติกับรายการงานบำรุงรักษาแต่ละรายการที่คุณสร้างขึ้น กิจกรรมโครงการถูกสร้างขึ้นในโครงการการคาดการณ์ที่ถูกเลือกในฟิลด์ **โครงการการคาดการณ์ในการบำรุงรักษา** บนแท็บ **สินทรัพย์** ของหน้า **พารามิเตอร์การจัดการสินทรัพย์** วัตถุประสงค์ของกิจกรรมโครงการคือ เพื่อจัดการการคาดการณ์ในชั่วโมง สินค้า และค่าใช้จ่าย ที่เกี่ยวข้องกับใบสั่งงาน การคาดการณ์ชนิดงานบำรุงรักษาจะถูกโอนย้ายโดยอัตโนมัติไปยังรายการใบสั่งงาน และจะมีการคัดลอกจากโครงการการคาดการณ์ไปยังโครงการของใบสั่งงานที่สร้างขึ้นสำหรับรายการใบสั่งงาน วัตถุประสงค์ของกิจกรรมโครงการคือ เพื่อจัดการการคาดการณ์ที่เกี่ยวข้องกับใบสั่งงาน

คุณสามารถตั้งค่าชุดงานเพื่อปรับปรุงการอ้างอิงเริ่มต้นของชนิดงานบำรุงรักษาได้ตามช่วงเวลาปกติ หรือคุณสามารถรันงานด้วยตนเองได้ เมื่อต้องการสร้างชุดงานหรือเรียกใช้การปรับปรุงด้วยตนเอง ให้เลือก **การจัดการสินทรัพย์** \> **ประจำงวด** \> **การบำรุงรักษาเชิงป้องกัน** \> **ปรับปรุงการอ้างอิงเริ่มต้นของชนิดงานบำรุงรักษา**

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>ภาพรวมของชนิดงานบำรุงรักษาที่เกี่ยวข้องกับสินทรัพย์

หลังจากที่คุณได้สร้างชุดเริ่มต้นของชนิดงานบำรุงรักษาที่จำเป็น คุณสามารถใช้หน้า **สินทรัพย์ทั้งหมด** เพื่อดูภาพรวมของค่าเริ่มต้นของชนิดงานบำรุงรักษาปัจจุบันซึ่งเกี่ยวข้องกับสินทรัพย์เฉพาะได้ ภาพรวมจะแสดชุดเริ่มต้นของชนิดงานบำรุงรักษาทั้งหมดที่สามารถใช้กับชนิดสินทรัพย์ที่เลือกไว้สำหรับสินทรัพย์ ชุดข้อมูลเหล่านี้รวมถึงชุดที่มีการเปลี่ยนแปลงของตัวแปรชนิดงานบำรุงรักษาและการค้าของงานบำรุงรักษา

1. เลือก **การจัดการสินทรัพย์** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด** หรือ **สินทรัพย์ที่ใช้งานอยู่**
2. ในรายการ ให้เลือกสินทรัพย์เพื่อดูภาพรวมของชุดของชนิดงานบำรุงรักษา
3. บนบานหน้าต่างการดำเนินการ บนแท็บ **ทั่วไป** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **ชนิดงานบำรุงรักษา**

    บานหน้าต่างด้านซ้ายของหน้า **ชนิดงานบำรุงรักษาสินทรัพย์** จะแสดงรายการของชุดของชนิดงานการบำรุงรักษาทั้งหมดที่เกี่ยวข้องกับสินทรัพย์ที่เลือก

4. เลือกชุดของชนิดงานบำรุงรักษาเพื่อดูการตั้งค่าที่เกี่ยวข้องสำหรับรายการตรวจสอบการบำรุงรักษา การคาดการณ์ และเครื่องมือ ส่วน **รายละเอียด** บนแท็บด่วน **ค่าเริ่มต้นของชนิดงานบำรุงรักษา** แสดงจำนวนของรายการตรวจสอบการบำรุงรักษาที่เกี่ยวข้อง ชั่วโมงที่คาดการณ์ สินค้า และอื่นๆ ที่เกี่ยวข้องกับชุดของชนิดงานบำรุงรักษาที่เลือก
5. ถ้าต้องการดูรายละเอียดสำหรับชนิดงานบำรุงรักษาที่เลือก เลือก **ชนิดงานบำรุงรักษา**

![หน้าชนิดของงานบำรุงรักษาสินทรัพย์](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>การปรับปรุงอัตโนมัติของการคาดการณ์ชนิดงานบำรุงรักษา

ในการบริหารสินทรัพย์ คุณสามารถปรับปรุงการเปลี่ยนแปลงใดๆ ไปยังการคาดการณ์ชนิดงานบำรุงรักษาได้โดยอัตโนมัติ สำหรับต้นทุนชั่วโมง ต้นทุนสินค้า และค่าใช้จ่ายที่มีการปรับปรุงในโมดูลอื่นๆ ด้วยวิธีนี้ คุณจะช่วยรับประกันได้ว่าการคาดการณ์ชนิดงานบำรุงรักษาของคุณจะใช้ราคาต้นทุนล่าสุดอยู่เสมอ

1. เลือก **การจัดการสินทรัพย์** \> **ประจำงวด** \> **การคาดการณ์** \> **ปรับปรุงการคาดการณ์ชนิดงานบำรุงรักษา**
2. ในกล่องโต้ตอบ **ปรับปรุงการคาดการณ์ของชนิดงานบำรุงรักษา** บนแท็บด่วน **เรกคอร์ดที่จะรวม** คุณสามารถเพิ่มการเลือกสำหรับชนิดงานการบำรุงรักษาเฉพาะได้ตามที่คุณต้องการ เลือก **ตัวกรอง** แล้วจากนั้น เลือก **เลือก** เพื่อทำการเลือก
3. บนแท็บด่วน **ทำงานในแบบเบื้องหลัง** คุณสามารถตั้งค่าการปรับปรุงอัตโนมัติเป็นชุดงานได้ตามที่คุณต้องการ
4. เลือก **ตกลง** เพื่อเริ่มต้นการปรับปรุงการคาดการณ์


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]