---
title: ตั้งค่าข้อจำกัดในการขนส่งสำหรับสินค้า
description: กระบวนงานนี้จะตั้งค่าข้อจำกัดในการขนส่ง เพื่อป้องกันสินค่าที่เลือกจากการถูกขนส่งแล้วไปยังฮับที่เลือก
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ccd7d79fbcdd600f78dbff98ce39c04865afe37
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146157"
---
# <a name="set-up-transportation-constraints-for-an-item"></a>ตั้งค่าข้อจำกัดในการขนส่งสำหรับสินค้า

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้จะตั้งค่าข้อจำกัดในการขนส่ง เพื่อป้องกันสินค่าที่เลือกจากการถูกขนส่งแล้วไปยังฮับที่เลือก โดยทั่วไปงานนี้จะดำเนินการโดยผู้ประสานงานขนส่ง คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง 


## <a name="create-an-item-constaint"></a>สร้างข้อจำกัดสินค้า
1. ไปที่ข้อจำกัด
2. คลิก สร้าง
3. ในฟิลด์ข้อจำกัดสินค้า ให้พิมพ์ค่า
4. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
5. ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
6. ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
7. ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า
8. ในฟิลด์ฮับ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
9. ในฟิลด์การดำเนินการข้อจำกัด ให้เลือกหนึ่งตัวเลือก
10. คลิก บันทึก
11. ปิดหน้า

