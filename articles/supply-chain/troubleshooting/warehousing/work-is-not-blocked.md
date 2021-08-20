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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719562"
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
