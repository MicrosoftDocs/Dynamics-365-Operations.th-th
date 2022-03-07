---
title: การกลับรายการการรายงานการเสร็จงานสร้างธุรกรรมที่เปิดค้างไว้ที่ไม่คาดคิด
description: การกลับรายการการรายงานการเสร็จงานที่เลือกจะสร้างธุรกรรมที่เปิดค้างไว้ซึ่งปริมาณที่กลับรายการมีมิติสินค้าคงคลังเดียวกันกับธุรกรรมที่กลับรายการ
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026961"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>การกลับรายการการรายงานการเสร็จงานสร้างธุรกรรมที่เปิดค้างไว้ที่ไม่คาดคิด

หมายเลข KB: 4612469

## <a name="symptoms"></a>อาการ

หากคุณกลับรายการการรายงานการเสร็จงานที่เลือก ระบบจะสร้างธุรกรรมที่เปิดค้างไว้ซึ่งปริมาณที่กลับรายการมีมิติสินค้าคงคลังเดียวกันกับธุรกรรมที่กลับรายการ

## <a name="resolution"></a>ความละเอียด

เมื่อคุณกลับรายการการดําเนินงานรายงานการเสร็จงาน มิติสินค้าคงคลังจะเริ่มต้นจากสมุดรายวันการผลิต ดังนั้นจึงได้รับหมายเลขชุดงาน เนื่องจากการทำเครื่องหมาย ธุรกรรมใบสั่งขายจะสืบทอดหมายเลขชุดงาน

มิติสามารถรีเซ็ตได้เมื่อลงรายการบัญชีการรายงานการเสร็จงาน
