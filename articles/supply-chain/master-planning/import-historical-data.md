---
title: นำเข้าข้อมูลในอดีตสำหรับการคาดการณ์ความต้องการ
description: เพื่อให้ได้การคาดการณ์ความต้องการที่ถูกต้อง คุณจำเป็นต้องมีข้อมูลความต้องการในอดีตสำหรับแต่ละสินค้าหรือคีย์การปันส่วนสินค้า บทความนี้อธิบายวิธีการใช้เอนทิตี้ข้อมูลเพื่อนำเข้าข้อมูลความต้องการในอดีตจากระบบใด ๆ เพื่อให้คุณทราบประวัติของข้อมูลการคาดการณ์ความต้องการที่ยาวนานขึ้น
author: t-benebo
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e36ea72322c31f7e0ea3377b474cd148d78bdd3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877608"
---
# <a name="import-historical-data-for-demand-forecasts"></a>นำเข้าข้อมูลในอดีตสำหรับการคาดการณ์ความต้องการ

[!include [banner](../includes/banner.md)]

เพื่อช่วยในการรับรองความถูกต้องของการคาดการณ์ความต้องการ คุณต้องมีข้อมูลความต้องการในอดีตที่มากเท่ากับข้อมูลที่คุณสามารถได้รับสำหรับแต่ละสินค้าหรือคีย์การปันส่วนสินค้า ถ้าข้อมูลความต้องการที่ผ่านมาไม่ได้ถูกนำเข้าอยู่แล้ว ใช้เอนทิตีข้อมูล **ความต้องการภายนอกที่ผ่านมา** (ReqDemPlanHistoricalExternalDemandEntity) ใน Dynamics 365 Supply Chain Management เพื่อนำเข้า

ในพื้นที่ทำงาน **การจัดการข้อมูล** คุณสามารถดูภาพรวมของฟิลด์ทั้งหมดในเอนทิตี้ได้

1. เปิดพื้นที่ทำงาน **การจัดการข้อมูล**
2. เลือกไทล์ **เอนทิตี้ข้อมูล**
3. ค้นหารายการเอนทิตี้สำหรับ **ความต้องการภายนอกในอดีต**
4. เลือก **ฟิลด์เป้าหมาย** ฟิลด์เอนทิตี้ต่อไปนี้เป็นฟิลด์บังคับ: ไซต์ (**DeliveringSiteId**) วันที่ (**DemandDate**) ปริมาณ (**DemandQuantity**) และหมายเลขสินค้า (**ItemNumber**) หรือคีย์การปันส่วนสินค้า (**ProductAllocationKeyId**) อย่างใดอย่างหนึ่ง

เพื่อใช้เอนทิตีข้อมูล คุณต้องมีไฟล์ Microsoft Excel หรือไฟล์ค่าที่คั่นด้วยจุลภาค (CSV) ที่ประกอบด้วยข้อมูลความต้องการที่ผ่านมา ตัวอย่างต่อไปนี้แสดงวิธีการนำเข้าข้อมูลจากไฟล์ CSV

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการนําเข้าข้อมูล รวมถึงวิธีการล้างข้อมูลหลังจากการนําเข้า โปรดดู [ภาพรวมของงานการนําเข้าและส่งออกข้อมูล](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) และบทความที่เกี่ยวข้อง

ดูเพิ่มเติมที่ [สร้างการคาดการณ์พื้นฐานทางสถิติ](generate-statistical-baseline-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]