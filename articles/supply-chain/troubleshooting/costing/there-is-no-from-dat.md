---
title: ไม่มีค่าวันที่เริ่มต้นบนแท็บราคาที่ใช้งานอยู่ของหน้าราคาสินค้า
description: ไม่มีค่าวันที่เริ่มต้นบนแท็บราคาที่ใช้งานอยู่ของหน้าราคาสินค้า
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dc0071bc508fc1b2fcfa5071f0756434641b7e6f872308ed4febb0cb34d37840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730141"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>ไม่มีค่าวันที่เริ่มต้นบนแท็บราคาที่ใช้งานอยู่ของหน้าราคาสินค้า

หมายเลข KB: 4613548

## <a name="symptoms"></a>อาการ

ไม่มีค่า **วันที่เริ่มต้น** บนแท็บ **ราคาที่ใช้งานอยู่** ของหน้า **ราคาสินค้า**

## <a name="resolution"></a>ความละเอียด

ค่า **วันที่เริ่มต้น** (วันที่มีผลบังคับใช้) ที่ตั้งค่าบนราคาที่ค้างอยู่จะไม่โอนย้ายไปที่ราคาที่ใช้งานอยู่

เมื่อเรกคอร์ดต้นทุนสินค้าถูกป้อนเป็นครั้งแรก จะมีสถานะและวันที่มีผลบังคับใช้ *รอดำเนินการ* เมื่อคุณเรียกใช้งานเรกคอร์ดต้นทุนสินค้า จะมีการอัพเดตสถานะเป็น *ที่ใช้งานอยู่* และวันที่มีผลบังคับถูกอัพเดตเป็นวันที่เรียกใช้ วันที่เรียกใช้ของราคาที่ใช้งานอยู่จะเป็นวันที่จริงของการเรียกใช้งานเสมอ

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของรุ่นการคิดต้นทุน](../../cost-management/costing-versions.md)
