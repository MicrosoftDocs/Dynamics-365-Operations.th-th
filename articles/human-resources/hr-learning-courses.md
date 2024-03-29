---
title: ตั้งค่าหลักสูตรการฝึกอบรม
description: ผู้ดูแลระบบทรัพยากรบุคคลและผู้จัดการสามารถใช้ลักษณะการทำงานของหลักสูตรในการรักษาข้อมูลเกี่ยวกับการฝึกอบรมที่ให้แก่ผู้ปฏิบัติงาน
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 45466b8f52ddc261737da7474767c21f5bd331f8
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689900"
---
# <a name="set-up-training-courses"></a>ตั้งค่าหลักสูตรการฝึกอบรม


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ผู้ดูแลระบบทรัพยากรบุคคลและผู้จัดการสามารถใช้ลักษณะการทำงานของหลักสูตรในการรักษาข้อมูลเกี่ยวกับการฝึกอบรมที่ให้แก่ผู้ปฏิบัติงาน

##  <a name="set-up-prerequisites"></a> ตั้งค่าข้อกำหนดเบื้องต้น

ข้อมูลต่อไปนี้จำเป็นและต้องตั้งค่าก่อนที่คุณจะสร้างหลักสูตร
-   **ชนิดของหลักสูตร**

ข้อมูลต่อไปนี้คือข้อมูลตัวเลือกที่คุณสามารถระบุสำหรับหลักสูตร หากคุณทราบว่าคุณจะป้อนข้อมูลนี้สำหรับหลักสูตร คุณควรตั้งค่าข้อมูลนี้ก่อนที่คุณจะสร้างเรกคอร์ดหลักสูตร
-   **กลุ่มห้องเรียน**
-   **กลุ่มหลักสูตร**
-   **สถานที่จัดหลักสูตร**
-   **ห้องเรียน**
-   **ผู้สอน**

## <a name="course-types"></a>ชนิดของหลักสูตร
คุณสามารถใช้ชนิดของหลักสูตรในการจัดประเภทหลักสูตรตามโครงสร้างหรือเนื้อหาของหลักสูตร คุณสามารถสร้างชนิดของหลักสูตรใน **หน้าชนิดของหลักสูตร** คุณต้องเลือกชนิดของหลักสูตรเมื่อคุณสร้างเรกคอร์ดหลักสูตร

## <a name="course-setup-type"></a>ตั้งค่าชนิดของหลักสูตร
ตารางต่อไปนี้แสดงรายการสามชนิดการตั้งค่าสำหรับหลักสูตร ชนิดการตั้งค่ากำหนดโครงสร้างของหลักสูตร

<table>
<thead>
<tr class="header">
<th>ชนิดการตั้งค่า</th>
<th>คำอธิบาย</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>มาตรฐาน</strong></td>
<td>เลือกชนิดนี้สำหรับหลักสูตรที่จะไม่มีการประชุมประจำวัน นี่คือชนิดการตั้งค่าเริ่มต้นเมื่อคุณสร้างหลักสูตรใหม่</td>
</tr>
<tr class="even">
<td><strong>วาระการประชุม</strong></td>
<td>เลือกชนิดนี้เพื่อวางแผนรายละเอียดของแต่ละวันของหลักสูตรที่เกิดขึ้นในช่วงหลายวัน</td>
</tr>
<tr class="odd">
<td><strong>วาระการประชุม+รอบเวลา</strong></td>
<td>เลือกชนิดนี้สำหรับหลักสูตรที่ซับซ้อนมากขึ้น ตัวอย่างเช่น คุณสามารถแบ่งวาระการประชุมสำหรับหลักสูตรเป็นแทร็คและรอบเวลา
<ul>
<li><strong>แทร็ค</strong> – แทร็คคือพื้นที่ชื่อเรื่องที่เฉพาะเจาะจงสำหรับหลักสูตร</li>
<li><strong>รอบเวลา</strong> – รอบเวลาแบ่งแทร็คและช่วยระบุกระบวนการเฉพาะหรือเทคนิคที่เกี่ยวข้องกับแทร็ค</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>งานหลักสูตร
สำหรับแต่ละหลักสูตร คุณสามารถทำงานต่อไปนี้
- ลงทะเบียนผู้เรียน
- ระบุกำหนดเวลาสิ้นสุดของการลงทะเบียน
- กำหนดจำนวนต่ำสุดและสูงสุดของผู้เรียน
- กำหนดสถานที่จัดหลักสูตรและห้องเรียน
- แนะนำโรงแรมให้ผู้เข้าร่วมหลักสูตร
- สร้างคำอธิบายหลักสูตร ซึ่งคุณสามารถโฆษณาบน **การบริการตนเองของพนักงาน**

  >**หมายเหตุ** คุณสามารถลบหลักสูตรเมื่อไม่มีใครลงทะเบียนเท่านั้น 

## <a name="course-statuses"></a>สถานะของหลักสูตร
ตารางต่อไปนี้แสดงสถานะหลักสูตรเป็นไปได้และการดำเนินการที่คุณสามารถทำได้เมื่อหลักสูตรที่มีสถานะเฉพาะ

<table>
<thead>
<tr class="header">
<th>สถานะ</th>
<th>การดำเนินการ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ที่สร้าง</strong></td>
<td><ul>
<li>ป้อนและแก้ไขข้อมูลหลักสูตร</li>
<li>เปลี่ยนสถานะหลักสูตรเป็น <strong>เปิด</strong> เพื่อให้ผู้ปฏิบัติงานสามารถลงทะเบียนสำหรับหลักสูตร</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>เปิด</strong></td>
<td><ul>
<li>ลงทะเบียนผู้เข้าร่วมสำหรับหลักสูตร</li>
<li>ลบผู้เข้าร่วมออกจากหลักสูตร</li>
<li>ยืนยันผู้เข้าร่วมสำหรับหลักสูตร</li>
<li>เปลี่ยนสถานะหลักสูตรเป็น<strong> ปิด</strong> หรือ <strong>ยกเลิกแล้ว</strong></li>
<li>วางแผนแบบสอบถามสำหรับผู้เรียนที่มีสถานะเป็น <strong>ยืนยันแล้ว</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ปิดแล้ว</strong></td>
<td>คุณสามารถเปิดหลักสูตรอีกครั้ง</td>
</tr>
<tr class="even">
<td><strong>ยกเลิกแล้ว</strong></td>
<td>คุณสามารถเปิดหลักสูตรอีกครั้ง</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>ผู้เข้าร่วมหลักสูตร
ผู้เข้าร่วมหลักสูตรคือ ผู้ปฏิบัติงานที่มีส่วนร่วมในหลักสูตรการฝึกอบรมหรือเหตุการณ์ คุณสามารถลงทะเบียนผู้เรียนสำหรับหลักสูตรที่เปิดเท่านั้น จำนวนผู้เรียนต่ำสุดและสูงสุดที่คุณสามารถลงทะเบียนได้สำหรับหลักสูตรที่มีการกำหนดไว้บนแท็บด่วน **ทั่วไป** บนหน้า **หลักสูตร**

## <a name="workflow"></a>ลำดับงาน

พนักงานที่ลงทะเบียนสำหรับหลักสูตรโดยผ่านหน้า **การบริการตนเองของพนักงาน** สามารถมีเส้นทางการลงทะเบียนผ่านลำดับงานเพื่ออนุมัติ คุณสามารถกำหนดลำดับงานให้กับหลักสูตรใน FastTab **ทั่วไป** บนหน้า **หลักสูตร**







[!INCLUDE[footer-include](../includes/footer-banner.md)]
