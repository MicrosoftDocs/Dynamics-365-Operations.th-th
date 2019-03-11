---
title: รหัสการโอนการครอบครองและรหัสเหตุผลการส่งคืน
description: สร้างและใช้รหัสเหตุผลการส่งคืนและรหัสการโอนการครอบครอง เพื่อสนับสนุนกระบวนการสำหรับการส่งคืนผลิตภัณฑ์
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e37bd328ebceacc8acf134c5fbb20e6d6a6428d5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "330298"
---
# <a name="disposition-codes-and-return-reason-codes"></a>รหัสการโอนการครอบครองและรหัสเหตุผลการส่งคืน 

[!include [banner](../includes/banner.md)]


สร้างและใช้รหัสเหตุผลการส่งคืนและรหัสการโอนการครอบครอง เพื่อสนับสนุนกระบวนการสำหรับการส่งคืนผลิตภัณฑ์

ใช้รหัสเหตุผลการส่งคืนใช้เพื่ออธิบายเหตุผลที่ลูกค้าต้องการส่งคืนสินค้า  คุณสามารถกำหนดรหัสเหตุผลในแบบฟอร์ม **สร้างใบสั่งส่งคืนสินค้า** ได้

กำหนดรหัสการโอนการครอบครองเมื่อรับสินค้า หรือในระหว่างการตรวจสอบทางกายภาพของสินค้าที่ส่งคืน  คุณสามารถใช้รหัสการโอนการครอบครองเพื่ออธิบายเงื่อนไขของสินค้า  คุณยังสามารถใช้รหัสการโอนการครอบครองเพื่อบ่งชี้ว่าการดำเนินการเพิ่มเติมจำเป็นสำหรับธุรกรรมหรือไม่  ตัวอย่างเช่น สร้างรหัสการโอนการครอบครองสำหรับการดำเนินการต่อไปนี้:

  - ทำสินค้าที่ส่งคืนเป็นของเสียและระบุสินค้าทดแทนให้กับลูกค้า

  - ส่งคืนสินค้าไปยังสินค้าคงคลัง และเครดิตลูกค้าสำหรับต้นทุนของสินค้า

  - ซ่อมสินค้าและส่งกลับให้ลูกค้า

## <a name="see-also"></a>ดูเพิ่มเติมที่

[การตั้งค่ารหัสเหตุผลการส่งคืน](set-up-return-reason-code.md)

[ตั้งค่ารหัสการโอนการครอบครอง](set-up-disposition-codes.md)




  


