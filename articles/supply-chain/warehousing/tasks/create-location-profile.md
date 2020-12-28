---
title: สร้างโพรไฟล์สถานที่
description: หัวข้อนี้อธิบายวิธีการสร้างโพรไฟล์สถานที่ใน Dynamics 365 Supply Chain Management
author: ShylaThompson
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 320059184dc69c4fd34c4b50265ceb142d47a467
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438348"
---
# <a name="create-a-location-profile"></a>สร้างโพรไฟล์สถานที่

[!include [banner](../../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการสร้างโพรไฟล์สถานที่ใน Dynamics 365 Supply Chain Management สถานที่ทุกแห่งในคลังสินค้าจะต้องมีโพรไฟล์สถานที่เกี่ยวข้องกันซึ่งอธิบายคุณสมบัติของสถานที่ดังกล่าว ตัวอย่างเช่น สถานที่แห่งนั้นอนุญาตสำหรับสินค้าผสมหรือไม่  ในกระบวนงานนี้ เราจะสร้างโพรไฟล์สำหรับสถานที่ที่ไม่จำเป็นต้องควบคุมป้ายทะเบียน เราจะเปิดใช้งานสินค้าผสม และสถานะของสินค้าคงคลังผสม และอนุญาตการตรวจนับตามรอบ คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF 


1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > คลังสินค้า > โพรไฟล์สถานที่**
2. เลือก **ใหม่**
3. ในฟิลด์ **รหัสโพรไฟล์สถานที่** ให้พิมพ์ค่า
4. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง
5. ในฟิลด์ **รูปแบบสถานที่** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
6. ในฟิลด์ **ชนิดของสถานที่** ให้ป้อนหรือเลือกค่า
7. ในฟิลด์ **รหัสโพรไฟล์การจัดการท่าสินค้า** ให้ป้อนหรือเลือกค่า
8. เลือก **ใช่** ในฟิลด์ **อนุญาตสินค้าผสม**
9. เลือก **ใช่** ในฟิลด์ **อนุญาตสถานะสินค้าคงคลังแบบผสม**
10. เลือก **ใช่** ในฟิลด์ **อนุญาตการตรวจนับตามรอบ**
11. เลือก **บันทึก**

