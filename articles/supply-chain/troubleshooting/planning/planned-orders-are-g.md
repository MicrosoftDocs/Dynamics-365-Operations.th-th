---
title: การวางแผนหลักสร้างแผนการใบสั่งสำหรับผลิตภัณฑ์แฝง
description: แผนการใบสั่งสร้างสำหรับผลิตภัณฑ์แฝงหลักจากเรียกใช้การวางแผนหลัก
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026956"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>การวางแผนหลักสร้างแผนการใบสั่งสำหรับผลิตภัณฑ์แฝง

หมายเลข KB: 4614729

## <a name="symptoms"></a>อาการ

แผนการใบสั่งสร้างสำหรับผลิตภัณฑ์แฝงหลักจากเรียกใช้การวางแผนหลัก

## <a name="resolution"></a>ความละเอียด

การตั้งค่าตัวเลือก **รายการแฝง** สำหรับผลิตภัณฑ์ที่นำออกใช้จะระบุชนิดรายการเริ่มต้นบนสูตรการผลิต (BOM) เมื่อตั้งค่าตัวเลือก **รายการแฝง** เป็น *ใช่* ระบบจะยังคงสร้างแผนการใบสั่งให้กับสินค้า แต่ตัวเลือก **ความต้องการที่ได้รับมาโดยตรง** สำหรับแต่ละแผนการใบสั่งจะตั้งค่าเป็น *ใช่* ดังนั้น จึงไม่สามารถยืนยันแผนการใบสั่งผลิตด้วยตนเองได้ ซึ่งจะรวมโดยอัตโนมัติเสมอเมื่อมีการยืนยันใบสั่งผลิตหลัก นอกจากนี้ บรรทัด BOM ของแผนการใบสั่งแฝงจะรวมอยู่ใน BOM ของใบสั่งผลิตหลัก
