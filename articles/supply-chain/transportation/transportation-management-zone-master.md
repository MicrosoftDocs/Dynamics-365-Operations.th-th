---
title: ต้นแบบโซนการจัดการการขนส่ง
description: หัวข้อนี้อธิบายวิธีการจัดการการขนส่งที่ช่วยให้คุณสามารถแบ่งที่ตั้งทางภูมิศาสตร์ออกเป็นโซนได้
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 7347add052ec4a9540417a5aeea64ab623026954
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880749"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="554eb-103">ต้นแบบโซนการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="554eb-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="554eb-104">การจัดการการขนส่งที่ช่วยให้คุณสามารถแบ่งที่ตั้งทางภูมิศาสตร์ออกเป็นโซนได้</span><span class="sxs-lookup"><span data-stu-id="554eb-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="554eb-105">การแบ่งที่ตั้งเป็นโซนสามารถช่วย:</span><span class="sxs-lookup"><span data-stu-id="554eb-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="554eb-106">**ทำการกำหนดราคาการขนส่งให้ง่าย** – การกำหนดราคาตามโซนเรียบง่ายกว่าการกำหนดราคาตามแต่ละสถานที่ โดยเฉพาะเมื่อสถานที่ขนส่งกระจัดกระจาย</span><span class="sxs-lookup"><span data-stu-id="554eb-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="554eb-107">**เพิ่มประสิทธิภาพการวางแผนการบรรทุก** – โดยการรวมบัญชีการโหลดตามโซน</span><span class="sxs-lookup"><span data-stu-id="554eb-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="554eb-108">**เพิ่มประสิทธิภาพการวางแผนเส้นทาง** – โดยการกำหนดแผนเส้นทางเฉพาะเป็นโซนเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="554eb-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="554eb-109">คุณกำหนดโซนตามค่าฟิลด์ข้อมูลเมตา (เช่น ประเทศ ช่วงรหัสไปรษณีย์ หรือบริการผู้ขนส่ง) ที่มีคุณสมบัติตรงตามแต่ละโซน</span><span class="sxs-lookup"><span data-stu-id="554eb-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="554eb-110">ไม่จำเป็นต้องใช้คำนิยามของโซนถ้าการกำหนดราคาการขนส่งของคุณไม่ใช้แนวคิดเกี่ยวกับโซน</span><span class="sxs-lookup"><span data-stu-id="554eb-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
