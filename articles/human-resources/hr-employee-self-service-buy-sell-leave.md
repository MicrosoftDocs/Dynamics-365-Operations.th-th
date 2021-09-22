---
title: ซื้อและขายวันลางาน
description: หัวข้อนี้จะอธิบายวิธีการส่งคำขอซื้อและขายวันลางานใน Dynamics 365 Human Resources
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 716afdc4e52c3e4a0432b987cb82077012d4d0c2
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431521"
---
# <a name="buy-and-sell-leave"></a>ซื้อและขายวันลางาน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ใน Dynamics 365 Human Resources คุณสามารถส่งคำขอเพื่อซื้อและขายวันลาตามนโยบายการซื้อและการขายที่ตั้งค่าโดยบริษัทของคุณ  

## <a name="request-to-buy-leave"></a>คำขอเพื่อซื้อการลางาน

1. ในพื้นที่ทำงาน **การบริการตนเองของพนักงาน** ให้เลือก **คำขอเพื่อซื้อการลางาน** ในไทล์ **ยอดดุลเวลาหยุดพัก** 

2. เพิ่ม **ชนิดการลางาน** และป้อน **จำนวน** สำหรับจำนวนของการลางานที่คุณต้องการซื้อ 

3. เลือก **ส่ง** เมื่อคุณพร้อมที่จะส่งคำขอของคุณ 

ยอดคงเหลือของคุณจะอัพเดตโดยอัตโนมัติหรือดำเนินการผ่านกระบวนการอนุมัติก่อนที่จะอัพเดต การดำเนินการนี้จะขึ้นอยู่กับวิธีการตั้งค่าคอนฟิกนโยบายการซื้อ

## <a name="request-to-sell-leave"></a>คำขอในการขายวันลา

1. ในพื้นที่ทำงาน **การบริการตนเองของพนักงาน** ให้เลือก **คำขอขายวันลา** ในไทล์ **ยอดการลาหยุดคงเหลือ** 

2. เพิ่ม **ชนิดการลางาน** และป้อน **จำนวน** สำหรับจำนวนของวันลาที่คุณต้องการขาย 

3. เลือก **ส่ง** เมื่อคุณพร้อมที่จะส่งคำขอของคุณ

ยอดคงเหลือของคุณจะอัพเดตโดยอัตโนมัติหรือดำเนินการผ่านกระบวนการอนุมัติก่อนที่จะอัพเดต การดำเนินการนี้จะขึ้นอยู่กับวิธีการตั้งค่าคอนฟิกนโยบายการซื้อ


## <a name="troubleshooting"></a>การแก้ไขปัญหา 

ถ้าลำดับงานคำขอการซื้อและขายวันลางานล้มเหลว ผู้ใช้ที่มีสิทธิ์ **EssLeaveBuySellRequestApprover** สามารถตรวจทานบันทึกข้อความของคำขอการซื้อและขายทั้งหมด ถ้าต้องการดำเนินการนี้ ให้ไปที่ **การลางานและการหยุดงาน >ลิงค์ > คำขอการซื้อและขายวันลางาน > ล็อกข้อความ** (บนซ้าย) **ล็อกข้อความ** จะแสดงผู้ใช้เกี่ยวกับวิธีการประมวลผลธุรกรรมและประวัติลำดับงานที่เกี่ยวข้อง


## <a name="see-also"></a>ดูเพิ่มเติมที่

[ภาพรวมการลางานและการขาดงาน](hr-leave-and-absence-overview.md)</br>
[จัดการนโยบายซื้อและขายวันลางาน](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
