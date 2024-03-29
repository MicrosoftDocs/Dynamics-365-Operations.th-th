---
title: สามารถเช็คเอาท์สินค้าที่ไม่มีสินค้าคงคลังได้
description: บทความนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเหลือเมื่อลูกค้าสามารถเพิ่มสินค้าที่ไม่มีในสต็อกลงในรถเข็นแล้วเช็คเอาท์ต่อไป
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282746"
---
# <a name="items-without-inventory-can-be-checked-out"></a>สามารถเช็คเอาท์สินค้าที่ไม่มีสินค้าคงคลังได้

[!include [banner](../../includes/banner.md)]

บทความนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเหลือเมื่อลูกค้าสามารถเพิ่มสินค้าที่ไม่มีในสต็อกลงในรถเข็นแล้วเช็คเอาท์ต่อไป

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
