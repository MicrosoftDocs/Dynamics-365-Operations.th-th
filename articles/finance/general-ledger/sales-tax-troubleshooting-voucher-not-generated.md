---
title: ไม่ได้สร้างใบสำคัญ
description: บทความนี้มีข้อมูลการแก้ไขปัญหาที่สามารถช่วยเมื่อควรสร้างใบสำคัญแต่ไม่ถูกสร้าง
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1200fe50bf9be4c6d1ca809ad9a86da2ff3e0ced
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909024"
---
# <a name="voucher-isnt-generated"></a>ใบสำคัญไม่ถูกสร้าง

[!include [banner](../includes/banner.md)]

ถ้าใบสำคัญควรจะสร้าง แต่หน้า **ธุรกรรมใบสำคัญ** ไม่แสดงใบสำคัญใด ๆ ให้ปฏิบัติตามขั้นตอนในส่วนต่อไปนี้ตามที่ต้องการเพื่อแก้ไขปัญหานี้

[![หน้าธุรกรรมใบสำคัญที่ไม่มีใบสำคัญ](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>ตรวจสอบการใช้งานภาษี

1. ไปที่ **ภาษี** \> **งานประจำงวด** \> **รายการสมุดรายวันของบัญชีแยกประเภทย่อยที่ยังไม่ได้โอนย้าย**
2. ถ้ามีเรกคอร์ดสมุดรายวัน ให้เลือกเรกคอร์ดนั้น แล้วเลือก **โอนย้ายทันที**

    [![ปุ่ม โอนย้ายทันที บนหน้ารายการสมุดรายวันของบัญชีแยกประเภทย่อยที่ยังไม่ได้โอนย้าย](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. เปิด **หน้าธุรกรรมใบสำคัญ** อีกครั้ง เพื่อดูว่ามีการสร้างใบสำคัญหรือไม่

## <a name="determine-whether-customization-exists"></a>ระบุว่ามีการเลือกเองอยู่หรือไม่

หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ไม่พบปัญหา ให้ระบุว่ามีการเลือกเองอยู่หรือไม่ ถ้าไม่มีการเลือกเองอยู่ ให้สร้างคำขอบริการของ Microsoft เพื่อขอความช่วยเหลือเพิ่มเติม

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
