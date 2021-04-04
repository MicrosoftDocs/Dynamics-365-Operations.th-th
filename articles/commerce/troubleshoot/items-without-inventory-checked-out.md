---
title: สามารถเช็คเอาท์สินค้าที่ไม่มีสินค้าคงคลังได้
description: หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเหลือเมื่อลูกค้าสามารถเพิ่มสินค้าที่ไม่มีในสต็อกลงในรถเข็นแล้วเช็คเอาท์ต่อไป
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585553"
---
# <a name="items-without-inventory-can-be-checked-out"></a>สามารถเช็คเอาท์สินค้าที่ไม่มีสินค้าคงคลังได้

[!include [banner](../../includes/banner.md)]

หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเหลือเมื่อลูกค้าสามารถเพิ่มสินค้าที่ไม่มีในสต็อกลงในรถเข็นแล้วเช็คเอาท์ต่อไป

## <a name="description"></a>คำอธิบาย

ผู้ใช้สามารถเพิ่มสินค้าลงในรถเข็นได้ แม้ว่าจะไม่มีสินค้าคงคลังคงเหลือในร้านค้า แล้วดําเนินการต่อไปยังหน้าเช็คเอาท์

## <a name="resolution"></a>ความละเอียด

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>เปิดใช้งานคุณสมบัติแสดงข้อผิดพลาดสินค้าคงคลังในโปรแกรมสร้างไซต์ Commerce

เปิดใช้งานคุณสมบัติ **แสดงข้อผิดพลาดไม่มีสินค้าในสต็อก** ในโปรแกรมสร้างไซต์ Commerce ตามขั้นตอนดังต่อไปนี้

1. เลือกไซต์ที่คุณพยายามใช้
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **หน้า**
1. เลือก **CartPage** เพื่อเปิด
1. เลือกช่อง **รถเข็น 1** เลือก **แก้ไข** จากนั้นในบานหน้าต่างคุณสมบัติ ให้เลือกกล่องกาเครื่องหมาย **แสดงข้อผิดพลาดไม่มีสินค้าในสต็อก**
1. บันทึกและเผยแพร่หน้า

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ใช้การตั้งค่าสินค้าคงคลัง](../inventory-settings.md)

[คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก](../calculated-inventory-retail-channels.md)

[ตั้งค่าคอนฟิกสินค้าคงคลังสำรองและระดับสินค้าคงคลัง](../inventory-buffers-levels.md)
