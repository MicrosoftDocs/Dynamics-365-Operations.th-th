---
title: นโยบายการรวบรวมต้นทุนและการคำนวณค่าโสหุ้ย
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการกำหนดระดับความถูกต้องขององค์ประกอบต้นทุนรอง และสร้างกฎการรวบรวมต้นทุนที่พอดีกับการรายงานขององค์กรและความสามารถในการติดตามต้นทุน
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy, CAMOverheadRatePolicy
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f35bf3e900b8dd9c1864be8668f7ff7296924c4d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874622"
---
# <a name="cost-rollup-policy-and-overhead-calculation"></a>นโยบายการรวบรวมต้นทุนและการคำนวณค่าโสหุ้ย 

[!include [banner](../includes/banner.md)]

การบัญชีต้นทุนช่วยให้คุณได้รับข้อมูลเชิงลึกว่า กระแสต้นทุนเกี่ยวข้องกับผลิตภัณฑ์และบริการที่ถูกจัดส่งภายในองค์กรได้อย่างไร เมื่อต้องการดูความโปร่งใสของต้นทุน จำเป็นต้องดำเนินการปันส่วนต้นทุนระหว่างออบเจ็กต์ต้นทุนที่ขึ้นอยู่กับฐานการปันส่วนที่เหมาะสมให้สำเร็จ โดยค่าเริ่มต้น การปันส่วนต้นทุนได้บรรลุเป้าหมายสำหรับองค์ประกอบต้นทุนหลัก ที่ต้องการในบางสถานการณ์ แต่มีผลกระทบสองสามรายการที่ควรได้รับการพิจารณา

-   ออบเจ็กต์ต้นทุนเสริมจะสิ้นสุดด้วยยอดดุลเป็นศูนย์ สำหรับองค์ประกอบต้นทุนหลักหลังจากการคำนวณค่าโสหุ้ย
-   ปริมาตรของรายการต้นทุนที่สร้างขึ้นโดยการคำนวณค่าโสหุ้ยอาจสูงมาก
-   ไม่สามารถติดตามกระแสต้นทุนระหว่างออบเจ็กต์ต้นทุนได้

เพื่อหลีกเลี่ยงผลกระทบเหล่านี้ การบัญชีต้นทุนช่วยให้คุณสามารถตั้งค่าคอนฟิกการปันส่วนต้นทุนได้ เพื่อให้พอดีกับข้อกำหนดในการรายงานการจัดการองค์กรจัดของคุณ บทความนี้อธิบายวิธีที่คุณสามารถกำหนดระดับที่ถูกต้องขององค์ประกอบต้นทุนรอง และสร้างกฎการรวบรวมต้นทุนที่พอดีกับการรายงานขององค์กรและความสามารถในการติดตามต้นทุน

> [!NOTE]
> คุณสามารถเปลี่ยนการตั้งค่าคอนฟิกได้ ถ้าข้อกำหนดในรายงานเปลี่ยน

## <a name="example-of-cost-rollup-policy-setup"></a>ตัวอย่างของการตั้งค่านโยบายการรวบรวมต้นทุน

สมมติว่าองค์กรมีโครงสร้างต่อไปนี้ พร้อมกับศูนย์ต้นทุน 4 ศูนย์

![ตัวอย่างของโครงสร้างองค์กร](./media/dimension-hierarchy-org.png)

**มิติออบเจ็กต์ต้นทุน**

| ศูนย์ต้นทุน | คำอธิบาย          |
|--------------|-----------|
| CC001        | HR        |
| CC002        | การเงิน   |
| CC003        | ชิ้นส่วนประกอบ  |
| CC004        | บรรจุภัณฑ์ |

**มิติองค์ประกอบต้นทุน**

| องค์ประกอบต้นทุน | คำอธิบาย | ชนิดข้อมูล    |
|---------------|-------------|---------|
| 1001          | ไฟฟ้า | หลัก |
| 1002          | เงินเดือน    | หลัก |
| 1003          | การโฆษณา | หลัก |

ลำดับชั้นของมิติที่ตอบสนองข้อกำหนดในการรายงานขององค์กร สามารถถูกตั้งค่าได้ดังต่อไปนี้

**รายละเอียดลำดับชั้นมิติ**

| ชื่อลำดับชั้นมิติ | มิติ    | ชื่อชนิดลำดับชั้นมิติ      | ลำดับชั้นรายการการเข้าถึง |
|--------------------------|--------------|------------------------------------|-----------------------|
| องค์กร             | ศูนย์ต้นทุน | ลำดับชั้นการจัดประเภทมิติ | ไม่                    |

**ลำดับชั้นของมิติ**

|    &nbsp;    | ช่วงสมาชิกมิติ | &nbsp;              |
|--------------|-------------------------|---------------------|
| **โหนด**        | **สมาชิกมิติเริ่มต้น**   | **สมาชิกมิติสิ้นสุด** |
| องค์กร |                         |                     |
| &nbsp;&nbsp;ผู้ดูแลระบบ             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;การเงิน              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;ทรัพยากรบุคคล               | CC002                   | CC002               |
| &nbsp;&nbsp;การผลิต               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;บรรจุภัณฑ์              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;ชิ้นส่วนประกอบ             | CC004                   | CC004               |

ลำดับชั้นของมิติที่ตอบสนองความต้องการของนโยบาย สามารถถูกตั้งค่าได้ดังต่อไปนี้

**รายละเอียดลำดับชั้นมิติ**

| ชื่อลำดับชั้นมิติ | มิติ     | ชื่อชนิดลำดับชั้นมิติ      |
|--------------------------|---------------|------------------------------------|
| งบกำไรขาดทุน  | องค์ประกอบต้นทุน | ลำดับชั้นการจัดประเภทมิติ |

**ลำดับชั้นของมิติ**

|      &nbsp;             | ช่วงสมาชิกมิติ |      &nbsp;         |
|-------------------------|-------------------------|---------------------|
| โหนด                   | สมาชิกมิติเริ่มต้น   | สมาชิกมิติสิ้นสุด |
| งบกำไรขาดทุน |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;ต้นทุนหลัก                    | 10001                   | 10003               |

หลังจากที่มีการประมวลผลรายการบัญชีแยกประเภททั่วไป ยอดดุลรายการต้นทุนโดยออบเจ็กต์ต้นทุนมีลักษณะเช่นนี้

|      &nbsp;          | **ออบเจ็กต์ต้นทุน** | &nbsp;    |  &nbsp;   |  &nbsp;   | **ยอดรวม**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **องค์ประกอบต้นทุน**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 ไฟฟ้า** | 100,00          | 200,00    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 เงินเดือน**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 การโฆษณา** | 0,00            | 4.000,00  | 0,00      | 0,00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**มิติทางสถิติ**

| องค์ประกอบทางสถิติ |    คำอธิบาย   |
|----------------------|------------------|
| SE-1                 | บริการ HR      |
| SE-2                 | บริการการเงิน |

ออบเจ็กต์ต้นทุน CC001 HR จัดสรรบริการ HR ไปยังออบเจ็กต์ต้นทุนหลายรายการ

บริการ HR จะถูกใช้โดยการแจกจ่ายของขนาดต่อไปนี้

| ออบเจ็กต์ต้นทุน | คำอธิบาย |   บริการ HR |
|-------------|-------------|----|
| CC002       | การเงิน     | 35 |
| CC003       | ชิ้นส่วนประกอบ    | 55 |
| CC004       | บรรจุภัณฑ์   | 10 |

ออบเจ็กต์ต้นทุน CC002 การเงิน กำลังจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ

บริการการเงินจะถูกใช้โดยการแจกจ่ายของขนาดต่อไปนี้

| ออบเจ็กต์ต้นทุน |   คำอธิบาย    |  บริการการเงิน   |
|-------------|------------------|----|
| CC003       | ชิ้นส่วนประกอบ         | 65 |
| CC004       | บรรจุภัณฑ์        | 35 |

นโยบายการปันส่วนต้นทุนคุณสามารถถูกตั้งค่าได้ดังต่อไปนี้

| ชื่อนโยบาย | คำอธิบาย     | ลำดับชั้นมิติออบเจ็กต์ต้นทุน | มิติทางสถิติ | มิติองค์ประกอบต้นทุน |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | การปันส่วนต้นทุน | องค์กร                    | องค์ประกอบทางสถิติ  | องค์ประกอบต้นทุน          |

กฎการปันส่วนต้นทุนคุณสามารถถูกตั้งค่าได้ดังต่อไปนี้

| โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน | พฤติกรรมต้นทุน | ฐานของการปันส่วน        |
|--------------------------------------|---------------|------------------------|
| CC001                                | ผลรวม         | **บริการ HR**        |
| CC002                                | ผลรวม         | **บริการทางการเงิน** |

## <a name="brhow-cost-flows-between-cost-centers"></a><br>วิธีการที่ต้นทุนเคลื่อนย้ายระหว่างศูนย์ต้นทุน 

ถ้าคุณต้องการเรียนรู้วิธีการที่ต้นทุนเคลื่อนย้ายระหว่างศูนย์ต้นทุนในองค์กร คุณสามารถสร้างองค์ประกอบต้นทุนชนิด **รอง** สำหรับแต่ละศูนย์ต้นทุนได้ จากนั้น องค์ประกอบต้นทุนเหล่านี้จะถูกใช้ในการโอนย้ายยอดดุลระหว่างศูนย์ต้นทุน ในระหว่างการคำนวณค่าโสหุ้ย

สมาชิกมิติองค์ประกอบต้นทุนสามารถถูกตั้งค่าได้ดังต่อไปนี้

| องค์ประกอบต้นทุน | ชนิดข้อมูล          |     &nbsp;    |
|---------------|---------------|---------------|
| 1001          | ไฟฟ้า   | หลัก       |
| 1002          | เงินเดือน      | หลัก       |
| 1003          | การโฆษณา   | หลัก       |
| **SC-CC001**  | **HR**        | **รอง** |
| **SC-CC002**  | **การเงิน**   | **รอง** |
| **SC-CC003**  | **การประกอบ**  | **รอง** |
| **SC-CC004**  | **บรรจุภัณฑ์** | **รอง** |

ลำดับชั้นมิติ **งบกำไรขาดทุน** จำเป็นต้องมีการอัปเดตด้วยมิติสมาชิกใหม่ เพื่อให้ลำดับชั้นมิติประกอบด้วยข้อมูลถูกต้องที่สามารถใช้สำหรับการกำหนดนโยบายและการรายงาน

**รายละเอียดลำดับชั้นมิติ**

| ชื่อลำดับชั้นมิติ | มิติ     | ชื่อชนิดลำดับชั้นมิติ      |
|--------------------------|---------------|------------------------------------|
| งบกำไรขาดทุน  | องค์ประกอบต้นทุน | ลำดับชั้นการจัดประเภทมิติ |

**ลำดับชั้นของมิติ**

|      &nbsp;             | ช่วงสมาชิกมิติ |  &nbsp;             |
|-------------------------|-------------------------|---------------------|
| โหนด                   | สมาชิกมิติเริ่มต้น   | สมาชิกมิติสิ้นสุด |
| งบกำไรขาดทุน |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;ต้นทุนหลัก                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;ต้นทุนรอง                         | **SC-CC001**            | **SC-CC004**        |

สร้าง **นโยบายการรวบรวมต้นทุน** ที่มีการแมปศูนย์ต้นทุนแต่ละแห่งไปยังองค์ประกอบต้นทุนที่สอดคล้องกันของชนิด **รอง**

**นโยบายการรวบรวมต้นทุน**

| ชื่อนโยบาย | คำอธิบาย | ลำดับชั้นมิติออบเจ็กต์ต้นทุน | ลำดับชั้นมิติองค์ประกอบต้นทุน |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | กระแสต้นทุน   | องค์กร                    | งบกำไรขาดทุน          |

**กฎการรวบรวมต้นทุน**

| โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน | โหนดลำดับชั้นมิติองค์ประกอบต้นทุน | ต้นทุนองค์ประกอบรอง |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | งบกำไรขาดทุน               | **SC-CC001**           |
| CC002                                | งบกำไรขาดทุน               | **SC-CC002**           |
| CC003                                | งบกำไรขาดทุน               | **SC-CC003**           |
| CC004                                | งบกำไรขาดทุน               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>ทำการคำนวณค่าโสหุ้ย

**สมุดรายวัน**

| สมุดรายวัน | ชนิดสมุดรายวัน            | รอบระยะเวลาปฏิทินทางการเงิน | ปี | รอบระยะเวลา | เวอร์ชัน       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | สมุดรายวันการปันส่วนต้นทุน | ทางการเงิน                 | 2017    | รอบระยะเวลา 1 | การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1 |

ขณะนี้ระบบจะใช้ **นโยบายการรวบรวมต้นทุน** เมื่อสร้าง **รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน**

**รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน**

| วันที่ลงบัญชี | ออบเจ็กต์ต้นทุน | คำอธิบาย  | องค์ประกอบต้นทุน | คำอธิบาย |  จำนวนเงิน |
|-----------------|-------------|--------------|----------|-----------|-----------|
| วันที่ 31-01-2017      | CC001       | ทรัพยากรบุคคล           | SC-CC001 | ทรัพยากรบุคคล        | 10.100,00 |
| วันที่ 31-01-2017      | CC002       | การเงิน      | SC-CC002 | การเงิน   | 17.735,00 |
| วันที่ 31-01-2017      | CC003       | ชิ้นส่วนประกอบ     | SC-CC003 | ชิ้นส่วนประกอบ  | 31.082,75 |
| วันที่ 31-01-2017      | CC004       | บรรจุภัณฑ์    | SC-CC004 | บรรจุภัณฑ์ | 15.717,25 |

> [!NOTE]
> รายการสมุดรายวันถูกสร้างขึ้นตามกฎใน **นโยบายการรวบรวมต้นทุน** ถ้ามีนโยบายอยู่ ยอดดุลที่แสดงเป็นยอดดุลของการคำนวณค่าโสหุ้ย

หน้า **รายละเอียดรายการสมุดรายวันยอดดุลต้นทุนของออบเจ็กต์ต้นทุน** ที่สามารถเข้าถึงได้จากรายการสมุดรายวันที่แสดงวิธีการได้รับยอดดุล

**ตัวอย่าง: รายการสมุดรายวันสำหรับออบเจ็กต์ต้นทุน CC002 การเงิน**

**รายละเอียดรายการสมุดรายวันยอดดุลต้นทุนของออบเจ็กต์ต้นทุน**

| สมาชิกมิติองค์ประกอบต้นทุน | คำอธิบาย |  จำนวนเงิน   |
|-------------------------------|-------------|-----------|
| 1001                          | ไฟฟ้า | 200,00    |
| 1002                          | เงินเดือน    | 10.000,00 |
| 1003                          | การโฆษณา | 4.000,00  |
| SC-CC001                      | ทรัพยากรบุคคล          | 3.535,00  |

**รายการต้นทุนที่สร้างขึ้นโดยการคำนวณค่าโสหุ้ย**

| ออบเจ็กต์ต้นทุน | คำอธิบาย  | องค์ประกอบต้นทุน   | คำอธิบาย  |        จำนวนเงิน     |       วันที่ลงบัญชี     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | ทรัพยากรบุคคล           | SC-CC001 | ทรัพยากรบุคคล              | \-10.100,00 | วันที่ 31-01-2017 |
| CC002       | การเงิน      | SC-CC001 | ทรัพยากรบุคคล              | 3.535,00    | วันที่ 31-01-2017 |
| CC003       | ชิ้นส่วนประกอบ     | SC-CC001 | ทรัพยากรบุคคล              | 5.555,00    | วันที่ 31-01-2017 |
| CC004       | บรรจุภัณฑ์    | SC-CC001 | ทรัพยากรบุคคล              | 1.010,00    | วันที่ 31-01-2017 |
| CC002       | การเงิน      | SC-CC002 | การเงิน         | \-17.735,00 | วันที่ 31-01-2017 |
| CC003       | ชิ้นส่วนประกอบ     | SC-CC002 | การเงิน         | 11.527,75   | วันที่ 31-01-2017 |
| CC004       | บรรจุภัณฑ์    | SC-CC002 | การเงิน         | 6.207,25    | วันที่ 31-01-2017 |

หลังจาก **การคำนวณค่าโส่หุ้ย** เสร็จสิ้น คุณสามารถรายงานผลโดยใช้เครื่องมือ เช่น Microsoft SharePoint Workspace Excel หรือ Power BI

## <a name="view-reporting-in-excel"></a>ดูการรายงานใน Excel 

ลำดับชั้นของมิติอนุญาตให้คุณสามารถดูข้อมูลในระดับการรวมค่าที่แตกต่างกันได้

นี่เป็นตัวอย่างของการรายงาน Power Pivot ใน Excel

| **งบกำไรขาดทุน** | **ออบเจ็กต์ต้นทุน** |      &nbsp;    |   &nbsp;      |     &nbsp;    |  **ยอดรวม**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **ต้นทุนหลัก**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| &nbsp;&nbsp;&nbsp;&nbsp;1001                            | 100,00          | 200,00         | 6.000,00      | 2.000,00      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                             | 0,00            | 4.000,00       | 0,00          | 0,00          | **4.000,00**  |
|**ต้นทุนรอง**                            | **-10.100,00**  | **-14.200,00** | **17.082.75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | \-10.100,00     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0,00            | \-17.735,00    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
| **ยอดรวม**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

การใช้ **นโยบายการรวบรวมต้นทุน** และ **องค์ประกอบต้นทุนของชนิดรอง** ช่วยให้คุณสามารถปล่อยให้ต้นทุนหลักสำหรับแต่ละออบเจ็กต์ต้นทุนสำหรับการรายงานภายใน เป็นต้นทุนหลักที่คงเหลือหลังจาก **การคำนวณค่าโสหุ้ย**

ถ้ามีการดำเนินการตัวอย่างเดียวกันโดยไม่ได้สร้าง **นโยบายการรวบรวมต้นทุน** ผลลัพธ์ที่รายงานจะเป็นดังแสดงด้านล่าง ต้นทุนเคลื่อนย้ายได้อย่างถูกต้อง แต่สูญเสียความสามารถในการติดตามและความเข้าใจเชิงลึกเกี่ยวกับวิธีการที่ต้นทุนเคลื่อนย้ายระหว่างศูนย์ต้นทุน

| **งบกำไรขาดทุน** | **ออบเจ็กต์ต้นทุน** |   &nbsp;  |    &nbsp;     |  &nbsp;       |          **ยอดรวม**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **ต้นทุนหลัก**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1001                              | 0,00            | 0,00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                             | 0,00            | 0,00      | 22.275,00     | 12.225,00     | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                              | 0,00            | 0,00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**ต้นทุนรอง**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
| **ยอดรวม**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

โดยขึ้นกับข้อกำหนดในการรายงานและความสามารถในการติดตามในองค์กรของคุณ คุณสามารถกำหนดระดับที่ถูกต้องขององค์ประกอบต้นทุนรอง และสร้างกฎการรวบรวมต้นทุนที่พอดีกับความต้องการของคุณ

การแยกที่ชัดเจนระหว่าง **การปันส่วนต้นทุน** และ **นโยบายการรวบรวมต้นทุน** ให้ความยืดหยุ่นในการอัปเดตอย่างต่อเนื่อง โดยไม่มีผลกับผู้อื่น



## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม
-  [มิติออบเจ็กต์ต้นทุน](cost-objects.md)
-  [มิติองค์ประกอบต้นทุน](cost-elements.md)
-  [ลำดับชั้นของมิติ](dimension-hierarchy.md)
-  [การคำนวณค่าโสหุ้ย](overhead-calculation.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
