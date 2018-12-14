---
title: "ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ PowerApps ได้"
description: "หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าผู้ดูแลระบบไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Microsoft PowerApps ได้"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: th-th
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="c21e6-103">ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ PowerApps ได้</span><span class="sxs-lookup"><span data-stu-id="c21e6-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c21e6-104">**ออก**</span><span class="sxs-lookup"><span data-stu-id="c21e6-104">**Issue**</span></span>

- <span data-ttu-id="c21e6-105">ผู้ดูแลระบบผู้เช่า/สภาพแวดล้อม ไม่สามารถสร้างได้ในศูนย์การจัดการ Microsoft PowerApps ได้</span><span class="sxs-lookup"><span data-stu-id="c21e6-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="c21e6-106">ยังไม่มีการกำหนดลิขสิทธิ์ที่ให้ผู้ใช้มีสิทธิ์ในการดำเนินการขั้นตอนการสร้างสภาพแวดล้อมให้ผู้ใช้ที่กำลังดำเนินการขั้นตอนนั้นโดยตรง</span><span class="sxs-lookup"><span data-stu-id="c21e6-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="c21e6-107">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="c21e6-107">**Solution**</span></span>

<span data-ttu-id="c21e6-108">ตรวจสอบให้แน่ใจว่า ผู้ดูแลระบบผู้เช่าได้กำหนดให้ลิขสิทธิ์ PowerApps P2 ที่ถูกต้องโดยตรงให้กับผู้ใช้ที่จะดำเนินการขั้นตอนการสร้างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="c21e6-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="c21e6-109">นี่คือแผนการบริการ Microsoft Dynamics ที่ให้สิทธิ์นั้น</span><span class="sxs-lookup"><span data-stu-id="c21e6-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="c21e6-110">หน่วยการเก็บสต็อกสินค้าของผลิตภัณฑ์โดยรวม (SKU)</span><span class="sxs-lookup"><span data-stu-id="c21e6-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="c21e6-111">แผนการบริการ PowerApps P2</span><span class="sxs-lookup"><span data-stu-id="c21e6-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="c21e6-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="c21e6-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="c21e6-113">PowerApps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c21e6-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="c21e6-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c21e6-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="c21e6-115">PowerApps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c21e6-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="c21e6-116">โปรดทราบว่า Microsoft Office SKUs ต่างๆ ยังให้สิทธิ์ ร่วมกับ PowerApps Plan 2 SKUs แบบสแตนด์อโลน</span><span class="sxs-lookup"><span data-stu-id="c21e6-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="c21e6-117">จุดสำคัญคือว่า หนึ่งใน SKUs เหล่านี้ต้องมีอยู่</span><span class="sxs-lookup"><span data-stu-id="c21e6-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="c21e6-118">ไปที่ [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)</span><span class="sxs-lookup"><span data-stu-id="c21e6-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="c21e6-119">สร้างสภาพแวดล้อมโดยการปฏิบัติตามคำแนะนำใน [Talent การเตรียมใช้งาน](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent)</span><span class="sxs-lookup"><span data-stu-id="c21e6-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

