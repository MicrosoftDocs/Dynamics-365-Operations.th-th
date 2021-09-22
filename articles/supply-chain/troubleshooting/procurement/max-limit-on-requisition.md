---
title: ขีดจำกัดสูงสุดของข้อตกลงการซื้อไม่มีผลบังคับใช้กับใบขอซื้อ
description: ขีดจำกัดสูงสุดของข้อตกลงการซื้อไม่มีผลบังคับใช้กับใบขอซื้อ
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477718"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>ขีดจำกัดสูงสุดของข้อตกลงการซื้อไม่มีผลบังคับใช้กับใบขอซื้อ

## <a name="symptoms"></a>อาการ

เมื่อใบสั่งซื้อเชื่อมโยงกับข้อตกลงการซื้อ ขีดจำกัดสูงสุดจากข้อตกลงการซื้อจะไม่มีผลบังคับในใบขอซื้อ มีการป้อนข้อมูลราคาเริ่มต้นไว้อย่างถูกต้อง แต่ไม่เกินขีดจำกัดสูงสุดของข้อตกลงการซื้อในใบขอซื้อ

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานนี้คาดการณ์ไว้ เนื่องจากใบขอซื้อไม่ได้รับการอนุมัติเสมอ ปริมาณหรือจำนวนเงินจึงไม่ควรถูกสงวนในข้อตกลงการซื้อ ดังนั้นคุณจึงไม่สามารถตอบสนองขีดจำกัดสูงสุดจากข้อตกลงการซื้อได้
