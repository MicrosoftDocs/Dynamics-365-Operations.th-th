---
title: กลุ่มภาษีเริ่มต้นและส่วนลดเงินสดเริ่มต้นไม่ได้รับการเติมข้อมูลจากบัญชีใบแจ้งหนี้
description: กลุ่มภาษีเริ่มต้นและส่วนลดเงินสดเริ่มต้นไม่ได้รับการเติมข้อมูลจากบัญชีใบแจ้งหนี้
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477733"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>กลุ่มภาษีเริ่มต้นและส่วนลดเงินสดเริ่มต้นไม่ได้รับการเติมข้อมูลจากบัญชีใบแจ้งหนี้

## <a name="symptoms"></a>อาการ

ถ้าคุณกำลังใช้บัญชีใบแจ้งหนี้ที่แตกต่างจากบัญชีลูกค้า กลุ่มภาษีเริ่มต้นและส่วนลดเงินสดเริ่มต้นจะไม่มีการเติมข้อมูลจากบัญชีใบแจ้งหนี้เมื่อสร้างใบสั่งซื้อ

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานนี้เกิดจากการออกแบบ ค่าเริ่มต้นสำหรับกลุ่มภาษี ส่วนลด เงินสด และข้อมูลราคาอื่นๆ จะขึ้นอยู่กับบัญชีลูกค้าไม่ใช่บัญชีใบแจ้งหนี้
