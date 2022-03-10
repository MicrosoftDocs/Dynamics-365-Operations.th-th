---
title: หมายเลขชุดงานจะถูกล้างข้อมูลเมื่อเลือกรหัสล็อตใหม่
description: เมื่อคุณทบทวนบรรทัดสมุดรายวันรายการเบิกสินค้า ค่าในฟิลด์หมายเลขชุดงานจะถูกล้างข้อมูลถ้าคุณเลือกค่าใหม่ในฟิลด์รหัสล็อต
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d71720b1d3a34a31639db0f829dee300d6f96d53fd61c0a8740be9f2306d6dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738830"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>หมายเลขชุดงานจะถูกล้างข้อมูลเมื่อเลือกรหัสล็อตใหม่

หมายเลข KB: 4613107

## <a name="symptoms"></a>อาการ

เมื่อคุณทบทวนบรรทัดสมุดรายวันรายการเบิกสินค้า ค่าในฟิลด์ **หมายเลขชุดงาน** จะถูกล้างข้อมูลถ้าคุณเลือกค่าใหม่ในฟิลด์ **รหัสล็อต**

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ ถ้าคุณเปลี่ยนรหัสล็อต คุณจะเปลี่ยนบริบทสินค้า ดังนั้นหมายเลขชุดงานจะถูกรีเซ็ต

เมื่อต้องการเชื่อมโยงหมายเลขชุดงานกับรหัสล็อต คุณต้องตั้งค่ารหัสล็อตก่อน
