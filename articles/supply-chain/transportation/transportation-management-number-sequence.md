---
title: ลำดับหมายเลขการจัดการการขนส่ง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าลำดับหมายเลขสำหรับการจัดการการขนส่ง
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2c3f087ac76412cd2dce93dcb31b796ce2cb3bc4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/29/2020
ms.locfileid: "4438947"
---
# <a name="transportation-management-number-sequence"></a>ลำดับหมายเลขการจัดการการขนส่ง

[!include [banner](../includes/banner.md)]

ใช้หน้า **ลำดับหมายเลข** ในโมดูลการจัดการการขนส่งเพื่อตั้งค่าตัวเลขที่หลากหลาย หมายเลข Pro ใช้โดยผู้ขนส่งเพื่อจัดระเบียบและติดตามความคืบหน้าของการจัดส่งสินค้าแต่ละครั้ง

## <a name="create-a-number-sequence-for-a-pro-number"></a>การสร้างลำดับหมายเลขสำหรับหมายเลข Pro

เมื่อต้องการสร้างลำดับหมายเลขสำหรับหมายเลข Pro ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง \> ลำดับหมายเลข**
1. เลือก **สร้าง** เพื่อสร้างลำดับหมายเลขใหม่
1. ป้อนรหัสเฉพาะและชื่อช่วยอธิบายสำหรับลำดับหมายเลข
1. ในฟิลด์ **ชนิดลำดับหมายเลข** *หมายเลข Pro* เป็นตัวเลือกเดียว
1. ในฟิลด์ **ตัวเลขการตรวจสอบ** *ตัวเลขการตรวจสอบ* มีเพียงตัวเลือกเดียวและตั้งค่าเป็นกลไกจัดการทั่วไป
1. บนแท็บด่วน **ลำดับ** ให้ข้อมูลเกี่ยวกับลำดับ
1. ปิดหน้า

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a>การเชื่อมโยงลำดับหมายเลขกับผู้ขนส่ง

เมื่อต้องการเชื่อมโยงลำดับหมายเลขกับผู้ขนส่ง ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง \> ผู้ขนส่งสินค้า**
1. เลือกผู้ขนส่งสินค้า
1. เลือก **แก้ไข**
1. บนแท็บด่วน **ภาพรวม** ให้เลือกตัวเลือกในฟิลด์ **ลำดับหมายเลข Pro**
1. ปิดหน้า


[!INCLUDE[footer-include](../../includes/footer-banner.md)]