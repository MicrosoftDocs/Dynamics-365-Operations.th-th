---
title: งานไม่ถูกบล็อค
description: งานไม่ถูกบล็อค
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924215"
---
# <a name="work-isnt-blocked"></a>งานไม่ถูกบล็อค

รหัสข้อผิดพลาด: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>อาการ

ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> ไม่ได้บล็อคงานที่มีรหัส %1

## <a name="cause"></a>สาเหตุ

ตัวเลือก **เวฟที่บล็อค** ในเวฟถูกตั้งค่าเป็น *ไม่* ไม่สามารถยกเลิกการบล็อคงานเนื่องจากไม่ได้บล็อคอยู่ในขณะนี้

## <a name="resolution"></a>ความละเอียด

 เฉพาะงานที่ตั้งค่าตัวเลือก **เวฟที่บล็อค** เป็น *ใช่* เท่านั้นที่สามารถถูกบล็อคได้
