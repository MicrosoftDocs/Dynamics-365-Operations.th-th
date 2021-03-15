---
title: สร้างมิติและนำเข้าสมาชิกมิติ
description: การบัญชีต้นทุนคือโมดูลอิสระที่กำหนดให้ต้องมีข้อมูลหลักจากโมดูลอื่น
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 610a9302610af7a074a91dfc2a8c87725b0a1a82
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009504"
---
# <a name="create-dimensions-and-import-dimension-members"></a>สร้างมิติและนำเข้าสมาชิกมิติ

[!include [banner](../includes/banner.md)]

การบัญชีต้นทุนคือโมดูลอิสระที่กำหนดให้ต้องมีข้อมูลจากโมดูลอื่น ข้อมูลนี้แบ่งออกได้ดังนี้:

-  องค์ประกอบต้นทุน
-  ออบเจ็กต์ต้นทุน
-  มิติทางสถิติ

**องค์ประกอบต้นทุน** สอดคล้องกับรายการต้นทุนที่เกี่ยวข้องในผังบัญชี **ออบเจ็กต์ต้นทุน** สอดคล้องกับชนิดของมิติทางการเงินใด ๆ เช่น ผลิตภัณฑ์ ศูนย์ต้นทุน และโครงการที่คุณต้องการประเมิน ปันส่วนต้นทุนไปยัง หรือวัดโดยตรง **มิติทางสถิติ** และสมาชิกถูกใช้ในการลงทะเบียนรายการที่ไม่ใช่เงินตรา สมาชิกของมิติทางสถิติสามารถใช้เป็นฐานการปันส่วนในการกระจายต้นทุน และการปันส่วนต้นทุน 

แผนภาพต่อไปนี้แสดงให้เห็นถึงมิติที่ใช้ในการบัญชีต้นทุน

[![มิติการบัญชีต้นทุน](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

หลังจากที่นำเข้าข้อมูลลงในการบัญชีต้นทุน คุณสามารถใช้เพื่อสร้างมุมมองต่าง ๆ ที่ให้ข้อมูลเชิงลึกกับผู้จัดการในทุกระดับขององค์กร หัวข้อต่อไปนี้แสดงข้อมูลเกี่ยวกับการสร้างมิติและนำเข้าสมาชิกมิติ 

-  [มิติองค์ประกอบต้นทุน](cost-elements.md)
-  [สร้างองค์ประกอบต้นทุน](./tasks/create-cost-elements.md)
-  [มิติออบเจ็กต์ต้นทุน](cost-objects.md)
-  [แม็ปสมาชิกมิติองค์ประกอบต้นทุนไปยังชุดทั่วไปของมิติ](map-cost-elements-dimension-members.md)
-  [แม็ปมิติองค์ประกอบต้นทุน](./tasks/map-cost-element-dimension.md)
-  [สมาชิกมิติทางสถิติและเท็มเพลตตัวให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]