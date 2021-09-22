---
title: เจ้าของสินค้าคงคลังไม่ได้รับอนุญาตเมื่อประมวลผลการย้าย
description: คุณอาจได้รับข้อผิดพลาด "เจ้าของสินค้าคงคลังไม่ได้รับอนุญาต %1" กระบวนการจัดการคลังสินค้าสนับสนุนเฉพาะสินค้าคงคลังที่เป็นของนิติบุคคลเท่านั้น
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477716"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>เจ้าของสินค้าคงคลังไม่ได้รับอนุญาตเมื่อประมวลผลการย้ายในแอปคลังสินค้า

## <a name="symptoms"></a>อาการ

เมื่อประมวลผลการย้ายในแอป Warehouse Management บนมือถือ คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> เจ้าของสินค้าคงคลัง %1 ไม่ได้รับอนุญาตในกระบวนการนี้

## <a name="cause"></a>สาเหตุ

ทั้งนี้เนื่องจากมิติการติดตาม **เจ้าของ** หายไปเมื่อแอป Warehouse Management บนมือถือใช้เพื่อทำการเคลื่อนย้าย สมุดรายวันการโอนย้ายสินค้าคงคลังปกติจากไคลเอนต์ Supply Chain Management จะปรากฏขึ้นเพื่อให้คุณสามารถลงรายการบัญชีได้อย่างถูกต้อง และสามารถลงรายการบัญชีได้เฉพาะเมื่อมีการกรอกข้อมูลมิติ **เจ้าของ** ไว้เท่านั้น

## <a name="resolution"></a>การแก้ปัญหา

Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน ขณะนี้ กระบวนการจัดการคลังสินค้าสนับสนุนเฉพาะสินค้าคงคลังที่เป็นของนิติบุคคลเท่านั้น
