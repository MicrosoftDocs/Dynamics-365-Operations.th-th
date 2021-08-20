---
title: คุณไม่สามารถอัปเดตต้นทุนต่อหน่วยที่คาดการณ์เมื่อคุณนําเข้าเรกคอร์ดการคาดการณ์ความต้องการ
description: เมื่อคุณใช้เอนทิตีข้อมูลเพื่อนําเข้าเรกคอร์ดการคาดการณ์ความต้องการ ราคาต้นทุนของเรกคอร์ดที่มีอยู่จะไม่อัปเดตเพื่อให้ตรงกับข้อมูลที่นําเข้า
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765381"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>คุณไม่สามารถอัปเดตต้นทุนต่อหน่วยที่คาดการณ์เมื่อคุณนําเข้าเรกคอร์ดการคาดการณ์ความต้องการ

หมายเลข KB: 4614109

## <a name="symptoms"></a>อาการ

เมื่อคุณใช้เอนทิตีข้อมูลเพื่อนําเข้าเรกคอร์ดการคาดการณ์ความต้องการ ค่า **ต้นทุนต่อหน่วยที่คาดการณ์** ของเรกคอร์ดที่มีอยู่จะไม่อัปเดตเพื่อให้ตรงกับข้อมูลที่นําเข้า

## <a name="cause"></a>สาเหตุ

**ต้นทุนต่อหน่วยที่คาดการณ์** เป็นฟิลด์อ่านอย่างเดียว ค่าขึ้นอยู่กับต้นทุนต่อหน่วยผลิตภัณฑ์และไม่สามารถตั้งค่าโดยตรงผ่านการนําเข้า

## <a name="resolution"></a>ความละเอียด

เนื่องจากฟิลด์เป็นแบบอ่านอย่างเดียว คุณจึงไม่สามารถนําเข้าค่าได้ ค่านี้จะคํานวณตามตรรกะทางธุรกิจที่มีอยู่
