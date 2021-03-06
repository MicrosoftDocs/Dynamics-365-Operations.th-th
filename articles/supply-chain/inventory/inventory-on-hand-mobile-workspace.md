---
title: พื้นที่ทำงานการเคลื่อนคงเหลือของสินค้าคงคลัง
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานแบบเคลื่อนที่ของปริมาณคงคลังคงเหลือ พื้นที่ทำงานนี้ช่วยให้คุณได้รับข้อมูลเชิงลึกเคลื่อนที่ในสินค้าคงคลังที่จองไว้และพร้อมใช้งานได้ตลอดเวลา และที่ใดก็ได้
author: Mirzaab
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7d0440514369f8271004993d009ef7c3a36edb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008086"
---
# <a name="inventory-on-hand-mobile-workspace"></a>พื้นที่ทำงานการเคลื่อนคงเหลือของสินค้าคงคลัง

[!include [banner](../includes/banner.md)]

หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานแบบเคลื่อนที่ของ **ปริมาณคงคลังคงเหลือ** พื้นที่ทำงานนี้ช่วยให้คุณได้รับข้อมูลเชิงลึกในสินค้าคงคลังที่จองไว้และพร้อมใช้งานได้ตลอดเวลา และที่ใดก็ได้

พื้นที่ทำงานแบบเคลื่อนที่นี้มีจุดมุ่งหมายเพื่อใช้กับแอปสำหรับอุปกรณ์เคลื่อนที่ Finance and Operations

## <a name="overview"></a>ภาพรวม
โดยทั่วไป บริษัทจะมีการจัดส่งและการรับสินค้าคงคลังหลายครั้งทุกวัน ความเคลื่อนไหวเหล่านี้จะเปลี่ยนสถานะปริมาณคงคลังคงเหลืออย่างสม่ำเสมอ พื้นที่ทำงานแบบเคลื่อนที่ของ **ปริมาณคงคลังคงเหลือ** ช่วยให้คุณเห็นสถานะปริมาณคงคลังคงเหลือระหว่างบริษัท เพื่อที่คุณจะได้รับข้อมูลเชิงลึกล่าสุดในข้อมูลสินค้าคงคลังบนอุปกรณ์เคลื่อนที่ที่คุณเลือก โดยไม่คำนึงถึงว่าคุณทำงานในคลังสินค้า การซื้อ การขาย การผลิต หรือการจัดการ หรือมีบทบาทอื่น คุณสามารถเข้าถึงข้อมูลปริมาณคงคลังคงเหลือได้ทุกเมื่อใด และที่ใดก็ได้ 

พื้นที่ทำงานแบบเคลื่อนที่แสดงมุมมองฉับพลันของสถานะคงคลังคงเหลือของสิ่งอำนวยความสะดวกต่างๆ ซึ่งช่วยให้คุณสามารถดูปริมาณสินค้าคงคลังคงเหลือของสิ่งอำนวยความสะดวกต่างๆ การจองวัตถุดิบปัจจุบัน และปริมาณคงคลังคงเหลือที่ไม่ได้จอง นอกจากนี้คุณยังสามารถป้อนหมายเลขเพื่อสอบถามปริมาณคงคลังคงเหลือ และสามารถทำการค้นหาผลิตภัณฑ์คงคลังคงเหลือหรือตัวแปรที่ถูกกรองข้อมูล 

โดยเฉพาะอย่างยิ่ง พื้นที่ทำงานแบบเคลื่อนที่จะมีคุณลักษณะเหล่านี้:

-   คุณสามารถค้นหาตามหมายเลขผลิตภัณฑ์หรือชื่อผลิตภัณฑ์เพื่อค้นหาผลิตภัณฑ์เพื่อดูสถานะสำหรับปริมาณคงคลังคงเหลือ
-   สำหรับผลิตภัณฑ์ที่เลือก คุณสามารถดูข้อมูลต่อไปนี้:

    -   ปริมาณคงคลังคงเหลือต่อไซต์
    -   ปริมาณคงคลังคงเหลือต่อคลังสินค้า
    -   ปริมาณคงคลังคงเหลือต่อสถานที่
    -   ปริมาณคงคลังคงเหลือต่อชุดงาน (สำหรับผลิตภัณฑ์ที่มีการควบคุมชุดงาน)
    -   ปริมาณคงคลังคงเหลือต่อสถานะสินค้าคงคลัง
    
-   ปริมาณคงคลังคงเหลือของผลิตภัณฑ์จะแสดงอยู่ในวิธีการต่อไปนี้:

    -   ตามสินค้าคงคลังทางกายภาพ (มุมมองนี้แสดงยอดเงินรวม)
    -   ตามสินค้าคงคลังที่จองไว้ (มุมมองนี้แสดงยอดเงินที่จองไว้)
    -   ตามรายการที่มีอยู่จริง (มุมมองนี้แสดงถึงจำนวนที่ใช้ที่ไม่มีการจอง)

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น
ข้อกำหนดเบื้องต้นจะแตกต่าง โดยขึ้นอยู่กับรุ่นของ Supply Chain Management ที่นำไปใช้งานสำหรับองค์กรของคุณ

### <a name="prerequisites-if-you-use-supply-chain-management"></a>มีข้อกำหนดเบื้องต้นถ้าคุณใช้ Supply Chain Management
ถ้า Supply Chain Management ได้รับการปรับใช้สำหรับองค์กรของคุณ ผู้ดูแลระบบต้องเผยแพร่ **สินค้าคงคลังที่มีอยู่** พื้นที่ทำงานแบบเคลื่อนที่ สำหรับคำแนะนำ ให้ดูที่ [เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>ข้อกำหนดเบื้องต้น ถ้าคุณใช้แพลตฟอร์ม 3 หรือใหม่กว่า 
ถ้ามีการปรับใช้แพลตฟอร์ม 3 หรือใหม่กว่าสำหรับองค์กรของคุณ ผู้ดูแลระบบต้องดำเนินการตามข้อกำหนดเบื้องต้นต่อไปนี้ให้เสร็จสมบูรณ์ 

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
<td>การใช้ KB 4013633</td>
<td>ผู้ดูแลระบบ</td>

<td>KB 4013633 คือการอัพเดต X ++ หรือโปรแกรมแก้ไขด่วนแบบข้อมูลเมตาที่ประกอบด้วยพื้นที่ทำงานแบบเคลื่อนที่ของ <strong>ปริมาณคงคลังคงเหลือ</strong> เมื่อต้องการใช้ KB 4013633 ผู้ดูแลระบบต้องทำตามขั้นตอนเหล่านี้
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">ดาวน์โหลดโปรแกรมแก้ไขด่วนข้อมูลเมตาจาก Microsoft Dynamics Lifecycle Services (LCS)</a></li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">ติดตั้งโปรแกรมแก้ไขด่วนแบบข้อมูลเมตา</a></li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">สร้างแพคเกจที่สามารถปรับใช้ได้</a> ที่ประกอบด้วยแบบจำลอง <strong>SCMMobile</strong> แล้วอัพโหลดแพคเกจที่สามารถปรับใช้ได้กับ LCS</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">ใช้แพคเกจที่สามารถปรับใช้ได้</a></li>

</ol></td>
</tr>
<tr class="even">
<td>เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่ของ <strong>ปริมาณคงคลังคงเหลือ</strong></td>
<td>ผู้ดูแลระบบ</td>
<td>ดู <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่</a></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>ดาวน์โหลดและติดตั้งแอพบนมือถือ

ดาวน์โหลดและติดตั้งแอปบนมือถือ Finance and Operations:

-   [สำหรับโทรศัพท์ Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [สำหรับ iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>ล็อกอินเข้าสู่แอพบนมือถือ

1.  เริ่มการทำงานแอพบนอุปกรณ์เคลื่อนที่ของคุณ
2.  ป้อน URL ของ Dynamics 365
3.  ในครั้งแรกที่คุณเข้าสู่ระบบ ระบบจะขอให้คุณป้อนชื่อผู้ใช้และรหัสผ่านของคุณ ป้อนข้อมูลประจำตัวของคุณ
4.  หลังจากที่คุณลงชื่อเข้าใช้แล้ว พื้นที่ทำงานที่พร้อมใช้งานสำหรับบริษัทของคุณจะแสดงขึ้น หมายเหตุว่าถ้าผู้ดูแลระบบของคุณเผยแพร่พื้นที่ทำงานใหม่ในภายหลัง คุณจะต้องรีเฟรชรายการของพื้นที่ทำงานแบบเคลื่อนที่

    [![ดึงเพื่อรีเฟรช](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>ดูปริมาณคงคลังคงเหลือสำหรับผลิตภัณฑ์โดยใช้พื้นที่ทำงานแบบเคลื่อนที่ของปริมาณคงคลังคงเหลือ

1.  บนอุปกรณ์เคลื่อนที่ เลือกพื้นที่ทำงาน **ปริมาณคงคลังคงเหลือ**

2.  เลือก **ตรวจสอบปริมาณคงคลังคงเหลือสำหรับสินค้า** คุณเห็นรายการของผลิตภัณฑ์ที่ถูกโหลดลงในแอพของคุณสำหรับการใช้งานแบบออฟไลน์ โดยค่าเริ่มต้น จะมีการโหลดไว้ 50 รายการ แต่นักพัฒนาสามารถเปลี่ยนแปลงจำนวนนี้ได้ สำหรับข้อมูลเพิ่มเติม นักพัฒนาควรดูที่ [แพลตฟอร์มเคลื่อนที่](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)
3.  ถ้าสินค้าของคุณไม่ได้อยู่ในรายการ เลือก **ค้นหาข้อมูลเพิ่มเติม** ค้นหาโดยใช้หมายเลขผลิตภัณฑ์ หรือสลับไปยังการค้นหาตามชื่อผลิตภัณฑ์

4.  เลือกผลิตภัณฑ์ >  ถ้าสินค้ามีรูปภาพ รูปภาพจะแสดงขึ้น
5.  เลือกหนึ่งในตัวเลือกต่อไปนี้เพื่อดูสถานะของปริมาณคงคลังคงเหลือ:

    -   ดูปริมาณคงคลังคงเหลือต่อไซต์
    -   ดูปริมาณคงคลังคงเหลือต่อคลังสินค้า
    -   ดูปริมาณคงคลังคงเหลือต่อสถานที่
    -   ดูปริมาณคงคลังคงเหลือต่อชุดงาน (สำหรับผลิตภัณฑ์ที่มีการควบคุมชุดงาน)
    -   ดูปริมาณคงคลังคงเหลือต่อสถานะสินค้าคงคลัง

    ปริมาณคงคลังคงเหลือของผลิตภัณฑ์จะแสดงอยู่ในวิธีการต่อไปนี้:
    -   ตามสินค้าคงคลังทางกายภาพ (มุมมองนี้แสดงยอดเงินรวม)
    -   ตามสินค้าคงคลังที่จองไว้ (มุมมองนี้แสดงยอดเงินที่จองไว้)
    -   ตามรายการที่มีอยู่จริง (มุมมองนี้แสดงถึงจำนวนที่ใช้ที่ไม่มีการจอง)
