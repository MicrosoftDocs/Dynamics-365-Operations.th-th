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
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764703"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>คุณไม่สามารถนําเข้าสินค้าโดยใช้เอนทิตีผลิตภัณฑ์ที่นําออกใช้ V2

หมายเลข KB: 4611825

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามนําเข้าสินค้าโดยใช้เอนทิตี *ผลิตภัณฑ์ที่นําออกใช้ V2* คุณจะได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:

> ไม่สามารถสร้างเรกคอร์ดในสินค้า - กลุ่มมิติการติดตาม (EcoResTrackingDimensionGroupItem) หมายเลขสินค้า: 2040663, ชุดงาน มีเรกคอร์ดอยู่แล้ว

## <a name="resolution"></a>ความละเอียด

เมื่อต้องการนําเข้าผลิตภัณฑ์ที่นําออกใช้ใหม่ คุณต้องใช้เอนทิตี *การสร้างผลิตภัณฑ์ที่นําออกใช้ V2* แทนเอนทิตี *ผลิตภัณฑ์ที่นําออกใช้ V2*
