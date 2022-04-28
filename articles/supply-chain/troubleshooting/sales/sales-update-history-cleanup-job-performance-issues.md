---
title: งานการล้างข้อมูลประวัติการอัปเดตการขายล้มเหลว หรือมีปัญหาด้านประสิทธิภาพ
description: ชุดงานการล้างข้อมูลประวัติการขายอาจล้มเหลวหรือใช้เวลานาน ถ้ามีข้อมูลอัปเดตการขายจํานวนมาก
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 124fb90ecafd4f4cccbd8a8bb443694c95365732
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570357"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>งานการล้างข้อมูลประวัติการอัปเดตการขายล้มเหลว หรือมีปัญหาด้านประสิทธิภาพ

## <a name="symptoms"></a>อาการ

ชุดงาน **การล้างข้อมูลประวัติการอัปเดตการขาย** ล้มเหลวหรือมีปัญหาด้านประสิทธิภาพ  

## <a name="cause"></a>สาเหตุ

ซึ่งอาจเกิดขึ้นได้เมื่อระบบของคุณมีการอัปเดตการขายจํานวนมาก ซึ่งอาจส่งผลกับข้อมูลการอัปเดตการขายจํานวนมาก งานการล้างข้อมูลพยายามล้างข้อมูลทั้งหมดในธุรกรรมเดียว ซึ่งส่งผลให้งานอาจใช้เวลานานเพื่อรันหรือล้มเหลว

## <a name="resolution"></a>การแก้ปัญหา

เวอร์ชันใหม่ของชุดงาน **การล้างข้อมูลประวัติการอัปเดตการขาย** พร้อมใช้งานเฉพาะกับ Supply Chain Management เวอร์ชัน 10.0.19 และสูงกว่า โดยค่าเริ่มต้น คุณลักษณะนี้จะไม่ถูกเปิดไว้ สำหรับรายละเอียดเกี่ยวกับวิธีการทำงานและวิธีการเปิดใช้งานในการจัดการคุณลักษณะ โปรดดู [จัดกำหนดการล้างข้อมูลประวัติการขาย](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md)

