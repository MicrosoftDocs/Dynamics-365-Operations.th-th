---
title: ใบสั่งซื้อที่ได้รับจริงจะไม่ปรากฏในรายงานการปิดบัญชีสินค้าคงคลัง
description: ใบสั่งซื้อที่ได้รับจริงจะไม่ปรากฏในรายงานการปิดบัญชีสินค้าคงคลังตรวจสอบปริมาณคงค้าง
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026949"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>ใบสั่งซื้อที่ได้รับจริงจะไม่ปรากฏในรายงานการปิดบัญชีสินค้าคงคลัง

หมายเลข KB: 4612595

## <a name="symptoms"></a>อาการ

ใบสั่งซื้อที่ได้รับจริงจะไม่ปรากฏในรายงานการปิดบัญชีสินค้าคงคลัง **ตรวจสอบปริมาณคงค้าง**

## <a name="resolution"></a>ความละเอียด

รายงาน **ตรวจสอบปริมาณคงค้าง** แสดงธุรกรรมการตัดสินค้าจากคลังที่ไม่สามารถจับคู่กับการรับสต็อกที่อัปเดตทางการเงิน ณ วันที่ปิดบัญชีที่เลือก คุณสามารถเลือกที่จะรวมการรับสินค้าตามจริงไว้ในรายงานได้ ในกรณีดังกล่าว จะมีการแสดงการรับสินค้าตามจริง หากใบรับสินค้าสามารถครอบคลุมธุรกรรมการตัดสินค้าจากคลังที่ไม่สามารถจับคู่ได้ - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจัดเตรียมการเรียกใช้การปิดบัญชีสินค้าคงคลัง](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close)
