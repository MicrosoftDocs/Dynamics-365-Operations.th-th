---
title: โฮมเพจบริการการบัญชีต้นทุน (การแสดงตัวอย่างแบบส่วนตัว)
description: หัวข้อนี้คือโฮมเพจสำหรับบริการการบัญชีต้นทุน
author: AndersGirke
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 7a1865115882d8b9e2beed7bdbc70be3d5118db8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839522"
---
# <a name="cost-accounting-service-home-page-private-preview"></a><span data-ttu-id="c1072-103">โฮมเพจบริการการบัญชีต้นทุน (การแสดงตัวอย่างแบบส่วนตัว)</span><span class="sxs-lookup"><span data-stu-id="c1072-103">Cost accounting service home page (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c1072-104">องค์กรระหว่างประเทศอยู่ภายใต้การเพิ่มแรงกดดันเพื่อให้เป็นไปตามข้อบังคับภายในประเทศทั้งสอง (หลักการการบัญชีที่รับรองโดยทั่วไปในประเทศ \[GAAP\]ภายในประเทศ) และมาตรฐานการบัญชีที่ใช้ร่วมกัน (เช่น US-GAAP มาตรฐาน Financial Reporting ระหว่างประเทศ \[IFRS\] และมาตรฐานการบัญชีระหว่างประเทศ \[IAS\]) แม้ในกรณีที่มาตรฐานและข้อบังคับที่แตกต่างกันอาจขัดแย้งกัน</span><span class="sxs-lookup"><span data-stu-id="c1072-104">International organizations are under increasing pressure to comply with both local regulations (local generally accepted accounting principles \[GAAP\]) and shared accounting standards (such as US-GAAP, International Financial Reporting Standards \[IFRS\], and International Accounting Standards \[IAS\]), even in situations where the different standards and regulations might be in conflict.</span></span>

<span data-ttu-id="c1072-105">องค์กรระหว่างประเทศที่มีบริษัทในเครือในประเทศหรือภูมิภาคที่มีสกุลเงินท้องถิ่นแบบความผันผวนสูง ฝ่ายการปกครองท้องถิ่นอาจจำเป็นต้องใช้ในการลงบัญชีและจัดการสินค้าคงคลังในสกุลเงินดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="c1072-105">International organizations that have subsidiaries in countries or regions where there is a hyper-fluctuating local currency might be required by the local government to account and manage inventory in that currency.</span></span> <span data-ttu-id="c1072-106">อย่างไรก็ตาม เพื่อให้เป็นไปตาม US-GAAP บริษัทในเครือยังจะต้องลงบัญชีและจัดการสินค้าคงคลังในสกุลเงินที่มั่นคง เช่น ดอลลาร์สหรัฐ (USD) ด้วย</span><span class="sxs-lookup"><span data-stu-id="c1072-106">However, to comply with US-GAAP, the subsidiary is also required to account and manage inventory in a stable currency, such as US dollars (USD).</span></span>

<span data-ttu-id="c1072-107">องค์กรอาจต้องการลงบัญชีสินค้าคงคลังตามต้นทุนมาตรฐานโดยเป็นส่วนหนึ่งของการตั้งค่าการบัญชีการจัดการ</span><span class="sxs-lookup"><span data-stu-id="c1072-107">Organizations might prefer to account inventory by standard cost as part of their management accounting setup.</span></span> <span data-ttu-id="c1072-108">อย่างไรก็ตาม IFRS รัฐบาลท้องถิ่น และหน่วยงานจัดเก็บภาษีท้องถิ่น จะไม่จดจำต้นทุนมาตรฐานเป็นวิธีการที่ยอมรับเสมอ</span><span class="sxs-lookup"><span data-stu-id="c1072-108">However, IFRS, local governments, and local tax authorities don't always recognize standard cost as an accepted method.</span></span> <span data-ttu-id="c1072-109">แต่โดยปกติแล้วพวกเขาจะใช้ค่าเฉลี่ย เข้าก่อนออกก่อน (FIFO) หรือการระบุรหัสประจำตัวเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c1072-109">Instead, they often require average, first in, first out (FIFO), or specific identification.</span></span>

<span data-ttu-id="c1072-110">Add-in ของบริการการบัญชีต้นทุนสำหรับ Microsoft Dynamics 365 Supply Chain Management จะช่วยให้คุณสามารถลงบัญชีสินค้าคงคลังในบัญชีแยกประเภทได้หลายบัญชี</span><span class="sxs-lookup"><span data-stu-id="c1072-110">The cost accounting service add-in for Microsoft Dynamics 365 Supply Chain Management lets you account inventory in multiple ledgers.</span></span> <span data-ttu-id="c1072-111">ดังนั้น จึงสนับสนุนสกุลเงินหลายสกุลและการประเมินค่าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="c1072-111">Therefore, it supports multiple currencies and multiple valuations.</span></span>

## <a name="related-resources"></a><span data-ttu-id="c1072-112">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c1072-112">Related resources</span></span>

[<span data-ttu-id="c1072-113">เริ่มต้นใช้งานบริการการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c1072-113">Get started with the cost accounting service</span></span>](cost-accounting-service-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]