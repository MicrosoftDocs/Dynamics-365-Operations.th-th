---
title: ตั้งค่าข้อจำกัดในการขนส่งสำหรับสินค้า
description: กระบวนงานนี้จะตั้งค่าข้อจำกัดในการขนส่ง เพื่อป้องกันสินค่าที่เลือกจากการถูกขนส่งแล้วไปยังฮับที่เลือก
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8eb9873f0ad6f404dc88d27ed5feedfc71fd62b5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201421"
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

