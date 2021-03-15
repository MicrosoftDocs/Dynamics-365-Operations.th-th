---
title: เพิ่มช่องทางในลำดับชั้นขององค์กร
description: หัวข้อนี้จะอธิบายวิธีการเพิ่มลำดับชั้นช่องทางลำดับชั้นขององค์กรใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 297bd34f9bde23d5cc7de266b8e8f49b1a752662
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993713"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>เพิ่มช่องทางในลำดับชั้นขององค์กร


[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการเพิ่มลำดับชั้นช่องทางลำดับชั้นขององค์กรใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

ช่องทางต้องเชื่อมโยงกับลำดับชั้นขององค์กรหนึ่งลำดับชั้นขึ้นไป ก่อนที่จะสร้างช่องทาง คุณต้องตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าลำดับชั้นขององค์กรของคุณแล้ว  

ดู [ลำดับชั้นขององค์กร](channels-org-hierarchies.md) สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับวิธีการสร้างลำดับชั้นขององค์กร

## <a name="select-a-hierarchy"></a>เลือกลำดับชั้น

ในการเลือกลำดับชั้น ให้ดำเนินการตามขั้นตอนเหล่านี้:

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ลำดับชั้นขององค์กร**
1. จากรายการ ให้เลือกลำดับชั้นขององค์กรที่คุณจะเพิ่มช่องทางให้
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **มุมมอง** เพื่อดูรายละเอียดของลำดับชั้น

รูปภาพต่อไปนี้แสดงรายละเอียดลำดับชั้นขององค์กรสำหรับลำดับชั้นที่เลือก

![รายละเอียดลำดับชั้นขององค์กรสำหรับลำดับชั้นที่เลือก](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>การเพิ่มช่องทางลงในโหนดลำดับชั้น

เมื่อต้องการเพิ่มช่องไปยังโหนดลำดับชั้น ให้ทำตามขั้นตอนเหล่านี้

1. บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**
1. เลือกโหนดลำดับชั้น ที่คุณต้องการเพิ่มช่องทางเข้าไป จากนั้นใน **แทรก** ให้เลือก **ช่องทางการขายปลีก** 
1. เลือกช่องทางที่จะเพิ่มแล้วเลือกปุ่ม **ตกลง**
1. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **เผยแพร่** และระบุ **วันที่มีผลบังคับใช้** ในอดีตเพื่อให้การดำเนินการนี้เกิดผลทันที

ภาพต่อไปนี้แสดงวิธีการเลือกช่องทาง เพื่อเพิ่มไปยังโหนดลำดับชั้น

![เลือกช่องทางเพื่อเพิ่มในโหนดลำดับชั้น](media/channel-add-to-org-hierarchy-2.png)

รูปภาพต่อไปนี้แสดงลำดับชั้นที่มีการเพิ่มช่องทางต่าง ๆ แล้ว

![ลำดับชั้นที่มีการเพิ่มช่องทางต่าง ๆ แล้ว](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของช่องทาง](channels-overview.md)

[ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง](channels-prerequisites.md)

[ภาพรวมขององค์กรและลำดับชั้นขององค์กร](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[วางแผนลำดับชั้นขององค์กรของคุณ](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[ลำดับชั้นขององค์กร](channels-org-hierarchies.md)

[ตั้งค่าช่องทางการขายปลีก](channel-setup-retail.md)
    
[ตั้งค่าช่องทางออนไลน์](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]