---
title: เพิ่มงานที่เกิดขึ้นก่อนหน้าในกิจกรรมขั้นตอนการผลิต
description: 'ในรุ่นขั้นตอนการผลิต กิจกรรมทั้งหมดต้องมีการจัดลำดับ '
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9b761e61bf6a810da9258870e9a994da4ced125
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981442"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>เพิ่มงานที่เกิดขึ้นก่อนหน้าในกิจกรรมขั้นตอนการผลิต

[!include [banner](../../includes/banner.md)]

ในรุ่นขั้นตอนการผลิต กิจกรรมทั้งหมดต้องมีการจัดลำดับ  กิจกรรมสามารถมีหนึ่งหรือหลายรายการก่อนหน้าหรืองานที่เกิดขึ้นตามมา 

กระบวนงานนี้แสดงวิธีการเชื่อมโยงงานที่เกิดขึ้นก่อนหน้ากับกิจกรรม 

คุณจำเป็นต้องใช้ขั้นตอนการผลิตที่มีรุ่นฉบับร่างที่มีกิจกรรมอย่างน้อยสองรายการที่สามารถเชื่อมต่อได้ 

ถ้าต้องการทราบข้อมูลเพิ่มเติม โปรดอ่านเอกสารทางเทคนิค "ขั้นตอนการผลิตและกิจกรรมใน Lean Manufacturing"


## <a name="find-the-production-flow-and-version"></a>ค้นหาขั้นตอนและรุ่นการผลิต
1. ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. คลิกกิจกรรม

## <a name="select-an-activity-and-add-a-predecessor"></a>เลือกกิจกรรมและเพิ่มงานที่เกิดขึ้นก่อนหน้า
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
2. คลิก เพิ่มงานที่เกิดขึ้นก่อนหน้า
3. ในฟิลด์กิจกรรม ให้ป้อนหรือเลือกค่า
4. ในฟิลด์อัตราส่วนเวลาวงจร ให้ป้อนหมายเลข
    * อัตราส่วนเวลาวงจรเริ่มต้นของความสัมพันธ์ของกิจกรรมคือ 1 โดยสมมติว่ากิจกรรมทั้งสองจะรันพร้อมกันหรือเวลาที่ใช้ในการผลิตแบบสมดุลเท่ากัน ถ้ากิจกรรมที่เกิดขึ้นก่อนหน้ารันเร็วกว่า (เวลาที่ใช้ในการผลิตแบบสมดุลต่ำกว่า) อัตราส่วนควรจะน้อยกว่า 1 ถ้ากิจกรรมที่เกิดขึ้นก่อนหน้ารันช้ากว่า (เวลาที่ใช้ในการผลิตแบบสมดุลสูงกว่า) อัตราส่วนเวลาวงจรจะมากกว่า 1  
5. คลิก ตกลง

