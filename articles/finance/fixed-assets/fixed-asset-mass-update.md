---
title: การอัพเดตสินทรัพย์ถาวรโดยรวม
description: ถ้าคุณใช้สมุดบัญชี คุณสามารถเปลี่ยนแบบแผนการคิดค่าเสื่อมราคาสำหรับกลุ่มของสินทรัพย์ที่เป็นส่วนหนึ่งของสมุดบัญชีเดียวกัน
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ccccfd3168cf132453b41a74c57f4fd2629fb22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994901"
---
# <a name="fixed-asset-mass-update"></a>การอัพเดตสินทรัพย์ถาวรโดยรวม

[!include [banner](../includes/banner.md)]

ถ้าคุณใช้สมุดบัญชี คุณสามารถเปลี่ยนแบบแผนการคิดค่าเสื่อมราคาสำหรับกลุ่มของสินทรัพย์ที่เป็นส่วนหนึ่งของสมุดบัญชีเดียวกัน

ตัวอย่างเช่น ถ้าคุณอยู่ในสหรัฐอเมริกา และคุณใช้สินทรัพย์ของคุณมากกว่า 40 เปอร์เซ็นต์ในบริการในระหว่างไตรมาสสี่ของปี คุณต้องใช้แบบแผนการคิดค่าเสื่อมราคากลางไตรมาส คุณสามารถใช้กระบวนการสำหรับการอัพเดตโดยรวมเพื่อเปลี่ยนสินทรัพย์ทั้งหมดที่ต้องใช้แบบแผนการคิดค่าเสื่อมราคาใหม่ 

เมื่อคุณอัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ คุณลบธุรกรรมค่าเสื่อมราคาทั้งหมดที่มีอยู่สำหรับสินทรัพย์ดังกล่าว คุณยังจะลบธุรกรรมทั้งหมดสำหรับการปรับปรุงค่าเสื่อมราคา ธุรกรรมค่าเสื่อมราคาโบนัส และธุรกรรมค่าเสื่อมราคาพิเศษของสินทรัพย์เหล่านั้น 

ถ้าต้องการอัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ซึ่งตัดจำหน่ายแล้ว คุณต้องลบธุรกรรมการตัดจำหน่ายที่มีอยู่ออกก่อน คุณต้องลบธุรกรรมทั้งหมดที่สร้างขึ้นเนื่องจากกระบวนการตัดจำหน่ายออกด้วย 

หลังจากคุณอัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ คุณสามารถดำเนินการในส่วนของค่าเสื่อมราคาและค่าเสื่อมราคาพิเศษของสินทรัพย์แต่ละรายการได้ คุณยังสามารถทำการปรับปรุงค่าเสื่อมราคาด้วยตนเอง ถ้าจำเป็นต้องมีการปรับปรุงใด ๆ





