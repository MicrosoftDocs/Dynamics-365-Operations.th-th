---
title: เกิดข้อยกเว้นระหว่างการลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย
description: เกิดข้อยกเว้น "เกิดข้อยกเว้นตามเป้าหมายของการเรียก" ระหว่างการลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ecc63cb7d0d2392105d8e4290f8e837945ae0781
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477736"
---
# <a name="an-exception-occurs-during-vendor-invoice-posting"></a>เกิดข้อยกเว้นระหว่างการลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย


## <a name="symptoms"></a>อาการ

คุณจะได้รับข้อยกเว้นต่อไปนี้เมื่อลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย:

> เกิดข้อยกเว้นตามเป้าหมายของการเรียก

## <a name="cause"></a>สาเหตุ

ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ

## <a name="resolution"></a>การแก้ปัญหา

เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ** สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)
