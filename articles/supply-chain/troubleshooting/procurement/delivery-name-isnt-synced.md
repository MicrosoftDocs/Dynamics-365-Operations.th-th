---
title: ไม่มีการซิงค์ชื่อการจัดส่งหลังจากที่เปลี่ยนที่อยู่ที่จัดส่งใบสั่งซื้อ
description: หลังจากที่คุณเปลี่ยนที่อยู่ที่จัดส่งในส่วนหัวของใบสั่งซื้อ จะไม่มีการซิงค์ชื่อการจัดส่ง
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
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477708"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>ไม่มีการซิงค์ชื่อการจัดส่งหลังจากที่เปลี่ยนที่อยู่ที่จัดส่งใบสั่งซื้อ

## <a name="symptoms"></a>อาการ

ที่อยู่ในส่วนหัวของใบสั่งซื้อจะถูกอัปเดตไปยังที่อยู่ที่ ไม่ใช่ที่อยู่ที่จัดส่ง ถึงแม้ว่ามีการอัปเดตที่อยู่บนใบสั่งซื้อ ก็จะไม่มีการอัปเดตชื่อการจัดส่งตามที่อยู่ที่อัปเดตแล้ว

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานนี้เกิดจากการออกแบบ ต้องจัดประเภทที่อยู่ที่เลือกเป็นที่อยู่ที่จัดส่ง มิฉะนั้นจะไม่มีการอัปเดตชื่อการจัดส่งตามที่อยู่ที่เลือก
