---
title: ปรับปรุงประสิทธิภาพการทำงานของโซลูชัน ER โดยการเพิ่มแหล่งข้อมูลฟิลด์ที่มีการคำนวณแบบพารามิเตอร์
description: บทความนี้จะอธิบายวิธีการที่คุณสามารถช่วยปรับปรุงประสิทธิภาพการทำงานของโซลูชันการรายงานทางอิเล็กทรอนิกส์ (ER) โดยการเพิ่มแหล่งข้อมูลฟิลด์ที่มีการคำนวณแบบพารามิเตอร์
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 34bb7c6256994f103c4da599157c06bd9d0795ef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288272"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>ปรับปรุงประสิทธิภาพการทำงานของโซลูชัน ER โดยการเพิ่มแหล่งข้อมูลฟิลด์ที่มีการคำนวณแบบพารามิเตอร์

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการที่คุณสามารถดำเนิน [การติดตามประสิทธิภาพ](trace-execution-er-troubleshoot-perf.md) ของรูปแบบ [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) ที่ทำงาน แล้วใช้ข้อมูลจากการติดตามเพื่อช่วยปรับปรุงประสิทธิภาพการทำงานได้ โดยการตั้งค่าคอนฟิกแหล่งข้อมูลของ **ฟิลด์ที่มีการคำนวณ** แบบพารามิเตอร์

ในฐานะที่เป็นส่วนหนึ่งของกระบวนการในการออกแบบการตั้งค่าคอนฟิก ER เพื่อสร้างเอกสารทางธุรกิจ คุณกำหนดวิธีการที่จะใช้ในการดึงข้อมูลออกจากแอปพลิเคชัน และป้อนข้อมูลในผลลัพธ์ที่สร้างขึ้น โดยการออกแบบแหล่งข้อมูล ER แบบพารามิเตอร์ของชนิด **ฟิลด์ที่มีการคำนวณ** คุณจะสามารถลดจำนวนการเรียกฐานข้อมูล และลดเวลาและต้นทุนที่เกี่ยวข้องในการรวบรวมรายละเอียดของการดำเนินการของรูปแบบ ER ได้อย่างมาก

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

- เมื่อต้องการดำเนินการตัวอย่างในบทความนี้ให้เสร็จสมบูรณ์ คุณต้องเข้าถึงหนึ่งใน [บทบาท](../sysadmin/tasks/assign-users-security-roles.md) ต่อไปนี้:

    - นักพัฒนาการรายงานทางอิเล็กทรอนิกส์
    - ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์
    - ผู้ดูแลระบบ

- บริษัทต้องตั้งค่าเป็น **DEMF**
- ทําตามขั้นตอนใน [ภาคผนวก 1](#appendix1) ของบทความนี้ เพื่อดาวน์โหลดส่วนประกอบของโซลูชัน Microsoft ER ตัวอย่างที่จําเป็นเพื่อทำตัวอย่างในบทความนี้ให้เสร็จสมบูรณ์
- ทำตามขั้นตอนใน [ภาคผนวก 2](#appendix2) ของบทความนี้ เพื่อตั้งค่าคอนฟิกชุดพารามิเตอร์ ER น้อยที่สุดที่จำเป็นสำหรับการใช้กรอบงาน ER เพื่อช่วยปรับปรุงประสิทธิภาพการทำงานของโซลูชัน Microsoft ER ตัวอย่าง

## <a name="import-the-sample-er-solution"></a>นำเข้าโซลูชัน ER ตัวอย่าง

สมมติว่าคุณต้องออกแบบโซลูชัน ER ใหม่เพื่อสร้างรายงานใหม่ที่แสดงธุรกรรมผู้จัดจำหน่าย ในปัจจุบัน คุณสามารถค้นหาธุรกรรมสำหรับผู้จัดจำหน่ายที่เลือกบนหน้า **ธุรกรรมผู้จัดจำหน่าย** (ไปยัง **บัญชีเจ้าหนี้** \> **ผู้จัดจำหน่าย** \> **ผู้จัดจำหน่ายทั้งหมด** ให้เลือกผู้จัดจำหน่าย และจากนั้น ในบานหน้าต่างการดำเนินการ บนแท็บ **ผู้จัดจำหน่าย** ในกลุ่ม **ธุรกรรม** ให้เลือก **ธุรกรรม**) อย่างไรก็ตาม คุณต้องการให้มีธุรกรรมผู้จัดจำหน่ายทั้งหมดพร้อมกันในเอกสารอิเล็กทรอนิกส์หนึ่งรายการในรูปแบบ XML โซลูชันนี้จะประกอบด้วยการตั้งค่าคอนฟิก ER ต่างๆ ที่มีรูปแบบข้อมูลที่จำเป็นต้องใช้ การแม็ปแบบจำลอง และส่วนประกอบรูปแบบ

ขั้นตอนแรกคือนำเข้าโซลูชัน ER ตัวอย่างเพื่อสร้างรายงานธุรกรรมผู้จัดจำหน่าย

1. ลงชื่อเข้าใช้อินสแตนซ์ของ Microsoft Dynamics 365 Finance ที่ได้เตรียมใช้งานสำหรับบริษัทของคุณ
2. ในบทความนี้ คุณจะสร้างและปรับเปลี่ยนการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง **Litware, Inc.** ตรวจสอบให้แน่ใจว่าได้เพิ่มตัวให้บริการการตั้งค่าคอนฟิกนี้ลงในอินสแตนซ์ Finance และทำเครื่องหมายเป็นใช้งานอยู่ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)
3. ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**
4. ในหน้า **การตั้งค่าคอนฟิก** นำเข้าการตั้งค่าคอนฟิก ER ที่คุณดาวน์โหลดเป็นข้อกำหนดเบื้องต้นลงใน Finance ตามลำดับต่อไปนี้: รูปแบบข้อมูล การแม็ปแบบจำลอง รูปแบบ สำหรับการตั้งค่าคอนฟิกแต่ละรายการ ทำตามขั้นตอนเหล่านี้:

    1. ในบานหน้าต่างการดำเนินการ เลือก **แลกเปลี่ยน** \> **โหลดจากไฟล์ XML**
    2. เลือก **เรียกดู** และเลือกไฟล์ที่เหมาะสมสำหรับการตั้งค่าคอนฟิก ER ในรูปแบบ XML
    3. เลือก **ตกลง**

![การตั้งค่าคอนฟิกที่นำเข้าบนหน้าการตั้งค่าคอนฟิก](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>ตรวจทานโซลูชัน ER ตัวอย่าง

### <a name="review-the-model-mapping"></a>ตรวจทานการแม็ปแบบจำลอง

1. บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **รูปแบบการปรับปรุงประสิทธิภาพ** จากนั้นเลือก **การแม็ปการปรับปรุงประสิทธิภาพ**
2. บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**
3. บนหน้า **การแม็ปแบบจำลองกับแหล่งข้อมูล** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**

    การแม็ปแบบจำลอง ER นี้ ได้รับการออกแบบมาให้ทำสิ่งต่อไปนี้:

    - ดึงข้อมูลรายการธุรกรรมของผู้จัดจำหน่ายที่จัดเก็บอยู่ในตาราง VendTrans (แหล่งข้อมูล **Trans**)
    - สำหรับธุรกรรมทั้งหมด ให้ดึงข้อมูลมาจากตาราง VendTable, เรกคอร์ดของผู้จัดจำหน่ายที่มีการลงรายการบัญชีธุรกรรมสำหรับ (แหล่งข้อมูล **\#Vend**)

    > [!NOTE]
    > แหล่งข้อมูล **\#Vend** ถูกตั้งค่าคอนฟิกเพื่อดึงข้อมูลเรกคอร์ดผู้จัดจำหน่ายที่สอดคล้องกันโดยใช้ความสัมพันธ์แบบกลุ่มต่อหนึ่งที่มีอยู่ **\@.'\>Relations'.VendTable\_AccountNum**

    การแม็ปแบบจำลองในการตั้งค่าคอนฟิกนี้จะใช้รูปแบบข้อมูลพื้นฐาน สำหรับรูปแบบ ER ใดๆ ที่สร้างขึ้นสำหรับรูปแบบนี้และเรียกใช้ใน Finance ดังนั้นจึงมีการเปิดเผยเนื้อหาของแหล่งข้อมูล **Trans** สำหรับรูปแบบ ER เช่น แหล่งข้อมูล **รูปแบบ**

    ![แหล่งข้อมูล Trans ในหน้าตัวออกแบบการแม็ปแบบจำลอง](media/er-calculated-field-ds-performance-mapping-1.png)

4. ปิดหน้า **ตัวออกแบบการแม็ปรูปแบบ**
5. ปิดหน้า **การแม็ปแบบจำลองกับแหล่งข้อมูล**

### <a name="review-format"></a>ตรวจทานรูปแบบ

1. บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **รูปแบบการปรับปรุงประสิทธิภาพ** จากนั้นเลือก **รูปแบบการปรับปรุงประสิทธิภาพ**
2. บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**
3. ในหน้า **ตัวออกแบบรูปแบบ** ในแท็บ **การแม็ป** ให้เลือก **ขยาย/ยุบ**
4. ขยายรายการ **รูปแบบ** **ข้อมูล** และ **ธุรกรรม**

    รูปแบบ ER นี้ได้รับการออกแบบมาเพื่อสร้างรายงานธุรกรรมของผู้จัดจำหน่ายในรูปแบบ XML

    ![จัดรูปแบบแหล่งข้อมูลและการรวมขององค์ประกอบรูปแบบที่ตั้งค่าคอนฟิกบนหน้าตัวออกแบบรูปแบบ](media/er-calculated-field-ds-performance-format.png)

5. ปิดหน้า **ตัวออกแบบรูปแบบ**

## <a name="run-the-sample-er-solution-to-trace-execution"></a>เรียกใช้โซลูชัน ER ตัวอย่างเพื่อติดตามการดำเนินการ

สมมติว่าคุณได้ออกแบบโซลูชัน ER รุ่นแรกเสร็จเรียบร้อยแล้ว ขณะนี้คุณต้องการทดสอบโซลูชันในอินสแตนซ์ Finance ของคุณ และวิเคราะห์ประสิทธิภาพในการดำเนินงาน

### <a name="turn-on-the-er-performance-trace"></a>เปิดการติดตามประสิทธิภาพ ER

1. เลือกบริษัท **DEMF**
2. ทำตามขั้นตอนใน [เปิดการติดตามประสิทธิภาพของ ER](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) เพื่อสร้างการติดตามประสิทธิภาพในขณะที่มีการเรียกใช้รูปแบบ ER

    ![กล่องโต้ตอบพารามิเตอร์ผู้ใช้](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>รันรูปแบบ ER

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบการปรับปรุงประสิทธิภาพ**
3. บนบานหน้าต่างการดำเนินการ เลือก **รัน**

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>ใช้การติดตามประสิทธิภาพเพื่อวิเคราะห์ประสิทธิภาพของการแม็ปแบบจำลอง

1. บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ปการปรับปรุงประสิทธิภาพ**
2. บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**
3. บนหน้า **การแม็ปแบบจำลอง** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**
4. บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** บนบานหน้าต่างการดำเนินการ ให้เลือก **การติดตามประสิทธิภาพ**
5. เลือกการติดตามล่าสุดที่สร้างขึ้น แล้วเลือก **ตกลง**

ข้อมูลใหม่จะกลายเป็นพร้อมใช้งานสำหรับรายการแหล่งข้อมูลบางอย่างของการแม็ปแบบจำลองปัจจุบัน:

- เวลาจริงที่ใช้ในการเรียกข้อมูลโดยใช้แหล่งข้อมูล
- เวลาเดียวกันที่แสดงเป็นเปอร์เซ็นต์ของเวลาทั้งหมดที่ใช้ในการรันการแม็ปแบบจำลองทั้งหมด

![รายละเอียดเวลาการดำเนินการบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-calculated-field-ds-performance-mapping-2.png)

ตาราง **สถิติประสิทธิภาพ** แสดงให้เห็นว่าแหล่งข้อมูล **Trans** เรียกตาราง VendTrans หนึ่งครั้ง ค่า **\[265\]\[Q:265\]** ของแหล่งข้อมูล **Trans** บ่งชี้ว่ามีการดึงข้อมูลธุรกรรมของผู้จัดจำหน่าย 265 รายการจากตารางของแอปพลิเคชันและส่งคืนเป็นรูปแบบข้อมูล

ตาราง **สถิติประสิทธิภาพ** ยังแสดงว่าการแม็ปแบบจำลองปัจจุบันทำซ้ำคำขอฐานข้อมูลในขณะที่มีการเรียกใช้แหล่งข้อมูล **\#Vend** การทำซ้ำนี้เกิดขึ้นเนื่องจากเหตุผลต่อไปนี้:

- ตารางผู้จัดจำหน่ายถูกเรียกสองครั้งสำหรับธุรกรรมผู้จัดจำหน่าย 265 รายการ สำหรับการเรียกทั้งหมด 530 รายการ:

    - ทำการเรียกหนึ่งครั้งเพื่อป้อนหมายเลขบัญชีของผู้จัดจำหน่าย
    - ทำการเรียกหนึ่งครั้งเพื่อป้อนชื่อผู้จัดจำหน่าย

- มีการเรียกตารางผู้จัดจำหน่ายสำหรับธุรกรรมผู้จัดจำหน่ายแต่ละราย ถึงแม้ว่าจะมีการลงรายการบัญชีธุรกรรมที่นำเข้าสำหรับผู้จัดจำหน่ายห้ารายเท่านั้น การเรียก 530 รายการ ซ้ำกัน 525 รายการ ภาพประกอบต่อไปนี้แสดงข้อความที่คุณได้รับเกี่ยวกับการเรียกที่ซ้ำ (การร้องขอฐานข้อมูล)

![ข้อความเกี่ยวกับการร้องขอฐานข้อมูลที่ซ้ำกันบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-calculated-field-ds-performance-mapping-2a.png)

เวลาที่ใช้ในการดำเนินการแม็ปแบบจำลองรวม (ประมาณแปดวินาที) โปรดสังเกตว่าเวลาที่ใช้ในการดึงข้อมูลจากตารางแอปพลิเคชัน VendTable มากกว่า 80 เปอร์เซ็นต์ (ประมาณหกวินาที) เปอร์เซ็นต์ดังกล่าวมากเกินกว่าสำหรับสองแอตทริบิวต์ของผู้จัดจำหน่ายห้าราย โดยเปรียบเทียบกับปริมาณของข้อมูลจากตารางแอปพลิเคชัน VendTrans

เมื่อต้องการลดจำนวนการเรียกที่จะทำเพื่อดูรายละเอียดผู้จัดจำหน่ายสำหรับแต่ละธุรกรรม และเพื่อปรับปรุงประสิทธิภาพการทำงานของการแม็ปแบบจำลอง คุณสามารถใช้การแคชสำหรับแหล่งข้อมูล **\#Vend**

> [!NOTE]
> แหล่งข้อมูล **Trans\\\#Vend** จะถูกแคชในขอบเขตของธุรกรรมปัจจุบันของแหล่งข้อมูล **Trans** ขณะรันไทม์

โดยการแคชแหล่งข้อมูล **\#Vend** คุณจะลดจำนวนครั้งของการเรียกที่ซ้ำจาก 525 เป็น 260 แต่คุณจะไม่สามารถขจัดการทำซ้ำได้อย่างสมบูรณ์ เมื่อต้องการตัดการทำซ้ำอย่างสมบูรณ์ คุณสามารถตั้งค่าคอนฟิกแหล่งข้อมูลแบบพารามิเตอร์ใหม่ของชนิด **ฟิลด์ที่มีการคำนวณ** ได้

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>ปรับปรุงการแม็ปแบบจำลองตามข้อมูลจากการติดตามการดำเนินการ

### <a name="change-the-logic-of-the-model-mapping"></a>เปลี่ยนตรรกะของการแม็ปแบบจำลอง

ทำตามขั้นตอนต่อไปนี้เพื่อใช้การแคชและแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ** เพื่อช่วยป้องกันการเรียกที่ซ้ำไปยังฐานข้อมูล

1. บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ปการปรับปรุงประสิทธิภาพ**
2. บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**
3. บนหน้า **การแม็ปแบบจำลอง** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**
4. บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** ให้ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มแหล่งข้อมูลของชนิด **เรกคอร์ดตาราง** เพื่อเข้าถึงเรกคอร์ดในตารางแอปพลิเคชัน VendTable:

    1. ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้ขยาย **Dynamics 365 for Operations** และเลือก **เรกคอร์ดตาราง**
    2. เลือก **เพิ่มราก**
    3. ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **Vend**
    4. ในฟิลด์ **ตาราง** ให้ป้อน **VendTable**
    5. เลือก **ตกลง**

5. คุณสามารถเรียกพารามิเตอร์เรียกไปยังแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ** เฉพาะเมื่อแหล่งข้อมูลเหล่านั้นอยู่ในคอนเทนเนอร์ ดังนั้น ให้ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มแหล่งข้อมูลชนิด **คอนเทนเนอร์เปล่า** เพื่อจัดเก็บแหล่งข้อมูลแบบพารามิเตอร์ใหม่ของชนิด **ฟิลด์ที่มีการคำนวณ**:

    1. ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้ขยาย **ทั่วไป** และเลือก **คอนเทอนเนอร์เปล่า**
    2. เลือก **เพิ่มราก**
    3. ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **Box**
    3. เลือก **ตกลง**

    ![แหล่งข้อมูล Box ในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-calculated-field-ds-performance-mapping-3.png)

6. ทำตามขั้นตอนต่อไปนี้เมื่อต้องการเพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ**:

    1. ในบานหน้าต่าง **แหล่งข้อมูล** ให้เลือก **Box**
    2. ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้ขยาย **ฟังก์ชัน** และเลือกรายการ **ฟิลด์ที่มีการคำนวณ**
    3. เลือก **เพิ่ม**
    4. ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **Vend**
    5. เลือก **แก้ไขสูตร**
    6. บนหน้า **ตัวออกแบบสูตร** ให้เลือก **พารามิเตอร์** เพื่อระบุพารามิเตอร์ที่ต้องระบุเมื่อมีการเรียกแหล่งข้อมูลนี้
    7. ในกล่องโต้ตอบ **พารามิเตอร์** ให้เลือก **สร้าง**
    8. ในฟิลด์ **ชื่อ** ให้ป้อน **parmVendAccNumber**
    9. ในฟิลด์ **ชนิด** เลือก **สตริง**
    10. เลือก **ตกลง**
    11. ในฟิลด์ **สูตร** ให้ป้อน **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**
    12. เลือก **บันทึก** และปิดหน้า **ตัวออกแบบสูตร**
    13. เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลใหม่

7. ทำตามขั้นตอนต่อไปนี้เพื่อทำเครื่องหมายแหล่งข้อมูลที่เพิ่มเป็นแคชในระหว่างการดำเนินการ:

    1. ในบานหน้าต่าง **แหล่งข้อมูล** ให้เลือก **Box\\Vend**
    2. เลือก **แคช**

    > [!NOTE]
    > แหล่งข้อมูล **Box\\Vend** จะถูกแคชในขอบเขตของธุรกรรมของผู้จัดจำหน่ายทั้งหมดของแหล่งข้อมูล **Trans** ขณะรันไทม์

8. ทำตามขั้นตอนต่อไปนี้เพื่ออัปเดตแหล่งข้อมูล **Trans\\\#Vend** ที่ซ้อนกันเพื่อให้สามารถใช้แหล่งข้อมูล **Box\\Vend** :

    1. ในบานหน้าต่าง **แหล่งข้อมูล** ให้ขยาย **Trans**
    2. เลือกแหล่งข้อมูล **Trans\\\#Vend** แล้วเลือก **แก้ไข** \> **แก้ไขสูตร**
    3. ในหน้า **ตัวออกแบบสูตร** ในฟิลด์ **สูตร** ให้ป้อน **Box.Vend(\@.AccountNum)**
    4. เลือก **บันทึก** แล้วปิดหน้า **ตัวออกแบบสูตร**
    5. เลือก **ตกลง** เพื่อทำการเปลี่ยนแปลงในแหล่งข้อมูลที่เลือกให้เสร็จสมบูรณ์

9. เลือก **บันทึก**

    ![แหล่งข้อมูล Vend ในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-calculated-field-ds-performance-mapping-4.png)

10. ปิดหน้า **ตัวออกแบบการแม็ปรูปแบบ**
11. ปิดหน้า **การแม็ปแบบจำลอง**

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ดำเนินการรุ่นที่แก้ไขของการแม็ปแบบจำลอง ER ให้เสร็จสมบูรณ์

1. บนหน้า **การตั้งค่าคอนฟิก** บนแท็บด่วน **รุ่น** ให้เลือกรุ่น **1.2** ของการตั้งค่าคอนฟิก **การแม็ปการปรับปรุงประสิทธิภาพ**
2. เลือก **เปลี่ยนสถานะ** \> **เสร็จสมบูรณ์** แล้วเลือก **ตกลง**

## <a name="run-the-modified-er-solution-to-trace-execution"></a>รันโซลูชัน ER ที่แก้ไขเพื่อติดตามการดำเนินการ

ทำซ้ำขั้นตอนในส่วน [รันรูปแบบ ER](#run-format) ก่อนหน้าในบทความนี้ เพื่อสร้างการติดตามประสิทธิภาพใหม่

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>ใช้การติดตามประสิทธิภาพเพื่อวิเคราะห์การปรับปรุงการแม็ปแบบจำลอง 

1. บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ปการปรับปรุงประสิทธิภาพ**
2. บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**
3. บนหน้า **การแม็ปแบบจำลอง** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**
4. บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** บนบานหน้าต่างการดำเนินการ ให้เลือก **การติดตามประสิทธิภาพ**
5. เลือกการติดตามล่าสุดที่สร้างขึ้น แล้วเลือก **ตกลง**

โปรดสังเกตว่าการปรับปรุงที่คุณทำไปยังการแม็ปแบบจำลอง มีการตัดการสอบถามที่ซ้ำกันไปยังฐานข้อมูล นอกจากนี้ ยังมีการลดจำนวนของการเรียกไปยังตารางฐานข้อมูลและแหล่งข้อมูลสำหรับการแม็ปแบบจำลองนี้ด้วย

![ข้อมูลสืบย้อนกลับในหน้าตัวออกแบบการแม็ปแบบจำลอง 1](./media/er-calculated-field-ds-performance-mapping-5.png)

เวลาที่ใช้ในการดำเนินการทั้งหมดลดลงประมาณ 20 เท่า (จากประมาณ 8 วินาทีเป็นประมาณ 400 มิลลิวินาที) ดังนั้น ประสิทธิภาพการทำงานของโซลูชัน ER ทั้งหมดได้รับการปรับปรุง

![ข้อมูลสืบย้อนกลับในหน้าตัวออกแบบการแม็ปแบบจำลอง 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>ภาคผนวก 1: ดาวน์โหลดส่วนประกอบของโซลูชัน Microsoft ER ตัวอย่าง

คุณต้องดาวน์โหลดและจัดเก็บไฟล์ต่อไปนี้ภายในเครื่อง

| ไฟล์                                        | ปริมาณความจุ |
|---------------------------------------------|---------|
| แบบจำลองการปรับปรุงประสิทธิภาพ.รุ่น.1     | [การตั้งค่าคอนฟิกรูปแบบข้อมูล ER ตัวอย่าง](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| การแม็ปการปรับปรุงประสิทธิภาพ.รุ่น.1.1 | [การตั้งค่าคอนฟิกการแม็ปรูปแบบ ER ตัวอย่าง](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| รูปแบบการปรับปรุงประสิทธิภาพ.รุ่น.1.1  | [การตั้งค่าคอนฟิกรูปแบบ ER ตัวอย่าง](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>ภาคผนวก 2: ตั้งค่าคอนฟิกกรอบงาน ER

ก่อนที่คุณจะสามารถเริ่มต้นการใช้กรอบงาน ER เพื่อปรับปรุงประสิทธิภาพการทำงานของโซลูชัน Microsoft ER ตัวอย่าง คุณต้องตั้งค่าคอนฟิกชุดพารามิเตอร์ ER ให้น้อยที่สุด

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ตั้งค่าคอนฟิกพารามิเตอร์ ER

1. ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**
2. บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**
3. ในหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์** บนแท็บ **ทั่วไป** ตั้งค่าตัวเลือก **เปิดใช้งานโหมดการออกแบบ** เป็น **ใช่**
4. บนแท็บ **เอกสารแนบ** ให้ตั้งค่าพารามิเตอร์ต่อไปนี้:

    - ในฟิลด์ **การตั้งค่าคอนฟิก** ให้เลือกชนิด **ไฟล์** สำหรับบริษัท **DEMF**
    - ในฟิลด์ **ที่เก็บงานถาวร** **ชั่วคราว** **พื้นฐาน** และ **อื่นๆ** ให้เลือกชนิด **ไฟล์**

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับพารามิเตอร์ ER ให้ดูที่ [ตั้งค่าคอนฟิกกรอบงาน ER](electronic-reporting-er-configure-parameters.md)

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER

มีการทำเครื่องหมายการตั้งค่าคอนฟิก ER ทั้งหมดที่มีการเพิ่มเป็นเจ้าของโดยผู้ให้บริการการตั้งค่าคอนฟิก ER ผู้ให้บริการการตั้งค่าคอนฟิก ER ที่เปิดใช้งานในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** จะใช้เพื่อวัตถุประสงค์นี้ ดังนั้นคุณต้องเรียกใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ก่อนที่คุณจะเริ่มต้นการเพิ่มหรือแก้ไขการตั้งค่าคอนฟิก ER

> [!NOTE]
> เฉพาะเจ้าของที่มีการตั้งค่าคอนฟิก ER เท่านั้นที่สามารถแก้ไขการตั้งค่าคอนฟิกได้ ดังนั้นก่อนที่จะแก้ไขการตั้งค่าคอนฟิก ER ต้องมีการเรียกใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ที่เหมาะสม

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ตรวจทานรายการของผู้ให้บริการการตั้งค่าคอนฟิก ER

1. ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**
2. บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **ผู้ให้บริการการตั้งค่าคอนฟิก**
3. บนหน้า **ตารางของผู้ให้บริการการตั้งค่าคอนฟิก** แต่ละเรกคอร์ดผู้ให้บริการจะมีชื่อและ URL ที่ไม่ซ้ำกัน ตรวจทานเนื้อหาของหน้านี้ ถ้ามีเรกคอร์ดสำหรับ **Litware, Inc.** อยู่แล้ว ให้ข้ามขั้นตอนถัดไป [เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่](#ActivateProvider)

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่

1. ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**
2. บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **ผู้ให้บริการการตั้งค่าคอนฟิก**
3. ในหน้า **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือก **ใหม่**
4. ในฟิลด์ **ชื่อ** ให้ป้อน **Litware, Inc.**
5. ในฟิลด์ **ที่อยู่อินเทอร์เน็ต** ให้ป้อน `https://www.litware.com`
6. เลือก **บันทึก**

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER

1. ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**
2. ในหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือกไทล์ **Litware, inc.** แล้วเลือก **กำหนดเป็นใช้งานอยู่**

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับผู้ให้บริการการตั้งค่าคอนฟิก ER ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)
- [ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพ](trace-execution-er-troubleshoot-perf.md)
- [สนับสนุนการเรียกแบบพารามิเตอร์ ของแหล่งข้อมูล ER ของชนิดฟิลด์ที่มีการคำนวณ](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
