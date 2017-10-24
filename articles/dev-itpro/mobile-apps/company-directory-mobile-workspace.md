---
title: "พื้นที่ทำงานไดเรกทอรีของบริษัทแบบเคลื่อนที่"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานไดเรกทอรีของบริษัทแบบเคลื่อนที่ ซึ่งช่วยให้ผู้ใช้ดูและติดต่อกับพนักงานคนอื่นๆ ในองค์กร"
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Talent, Operations, UnifiedOperations
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 6a08be4608d131967eec00fc0d6d0e606a2f9f53
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="company-directory-mobile-workspace"></a>พื้นที่ทำงานไดเรกทอรีของบริษัทแบบเคลื่อนที่

[!include[banner](../includes/banner.md)]

หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานแบบเคลื่อนที่ของ **ไดเรกทอรีบริษัท** พื้นที่ทำงานนี้ช่วยให้ผู้ใช้ดูและติดต่อพนักงานคนอื่นในองค์กร

สามารถใช้พื้นที่ทำงานนี้กับแอพบนมือถือ Microsoft Dynamics 365 for Unified Operations

## <a name="overview"></a>ภาพรวม
พื้นที่ทำงานบนมือถือ **ไดเรกทอรีบริษัท** ช่วยให้ผู้ใช้ทำงานเหล่านี้ได้:

- ดูรายการของพนักงานในองค์กร
- ค้นหาพนักงานในองค์กร
- ดูข้อมูลผู้ติดต่อสำหรับพนักงาน
- ติดต่อพนักงานจากข้อมูลโพรไฟล์

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น
ก่อนที่คุณจะสามารถใช้พื้นที่ทำงานนี้ ต้องเป็นไปตามข้อกำหนดเบื้องต้นต่อไปนี้

<table>
<thead>
<tr class="header">
<th>ข้อกำหนดเบื้องต้น</th>
<th>บทบาท</th>
<th>คำอธิบาย</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>จะต้องนำผลิตภัณฑ์ต่อไปนี้อย่างใดอย่างหนึ่งไปใช้ในองค์กรของคุณ:
<ul><li>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017)</li>
<li>Microsoft Dynamics 365 for Talent</li>
</ul>
</td>
<td>ผู้ดูแลระบบ</td>
<td>ถ้าคุณไม่มี Finance and Operations ที่นำไปใช้ในองค์กรของคุณ ดู <a href="../deployment/deploy-demo-environment.md">ปรับใช้สภาพแวดล้อมสาธิต</a> ถ้าคุณยังไม่มี Talent ที่นำไปใช้ในองค์กรของคุณ ผู้ดูแลระบบสามารถเข้าถึงรุ่นทดลองใช้จาก <a href="https://www.microsoft.com/en-us/dynamics365/talent">เว็บเพจ Talent</a>.
</td>
</tr>
<tr class="even">
<td>ต้องมีการเผยแพร่พื้นที่ทำงานแบบเคลื่อนที่ของ <strong>ไดเรกทอรีบริษัท</strong></td>
<td>ผู้ดูแลระบบ</td>
<td>ดู <a href="publish-mobile-workspace.md">เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่</a></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>ดาวน์โหลดและติดตั้งแอพบนมือถือ
ดาวน์โหลดและติดตั้งแอพบนมือถือ Dynamics 365 for Unified Operations

-   [สำหรับโทรศัพท์ Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [สำหรับ iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>ล็อกอินเข้าสู่แอพบนมือถือ
1.  เริ่มการทำงานแอพบนอุปกรณ์เคลื่อนที่ของคุณ
2.  ป้อน URL ของ Microsoft Dynamics 365 ของคุณ
3.  ในครั้งแรกที่คุณเข้าสู่ระบบ ระบบจะขอให้คุณป้อนชื่อผู้ใช้และรหัสผ่านของคุณ ป้อนข้อมูลประจำตัวของคุณ
4.  หลังจากที่คุณลงชื่อเข้าใช้แล้ว พื้นที่ทำงานที่พร้อมใช้งานสำหรับบริษัทของคุณจะแสดงขึ้น หมายเหตุว่าถ้าผู้ดูแลระบบของคุณเผยแพร่พื้นที่ทำงานใหม่ในภายหลัง คุณจะต้องรีเฟรชรายการของพื้นที่ทำงานแบบเคลื่อนที่

[![ดึงเพื่อรีเฟรช](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a>ดูไดเรกทอรีของบริษัทโดยการใช้พื้นที่ทำงานแบบเคลื่อน
1.  ในแอพบนมือถือ เลือกพื้นที่ทำงาน **ไดเรกทอรี่ของบริษัท** แสดงรายชื่อของพนักงาน
3.  เลือกพนักงาน หน้า **โพรไฟล์พนักงาน** ปรากฏขึ้น ข้อมูลบนหน้านี้ประกอบด้วยชื่อ นามสกุล ตำแหน่ง และแผนกของพนักงาน

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a>ค้นหาไดเรกทอรีของบริษัทโดยการใช้พื้นที่ทำงานแบบเคลื่อน
1.  ในแอพบนมือถือ เลือกพื้นที่ทำงาน **ไดเรกทอรี่ของบริษัท**
2.  ในฟิลด์ **ค้นหา** ป้อนชื่อ นามสกุล ตำแหน่ง หรือแผนกของพนักงานเพื่อเริ่มต้นการค้นหา
3.  เลือกพนักงาน หน้า **โพรไฟล์พนักงาน** ปรากฏขึ้น ข้อมูลบนหน้านี้ประกอบด้วยชื่อ นามสกุล ตำแหน่ง และแผนกของพนักงาน

