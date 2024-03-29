---
title: การแปลงสกุลเงินระหว่างบริษัท
description: บทความนี้อธิบายการแปลงสกุลเงินของธุรกรรมระหว่างบริษัท
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851491"
---
# <a name="intercompany-currency-conversions"></a>การแปลงสกุลเงินระหว่างบริษัท

[!include [banner](../../includes/banner.md)]

เมื่อรหัสสกุลเงินในใบสั่งขายดั้งเดิมและใบสั่งซื้อระหว่างบริษัทแตกต่างกัน ระบบจะแปลงสกุลเงินในฟิลด์ต่อไปนี้ถ้ามีการเปิดใช้งานการซิงโครไนส์:

- **ราคาต่อหน่วย**
- **ค่าธรรมเนียมการขาย** หรือ **ค่าธรรมเนียมของการซื้อ**
- **ส่วนลด**
- **ส่วนลดต่อสินค้าหลายรายการ**

ฟิลด์เหล่านี้จะซิงโครไนส์กับบรรทัดใบสั่งขายระหว่างบริษัท

อย่างไรก็ตาม เนื่องจากสกุลเงินในใบสั่งซื้อระหว่างบริษัทและใบสั่งขายระหว่างบริษัทมีการซิงโครไนส์กันอยู่เสมอ ฟิลด์ต่อไปนี้จึงมีการซิงโครไนส์โดยไม่มีการแปลงสกุลเงิน:

- **ราคาต่อหน่วย**
- **ค่าธรรมเนียมการขาย** หรือ **ค่าธรรมเนียมของการซื้อ**
- **ส่วนลด**
- **เปอร์เซ็นต์ส่วนลด**
- **ส่วนลดต่อสินค้าหลายรายการ**
- **เปอร์เซ็นต์ส่วนลดต่อสินค้าหลายรายการ**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
