---
title: คุณไม่สามารถนําเข้าสินค้าโดยใช้เอนทิตีผลิตภัณฑ์ที่นําออกใช้ V2
description: คุณไม่สามารถนําเข้าสินค้าโดยใช้เอนทิตีผลิตภัณฑ์ที่นําออกใช้ V2
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026941"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>คุณไม่สามารถนําเข้าสินค้าโดยใช้เอนทิตีผลิตภัณฑ์ที่นําออกใช้ V2

หมายเลข KB: 4611825

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามนําเข้าสินค้าโดยใช้เอนทิตี *ผลิตภัณฑ์ที่นําออกใช้ V2* คุณจะได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:

> ไม่สามารถสร้างเรกคอร์ดในสินค้า - กลุ่มมิติการติดตาม (EcoResTrackingDimensionGroupItem) หมายเลขสินค้า: 2040663, ชุดงาน มีเรกคอร์ดอยู่แล้ว

## <a name="resolution"></a>ความละเอียด

เมื่อต้องการนําเข้าผลิตภัณฑ์ที่นําออกใช้ใหม่ คุณต้องใช้เอนทิตี *การสร้างผลิตภัณฑ์ที่นําออกใช้ V2* แทนเอนทิตี *ผลิตภัณฑ์ที่นําออกใช้ V2*
