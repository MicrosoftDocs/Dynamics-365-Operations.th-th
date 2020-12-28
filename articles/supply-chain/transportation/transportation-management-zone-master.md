---
title: ต้นแบบโซนการจัดการการขนส่ง
description: หัวข้อนี้อธิบายวิธีการจัดการการขนส่งที่ช่วยให้คุณสามารถแบ่งที่ตั้งทางภูมิศาสตร์ออกเป็นโซนได้
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2112e7131281cd485b580fd71536981c1ba4aefd
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/29/2020
ms.locfileid: "4438950"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="bc9d6-103">ต้นแบบโซนการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="bc9d6-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc9d6-104">การจัดการการขนส่งที่ช่วยให้คุณสามารถแบ่งที่ตั้งทางภูมิศาสตร์ออกเป็นโซนได้</span><span class="sxs-lookup"><span data-stu-id="bc9d6-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="bc9d6-105">การแบ่งที่ตั้งเป็นโซนสามารถช่วย:</span><span class="sxs-lookup"><span data-stu-id="bc9d6-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="bc9d6-106">**ทำการกำหนดราคาการขนส่งให้ง่าย** – การกำหนดราคาตามโซนเรียบง่ายกว่าการกำหนดราคาตามแต่ละสถานที่ โดยเฉพาะเมื่อสถานที่ขนส่งกระจัดกระจาย</span><span class="sxs-lookup"><span data-stu-id="bc9d6-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="bc9d6-107">**เพิ่มประสิทธิภาพการวางแผนการบรรทุก** – โดยการรวมบัญชีการโหลดตามโซน</span><span class="sxs-lookup"><span data-stu-id="bc9d6-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="bc9d6-108">**เพิ่มประสิทธิภาพการวางแผนเส้นทาง** – โดยการกำหนดแผนเส้นทางเฉพาะเป็นโซนเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bc9d6-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="bc9d6-109">คุณกำหนดโซนตามค่าฟิลด์ข้อมูลเมตา (เช่น ประเทศ ช่วงรหัสไปรษณีย์ หรือบริการผู้ขนส่ง) ที่มีคุณสมบัติตรงตามแต่ละโซน</span><span class="sxs-lookup"><span data-stu-id="bc9d6-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="bc9d6-110">ไม่จำเป็นต้องใช้คำนิยามของโซนถ้าการกำหนดราคาการขนส่งของคุณไม่ใช้แนวคิดเกี่ยวกับโซน</span><span class="sxs-lookup"><span data-stu-id="bc9d6-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>
