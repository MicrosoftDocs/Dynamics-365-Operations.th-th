---
title: สร้างผลิตภัณฑ์ใหม่
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างผลิตภัณฑ์ที่ใช้ร่วมกันใหม่
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d313d76d40476bec5c8bc9c8ea5fc93b217e7e87
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007577"
---
# <a name="create-a-new-product"></a>สร้างผลิตภัณฑ์ใหม่

[!include [banner](../../includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการสร้างผลิตภัณฑ์ที่ใช้ร่วมกันใหม่ ซึ่งมักจะถูกดำเนินการโดยผู้ออกแบบผลิตภัณฑ์  บริษัทข้อมูลสาธิตที่ใช้ในการสร้างงานนี้คือ USMF


## <a name="create-a-product"></a>สร้างผลิตภัณฑ์
1. ในบานหน้าต่างนำทาง ไปยัง **โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์**
2. เลือก **ใหม่**
3. ในฟิลด์ **หมายเลขผลิตภัณฑ์** ให้พิมพ์ค่า ถ้าลำดับหมายเลขไม่ได้ถูกตั้งค่าสำหรับหมายเลขผลิตภัณฑ์ ต้องมีการป้อนด้วยตนเอง  
4. ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้พิมพ์ค่า ชื่อผลิตภัณฑ์เป็นค่าเริ่มต้นที่ใช้เป็นชื่อค้นหา  คุณสามารถเปลี่ยนข้อมูลนี้ได้ถ้าจำเป็น  
5. เลือก **ตกลง**

## <a name="set-up-dimension-groups"></a>ตั้งค่ากลุ่มมิติ
1. เลือก **กลุ่มมิติ** เพื่อเปิดกล่องโต้ตอบการวาง
2. ในฟิลด์ **กลุ่มมิติการจัดเก็บ** ให้ป้อนหรือเลือกค่า กลุ่มมิติการจัดเก็บจะกำหนดว่า มิติการจัดเก็บใดที่คุณต้องป้อนในแต่ละธุรกรรมสำหรับผลิตภัณฑ์ และวิธีการติดตามในสินค้าคงคลัง  
3. ในฟิลด์ **กลุ่มมิติการติดตาม** ให้ป้อนหรือเลือกค่า กลุ่มมิติการติดตามจะกำหนดว่า มิติการติดตามใดที่คุณต้องป้อนสำหรับแต่ละธุรกรรมสำหรับผลิตภัณฑ์ และวิธีการจัดการในสินค้าคงคลัง  
4. เลือก **ตกลง**

