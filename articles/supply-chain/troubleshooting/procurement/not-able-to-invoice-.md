---
title: คุณไม่สามารถออกใบแจ้งหนี้ใบสั่งขายที่เชื่อมต่อกับลูกค้าได้
description: คุณไม่สามารถออกใบแจ้งหนี้ใบสั่งขายต้นฉบับและใบสั่งซื้อต้นฉบับโดยตรงได้อีกต่อไปหลังจากที่คุณเปิดใช้งานตัวเลือกลงรายการบัญชีใบแจ้งหนี้โดยอัตโนมัติ
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026945"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>คุณไม่สามารถออกใบแจ้งหนี้ใบสั่งขายที่เชื่อมต่อกับลูกค้าได้

หมายเลข KB: 4611793

## <a name="symptoms"></a>อาการ

คุณไม่สามารถออกใบแจ้งหนี้ใบสั่งขายต้นฉบับและใบสั่งซื้อต้นฉบับโดยตรงได้อีกต่อไปหลังจากที่คุณเปิดใช้งานตัวเลือก  **ลงรายการบัญชีใบแจ้งหนี้โดยอัตโนมัติ** บนหน้า **ระหว่างบริษัท** สำหรับผู้จัดจำหน่าย

## <a name="resolution"></a>ความละเอียด

ลักษณะการซิงโครไนส์ของใบแจ้งหนี้ใบสั่งระหว่างบริษัทและใบแจ้งหนี้ใบสั่งการจัดส่งโดยตรงจะถูกควบคุมและบังคับโดยพารามิเตอร์ที่อธิบายไว้ใน [ตั้งค่าพารามิเตอร์เพื่อลงรายการบัญชีใบสั่งระหว่างบริษัท](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order)

หลังจากที่คุณตั้งค่าพารามิเตอร์เหล่านั้นแล้ว คุณต้องออกใบแจ้งหนี้ใบสั่งขายระหว่างบริษัทก่อน จากนั้นจะมีการซิงโครไนส์ใบสั่งขายและใบสั่งซื้อต้นฉบับ
