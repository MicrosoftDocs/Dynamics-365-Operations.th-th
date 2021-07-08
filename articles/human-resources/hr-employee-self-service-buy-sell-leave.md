---
title: ซื้อและขายวันลางาน
description: ใน Dynamics 365 Human Resources คุณสามารถส่งคำขอเพื่อซื้อและขายวันลาตามนโยบายการซื้อและการขายที่ตั้งค่าโดยบริษัทของคุณ
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271507"
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
